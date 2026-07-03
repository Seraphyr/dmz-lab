# dmz-lab
dmz-lab 4geeks


# DMZ Segura — Cisco Packet Tracer

Laboratorio de configuración de una DMZ usando un router Cisco ISR 2911. Se expone un servidor web a Internet mediante NAT estático y se protege la red interna con ACLs.

## Topología

Tres segmentos conectados al Router_FW:
- **LAN** (192.168.1.0/24) — PC interno
- **DMZ** (192.168.2.0/24) — servidor web
- **Externa** (192.168.3.0/24) — Internet simulado

## Qué hace cada ACL

- **ACL 101** en Gi0/2: solo deja pasar HTTP (puerto 80) desde Internet al servidor. El ping queda bloqueado por el deny implícito.
- **ACL 102** en Gi0/1: impide que la DMZ inicie conexiones hacia la LAN, pero deja pasar las respuestas HTTP con `established`.

## Contenido

```
├── dmz-lab.pkt       # Topología en Packet Tracer
├── informe_dmz.docx  # Informe con configuración y evidencias
└── README.md
```
