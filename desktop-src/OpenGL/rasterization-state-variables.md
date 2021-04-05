---
title: Variabili di stato di rasterizzazione
description: Variabili di stato di rasterizzazione
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Variabili di stato di rasterizzazione OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1667c530ea1db8c9e463be0edad5de98e8b107
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718499"
---
# <a name="rasterization-state-variables"></a>Variabili di stato di rasterizzazione

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>\_dimensioni punto \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Dimensioni dei punti                         |
| Gruppo di attributi: | point                              |
| Valore iniziale:   | 1.0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_punto GL \_ smussato</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Alias di punti su                  |
| Gruppo di attributi: | punto/Abilita                       |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_spessore linea \_ GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Spessore linea                                                                     |
| Gruppo di attributi: | line                                                                           |
| Valore iniziale:   | 1.0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>\_linea GL \_ smussata</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Anti-aliasing della riga in               |
| Gruppo di attributi: | riga/Abilita                        |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_ \_ modello stipple linea \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Linea stipple                                                                     |
| Gruppo di attributi: | line                                                                             |
| Valore iniziale:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>\_ \_ ripetizione stipple riga \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Ripetizione riga stipple                                                              |
| Gruppo di attributi: | line                                                                             |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>\_stipple linea \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Abilita riga stipple                |
| Gruppo di attributi: | riga/Abilita                        |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>superficie di selezione GL \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Abbattimento poligono abilitato            |
| Gruppo di attributi: | poligono/Abilita                     |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_ \_ modalità faccia selezione \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Eliminare i poligoni front-end/back-facing                                           |
| Gruppo di attributi: | polygon                                                                          |
| Valore iniziale:   | indietro per GL \_                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>front-end GL \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Indicatore CW/CCW anteriore poligono                                              |
| Gruppo di attributi: | polygon                                                                          |
| Valore iniziale:   | \_CCW                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>\_poligono GL \_ smussato</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Anti-aliasing poligono in            |
| Gruppo di attributi: | poligono/Abilita                     |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_modalità poligono GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Modalità di rasterizzazione del poligono (anteriore e posteriore)                                      |
| Gruppo di attributi: | polygon                                                                          |
| Valore iniziale:   | \_riempimento GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>\_stipple poligono GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Stipple poligono abilitato             |
| Gruppo di attributi: | poligono/Abilita                     |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 



|                  |                                                    |
|------------------|----------------------------------------------------|
| Descrizione:     | Modello stipple poligono                            |
| Gruppo di attributi: | poligono-stipple                                    |
| Valore iniziale:   | 1                                                |
| Comando Get:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




