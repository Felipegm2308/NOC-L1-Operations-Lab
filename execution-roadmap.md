# Hoja de ruta de ejecución

## Fase 1 — Base operativa

1. Preparar Git, estructura del repositorio y reglas para secretos.
2. Crear las máquinas virtuales y asignar direcciones estáticas.
3. Verificar conectividad y sincronización de tiempo.
4. Registrar una línea base de CPU, memoria, disco y red.

## Fase 2 — Monitoreo y eventos

1. Instalar Prometheus y Grafana en `noc-monitor`.
2. Instalar Node Exporter en los tres nodos.
3. Agregar Blackbox Exporter para ICMP, HTTP, DNS y TCP.
4. Agregar SNMP Exporter para dispositivos compatibles.
5. Crear dashboards y reglas de alerta.
6. Ejecutar scripts Bash por cron cada cinco minutos.

## Fase 3 — Servicios y continuidad

1. Implementar DNS, DHCP, proxy, web, correo y NTP.
2. Aplicar reglas UFW y verificar puertos permitidos.
3. Configurar rsync y DRBD para replicación.
4. Configurar Keepalived y probar la migración de la VIP.
5. Agregar health checks y balanceo básico.

## Fase 4 — Routing y switching

1. Configurar IPv4 y subnetting.
2. Ejecutar laboratorios de rutas estáticas y RIPv2.
3. Configurar OSPF y BGP básico.
4. Configurar VLAN, trunks, STP, PortFast y EtherChannel.
5. Agregar NAT, VPN y un escenario básico de red inalámbrica.
6. Introducir fallas controladas y documentar el diagnóstico.

## Fase 5 — Operación NOC

1. Crear matriz de severidad, prioridad y SLA.
2. Registrar alertas como incidentes.
3. Mantener work notes cronológicas.
4. Preparar comunicaciones para usuarios y equipos internos.
5. Escalar casos siguiendo un runbook.
6. Completar revisión postincidente y acción de mejora.

## Fase 6 — Publicación

1. Ejecutar todas las pruebas desde un entorno limpio.
2. Guardar evidencia real y sanitizada.
3. Actualizar la matriz de requisitos.
4. Revisar ortografía en español e inglés.
5. Crear una versión etiquetada y publicar el repositorio.

