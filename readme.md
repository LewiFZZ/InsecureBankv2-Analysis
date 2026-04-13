# InsecureBankv2 — Análisis de Seguridad Android

Repositorio de evidencias del análisis de seguridad realizado sobre la aplicación
**InsecureBankv2** como parte de la actividad NF3 del módulo *Puesta en Producción
Segura* (5023) del Ciclo de Especialización en Ciberseguridad en Entornos de IT.

## Contenido del repositorio

| Carpeta / Archivo | Descripción |
|---|---|
| `Static_Analisis.pdf` | Informe completo generado por MobSF v4.5.0 (score 28/100 — CRITICAL) |
| `screenshots/` | Capturas de Wireshark, ADB y MobSF Dynamic Analyzer |
| `InsecureBankv2.apk.jadx` | Código fuente descompilado con JADX |

## Vulnerabilidades identificadas

| ID | Vulnerabilidad | Severidad | OWASP |
|---|---|---|---|
| VULN-01 | Comunicación HTTP sin cifrado | CRÍTICO | M5 |
| VULN-02 | Bypass de autenticación via ADB | CRÍTICO | M4 |
| VULN-03 | Almacenamiento inseguro (SharedPreferences) | ALTO | M2 |
| VULN-04 | Credenciales transmitidas por Intent | ALTO | M7 |
| VULN-05 | Exposición de endpoints del servidor | ALTO | M5 |
| VULN-06 | Modo debug habilitado en producción | ALTO | M7 |
| VULN-07 | allowBackup habilitado | MEDIO | M2 |
| VULN-08 | Vulnerabilidad Janus (firma solo v1) | ALTO | M7 |

## Herramientas utilizadas

- **MobSF v4.5.0** — Análisis estático y dinámico
- **Wireshark** — Captura y análisis de tráfico de red
- **JADX** — Descompilación e ingeniería inversa del APK
- **ADB** — Interacción con el emulador Android
- **Android Studio** — Emulador AOSP API 28 (Android 9.0)

## Aplicación analizada

- **Nombre:** InsecureBankv2
- **Paquete:** `com.android.insecurebankv2`
- **Autor original:** [Dinesh Shetty](https://github.com/dineshshetty/Android-InsecureBankv2)
- **Propósito:** Aplicación intencionalmente vulnerable para formación en pentesting móvil

## Aviso legal

Este análisis se realizó en un entorno controlado con fines exclusivamente educativos.
Todos los datos expuestos (credenciales, cuentas, importes) son ficticios y pertenecen
a la aplicación de laboratorio. No se realizaron pruebas sobre sistemas reales.

---

*Leví Josué Candeias de Figueiredo — 2026*