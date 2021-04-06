---
title: Variabili di stato Implementation-Dependent
description: Variabili di stato Implementation-Dependent
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Variabili di stato Implementation-Dependent OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb42c13765678218efcaf58f2b02a01d2f0e160
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045756"
---
# <a name="implementation-dependent-state-variables"></a>Variabili di stato Implementation-Dependent

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>\_luci massime GL \_</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Descrizione:     | Numero massimo di spie               |
| Gruppo di attributi: |                                        |
| Valore iniziale:   | 8                                      |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>\_massimo \_ piani di RItaglio GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Numero massimo di piani di ritaglio utente                                           |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 6                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>\_ \_ \_ profondità dello stack MODELVIEW max per GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima stack Modelview-Matrix                                             |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>\_ \_ \_ profondità dello stack di proiezione max GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità dello stack della matrice di proiezione massima                                            |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>\_ \_ \_ profondità stack trama massimo \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack della matrice di trama                                            |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>\_bit SOTTOPIXEL \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Numero di bit di precisione dei subpixel in *x*   e *y*                              |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 4                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>\_dimensioni massime \_ trama GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Altezza o larghezza massima di un'immagine di trama (senza bordi)                     |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>\_tabella di \_ \_ mappa pixel max GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Dimensioni massime di una tabella di conversione **glPixelMap**                               |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>\_ \_ \_ profondità stack nome massimo \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità stack nome-selezione massima                                               |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_ \_ annidamento elenco GL Max \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Visualizzazione massima dell'annidamento delle chiamate all'elenco                                                |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>ordine di valutazione \_ massimo GL \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Ordine polinomiale dell'analizzatore massimo                                               |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 8                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>\_ \_ Dim viewport Max \_ viewport</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Dimensioni massime viewport                                                      |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>\_ \_ \_ profondità dello stack dell'attrib massimo per GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Profondità massima dello stack di attributi                                             |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 16                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>\_buffer aux \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Numero di buffer ausiliari                                                      |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 0                                                                                |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>\_modalità RGBA \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | True se i buffer dei colori archiviano RGBA                                                 |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>\_modalità Indice \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | True se i buffer dei colori archiviano gli indici                                              |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>\_DOUBLEBUFFER GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | True se i buffer anteriore e posteriore sono presenti                                             |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>\_stereo GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | True se sono presenti buffer a sinistra e a destra                                           |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>\_ \_ intervallo dimensioni punti \_ GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Intervallo (da basso a alto) di dimensioni dei punti con alias                                 |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>\_ \_ granularità delle dimensioni del punto GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Granularità delle dimensioni in punti antialias                                             |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>\_intervallo di \_ lunghezza \_ riga GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Intervallo (da basso a alto) di larghezze linea con alias                                 |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>\_ \_ granularità della lunghezza linea GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Granularità della lunghezza di riga con antialias                                             |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




