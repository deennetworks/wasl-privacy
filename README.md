# Política de privacidad de Wasl

**Última actualización: 29 de octubre de 2026**

Wasl (وصل) es una aplicación del Corán y de los horarios de rezo creada por Deen Networks. Esta política explica de forma directa qué datos usa la app y qué se hace con ellos.

**El resumen:** Wasl no muestra anuncios y no usa analítica ni rastreadores. Por defecto, todo lo que la app guarda se queda en tu dispositivo. Solo sale algo de él en dos casos que eliges tú: si inicias sesión con Google en Android (una cuenta **opcional** para sincronizar tus rezos y marcadores) y el registro del dispositivo para las notificaciones push del iPhone (OneSignal). En iPhone, la cuenta opcional con **Iniciar sesión con Apple** se guarda en el llavero del teléfono y **no se envía a ningún servidor**. Todo se explica más abajo.

## Cómo funciona (y por qué casi no hay nada que recopilar)

- Wasl funciona entera en tu teléfono: los horarios, el Corán y tu historial no salen de él, y no hay ningún servidor nuestro. (Las excepciones son la cuenta opcional de Android y el registro para las notificaciones push del iPhone.)
- La versión para Android usa Internet **solo para la cuenta opcional**: si no inicias sesión, no envía nada.
- El texto del Corán y sus traducciones **vienen incluidos en la app**: no se descargan de ningún servidor.
- Los horarios de rezo y la dirección de la Qibla se calculan **en el propio dispositivo**, a partir de tu ubicación o de la ciudad que elijas.

## Qué guarda la app en tu dispositivo

| Dato | Para qué | Dónde está |
| --- | --- | --- |
| Ubicación aproximada — **opcional** | Calcular los horarios de rezo y la dirección de la Qibla | Solo en tu teléfono: se calcula ahí mismo y no se envía a ningún servidor nuestro |
| Ciudad, método de cálculo, madhab e idioma | Recordar tu configuración | Almacenamiento privado de la app |
| Marcas de rezos, racha e historial | Que la app lleve tu registro | Almacenamiento privado de la app |
| Progreso de lectura y marcadores | «Continuar leyendo» y tus referencias | Almacenamiento privado de la app |
| Identificador de Apple, nombre y correo — solo si inicias sesión con Apple en iPhone | Mostrar tu cuenta y permitir eliminarla | Llavero del iPhone; no se envía a ningún servidor |

La ubicación es **opcional**: si no la concedes, puedes elegir tu ciudad a mano y todo funciona igual.

## Cuenta opcional en iPhone (Iniciar sesión con Apple)

En la primera apertura, la app ofrece **iniciar sesión con Apple**; el botón **Omitir** está visible y la app funciona entera sin cuenta. Si entras, la app guarda en el **llavero del iPhone** el identificador estable de Apple y, si lo autorizas, tu nombre y tu correo. No hay servidor nuestro, no se guardan tokens de Apple y esa información no se usa para publicidad, analítica ni para vincularla al push.

- La cuenta no da acceso a ninguna función: sirve para mostrar quién ha iniciado sesión y poder eliminarla.
- Se guarda con `AfterFirstUnlockThisDeviceOnly`: no se sincroniza con iCloud y no sale del teléfono.
- Si retiras el acceso de Wasl a tu Apple ID desde los Ajustes del iPhone, la app cierra la sesión; tus rezos, historial, lectura y ajustes se quedan.
- Para **eliminar la cuenta**, abre **Ajustes → icono de persona (arriba a la derecha) → Eliminar cuenta**. Se borran la identidad y todos los datos de Wasl en este iPhone (historial, marcas, progreso, marcadores y ajustes) de forma inmediata, con confirmación.

## Cuenta opcional y sincronización (Android)

Desde la versión 0.3.0, la app de Android te deja, **si quieres**, iniciar sesión con tu cuenta de Google para guardar una copia de algunos datos en la nube y recuperarlos en otro teléfono. Sin cuenta, la app funciona exactamente igual y no envía nada.

| Dato | Para qué |
| --- | --- |
| Correo, nombre e identificador de tu cuenta de Google | Identificar tu cuenta (te los pide Google al iniciar sesión) |
| Rezos marcados de cada día | Tenerlos en todos tus teléfonos |
| Marcadores del Corán y posición de lectura | Tenerlos en todos tus teléfonos |

