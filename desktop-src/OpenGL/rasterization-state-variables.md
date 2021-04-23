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
ms.openlocfilehash: 6210f93c23dc52f19f3e01ea01ebe8fc9d631c8c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909839"
---
# <a name="rasterization-state-variables"></a>Variabili di stato di rasterizzazione

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>DIMENSIONI \_ DEI PUNTI GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Dimensioni dei punti                         |
| Gruppo di attributi: | point                              |
| Valore iniziale:   | 1,0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL \_ POINT \_ SMOOTH</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Aliasing dei punti su                  |
| Gruppo di attributi: | point/enable                       |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>LARGHEZZA LINEA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Spessore linea                                                                     |
| Gruppo di attributi: | line                                                                           |
| Valore iniziale:   | 1,0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL \_ LINE \_ SMOOTH</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Antialiasing linea su               |
| Gruppo di attributi: | line/enable                        |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>MODELLO \_ DI \_ STIPPLE DELLA RIGA \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Stipple di linea                                                                     |
| Gruppo di attributi: | line                                                                             |
| Valore iniziale:   | 1 di                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL \_ LINE \_ STIPPLE \_ REPEAT</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Ripetizione della punta della riga                                                              |
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
| Descrizione:     | Poligoni rivolti anteriore/posteriore                                           |
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



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL \_ POLYGON \_ STIPPLE</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Abilitazione dello stipple poligono             |
| Gruppo di attributi: | polygon/enable                     |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 



| Proprietà | Valore |
|------------------|----------------------------------------------------|
| Descrizione:     | Modello a stipple poligono                            |
| Gruppo di attributi: | stipple poligono                                    |
| Valore iniziale:   | 1 di                                                |
| Comando Get:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




