# mejorar-prompt

Plugin para Claude Code (terminal y app de escritorio). Antes de que Claude lea tu mensaje, Haiku lo reescribe en primera persona con estas secciones: Objetivo, Contexto, Requisitos, Restricciones y Dudas. Para entender referencias como "eso" o "lo de antes", Haiku ve también los últimos 6 mensajes de la conversación. Además, Claude te pregunta lo que no esté claro en vez de suponer.

## Descarga

Descarga `mejorar-prompt.zip` desde esta página (botón **Code → Download ZIP** o el propio archivo) y descomprímelo en una carpeta fija, por ejemplo `C:\Users\tu-usuario\Proyectos\mejorar-prompt`.

## Instalación

Desde un terminal, con la carpeta ya descomprimida:

```bash
claude plugin marketplace add C:\Users\tu-usuario\Proyectos\mejorar-prompt
claude plugin install mejorar-prompt@mejorar-prompt-local
```

En la app de escritorio: pulsa + junto al cuadro de texto, luego Plugins, Add marketplace con la carpeta, y después Add plugin. Se carga en las sesiones nuevas.

Para quitarlo: `claude plugin uninstall mejorar-prompt@mejorar-prompt-local`.

## Modos

| Comando | Qué pasa al pulsar Enter |
| --- | --- |
| `/mejorar revisar` (por defecto) | Tu mensaje **no se envía**: vuelve mejorado a la caja de texto. Lo revisas o lo editas y pulsas Enter otra vez. Solo entonces se procesa, una única vez. |
| `/mejorar sustituir` | Se envía directamente la versión mejorada. Tu original se le pasa a Claude de forma oculta, por si acaso. |
| `/mejorar off` | No toca nada. |
| `/mejorar on` | Vuelve al último modo activo. |
| `/mejorar` | Muestra el modo actual. |

Si Haiku falla o tarda más de 8 s, se envía tu mensaje original.

## Licencia

MIT. Ver [LICENSE](LICENSE).