- Se procesan con **Google Firebase** (Firebase Authentication para el inicio de sesión y Cloud Firestore para los datos), como proveedor técnico. Los datos sincronizados se guardan en servidores de Google en Europa.
- Viajan cifrados (HTTPS) y las reglas de la base de datos solo dejan leerlos y escribirlos a tu propia cuenta. Wasl no ve ni guarda tu contraseña: el inicio de sesión lo hace Google.
- **No se sube** nada más: ni tu ubicación, ni tu ciudad, ni tus ajustes o avisos.
- No se usan para publicidad, analítica ni perfiles, y no se venden ni se comparten con nadie.
- Puedes **cerrar sesión** cuando quieras (deja de sincronizar) o **eliminar la cuenta** en Ajustes → icono de persona (arriba a la derecha) → Eliminar cuenta: se borran al momento la cuenta y todo lo guardado en la nube; lo que hay en tu teléfono se queda. También puedes pedirlo por correo: ver [Eliminar la cuenta](https://deennetworks.github.io/wasl-privacy/eliminar-cuenta.html).

## Permisos en Android

| Permiso | Para qué |
| --- | --- |
| Ubicación aproximada | Horarios de rezo y Qibla (opcional) |
| Notificaciones | Los avisos de los rezos |
| Alarmas exactas | Que el aviso suene a su hora |
| Ejecución tras reinicio | Reprogramar los avisos si reinicias el teléfono |
| Internet | Solo la cuenta opcional y la sincronización |

Las bibliotecas de AndroidX que la app usa para los widgets añaden permisos auxiliares (mantener el dispositivo activo, consultar el estado de la red), que no envían datos.

## Permisos en iPhone

| Permiso | Para qué |
| --- | --- |
| Ubicación (al usar la app) | Horarios de rezo y Qibla (opcional) |
| Notificaciones | Los avisos de los rezos y las notificaciones que envía el administrador de la app |

## Notificaciones push en iPhone

La versión de iPhone puede recibir **notificaciones push** (avisos que el administrador de Wasl envía desde fuera de la app, por ejemplo un comunicado). La entrega la hace **OneSignal**, un servicio de notificaciones, a través del sistema de notificaciones de Apple (APNs):

- Al activar las notificaciones, tu dispositivo se registra con OneSignal con un **identificador de suscripción** (derivado del identificador que asigna Apple). Es lo único que se envía: **ni nombre, ni correo, ni cuenta**, y no va asociado a tu identidad.
- Ese identificador se usa **solo** para entregar las notificaciones de la app. No se usa para publicidad, ni para elaborar perfiles, ni para rastrearte.
- Los **avisos de los rezos no pasan por OneSignal**: los programa tu propio iPhone (notificaciones locales) y se calculan en el dispositivo.
- Si no quieres nada de esto, basta con **no conceder el permiso de notificaciones**: la app funciona igual.

## Lo que Wasl no hace

- No exige cuenta: en iPhone la de Apple es opcional y local; en Android la de Google es opcional. La app funciona igual sin ella.
- No usa anuncios, analítica ni rastreadores.
- No vende datos ni los usa para publicidad o seguimiento. Los únicos terceros que intervienen son proveedores técnicos: **Apple** para Iniciar sesión con Apple (solo autenticación; los datos se quedan en el teléfono), **Google Firebase** para la cuenta opcional de Android y **OneSignal** para las notificaciones push del iPhone.
- No elabora perfiles ni toma decisiones automatizadas sobre ti.

## Copias de seguridad del teléfono

Si tienes activadas las copias de seguridad del sistema (tu cuenta de Google en Android, iCloud en iPhone), es posible que los datos de la app se incluyan en esa copia. Es una función del propio teléfono: la gestiona tu proveedor (Google o Apple) y se controla desde los ajustes del dispositivo. El desarrollador no accede a ella.

## En iPhone

En iPhone, todo se calcula y se guarda en el dispositivo. La cuenta opcional con Iniciar sesión con Apple también se queda en el llavero del teléfono y no se envía a ningún servidor; se elimina desde Ajustes → icono de persona → Eliminar cuenta, junto con los datos de la app en este iPhone. Al usar tu ubicación, el sistema de Apple puede traducir las coordenadas a un nombre de lugar y una zona horaria con su servicio de mapas; esa consulta la hace el sistema operativo bajo la política de privacidad de Apple, y Wasl no la recibe ni la almacena. Las notificaciones push se explican arriba.

## Tus datos están en tus manos

- Al desinstalar la app se borra todo lo que guardaba (y el registro para el push se da de baja); también puedes borrar sus datos desde los ajustes de tu teléfono. Lo guardado en la nube con la cuenta opcional de Android **no** se borra al desinstalar: para eso, elimina la cuenta.
- La cuenta se elimina desde la app (Ajustes → icono de persona → Eliminar cuenta). En Android se borra además la copia en la nube; en iPhone no hay copia en la nube. También puedes pedirlo por correo: ver [Eliminar la cuenta](https://deennetworks.github.io/wasl-privacy/eliminar-cuenta.html).
- Para cualquier otra petición sobre tus datos (acceso, rectificación), escríbenos al correo de contacto.

## Menores

Wasl es apta para todos los públicos. No pide ningún dato para funcionar; la cuenta es opcional.

## Cambios en esta política

Si esta política cambia, la versión actualizada se publicará aquí mismo con una fecha nueva. Si el cambio fuera importante, se avisará en la ficha de la app.

## Contacto

Dudas sobre privacidad: **deennetworks@gmail.com**

---

# Privacy Policy — Wasl

**Last updated: 29 October 2026**

Wasl (وصل) is a Quran and prayer-times app made by Deen Networks. This policy explains plainly what data the app uses and what happens to it.

**The short version:** Wasl shows no ads and uses no analytics or trackers. By default, everything the app saves stays on your device. Something leaves it only in two cases you choose: if you sign in with Google on Android (an **optional** account to sync your prayers and bookmarks) and the device registration for iPhone push notifications (OneSignal). On iPhone, the optional **Sign in with Apple** account is stored in the phone's Keychain and **is never sent to a server**. Everything is explained below.

## How it works (and why there is almost nothing to collect)

- Wasl runs entirely on your phone: prayer times, the Quran and your history never leave it, and there is no server of ours. (The exceptions are the optional Android account and the registration for iPhone push notifications.)
- The Android version uses the Internet **only for the optional account**: if you do not sign in, it sends nothing.
- The Quran text and its translations **are included in the app**: nothing is downloaded from a server.
- Prayer times and the Qibla direction are calculated **on the device itself**, from your location or the city you choose.

## What the app stores on your device

| Data | What it is for | Where it lives |
| --- | --- | --- |
| Approximate location — **optional** | Calculating prayer times and the Qibla direction | On your phone only: computed there and never sent to any server of ours |
| City, calculation method, madhab and language | Remembering your settings | The app's private storage |
| Prayer marks, streak and history | Keeping your record | The app's private storage |
| Reading progress and bookmarks | "Continue reading" and your references | The app's private storage |
| Apple identifier, name and email — only if you sign in with Apple on iPhone | Showing your account and allowing deletion | iPhone Keychain; never sent to any server |

Location is **optional**: if you do not grant it, you can pick your city by hand and everything works the same.

## Optional iPhone account (Sign in with Apple)

On first launch the app offers **Sign in with Apple**; the **Skip** button is visible and the app works fully without an account. If you sign in, the app stores the stable Apple identifier and, if you authorize it, your name and email in the **iPhone Keychain**. There is no server of ours, no Apple tokens are stored, and that information is not used for advertising, analytics or linked to push.

- The account does not unlock any feature: it shows who is signed in and allows deletion.
- It is stored with `AfterFirstUnlockThisDeviceOnly`: it is not synced to iCloud and does not leave the phone.
- If you remove Wasl's access to your Apple ID in iPhone Settings, the app signs out; your prayers, history, reading and settings stay.
- To **delete the account**, open **Settings → person icon (top right) → Delete account**. The identity and all Wasl data on this iPhone (history, marks, reading progress, bookmarks and settings) are erased immediately, with confirmation.

## Optional account and sync (Android)

Since version 0.3.0, the Android app lets you, **if you want**, sign in with your Google account to keep a copy of some data in the cloud and get it back on another phone. Without an account, the app works exactly the same and sends nothing.

| Data | What it is for |
| --- | --- |
| Your Google account's email, name and identifier | Identifying your account (Google asks you when you sign in) |
| Prayers marked each day | Having them on all your phones |
| Quran bookmarks and reading position | Having them on all your phones |

- They are processed by **Google Firebase** (Firebase Authentication for sign-in and Cloud Firestore for the data), acting as a technical provider. Synced data is stored on Google servers in Europe.
- They travel encrypted (HTTPS), and the database rules only let your own account read or write them. Wasl never sees or stores your password: Google handles the sign-in.
- **Nothing else is uploaded**: not your location, your city, your settings or your reminders.
- They are not used for advertising, analytics or profiling, and are never sold or shared with anyone.
- You can **sign out** at any time (syncing stops) or **delete the account** in Settings → person icon (top right) → Delete account: the account and everything stored in the cloud are erased right away; what is on your phone stays. You can also ask by email: see [Delete your account](https://deennetworks.github.io/wasl-privacy/eliminar-cuenta.html).

## Android permissions

| Permission | Why |
| --- | --- |
| Approximate location | Prayer times and Qibla (optional) |
| Notifications | Prayer reminders |
| Exact alarms | So reminders fire on time |
| Run after restart | Rescheduling reminders after a reboot |
| Internet | Only the optional account and sync |

The AndroidX libraries the app uses for its widgets add auxiliary permissions (keeping the device awake, checking network state); none of them send data.

## iPhone permissions

| Permission | Why |
| --- | --- |
| Location (while using the app) | Prayer times and Qibla (optional) |
| Notifications | Prayer reminders and notices sent by the app's administrator |

## Push notifications on iPhone

The iPhone version can receive **push notifications** (notices the Wasl administrator sends from outside the app, for example an announcement). Delivery is handled by **OneSignal**, a notification service, through Apple's push system (APNs):

- When you enable notifications, your device registers with OneSignal with a **subscription identifier** (derived from the identifier Apple assigns). That is the only thing sent: **no name, no email, no account**, and it is not linked to your identity.
- That identifier is used **only** to deliver the app's notifications. It is not used for advertising, profiling, or tracking you.
- **Prayer reminders do not go through OneSignal**: your own iPhone schedules them (local notifications) and they are computed on the device.
- If you do not want any of this, simply **do not grant the notification permission**: the app works the same.

## What Wasl does not do

- No account required: on iPhone the Apple account is optional and local; on Android the Google account is optional. The app works the same without one.
- No ads, analytics or trackers.
- No selling of data and no use of it for advertising or tracking. The only third parties involved are technical providers: **Apple** for Sign in with Apple (authentication only; the data stays on the phone), **Google Firebase** for the optional Android account and **OneSignal** for iPhone push notifications.
- No profiling and no automated decisions about you.

## Device backups

If you have system backups enabled (your Google account on Android, iCloud on iPhone), the app's data may be included in that backup. That is a feature of your phone: it is handled by your provider (Google or Apple) and controlled from your device settings. The developer has no access to it.

## On iPhone

On iPhone, everything is computed and stored on the device. The optional Sign in with Apple account also stays in the phone's Keychain and is never sent to a server; it is deleted in Settings → person icon → Delete account, together with the app's data on this iPhone. When you use your location, Apple's system may translate the coordinates into a place name and time zone using its maps service; that lookup is made by the operating system under Apple's privacy policy, and Wasl does not receive or store it. Push notifications are explained above.

## Your data stays with you

- Uninstalling the app erases everything it stored (and the push registration is dropped); you can also clear its data from your phone settings. What the optional Android account stored in the cloud is **not** erased by uninstalling: to erase it, delete the account.
- The account can be deleted from the app (Settings → person icon → Delete account). On Android this also deletes the cloud copy; on iPhone there is no cloud copy. You can also ask by email: see [Delete your account](https://deennetworks.github.io/wasl-privacy/eliminar-cuenta.html).
- For any other request about your data (access, correction), write to the contact address.

## Children

Wasl is suitable for all audiences. It asks for no data in order to work; the account is optional.

## Changes to this policy

If this policy changes, the updated version will be published right here with a new date. Significant changes will be announced on the app's store listing.

## Contact

Privacy questions: **deennetworks@gmail.com**

<!-- Mantenimiento: este mismo texto se publica como página en index.html (GitHub Pages).
     Al cambiar la política, actualizar los dos archivos. -->
