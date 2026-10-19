# Módulo 1: Introducción a la nube

## ¿Qué es la computación en la nube?
Entrega bajo demanda de recursos de TI a través de internet, con precios de pago por uso.

## Tipos de implementación
- **Basada en la nube**
- **En las instalaciones** (on-premises)
- **Híbrida**

## Regiones y zonas de disponibilidad (AZ)
Una región es una ubicación física en el mundo que contiene grupos de centros de
datos, llamados zonas de disponibilidad (AZs). Cada región tiene mínimo 3 centros
de datos.

## Modelo de responsabilidad compartida de AWS
- **Responsabilidad del cliente:** datos del cliente, cifrado de datos del cliente →
  seguridad **EN** la nube
- **Responsabilidad del cliente o de AWS** (varía según el servicio): cifrado del
  servidor, protección del tráfico de red, administración de plataforma y
  aplicaciones, configuración de SO/red/firewall
- **Responsabilidad de AWS:** software para cómputo/almacenamiento/base de
  datos/redes, hardware e infraestructura global → seguridad **DE** la nube

## Notas adicionales
- **Parche vs. actualización:** un parche corrige algo específico (ej. un fallo de
  seguridad); una actualización es un cambio mayor que añade funciones o cambia
  de versión.
- **Latencia:** tiempo que tardan los datos en viajar de un punto a otro y recibir
  respuesta (se mide en ms) — no confundir con ancho de banda (cantidad de datos
  que caben en la red).
- **Resiliencia de datos:** capacidad de un sistema para absorber interrupciones,
  proteger la información y recuperarse rápido ante fallos o ataques. Distinto de
  un simple backup (que solo es el archivo guardado).
