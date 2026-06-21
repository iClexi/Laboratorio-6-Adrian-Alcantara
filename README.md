<div align="center">

# Laboratorio 6 - Seguridad en Linux

### Practicas de cifrado, firewall, IDS Snort y autenticacion 2FA para acceso SSH.

![Platform](https://img.shields.io/badge/Platform-Ubuntu%20Server-E95420?logo=ubuntu&logoColor=white)
![Crypto](https://img.shields.io/badge/Crypto-GnuPG-blue)
![Firewall](https://img.shields.io/badge/Firewall-iptables%20%7C%20UFW-orange)
![IDS](https://img.shields.io/badge/IDS-Snort-red)
![Auth](https://img.shields.io/badge/Auth-2FA%20PAM-green)
![Topic](https://img.shields.io/badge/Topic-Linux%20Security-purple)

</div>

---

## Descripcion

Este laboratorio esta enfocado en seguridad practica sobre Ubuntu Server. Incluye cifrado de archivos con GnuPG, control de trafico con `iptables` y UFW, deteccion de trafico con Snort y configuracion de doble factor de autenticacion para SSH usando PAM y Google Authenticator.

## Practicas incluidas

| Practica | Tema | Herramientas |
| --- | --- | --- |
| Practica 1 | Cifrado | GnuPG |
| Practica 2 | Firewall | iptables, UFW |
| Practica 3 | IDS | Snort |
| Practica 4 | 2FA en SSH | PAM, Google Authenticator |

## How-To: ejecutar el laboratorio

1. Usa una VM Ubuntu Server de laboratorio.
2. Lee cada archivo antes de ejecutar reglas de seguridad.
3. En practicas de firewall, mantén una consola abierta por si bloqueas SSH.
4. En 2FA, prueba una segunda conexion antes de cerrar la sesion actual.
5. Documenta las pruebas de deteccion, bloqueo y autenticacion.

## Requisitos

- Ubuntu Server.
- Acceso `sudo`.
- Red local o entorno de pruebas.
- Servicio SSH instalado.
- Cuidado especial al aplicar reglas de firewall.

## Comandos clave

```bash
sudo apt install -y gnupg2
sudo iptables -L INPUT -v -n --line-numbers
sudo ufw status verbose
sudo apt install -y snort
sudo snort -T -c /etc/snort/snort.conf
sudo apt install -y libpam-google-authenticator
google-authenticator
```

## Estructura del repositorio

```text
Laboratorio-6-Adrian-Alcantara/
├── Practica 1 - Cifrado
├── Practica 2 - IP tables y ufw
├── Practica 3 - IDS Snort
├── Practica 4 - Configurar 2FA con google authenticator Modulo PAM para Acceso SSH
└── README.md
```

## Resultado esperado

Al completar el laboratorio, el estudiante debe saber cifrar informacion, aplicar reglas de firewall, detectar trafico con un IDS y fortalecer el acceso SSH con segundo factor de autenticacion.
