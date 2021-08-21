---
title: Variabili di stato del controllo Framebuffer
description: Variabili di stato del controllo Framebuffer
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variabili di stato del controllo Framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 276019f790e5f4750e446cf4ae2d035e0178d0e79130100a5a5e1954cbdcb73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061913"
---
# <a name="framebuffer-control-state-variables"></a>Variabili di stato del controllo Framebuffer

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>BUFFER \_ DI DISEGNO GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------|
| Descrizione:     | Buffer selezionati per il disegno           |
| Gruppo di attributi: | color-buffer                           |
| Valore iniziale:   |                                        |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_ \_ WRITEMASK DELL'INDICE GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Maschera di scrittura dell'indice dei colori                                                            |
| Gruppo di attributi: | color-buffer                                                                     |
| Valore iniziale:   | 1 di                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK COLORE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | La scrittura a colori abilita; R, G, B o A                                               |
| Gruppo di attributi: | color-buffer                                                                     |
| Valore iniziale:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_ \_ WRITEMASK DI PROFONDITÀ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Buffer di profondità abilitato per la scrittura                                                 |
| Gruppo di attributi: | depth-buffer                                                                     |
| Valore iniziale:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_ \_ WRITEMASK DI STENCIL GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Maschera di scrittura stencil-buffer                                                         |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | 1 di                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>VALORE DI \_ CANCELLAZIONE \_ COLORE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Valore non crittografato del buffer di colore (modalità RGBA)                                           |
| Gruppo di attributi: | color-buffer                                                                   |
| Valore iniziale:   | 0, 0, 0, 0                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>VALORE DI \_ CANCELLAZIONE DELL'INDICE GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Valore non crittografato del buffer di colore (modalità indice colori)                                    |
| Gruppo di attributi: | color-buffer                                                                   |
| Valore iniziale:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>VALORE DI \_ CANCELLAZIONE \_ PROFONDITÀ GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Valore di cancellazione del buffer di profondità                                                         |
| Gruppo di attributi: | depth-buffer                                                                     |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>VALORE DI \_ CANCELLAZIONE DELLO STENCIL \_ \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Valore di cancellazione del buffer di stencil                                                       |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL \_ ACCUM \_ CLEAR \_ VALUE</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Valore di cancellazione del buffer di accumulo                                                |
| Gruppo di attributi: | accum-buffer                                                                   |
| Valore iniziale:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




