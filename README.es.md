[English](README.md) | [Español](README.es.md)

# ❤️🪵

*Protocolo Radicle Heartwood & Stack*

Heartwood es la tercera versión del Protocolo Radicle, una poderosa colaboración de codigo peer-to-peer (entre pares) y publicación de stack. El repositorio tiene una implementación completa de Heartwood, hecha con una interfaz de línea de comandos amigable y fácil de usar (`rad`) y un daemon de red (`radicle-node`).

Radicle se diseñó para ser una alternativa segura, descentralizada y poderosa frente a plataformas de código abierto como GitHub y GitLab, que preserva la soberanía y la libertad de los usuarios.

Mira la [Página de inicio de Radicle](https://radicle.dev/) para obtener información general, y el [Zulip chat](https://radicle.zulipchat.com/) para hablar con el equipo del proyecto.

Mira la [Guía del protocolo](https://radicle.dev/guides/protocol) para obtener una descripción detallada del funcionamiento de Radicle.


## Instalación

**Requisitos**

* Sistema operativo basado en *Linux* o *Unix*.
* Git 2.34 o superior
* OpenSSH 9.1 o superior con `ssh-agent`


### 📀 Desde los binarios

> Requiere `curl` y `tar`.

Ejecuta el siguiente comando para instalar la ultima versión del binario:

    curl -sSf https://radicle.dev/install | sh

O visita nuestra página de [descargas](https://radicle.dev/download).

### 📦 Desde el código fuente & Toolchain

> Requiere la toolchain de Rust.

Puedes instalar el stack de Radicle desde el código fuente ejecutando los siguientes comandos listados, desde adentro de este repositorio:

    cargo install --path crates/radicle-cli --force --locked --root ~/.radicle
    cargo install --path crates/radicle-node --force --locked --root ~/.radicle
    cargo install --path crates/radicle-remote-helper --force --locked --root ~/.radicle

O directamente desde nuestro nodo semilla:

    cargo install --force --locked --root ~/.radicle \
        --git https://seed.radicle.dev/z3gqcJUoA1n9HaHKufZs5FCSGazv5.git \
        crates/radicle-cli crates/radicle-node crates/radicle-remote-helper

## Ejecución

Los unit files de *Systemd* para el nodo se encuentran en la carpeta `/systemd`. Estos pueden utilizarse como punto de partida para personalizarlo/customizarlo más.

Para ejecutar en modo debug, mira [HACKING.md](HACKING.md).

## Feedback

Si tienes algún comentario o feedback, siéntete libre de crear issues usando `rad issue`, unirte a [nuestro Zulip][zulip], o enviar un email a [feedback@radicle.dev][mail-feedback].
Los emails enviados a esta dirección se [postean automaticamente][zulip-help-email] en [nuestro canal **publico** de #feedback en Zulip][zulip-feedback], mostrando el [Encabezado `From`][rfc2822s3.6.2] (que suele contener tu nombre y direccion de email). Esto nos permite debatir tus comentarios/feedback en Zulip y, si es necesario, responderte vía email.

## Contribuciones

Mira [CONTRIBUTING.md](CONTRIBUTING.md) y [HACKING.md](HACKING.md) para una introducción sobre como contribuir en Radicle.

## Paquetes

Los miembros de la comunidad mantienen paquetes para varios package managers.
Esto hace mucho más fácil intalar Radicle y permite una integracion mas completa de Radicle con varias Distribuciones. Gracias!

### APT (Debian, etc.)

Mira <https://radicle.dev/apt/>
y <rad:z2nDKoCF4hg6xVrv7v93LmWHDJKUr>
mantenido por [Lars Wirzenius](https://liw.fi) y [Richard Levitte](https://richard.levitte.org)

### Arch

Mira [archlinux.org/packages](https://archlinux.org/packages/?q=radicle)
y [gitlab.archlinux.org](https://gitlab.archlinux.org/archlinux/packaging/packages/radicle)
mantenido por [tippfehlr](https://tippfehlr.dev) y [kpcyrd](https://vulns.xyz).

### NixOS

Mira [search.nixos.org/packages](https://search.nixos.org/packages?query=radicle)
y [search.nixos.org/options](https://search.nixos.org/options?query=services.radicle)
mantenido por [@NixOS/radicle](https://github.com/orgs/NixOS/teams/radicle).

También mira [home-manager-options.extranix.com](https://home-manager-options.extranix.com/?query=radicle)
para usarlo como home-manager.

## Licencia

Radicle se distribuye bajo los términos tanto de la Licencia MIT como de la Licencia Apache (Version 2.0).

Mira [LICENSE-APACHE](LICENSE-APACHE) y [LICENSE-MIT](LICENSE-MIT) para obtener más detalles.

[zulip]: https://radicle.zulipchat.com/
[zulip-feedback]: https://radicle.zulipchat.com/#narrow/channel/392584-feedback
[zulip-help-email]: https://talently.zulip.com/help/message-a-channel-by-email
[mail-feedback]: mailto:feedback@radicle.dev
[rfc2822s3.6.2]: https://datatracker.ietf.org/doc/html/rfc2822#section-3.6.2
