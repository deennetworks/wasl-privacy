# Política de privacidad de Wasl

**Última actualización: 12 de octubre de 2026**

Wasl (وصل) es una aplicación del Corán y de los horarios de rezo creada por Deen Networks. Esta política explica de forma directa qué datos usa la app y qué se hace con ellos.

**El resumen:** Wasl **no recopila datos personales**, no tiene cuentas de usuario, no muestra anuncios y no usa analítica ni rastreadores. Todo lo que la app guarda se queda en tu dispositivo. La única conexión con el exterior es el registro del dispositivo para las notificaciones push del iPhone (OneSignal), explicado más abajo.

## Cómo funciona (y por qué casi no hay nada que recopilar)

- Wasl funciona entera en tu teléfono: los horarios, el Corán y tu historial no salen de él, y no hay ningún servidor nuestro. (La excepción es el registro del dispositivo para las notificaciones push del iPhone — ver «Notificaciones push en iPhone».)
- La versión para Android **no incluye el permiso de Internet** (`android.permission.INTERNET`), así que no puede transmitir nada por la red.
- El texto del Corán y sus traducciones **vienen incluidos en la app**: no se descargan de ningún servidor.
- Los horarios de rezo y la dirección de la Qibla se calculan **en el propio dispositivo**, a partir de tu ubicación o de la ciudad que elijas.

## Qué guarda la app (todo en tu dispositivo)

| Dato | Para qué | Dónde está |
| --- | --- | --- |
| Ubicación aproximada — **opcional** | Calcular los horarios de rezo y la dirección de la Qibla | Solo en tu teléfono: se calcula ahí mismo y no se envía a ningún servidor nuestro |
| Ciudad, método de cálculo, madhab e idioma | Recordar tu configuración | Almacenamiento privado de la app |
| Marcas de rezos, racha e historial | Que la app lleve tu registro | Almacenamiento privado de la app |
| Progreso de lectura y marcadores | «Continuar leyendo» y tus referencias | Almacenamiento privado de la app |

La ubicación es **opcional**: si no la concedes, puedes elegir tu ciudad a mano y todo funciona igual.

## Permisos en Android

| Permiso | Para qué |
| --- | --- |
| Ubicación aproximada | Horarios de rezo y Qibla (opcional) |
| Notificaciones | Los avisos de los rezos |
| Alarmas exactas | Que el aviso suene a su hora |
| Ejecución tras reinicio | Reprogramar los avisos si reinicias el teléfono |

Las bibliotecas de AndroidX que la app usa para los widgets añaden permisos auxiliares (mantener el dispositivo activo, consultar el estado de la red), que no permiten enviar datos. La app **no incluye el permiso de Internet**: no existe ninguna vía por la que pueda transmitir información.

## Permisos en iPhone

| Permiso | Para qué |
| --- | --- |
| Ubicación (al usar la app) | Horarios de rezo y Qibla (opcional) |
| Notificaciones | Los avisos de los rezos y las notificaciones que envía el administrador de la app |

## Notificaciones push en iPhone

La versión de iPhone puede recibir **notificaciones push** (avisos que el administrador de Wasl envía desde fuera de la app, por ejemplo un comunicado). La entrega la hace **OneSignal**, un servicio de notificaciones, a través del sistema de notificaciones de Apple (APNs):

- Al activar las notificaciones, tu dispositivo se registra con OneSignal con un **identificador de suscripción** (derivado del identificador que asigna Apple). Es lo único que se envía: **ni nombre, ni correo, ni cuenta** —la app no tiene cuentas— y no va asociado a tu identidad.
- Ese identificador se usa **solo** para entregar las notificaciones de la app. No se usa para publicidad, ni para elaborar perfiles, ni para rastrearte.
- Los **avisos de los rezos no pasan por OneSignal**: los programa tu propio iPhone (notificaciones locales) y se calculan en el dispositivo.
- Si no quieres nada de esto, basta con **no conceder el permiso de notificaciones**: la app funciona igual.

## Lo que Wasl no hace

- No pide cuenta ni registro.
- No usa anuncios, analítica ni rastreadores.
- No vende datos ni los usa para publicidad o seguimiento. El único tercero que interviene es **OneSignal**, como proveedor técnico de las notificaciones push del iPhone (con el único dato del punto anterior).
- No elabora perfiles ni toma decisiones automatizadas sobre ti.

## Copias de seguridad del teléfono

Si tienes activadas las copias de seguridad del sistema (tu cuenta de Google en Android, iCloud en iPhone), es posible que los datos de la app se incluyan en esa copia. Es una función del propio teléfono: la gestiona tu proveedor (Google o Apple) y se controla desde los ajustes del dispositivo. El desarrollador no accede a ella.

## En iPhone

La app funciona igual que en Android: todo se calcula y se guarda en el dispositivo. El matiz: al usar tu ubicación, el sistema de Apple puede traducir las coordenadas a un nombre de lugar y una zona horaria con su servicio de mapas; esa consulta la hace el sistema operativo bajo la política de privacidad de Apple, y Wasl no la recibe ni la almacena. Las notificaciones push se explican arriba.

