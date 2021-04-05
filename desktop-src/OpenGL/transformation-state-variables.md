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
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334276"
---
# <a name="transformation-state-variables"></a>Variabili di stato della trasformazione

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_matrice GL MODELVIEW \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Stack matrice Modelview             |
| Gruppo di attributi: |                                    |
| Valore iniziale:   | Identità                           |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matrice di proiezione GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Stack matrice di proiezione                                                        |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | Identità                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matrice di trama GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Stack matrice trama                                                           |
| Gruppo di attributi: |                                                                                |
| Valore iniziale:   | Identità                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_riquadro di visualizzazione GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Origine e extent del viewport                                                       |
| Gruppo di attributi: | riquadro di visualizzazione                                                                         |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_intervallo di profondità GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Intervallo di profondità vicino e lontano                                                       |
| Gruppo di attributi: | riquadro di visualizzazione                                                                       |
| Valore iniziale:   | 0, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_ \_ profondità dello stack MODELVIEW GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Puntatore dello stack della matrice Modelview                                                   |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_ \_ profondità dello stack di proiezione GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Puntatore dello stack della matrice di proiezione                                                  |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_ \_ profondità dello stack di trama GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Puntatore dello stack della matrice di trama                                                     |
| Gruppo di attributi: |                                                                                  |
| Valore iniziale:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_modalità matrice \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Modalità matrice corrente                                                              |
| Gruppo di attributi: | trasformazione                                                                        |
| Valore iniziale:   | \_MODELVIEW GL                                                                    |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_normalizzare GL</dt> <dd> 

|                  |                                     |
|------------------|-------------------------------------|
| Descrizione:     | Normalizzazione normale corrente |
| Gruppo di attributi: | trasforma/Abilita                    |
| Valore iniziale:   | GL \_ false                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Piano di ritaglio GL \_ *i*</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Coefficienti del piano di ritaglio utente         |
| Gruppo di attributi: | trasformazione                                |
| Valore iniziale:   | 0, 0, 0, 0                               |
| Comando Get:     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Piano di ritaglio GL \_ *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | *i* TH il piano di ritaglio utente è abilitato |
| Gruppo di attributi: | trasforma/Abilita                   |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




