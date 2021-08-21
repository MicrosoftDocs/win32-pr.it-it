---
title: Texturing delle variabili di stato
description: Texturing delle variabili di stato
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Texturing State Variables OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7393fc6e700b028ba3783e5c78d8175e0c3fba4937bf3830d5cae8897aa0d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776581"
---
# <a name="texturing-state-variables"></a>Texturing delle variabili di stato

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ TEXTURE \_ *x*</dt> <dd> 

| Proprietà | Valore |
|------------------|-------------------------------------------------------|
| Descrizione:     | True se *x* - D texturing abilitato (*x* è 1-D o 2-D) |
| Gruppo di attributi: | trama/abilitazione                                        |
| Valore iniziale:   | GL \_ FALSE                                             |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>TRAMA \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------|
| Descrizione:     | *x* - Immagine trama D al livello di dettaglio *i* |
| Gruppo di attributi: |                                              |
| Valore iniziale:   |                                              |
| Comando Get:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>LARGHEZZA TRAMA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------|
| Descrizione:     | *x* - Larghezza dell'immagine della trama D *i*                       |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>ALTEZZA TRAMA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------|
| Descrizione:     | *x* - Altezza dell'immagine della trama D *i*                      |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>BORDO DELLA TRAMA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------|
| Descrizione:     | *x* - Bordo dell'immagine della trama D *i*                      |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>COMPONENTI DELLA TRAMA GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------|
| Descrizione:     | Componenti dell'immagine di trama                                 |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 1                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>COLORE BORDO TRAMA GL \_ \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------------|
| Descrizione:     | Colore bordo trama                           |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | 0, 0, 0, 0                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>FILTRO MIN TRAMA GL \_ \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------------|
| Descrizione:     | Funzione di minificazione della trama                  |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | GL \_ NEAREST \_ MIPMAP \_ LINEAR                    |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>FILTRO \_ MAG \_ TRAMA GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------------|
| Descrizione:     | Funzione di ingrandimento della trama                 |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | GL \_ LINEAR                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ TEXTURE \_ WRAP \_ *x*</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------------|
| Descrizione:     | Modalità di ritorno a capo trame (*x* è S o T)              |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | RIPETIZIONE \_ DELLA CONTABILITÀ GENERALE                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>MODALITÀ DI \_ ENV \_ TRAME GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------|
| Descrizione:     | Funzione dell'applicazione Texture         |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   | \_MODULAZIONE DELLA CONTABILITÀ GENERALE                         |
| Comando Get:     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>COLORE \_ \_ DELL'AMBIENTE DI TRAMA GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------|
| Descrizione:     | Colore dell'ambiente di trama            |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   | 0, 0, 0, 0                           |
| Comando Get:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ TEXTURE \_ GEN \_ *x*</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Texgen è abilitato (*x* è S, T, R o Q) |
| Gruppo di attributi: | trama/abilitazione                           |
| Valore iniziale:   | GL \_ FALSE                                |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL \_ EYE \_ PLANE</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------|
| Descrizione:     | Coefficienti delle equazioni del piano texgen   |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>PIANO OGGETTI GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------|
| Descrizione:     | Coefficienti lineari dell'oggetto Texgen    |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>MODALITÀ GEN TRAMA GL \_ \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------|
| Descrizione:     | Funzione usata per texgen             |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   | GL \_ EYE \_ LINEAR                      |
| Comando Get:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




