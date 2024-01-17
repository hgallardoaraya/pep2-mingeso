# PEP2 Métodos de Ingeniería de Software
Aplicación web con un estilo de arquitectura de microservicios desarrollada como proyecto para la asignatura Métodos de Ingeniería de Software de la USACH.

El foco de este proyecto está en implementar las distintas funcionalidades, cumplir con las reglas de negocio, utilizar una arquitectura de microservicios, contenerizar las aplicaciones y desplegarlas en un cluster de Kubernetes, ya sea en local o en la nube.

Las funcionalidades están dadas por un enunciado que nos sitúa en el contexto de un preuniversitario que necesita gestionar los pagos de arancel de sus estudiantes (ver "enunciado.pdf"), las historias de usuario que han sido implementadas son las siguientes:
 
- HU1: Ingreso de datos de los estudiantes desde pantalla. (M1)
- HU2: Listar datos de los estudiantes por pantalla. (M1)
- HU3: Generar cuotas de pago. (M2)
- HU4: Listar cuotas de pago de un estudiante y el estado de pago de cada cuota. (M2)
- HU5: Registrar pagos de cuotas de arancel. (M2)
- HU6: Importar notas de exámenes desde archivo Excel. (M3)
- HU7: Calcular planilla de pagos de arancel. (M3)
- HU8: Calcular reporte resumen de estado de pagos de los estudiantes. (M3)
  ▪ RUT estudiante
  ▪ Nombre del estudiante
  ▪ Nro. exámenes rendidos
  ▪ Promedio puntaje exámenes
  ▪ Monto total arancel a pagar
  ▪ Tipo Pago (Contado/Cuotas)
  ▪ Nro. total de cuotas pactadas
  ▪ Nro. cuotas pagadas
  ▪ Monto total pagado
  ▪ Fecha último pago
  ▪ Saldo por pagar
  ▪ Nro. Cuotas con retraso

## Tecnologias relevantes

- Docker para correr dentro de contenedores las distintas aplicaciones.
- Kubernetes para correr y gestionar los contenedores, se pueden ver las distintas configuraciones en /kubernetes.
- Spring Boot para el desarrollo de los tres microservicios, un config server, un service discovery, y un gateway. 
- MySQL como base de datos (se crea una por microservicio).
- Terraform para levantar el cluster kubernetes en Azure, se puede rervisar el script en /terraform.
- Next.js para el desarrollo del Frontend, sin embargo, el enfoque está en consumir las APIs y mostrar los datos, y no en la estética de la UI, esto debido a que lo más relevante del proyecto es comprender e implementar los componentes más básicos de una arquitectura de microservicios en un cluster de Kubernetes.
