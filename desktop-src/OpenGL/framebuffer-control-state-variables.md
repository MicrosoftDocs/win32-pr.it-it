---
title: Variabili di stato del controllo framebuffer
description: Variabili di stato del controllo framebuffer
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variabili di stato del controllo framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857073"
---
# <a name="framebuffer-control-state-variables"></a>Variabili di stato del controllo framebuffer

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_buffer di disegni GL \_</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Descrizione:     | Buffer selezionati per il disegno           |
| Gruppo di attributi: | buffer a colori                           |
| Valore iniziale:   |                                        |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK indice \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Writemask indice colori                                                            |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK colore \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Abilitazione della scrittura di colori; R, G, B o A                                               |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | GL \_ true                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_WRITEMASK profondità \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Buffer di profondità abilitato per la scrittura                                                 |
| Gruppo di attributi: | buffer di profondità                                                                     |
| Valore iniziale:   | GL \_ true                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK stencil \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Stencil-buffer writemask                                                         |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_valore di \_ cancellazione del colore GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Valore Clear del buffer dei colori (modalità RGBA)                                           |
| Gruppo di attributi: | buffer a colori                                                                   |
| Valore iniziale:   | 0, 0, 0, 0                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_valore di \_ cancellazione \_ indice GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Valore Clear del buffer dei colori (modalità di indicizzazione dei colori)                                    |
| Gruppo di attributi: | buffer a colori                                                                   |
| Valore iniziale:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ valore Clear profondità \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Depth-valore Clear del buffer                                                         |
| Gruppo di attributi: | buffer di profondità                                                                     |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ valore chiaro stencil \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Stencil-valore non crittografato del buffer                                                       |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_ \_ valore non crittografato \_ Contabilità GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Accumulo-valore Clear buffer                                                |
| Gruppo di attributi: | accut-buffer                                                                   |
| Valore iniziale:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




