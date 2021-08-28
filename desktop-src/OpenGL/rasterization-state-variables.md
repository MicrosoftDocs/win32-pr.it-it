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
ms.openlocfilehash: 1586861eee26f93bca85b8c0f03e9f746e983046bbda755b67a792d65d660b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776891"
---
# <a name="rasterization-state-variables"></a>Variabili di stato di rasterizzazione

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>DIMENSIONI \_ DEI PUNTI GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Dimensioni dei punti                         |
| Gruppo di attributi: | point                              |
| Valore iniziale:   | 1.0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL \_ POINT \_ SMOOTH</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Aliasing dei punti in                  |
| Gruppo di attributi: | point/enable                       |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>LARGHEZZA LINEA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Spessore linea                                                                     |
| Gruppo di attributi: | line                                                                           |
| Valore iniziale:   | 1.0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL \_ LINE \_ SMOOTH</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Antialiasing di riga in               |
| Gruppo di attributi: | line/enable                        |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>MODELLO \_ GL LINE \_ STIPPLE \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Stippla di linea                                                                     |
| Gruppo di attributi: | line                                                                             |
| Valore iniziale:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL \_ LINE \_ STIPPLE \_ REPEAT</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Ripetizione di stipple di riga                                                              |
| Gruppo di attributi: | line                                                                             |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL \_ LINE \_ STIPPLE</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Line stipple enable (Abilita stipple riga)                |
| Gruppo di attributi: | line/enable                        |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL \_ CULL \_ FACE</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Culling dei poligoni abilitato            |
| Gruppo di attributi: | polygon/enable                     |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>MODALITÀ \_ VISO GL CULL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Cull front-facing/back-facing polygons                                           |
| Gruppo di attributi: | polygon                                                                          |
| Valore iniziale:   | GL \_ BACK                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL \_ FRONT \_ FACE</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Indicatore CW/CCW anteriore poligono                                              |
| Gruppo di attributi: | polygon                                                                          |
| Valore iniziale:   | GL \_ CCW                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>ARROTONDAMENTO \_ POLIGONO GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Antialiasing poligono su            |
| Gruppo di attributi: | polygon/enable                     |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>MODALITÀ \_ POLIGONO GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Modalità di rasterizzazione poligono (anteriore e posteriore)                                      |
| Gruppo di attributi: | polygon                                                                          |
| Valore iniziale:   | GL \_ FILL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>\_ \_ STIPPLE POLIGONO GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Abilitazione dello stipple poligono             |
| Gruppo di attributi: | polygon/enable                     |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 



| Proprietà | Valore |
|------------------|----------------------------------------------------|
| Descrizione:     | Modello a punta poligono                            |
| Gruppo di attributi: | polygon-stipple                                    |
| Valore iniziale:   | 1 di                                                |
| Comando Get:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




