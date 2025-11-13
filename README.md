# 🔰 Escuadrón Financiero — Demo Pública  
*Plataforma profesional para gestión de préstamos diseñada para personal militar.*

Este repositorio contiene una **demostración técnica** del proyecto **Escuadrón Financiero**, un sistema completo de administración de solicitudes de préstamo, documentos, contratos, planes de pago, panel administrativo y portal del usuario.

> ⚠️ **Nota:**  
> Esta es solo una **versión de muestra**.  
> El código fuente completo es **privado** y no se incluye por motivos de seguridad, privacidad y propiedad intelectual.

---

# Escuadrón Financiero API (Versión Demo)

A secure and modular **RESTful API** built for **Escuadrón Financiero**, a financial platform designed to manage military loan applications, digital contracts, and payment plans.  
This backend powers both the user and admin interfaces of the system.

[Link API Render](https://escuadron-financiero-back-end.onrender.com)

---

## 🚀 Features (Resumen General)

- **Arquitectura modular limpia** (helpers, usecases, middlewares, models, routes, utils)  
- **Autenticación JWT con control de roles** (Admin & User)  
- **Flujo completo de solicitud de préstamo**  
- **Generación automática de contratos PDF** con firma digital/manual  
- **Planes de pago automáticos** según monto y modalidad  
- **Integración AWS S3** para documentos y contratos  
- **SendGrid** para emails transaccionales  
- **MongoDB Atlas** con Mongoose  
- **Capa de seguridad avanzada**: Helmet, CORS, Rate Limiting, Sanitización  
- **Endpoint de contacto** protegido por limitador de velocidad  

---

## 🏗️ Arquitectura del Proyecto (Demo)

```
src/
│
├── helpers/              # Contract & PDF generation utilities
├── lib/                  # Integrations (AWS, DB, Email, Encryption, JWT)
│   ├── AWS/
│   ├── DB/
│   ├── Email/
│   ├── encryptions.js
│   └── jwt.js
│
├── middlewares/          # Auth, role check, upload handlers, rate limiters
├── models/               # Mongoose schemas (User, Application, Credit, etc.)
│
├── routes/               # All API routes
│   ├── admin/
│   ├── user/
│   ├── auth.routes.js
│   └── contact.routes.js
│
├── templates/            # Contract & email templates
├── usecases/             # Business logic
├── utils/                # Global utils
├── views/                # HTML Responses
│
└── server.js             # Express configuration
```

---

## ⚙️ Variables de Entorno (Demo)

```bash
PORT=4000

# MongoDB
DB_USER=demo
DB_PASSWORD=demo
DB_HOST=demo.mongodb.net
DB_NAME=escuadronfinanciero

# JWT
JWT_SECRET=demo_secret

# AWS S3
AWS_REGION=us-east-1
AWS_ACCESS_KEY_ID=demo_key
AWS_SECRET_ACCESS_KEY=demo_secret
AWS_BUCKET_NAME=demo_bucket

# SendGrid
SENDGRID_API_KEY=demo_key

# Frontend URL
FRONTEND_URL=https://demo-frontend.com
```

---

## 📡 Endpoints Principales (Demo)

### 🔑 AUTH
- Registro, Login, Validación de Token  
- Recuperación de contraseña  
- Verificación de correo  
- Obtener perfil  

### 👤 USER
- Crear y gestionar solicitudes  
- Subir documentos  
- Firmar contrato  
- Ver créditos y subir comprobantes  

### 🛠️ ADMIN
- Revisar solicitudes  
- Aprobar/Rechazar  
- Generar contratos y activar créditos  
- Validar pagos del usuario  

### 📬 CONTACT
- Enviar mensajes vía SendGrid (rate limited)

---

## 🧠 Tech Stack

- Node.js + Express  
- MongoDB + Mongoose  
- AWS S3  
- SendGrid  
- JWT  
- Helmet + Rate Limit + CORS  

---

## 💻 Scripts

```bash
npm run dev
npm start
```

---

## 📘 Licencia

ISC License — Demo Version  
© 2025 Escuadrón Financiero

---

## 👤 Autor

**Adán Lugo Barrientos**  
Full-Stack Developer — Escuadrón Financiero  
GitHub: https://github.com/ElderL99