# LM Express - Simulacro WhatsApp

Flow de n8n para demo/simulacro del agente de WhatsApp para LM Express (courier Costa Rica).

## Qué hace

El cliente manda un mensaje por WhatsApp preguntando por su paquete → el agente busca en Google Sheets → responde con el estado, fecha estimada y sucursal de retiro.

## Google Sheet de prueba

ID: `1qAujKlGm0l6uNAz35nLCaV6OdT88OT_WRVmrPr-ENRU`

Paquetes de prueba incluidos:
| Tracking | Cliente | Estado |
|---|---|---|
| UPS123456789 | Juan Pérez | En bodega USA |
| FDX987654321 | María López | En tránsito a CR |
| USPS456789123 | Carlos Mora | En aduana CR |
| DHL321654987 | Ana Rodríguez | Listo para retirar (Liberia) |
| UPS741852963 | Pedro Jiménez | En bodega USA |
| FDX159357486 | Laura Solano | En tránsito a CR |

## Setup para importar en n8n

1. Importar `whatsapp_flow.json` en n8n
2. Conectar credencial de **Google Sheets** (OAuth2)
3. Configurar variables de entorno:
   - `GREEN_API_INSTANCE` → ID de instancia Green API
   - `GREEN_API_TOKEN` → Token de Green API
4. Activar el webhook
