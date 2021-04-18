---
title: Variabili di stato di texturing
description: Variabili di stato di texturing
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variabili di stato di texturing OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299103"
---
# <a name="texturing-state-variables"></a>Variabili di stato di texturing

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Trama GL \_ *x*</dt> <dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| Descrizione:     | True se il   texturing x-d è abilitato (*x* è 1-d o 2-d) |
| Gruppo di attributi: | trama/Abilita                                        |
| Valore iniziale:   | GL \_ false                                             |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_trama GL</dt> <dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| Descrizione:     | *x*   -D immagine trama al livello di dettaglio *i* |
| Gruppo di attributi: |                                              |
| Valore iniziale:   |                                              |
| Comando Get:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_spessore trama \_ GL</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descrizione:     | *x*   -D immagine trama *i*   ' altezza                       |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_altezza trama \_ GL</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descrizione:     | *x*   -D immagine trama *i*   ' altezza                      |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_bordo trama \_ GL</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descrizione:     | *x*   -D bordo immagine di trama *i*                        |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componenti di trama GL \_</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descrizione:     | Componenti immagine trama                                 |
| Gruppo di attributi: |                                                          |
| Valore iniziale:   | 1                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_ \_ colore bordo trama \_ GL</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descrizione:     | Colore bordo trama                           |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | 0, 0, 0, 0                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_ \_ Filtro minimo trama \_ GL</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descrizione:     | Texture minification (funzione)                  |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | GL \_ più vicino \_ MIPMAP \_ lineare                    |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ filtro mag trama di contabilità \_</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descrizione:     | Funzione di ingrandimento trama                 |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | \_linea GL                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Trama GL a \_ \_ capo \_ *x*</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descrizione:     | Modalità a capo trama (*x*   è S o T)              |
| Gruppo di attributi: | trama                                        |
| Valore iniziale:   | \_ripetizione GL                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_ \_ modalità ENV trama \_ GL</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descrizione:     | Funzione texture Application         |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   | \_modulazione GL                         |
| Comando Get:     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>\_ \_ colore ENV trama \_ GL</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descrizione:     | Colore ambiente trama            |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   | 0, 0, 0, 0                           |
| Comando Get:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>\_Gen trama \_ GL \_ *x*</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Texgen è abilitato (*x*   è S, T, R o Q) |
| Gruppo di attributi: | trama/Abilita                           |
| Valore iniziale:   | GL \_ false                                |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_piano d'occhio GL \_</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descrizione:     | Coefficienti di equazione del piano Texgen   |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_piano oggetto \_ GL</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descrizione:     | Coefficienti lineari oggetto Texgen    |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_modalità di \_ generazione \_ trama GL</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descrizione:     | Funzione utilizzata per texgen             |
| Gruppo di attributi: | trama                              |
| Valore iniziale:   | GL \_ occhio \_ lineare                      |
| Comando Get:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




