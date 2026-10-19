# Módulo 3: Exploración de los servicios de cómputo

## Introducción a la computación sin servidor
Permite ejecutar apps sin administrar infraestructura.

- **Servicios no administrados** (ej. EC2): el cliente es responsable del cuidado,
  mantenimiento y actualizaciones
- **Servicios administrados:** transfieren más responsabilidad a AWS, con
  distintos grados de personalización (ej. ELB, SNS, SQS)
- **Servicios completamente administrados** (serverless, ej. AWS Lambda): no se
  puede ver ni acceder a la infraestructura subyacente; AWS se encarga de todo
  (aprovisionamiento, escalado, disponibilidad, mantenimiento)

## AWS Lambda
Servicio administrado sin servidor (cómputo serverless). Consiste en crear
funciones y configurar un "disparador" (trigger) — duración máxima de 15 minutos.
Procesos rápidos basados en eventos; escala automáticamente según el volumen de
solicitudes.

**Casos de uso:** procesamiento de imágenes en tiempo real, entrega de contenido
personalizado, gestión de eventos en tiempo real.

**AWS IAM** (Identity and Access Management) — control de permisos.

## Contenedores y orquestación en AWS
Un **clúster de servidores** es un grupo de servidores conectados que funcionan
como una sola unidad lógica. Los **contenedores** empaquetan todo lo que una app
necesita para ejecutarse: código, tiempo de ejecución, dependencias y
configuración.

**Contenedores vs. máquinas virtuales:** los contenedores comparten el sistema
operativo del host (más rápidos y livianos); las VM usan un hipervisor para
sistemas operativos completos e independientes (menos eficientes, inicio más
lento).

### Servicios de orquestación
Gestionan el ciclo de vida de los contenedores (iniciar, detener, ejecutar) y
escalan automáticamente.
- **Amazon ECS** (Elastic Container Service): simplificado, integrado, totalmente
  administrado
- **Amazon EKS** (Elastic Kubernetes Service): plataforma de código abierto, más
  compleja, más control y flexibilidad

### Registro de contenedores
- **Amazon ECR** (Elastic Container Registry): registro Docker totalmente
  administrado que almacena imágenes de contenedores

### Dónde se ejecutan
- **EC2:** tú gestionas la infraestructura
- **AWS Fargate:** sin servidor, solo gestionas los contenedores (eficiente para
  startups o equipos pequeños con tráfico variable)

**Tipos de lanzamiento:**
- ECS/EKS con EC2 → ideal para empresas que necesitan control total de la
  infraestructura
- ECS/EKS con Fargate → ideal para equipos pequeños/startups que no quieren
  administrar servidores

### Otros servicios de cómputo
- **Elastic Beanstalk:** servicio completamente administrado que optimiza
  implementación, administración y escalado de apps web. Ideal para apps web,
  APIs RESTful, backend móvil, microservicios.
- **AWS Batch:** servicio administrado para ejecutar cargas de trabajo por
  lotes — administra y optimiza recursos según los requisitos del trabajo. Ideal
  para cómputo científico, análisis de riesgos financieros, machine learning,
  investigación genómica.
- **Lightsail:** servidores privados virtuales (VPS) — almacenamiento, bases de
  datos y redes. Ideal para apps web básicas, sitios con poco tráfico, blogs,
  entornos de desarrollo.
- **Outposts:** solución de nube híbrida que extiende la infraestructura y
  servicios de AWS a centros de datos propios. Ideal para baja latencia,
  ubicaciones remotas, cumplimiento normativo.
