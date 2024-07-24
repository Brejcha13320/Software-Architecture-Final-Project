
<p  align="center"  >

<img  src="https://handwiki.org/wiki/images/thumb/d/d5/UML_logo.svg/375px-UML_logo.svg.png"  width="200"  />

<img  src="https://www.ovhcloud.com/sites/default/files/styles/text_media_horizontal/public/2021-04/K8S-logo.png"  width="160"  />

<img  src="https://static-00.iconduck.com/assets.00/docker-icon-1024x876-69aqwp3k.png"  width="160"  />

</p>

  

##  Presentación

  

- Universidad San Buenaventura Cali

  

- Especialización en Procesos de Desarrollo de Software

  

- Arquitectura de Software

  

##  Autor

  

- Jesus David Mejia Vergara

- Christian David Fajardo Alzate

- Edgar Gustavo Navarro Renza

- Jhon Edinson Acevedo Rojas  

#  Sistema de Monitoreo y Telemetría para Empresa de Buses

  

##  Contexto

  

- La empresa de transporte de pasajeros "Buses Seguros S.A." busca implementar un sistema de monitoreo y telemetría para mejorar la seguridad y eficiencia de su flota de autobuses. Cada autobús estará equipado con un cluster Kubernetes que recolectará datos de diversos sensores (combustible, presión de aire en las llantas, ambiente, temperatura, velocidad y GPS). Estos datos se procesarán en tiempo real para generar alertas y se transmitirán a la central de la empresa cuando el autobús llegue a las terminales, usando colas de mensajería para asegurar la captura y transmisión de todos los datos.

  

- El diagrama muestra los componentes principales, incluyendo los sensores en el bus, el cluster Kubernetes en el bus, los pods para cada sensor, un pod de colector de datos, colas de mensajería (RabbitMQ o Kafka), y los componentes para la transmisión de datos al sistema central cuando el bus llega a las terminales. También se incluye un sistema de monitoreo en tiempo real para alertas de velocidad.

  

##  Objetivos

  

-  **Monitoreo en Tiempo Real:** Capturar y procesar datos de múltiples sensores en el autobús en tiempo real para proporcionar una visión actualizada de las condiciones y el rendimiento del autobús.

  

-  **Almacenamiento y Transmisión de Datos Confiable:** Utilizar colas de mensajería (RabbitMQ o Kafka) para asegurar que todos los datos de los sensores se almacenen temporalmente y se transmitan de manera confiable a la central sin pérdida de información.

  

-  **Escalabilidad y Flexibilidad:** Implementar un cluster Kubernetes en cada autobús para gestionar los contenedores que procesan los datos de los sensores, permitiendo la fácil adición de nuevos sensores o la modificación de los existentes sin interrumpir el sistema.

  

-  **Integración Eficiente con la Central:** Transmitir los datos recopilados en formato JSON a los servicios de recepción en la central cuando los autobuses arriben a las terminales, asegurando una integración fluida y eficiente con los sistemas centrales.

  

-  **Análisis y Almacenamiento de Datos:** Procesar y almacenar los datos recibidos en bases de datos en la central para su posterior análisis, permitiendo la generación de informes y la toma de decisiones basadas en datos históricos y en tiempo real.

  

-  **Generación de Alertas:** Monitorear la velocidad del autobús en tiempo real y generar alertas automáticas si se superan las restricciones locales, mejorando la seguridad y el cumplimiento de las normativas.

  

-  **Optimización de Recursos:** Utilizar contenedores Docker y clusters Kubernetes para optimizar el uso de recursos en cada autobús, asegurando que el sistema sea eficiente y tenga un bajo impacto en el rendimiento del autobús.

  

-  **Mantenimiento y Actualización Fácil:** Facilitar el mantenimiento y la actualización del sistema mediante el uso de tecnologías de contenedorización y orquestación (Docker y Kubernetes), permitiendo desplegar nuevas versiones de software sin interrupciones significativas.

  

-  **Seguridad de los Datos:** Asegurar que los datos transmitidos desde los autobuses a la central estén protegidos mediante encriptación y mecanismos de autenticación, garantizando la privacidad y la integridad de la información.

  

-  **Cumplimiento Normativo:** Cumplir con las regulaciones locales e internacionales respecto a la operación de vehículos de transporte, especialmente en lo que se refiere a la velocidad y las condiciones de operación, ayudando a la empresa a evitar multas y mejorar la seguridad en las carreteras.

  
  

##  Descripción del Proceso
