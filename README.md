# NOC-L1-Operations-Lab
Laboratorio integral orientado al puesto NOC Network Technician L1 de DXC. El proyecto reproduce el ciclo operativo de un NOC: detectar un evento, validar su impacto, ejecutar diagnóstico de nivel 1, registrar el incidente, comunicar avances, escalar dentro del SLA y documentar la restauración del servicio.

Estado: en construcción. Los documentos y configuraciones solo se marcarán como completados después de ejecutar las pruebas y guardar evidencia verificable.

Objetivo

Construir un entorno reproducible que demuestre competencias iniciales en:

Monitoreo de infraestructura y servicios.

TCP/IP, IPv4, subnetting, routing y switching.

VLAN, trunking, STP, PortFast y EtherChannel.

DNS, DHCP, NAT, VPN, NTP, proxy, web y correo.

Diagnóstico básico de OSPF, BGP, firewalls y balanceo de carga.

Linux, Bash, cron, UFW, rsync, DRBD y Keepalived.

Gestión de incidentes, prioridades, SLA, notas cronológicas y escalamiento.

Elaboración de runbooks, SOP, artículos de conocimiento y reportes operativos.

Arquitectura funcional

flowchart TD
    A["Dispositivos y servicios"] --> B["Prometheus, SNMP y Blackbox"]
    B --> C["Grafana y Alertmanager"]
    C --> D["Validación y diagnóstico L1"]
    D --> E["Incidente en ITSM"]
    E --> F["Resolución o escalamiento"]
    F --> G["Cierre, reporte y mejora"]

El laboratorio utilizará tres nodos Linux y una topología de red virtual. La primera versión podrá ejecutarse con máquinas virtuales; una demostración reducida con contenedores facilitará las pruebas rápidas.

Módulos

Módulo

Contenido

Resultado demostrable

01-monitoring/

Prometheus, Grafana, Alertmanager, Blackbox Exporter, SNMP Exporter, Bash y cron

Dashboard, alertas y validación de disponibilidad, CPU, RAM, disco, latencia y servicios

02-network-services-ha/

DNS, DHCP, proxy, web, correo, NTP, UFW, rsync, DRBD y Keepalived

Servicios documentados, VIP activo-pasivo y pruebas de recuperación

03-networking/

Static routing, RIPv2, OSPF, BGP, VLAN, trunks, STP, PortFast, EtherChannel, NAT y VPN

Configuraciones, tabla de direccionamiento, pruebas y escenarios de falla

04-incident-management/

Flujo ITSM, matriz de prioridad/SLA, bitácora, escalamiento y comunicaciones

Tickets de ejemplo con trazabilidad completa

05-runbooks/

Procedimientos de diagnóstico y recuperación

Runbooks ejecutables para incidentes frecuentes

06-evidence/

Capturas, salidas de comandos, reportes y resultados

Evidencia que respalda cada afirmación del CV

Herramientas

Observabilidad: Prometheus, Grafana, Alertmanager, Blackbox Exporter y SNMP Exporter.

Redes: GNS3 o EVE-NG con imágenes obtenidas legalmente; FRRouting como alternativa abierta.

Sistemas: Linux Server, Bash, cron y UFW.

Servicios: BIND9, Kea DHCP, Squid, Nginx, Postfix y Chrony.

Alta disponibilidad: Keepalived, rsync y DRBD.

ITSM: ServiceNow Developer Instance cuando esté disponible; los artefactos del repositorio permiten demostrar el flujo sin publicar credenciales ni datos sensibles.

Control de versiones: Git y GitHub.

SolarWinds, ScienceLogic SL1 y NetBrain son plataformas empresariales propietarias. Este laboratorio no afirmará experiencia práctica con ellas sin acceso real. Prometheus, Grafana, SNMP, Blackbox y GNS3 demostrarán los mismos fundamentos operativos de monitoreo, correlación, topología y diagnóstico requeridos para aprender esas plataformas.

Escenarios principales

Un servidor supera el umbral de CPU durante cinco minutos.

El servicio DNS deja de responder, aunque el host continúa accesible.

Se pierde conectividad entre dos VLAN por una configuración incorrecta de trunk.

Un enlace WAN aumenta su latencia o presenta pérdida de paquetes.

El nodo web principal falla y la IP virtual migra al nodo secundario.

Un ticket se aproxima al límite de SLA y requiere escalamiento.

Cada escenario seguirá este flujo:

alerta → validación → impacto → diagnóstico L1 → ticket → comunicación → resolución/escalamiento → cierre → mejora

Criterio de finalización

Un módulo se considera terminado únicamente cuando contiene:

Configuración o código versionado.

Procedimiento reproducible.

Resultado esperado y criterio de éxito.

Evidencia real sin información sensible.

Ticket o bitácora del incidente.

Explicación breve para entrevista.

Integridad del portafolio

No se incluirán capturas inventadas ni resultados no ejecutados. Las credenciales, direcciones públicas y archivos propietarios quedan excluidos mediante .gitignore. Las imágenes de Cisco u otros fabricantes no se distribuirán en este repositorio.

