# Módulo 2: Computación en la nube

## Amazon EC2 (Elastic Compute Cloud)
Las instancias son máquinas virtuales en la nube. Varias instancias comparten un
host físico subyacente — esto se llama **multitenencia (multi-tenancy)**, y se
logra con un software llamado **hipervisor**.

- **Aprovisionar** = configurar
- **Escalar verticalmente:** modificar la instancia para tener más memoria/CPU
  (y reducir de igual forma)
- **AMI:** Imagen de Máquina de Amazon
- **RDP:** Remote Desktop Protocol

Flujo: Lanzar → Conectar → Usar

### Familias de instancias (5)
Uso general · Optimizadas para cómputo · Optimizadas para memoria · Cómputo
acelerado (GPU) · Optimizadas para almacenamiento

### Cómo aprovisionar recursos
3 formas: Consola de administración de AWS, CLI (interfaz de línea de comandos),
SDK (kit de desarrollo de software)

### Precios de EC2
- **Bajo demanda:** pago por hora/segundo sin compromiso
- **Savings Plans:** hasta 72% de ahorro por comprometerse 1-3 años
- **Instancias reservadas:** hasta 75% menos por 1-3 años
- **Instancias spot:** hasta 90% menos, pero AWS puede interrumpirlas
- **Hosts dedicados:** servidor físico exclusivo, control total
- **Instancias dedicadas:** hardware exclusivo para tu cuenta, aisladas de otros
  clientes

## Escalado EC2: escalabilidad y elasticidad
- **Escalabilidad:** potencial de un sistema para crecer con el tiempo (vertical =
  más recursos/capacidad; horizontal = más máquinas)
- **Elasticidad:** ajuste dinámico automático según la demanda en tiempo real
- **EC2 Auto Scaling:** ajusta automáticamente la cantidad de instancias según la
  demanda — escalado dinámico o predictivo (capacidad mínima, deseada, máxima)

## Elastic Load Balancing (ELB)
Un balanceador de carga recibe solicitudes y las dirige a las instancias — único
punto de contacto para el tráfico web.

**Métodos de enrutamiento:**
- **Round Robin:** distribuye el tráfico de forma uniforme y cíclica
- **Least Connections:** dirige al servidor con menos conexiones activas
- **IP Hash:** usa la IP del cliente para dirigir siempre al mismo servidor
- **Least Response Time:** dirige al servidor con el tiempo de respuesta más
  rápido

## Mensajería y colas
- **Arquitectura estrechamente acoplada:** los componentes se comunican
  directamente — si uno falla, probablemente el resto también
- **Arquitectura débilmente acoplada:** usa colas de mensajes entre componentes,
  más resiliente

- **Amazon SQS (Simple Queue Service):** envía, almacena y recibe mensajes entre
  componentes. Los datos dentro de un mensaje se llaman "carga útil"; los
  mensajes se colocan en cola hasta ser procesados.
- **Amazon SNS (Simple Notification Service):** canal de entrega de mensajes que
  necesita respuesta inmediata — notificaciones a usuarios por push, SMS, correo.
- **Amazon EventBridge:** servicio sin servidor que dirige eventos desde fuentes
  personalizadas, simplificando recepción, filtrado, transformación y entrega.
  Permite sistemas escalables basados en eventos.

**Aplicaciones monolíticas vs. microservicios:** en una monolítica, todo (pedidos,
inventario, pagos, envío) está en un solo servicio; en microservicios, cada parte
es un servicio independiente conectado a los demás.
