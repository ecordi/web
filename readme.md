# Sistema de Reservas de Celeste

Un sistema completo de reservas para sesiones de sanación espiritual con integración de pagos, gestión de disponibilidad y panel de administración.

## 🌟 Características Principales

- **Sistema de Reservas Completo**: Calendario interactivo para reservar sesiones
- **Pagos con QR**: Integración con MercadoPago para pagos seguros
- **Reservas Temporales**: Bloqueo automático de horarios durante el proceso de pago
- **Panel de Administración**: Gestión completa de reservas, servicios y disponibilidad
- **Notificaciones**: Alertas del navegador para cambios importantes
- **Diseño Responsivo**: Funciona perfectamente en móviles, tablets y desktop
- **Base de Datos**: Persistencia de datos con Supabase

## 🚀 Tecnologías Utilizadas

- **Frontend**: Next.js 14, React, TypeScript
- **Styling**: Tailwind CSS, shadcn/ui
- **Base de Datos**: Supabase
- **Pagos**: MercadoPago API
- **Autenticación**: Sistema personalizado
- **Notificaciones**: Web Notifications API

## 📋 Requisitos Previos

- Node.js 18+ 
- Cuenta de Supabase
- Cuenta de MercadoPago (para pagos)

## ⚙️ Variables de Entorno

Crea un archivo `.env.local` con las siguientes variables:

```env
# Supabase
NEXT_PUBLIC_SUPABASE_URL=tu_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=tu_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=tu_service_role_key

# MercadoPago
MERCADOPAGO_ACCESS_TOKEN=tu_mercadopago_access_token

# Base URL (para webhooks)
NEXT_PUBLIC_BASE_URL=https://tu-dominio.com
```

## 🛠️ Instalación

1. **Clona el repositorio**
   ```bash
   git clone <repository-url>
   cd sistema-reservas-celeste
   ```

2. **Instala las dependencias**
   ```bash
   npm install
   ```

3. **Configura las variables de entorno**
   - Copia `.env.example` a `.env.local`
   - Completa todas las variables requeridas

4. **Configura la base de datos**
   - Las tablas se crean automáticamente al usar el sistema
   - O ejecuta los scripts SQL incluidos en `/sql`

5. **Inicia el servidor de desarrollo**
   ```bash
   npm run dev
   ```

6. **Abre tu navegador**
   - Ve a `http://localhost:3000`

## 📊 Estructura de la Base de Datos

### Tablas Principales

- **services**: Servicios disponibles (Registros Akáshicos, Limpieza Energética, etc.)
- **availability**: Días y horarios disponibles para reservas
- **bookings**: Reservas realizadas por los usuarios
- **admin_users**: Usuarios administradores del sistema

## 🎯 Funcionalidades

### Para Usuarios
- ✅ Reservar sesiones con calendario interactivo
- ✅ Seleccionar servicios disponibles
- ✅ Pagar con QR de MercadoPago
- ✅ Recibir confirmaciones por email
- ✅ Contacto directo por WhatsApp

### Para Administradores
- ✅ Gestionar disponibilidad de horarios
- ✅ Ver y administrar todas las reservas
- ✅ Editar servicios y precios
- ✅ Cambiar estados de reservas
- ✅ Reprogramar sesiones
- ✅ Enviar emails automáticos

## 🔧 Uso del Sistema

### Acceso de Usuario
1. Ve a la página principal
2. Haz clic en "Reservar Sesión"
3. Selecciona servicio, fecha y hora
4. Completa tus datos
5. Paga con el QR generado
6. ¡Listo! Recibirás confirmación

### Acceso de Administrador
1. Ve a `/admin`
2. Inicia sesión con tus credenciales
3. Gestiona reservas en las pestañas:
   - **Disponibilidad**: Configura días y horarios
   - **Reservas**: Ve y administra todas las reservas
   - **Servicios**: Edita precios y descripciones

## 🔐 Seguridad

- Autenticación requerida para panel de administración
- Validación de datos en frontend y backend
- Sanitización de inputs
- Tokens seguros para sesiones
- HTTPS requerido en producción

## 📱 Páginas Principales

- `/` - Página principal con información y reservas
- `/admin` - Panel de administración
- `/booking/success` - Confirmación de pago exitoso
- `/booking/failure` - Error en el pago
- `/booking/pending` - Pago pendiente

## 🚀 Despliegue

### Vercel (Recomendado)
1. Conecta tu repositorio a Vercel
2. Configura las variables de entorno
3. Despliega automáticamente

### Otros Proveedores
- Asegúrate de que soporten Next.js 14
- Configura las variables de entorno
- Habilita HTTPS para webhooks de MercadoPago

## 🔄 Scripts Disponibles

```bash
npm run dev          # Servidor de desarrollo
npm run build        # Construir para producción
npm run start        # Servidor de producción
npm run lint         # Verificar código
```

## 🐛 Solución de Problemas

### Error de conexión a Supabase
- Verifica las variables de entorno
- Asegúrate de que las URLs sean correctas
- Revisa los permisos de las tablas

### Problemas con MercadoPago
- Verifica el access token
- Asegúrate de usar HTTPS en producción
- Revisa los logs de webhooks

### Reservas no aparecen
- Verifica la configuración de disponibilidad
- Revisa los logs del navegador
- Asegúrate de que las fechas sean futuras

## 📞 Soporte

Para soporte técnico:
- Revisa los logs en la consola del navegador
- Verifica las variables de entorno
- Contacta al desarrollador: [tu-email@ejemplo.com]

## 📄 Licencia

Este proyecto es privado y propietario. Todos los derechos reservados.

## 🙏 Créditos

Desarrollado con ❤️ para Celeste - Sanación Espiritual

---

**¿Necesitas ayuda?** Contacta por WhatsApp: +54 9 351 650-1371
```

¡Listo! Este README incluye:

✅ **Descripción completa** del sistema
✅ **Instrucciones de instalación** paso a paso
✅ **Configuración** de variables de entorno
✅ **Estructura** de la base de datos
✅ **Funcionalidades** para usuarios y admins
✅ **Guías de uso** detalladas
✅ **Solución de problemas** comunes
✅ **Información de despliegue**

El README está diseñado para que cualquier desarrollador pueda entender, instalar y mantener el sistema fácilmente.
