---
title: Variabili di stato della trasformazione
description: Variabili di stato della trasformazione
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variabili di stato della trasformazione OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c79b4363419d97a64184dd2408a9f6221ada52adc49adbb28eb3d049a4b2a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011919"
---
# <a name="transformation-state-variables"></a>Variabili di stato della trasformazione

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>MATRICE \_ DI MODELVIEW \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Stack di matrici di Modelview             |
| Gruppo di attributi: |                                    |
| Valore iniziale:   | Identità                           |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>MATRICE DI \_ \_ PROIEZIONE GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Stack matrice di proiezione                                                        |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | Identità                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>MATRICE DI TRAMA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Stack matrice di trame                                                           |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | Identità                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ VIEWPORT</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Origine ed extent del viewport                                                       |
| Gruppo di attributi: | riquadro di visualizzazione                                                                         |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>INTERVALLO DI PROFONDITÀ GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Intervallo di profondità vicino e lontano                                                       |
| Gruppo di attributi: | riquadro di visualizzazione                                                                       |
| Valore iniziale:   | 0, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ MODELVIEW \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Puntatore dello stack della matrice di Modelview                                                   |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL \_ PROJECTION \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Puntatore dello stack della matrice di proiezione                                                  |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL \_ TEXTURE \_ STACK \_ DEPTH</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Puntatore dello stack della matrice di trame                                                     |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>MODALITÀ MATRICE GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Modalità matrice corrente                                                              |
| Gruppo di attributi: | trasformazione                                                                        |
| Valore iniziale:   | GL \_ MODELVIEW                                                                    |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ NORMALIZE</dt> <dd> 

| Proprietà | Valore |
|------------------|-------------------------------------|
| Descrizione:     | Normalizzazione normale corrente on/off |
| Gruppo di attributi: | transform/enable                    |
| Valore iniziale:   | GL \_ FALSE                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Coefficienti del piano di ritaglio utente         |
| Gruppo di attributi: | trasformazione                                |
| Valore iniziale:   | 0, 0, 0, 0                               |
| Comando Get:     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | *i* th user clipping plane enabled |
| Gruppo di attributi: | transform/enable                   |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




