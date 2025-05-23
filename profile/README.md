# I-Wellness 


## 🌍 Descripción general

I-Wellness es una solución tecnológica concebida para fortalecer el ecosistema del turismo de bienestar en La Fortuna, Costa Rica. El sistema permite la interacción entre turistas, proveedores de servicios y administradores, a través de funcionalidades distribuidas en microservicios independientes, coordinadas mediante una interfaz centralizada accesible vía web.

La arquitectura está orientada a fomentar la colaboración y el valor compartido entre los actores del ecosistema, permitiendo a los proveedores gestionar sus servicios de forma autónoma, a los turistas registrar sus preferencias y acceder a recomendaciones personalizadas, y a los administradores visualizar datos estratégicos sobre el comportamiento turístico.

El diseño busca garantizar la personalización de la experiencia del usuario, la consolidación de información clave para la toma de decisiones, y la escalabilidad del sistema para futuras integraciones con nuevos servicios o regiones turísticas.

## 🧩 Arquitectura general

La solución se basa en microservicios desacoplados que se comunican entre sí mediante colas de mensajería (RabbitMQ). Cada componente cumple una responsabilidad específica.

### 📦 Microservicios principales

| Servicio               | Descripción                                                  |
|------------------------|--------------------------------------------------------------|
|  [`admin_users_api`](https://github.com/IWellnessTesis/IWellness_data_services/tree/main).      | Gestión de usuarios, autenticación y roles                   |
| [`providers_api`](https://github.com/IWellnessTesis/providers_api).        | Gestión de servicios turísticos            |
| [`user_preferences_api`](https://github.com/IWellnessTesis/user_preferences_api). | Registro y actualización de preferencias de turistas         |
| [`IWellness_Data_Services`](https://github.com/IWellnessTesis/IWellness_data_services/tree/main). | Almacenamiento de datos y analítica para dashboards     |
| [`Queue_Rabbit`](https://github.com/IWellnessTesis/Queue-Rabbit)         | Consumidor de colas RabbitMQ para persistencia de mensajes   |
| [`IWellness_DB`](https://github.com/IWellnessTesis/IWellness-DB). | Base de datos para la persistencia y análisis de datos

### 🎨 Frontend

-[`FrontEnd_IWellness`](https://github.com/IWellnessTesis/FrontEnd_IWellness). 
  Aplicación Angular que permite la interacción entre usuarios y los distintos microservicios.

## 🛠️ Tecnologías utilizadas

- Java 17 + Spring Boot
- Angular 19
- Firebase Authentication / JWT
- MySQL / SQLite
- RabbitMQ
- Docker / Docker Compose
- Python (para consumo de mensajes y analítica)

## 🔄 Comunicación entre servicios

La comunicación se da por:

- REST APIs (entre microservicios y frontend)
- RabbitMQ (para enviar eventos o datos transaccionales que deben persistirse en bloque)

## ⚙️ Instrucciones

1. Clonar los repositorios de cada microservicio y frontend
2. Leer el README de cada repo para conocer su funcionalidad especifica y levantar contenedores de ser necesario
3. Luego, ejecutar el front y los microservicios
4. Una vez esten en ejecución, ejecutar la cola, el consumidor, la base de datos de persistencia y el analista para que I-Wellness funcione de forma completa
5. Disfrutar de nuestro MVP! :)

# 🤝 EQUIPO
Somos 4 futuros ingenieros de la Pontificia Universidad Javeriana. Este es nuestro Trabajo de Grado!
- Maria Andrea Méndez
  ![Imagen de WhatsApp 2025-05-22 a las 22 23 10_24af235f](https://github.com/user-attachments/assets/d6bbf8a1-3fd9-4d9e-a510-260326e911af)
- Daniela Florez
- ![Imagen de WhatsApp 2025-05-22 a las 22 17 18_8b5d4c76](https://github.com/user-attachments/assets/74a6bdf7-c402-4ddb-8f7d-165ba9b6999e)
- Juan David Hernandez
- Sara Peña