## Tus datos están en tus manos

- Al desinstalar la app se borra todo lo que guardaba (y el registro para el push se da de baja); también puedes borrar sus datos desde los ajustes de tu teléfono.
- Como no recopilamos datos personales, no hay nada que podamos entregarte, corregir ni borrar: no hay tratamiento por nuestra parte.

## Menores

Wasl es apta para todos los públicos y no recopila datos de nadie, tampoco de menores.

## Cambios en esta política

Si esta política cambia, la versión actualizada se publicará aquí mismo con una fecha nueva. Si el cambio fuera importante, se avisará en la ficha de la app.

## Contacto

Dudas sobre privacidad: **deennetworks@gmail.com**

---

# Privacy Policy — Wasl

**Last updated: 12 October 2026**

Wasl (وصل) is a Quran and prayer-times app made by Deen Networks. This policy explains plainly what data the app uses and what happens to it.

**The short version:** Wasl **does not collect personal data**. There are no user accounts, no ads, and no analytics or trackers. Everything the app saves stays on your device. The only external connection is the device registration for iPhone push notifications (OneSignal), explained below.

## How it works (and why there is almost nothing to collect)

- Wasl runs entirely on your phone: prayer times, the Quran and your history never leave it, and there is no server of ours. (The exception is the device registration for iPhone push notifications — see "Push notifications on iPhone".)
- The Android version **does not include the Internet permission** (`android.permission.INTERNET`), so it cannot transmit anything over the network.
- The Quran text and its translations **are included in the app**: nothing is downloaded from a server.
- Prayer times and the Qibla direction are calculated **on the device itself**, from your location or the city you choose.

## What the app stores (all on your device)

| Data | What it is for | Where it lives |
| --- | --- | --- |
| Approximate location — **optional** | Calculating prayer times and the Qibla direction | On your phone only: computed there and never sent to any server of ours |
| City, calculation method, madhab and language | Remembering your settings | The app's private storage |
| Prayer marks, streak and history | Keeping your record | The app's private storage |
| Reading progress and bookmarks | "Continue reading" and your references | The app's private storage |

Location is **optional**: if you do not grant it, you can pick your city by hand and everything works the same.

## Android permissions

| Permission | Why |
| --- | --- |
| Approximate location | Prayer times and Qibla (optional) |
| Notifications | Prayer reminders |
| Exact alarms | So reminders fire on time |
| Run after restart | Rescheduling reminders after a reboot |

The AndroidX libraries the app uses for its widgets add auxiliary permissions (keeping the device awake, checking network state); none of them allow sending data. The app **does not include the Internet permission**: there is no way for it to transmit information anywhere.

## iPhone permissions

| Permission | Why |
| --- | --- |
| Location (while using the app) | Prayer times and Qibla (optional) |
| Notifications | Prayer reminders and notices sent by the app's administrator |

## Push notifications on iPhone

The iPhone version can receive **push notifications** (notices the Wasl administrator sends from outside the app, for example an announcement). Delivery is handled by **OneSignal**, a notification service, through Apple's push system (APNs):

- When you enable notifications, your device registers with OneSignal with a **subscription identifier** (derived from the identifier Apple assigns). That is the only thing sent: **no name, no email, no account** — the app has no accounts — and it is not linked to your identity.
- That identifier is used **only** to deliver the app's notifications. It is not used for advertising, profiling, or tracking you.
- **Prayer reminders do not go through OneSignal**: your own iPhone schedules them (local notifications) and they are computed on the device.
- If you do not want any of this, simply **do not grant the notification permission**: the app works the same.

## What Wasl does not do

- No account and no sign-up.
- No ads, analytics or trackers.
- No selling of data and no use of it for advertising or tracking. The only third party involved is **OneSignal**, acting as the technical provider for iPhone push notifications (with the single piece of data described above).
- No profiling and no automated decisions about you.

## Device backups

If you have system backups enabled (your Google account on Android, iCloud on iPhone), the app's data may be included in that backup. That is a feature of your phone: it is handled by your provider (Google or Apple) and controlled from your device settings. The developer has no access to it.

## On iPhone

The app behaves the same as on Android: everything is computed and stored on the device. The nuance: when you use your location, Apple's system may translate the coordinates into a place name and time zone using its maps service; that lookup is made by the operating system under Apple's privacy policy, and Wasl does not receive or store it. Push notifications are explained above.

## Your data stays with you

- Uninstalling the app erases everything it stored (and the push registration is dropped); you can also clear its data from your phone settings.
- Since we do not collect personal data, there is nothing for us to provide, correct or delete: no processing takes place on our side.

## Children

Wasl is suitable for all audiences and collects no one's data, children included.

## Changes to this policy

If this policy changes, the updated version will be published right here with a new date. Significant changes will be announced on the app's store listing.

## Contact

Privacy questions: **deennetworks@gmail.com**

<!-- Mantenimiento: este mismo texto se publica como página en index.html (GitHub Pages).
     Al cambiar la política, actualizar los dos archivos. -->
