---
title: Implementation-Dependent di stato
description: Implementation-Dependent di stato
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent State Variables OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da38f841408bd6ddf481473837f36544d21d896f2764317957c65158be27fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061459"
---
# <a name="implementation-dependent-state-variables"></a>Implementation-Dependent di stato

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ MAX \_ LIGHTS</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------|
| Descrizione:     | Numero massimo di luci               |
| Gruppo di attributi: |                                        |
| Valore iniziale:   | 8                                      |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL \_ MAX \_ CLIP \_ PLANES</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Numero massimo di piani di ritaglio utente                                           |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 6                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack modelview-matrix                                             |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL \_ MAX \_ PROJECTION \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack della matrice di proiezione                                            |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL \_ MAX \_ TEXTURE \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack della matrice di trame                                            |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>BIT \_ SUBPIXEL GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Numero di bit di precisione dei subpixel in *x* e *y*                              |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 4                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL \_ MAX \_ TEXTURE \_ SIZE</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Altezza o larghezza massima di un'immagine di trama (senza bordi)                     |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL \_ MAX \_ PIXEL \_ MAP \_ TABLE</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Dimensioni massime di una **tabella di conversione glPixelMap**                               |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL \_ MAX \_ NAME \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack dei nomi di selezione                                               |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_ \_ ANNIDAMENTO ELENCO MAX GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Nidificazione massima delle chiamate dell'elenco di visualizzazione                                                |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ MAX \_ EVAL \_ ORDER</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Ordine polinomiale massimo dell'analizzatore                                               |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 8                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ MAX \_ VIEWPORT \_ DIMS</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Dimensioni massime del viewport                                                      |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack di attributi                                             |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 16                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>BUFFER \_ DELL'ESPERIENZA \_ UTENTE GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Numero di buffer ausiliari                                                      |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 0                                                                                |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>MODALITÀ \_ GL \_ RGBA</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | True se i buffer dei colori archiviano RGBA                                                 |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>MODALITÀ \_ DI INDICIZZAZIONE GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | True se i buffer dei colori archiviano gli indici                                              |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | True se esistono buffer front-and-back                                             |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ STEREO</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | True se esistono buffer sinistro e destro                                           |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>INTERVALLO \_ DI DIMENSIONI DEI PUNTI \_ GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Intervallo (da basso a alto) di dimensioni dei punti antialias                                 |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GRANULARITÀ \_ DELLE \_ DIMENSIONI DEI \_ PUNTI GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Granularità delle dimensioni dei punti con antialias                                             |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>INTERVALLO \_ LARGHEZZA \_ LINEA GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Intervallo (da basso a alto) di larghezze delle linee con antialias                                 |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>\_GRANULARITÀ LARGHEZZA \_ \_ LINEA GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Granularità della larghezza della linea con antialias                                             |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




