

# Memoria Técnica – Sistemas Informáticos

# Autor: Daniel Ortiz Jiménez

# Ciclo: DAM/DAW – Campus Cámara de Comercio Sevilla

# Fecha: 15/05/2026

# 

# ÍNDICE

[**1\. Análisis de Necesidades	2**](#1.-análisis-de-necesidades)

[1.1. Contexto y Problemática Actual	2](#1.1.-contexto-y-problemática-actual)

[1.2. Solución Propuesta: Infraestructura Híbrida Docker–Guacamole	2](#1.2.-solución-propuesta:-infraestructura-híbrida-docker–guacamole)

[1.3. Justificación Técnica y Beneficios (TCO)	2](#1.3.-justificación-técnica-y-beneficios-\(tco\))

# 1\. Análisis de Necesidades {#1.-análisis-de-necesidades}

## 1.1. Contexto y Problemática Actual {#1.1.-contexto-y-problemática-actual}

Antes de la intervención técnica, la empresa presentaba una infraestructura dispersa y difícil de administrar. Los técnicos necesitaban acceder a múltiples máquinas remotas mediante conexiones directas RDP y SSH, lo que obligaba a abrir numerosos puertos en el firewall corporativo. Esta práctica incrementa la superficie de ataque y exponía servicios críticos a intentos de intrusión. Asimismo, la falta de un punto de acceso centralizado generaba ineficiencias operativas: cada técnico debe configurar sus propios clientes, mantener credenciales locales y gestionar conexiones manualmente, lo que aumentaba el riesgo de errores humanos y dificulta la trazabilidad de las acciones realizadas en los sistemas.

En consecuencia, la empresa carecía de un mecanismo unificado para controlar accesos, auditar sesiones o aplicar políticas de seguridad homogéneas. Esta situación comprometía la disponibilidad y la integridad de los servicios internos, especialmente en un entorno donde el teletrabajo y la movilidad del personal son habituales.

## 1.2. Solución Propuesta: Infraestructura Híbrida Docker–Guacamole {#1.2.-solución-propuesta:-infraestructura-híbrida-docker–guacamole}

Tras analizar los requisitos de seguridad, accesibilidad y mantenimiento, se ha implementado una infraestructura basada en Apache Guacamole desplegada mediante Docker Compose. Esta solución permite centralizar todos los accesos remotos a través de una única interfaz web, reduciendo la exposición de puertos a un único punto controlado (HTTP/HTTPS). Asimismo, el uso de contenedores garantiza aislamiento entre servicios, evitando conflictos de dependencias y facilitando la escalabilidad horizontal.

Docker proporciona un entorno reproducible, portable y fácil de versionar, lo que permite que la infraestructura pueda ser replicada o restaurada rápidamente en caso de fallo. Guacamole, por su parte, elimina la necesidad de instalar clientes RDP o SSH en los equipos de los técnicos, simplificando la experiencia de uso y permitiendo una auditoría centralizada de todas las conexiones.

## 1.3. Justificación Técnica y Beneficios (TCO) {#1.3.-justificación-técnica-y-beneficios-(tco)}

La elección de esta arquitectura responde a criterios de eficiencia, seguridad y reducción del Coste Total de Propiedad (TCO). Al utilizar software bajo licencias permisivas como Apache License 2.0 y PostgreSQL License, la empresa evita costes de licenciamiento y puede destinar esos recursos a mejorar la seguridad o ampliar su infraestructura. Asimismo, la centralización del acceso reduce el tiempo de soporte técnico y minimiza la necesidad de configurar clientes individuales.

Por consiguiente, la solución implementada mejora la disponibilidad del sistema, reduce riesgos de seguridad y garantiza un control exhaustivo de las conexiones remotas. Según la literatura académica, un análisis de requisitos adecuado permite evitar fallos críticos en producción y optimizar la calidad del software desplegado (Drake, 2008; García Notario, 2015). En consecuencia, la infraestructura Docker–Guacamole constituye una respuesta profesional, escalable y alineada con las buenas prácticas de la ingeniería del software.

