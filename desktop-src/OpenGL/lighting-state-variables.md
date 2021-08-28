---
title: Variabili di stato di illuminazione
description: Variabili di stato di illuminazione
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variabili di stato di illuminazione OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfeb867f979a0f5f2da838cdd225c91da2b67913c18cdda89c5d40a3f8ed6b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034911"
---
# <a name="lighting-state-variables"></a>Variabili di stato di illuminazione

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>ILLUMINAZIONE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | True se l'illuminazione è abilitata        |
| Gruppo di attributi: | illuminazione/abilitazione                    |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>MATERIALE A COLORI GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | True se il rilevamento dei colori è abilitato  |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>PARAMETRO DEL MATERIALE COLORE GL \_ \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Proprietà dei materiali che tracciano il colore corrente                                       |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | AMBIENTE \_ GL \_ E \_ DIFFUSE                                                        |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>VISO MATERIALE \_ A \_ COLORI \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Visi interessati dal rilevamento dei colori                                                 |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | GL \_ FRONT \_ AND \_ BACK                                                             |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>AMBIENTE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Colore del materiale ambientale                   |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.2,0.2,0.2,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFFUSE</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Colore materiale diffuso                   |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.8,0.8,0.8,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ SPECULAR</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Colore del materiale speculare                  |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.0,0.0,0.0,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>EMISSIONE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Colore materiale emissivo                  |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.0,0.0,0.0,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ BRILLANTEZZA</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------------|
| Descrizione:     | Esponente speculare del materiale            |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | 0,0                                      |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>AMBIENTE \_ DEL \_ MODELLO \_ GL LIGHT</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Colore della scena di ambiente                                                            |
| Gruppo di attributi: | illuminazione                                                                       |
| Valore iniziale:   | (0.2,0.2,0.2,1.0)                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Il visualizzatore è locale                                                                  |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | GL \_ FALSE                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE</dt> <dd> 

| Proprietà | Valore |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Usare l'illuminazione a due lati                                                           |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | GL \_ FALSE                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>AMBIENTE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Intensità ambientale della luce *i*     |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | (0.0,0.0,0.0,1.0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFFUSE</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Intensità diffusa della luce *i*     |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>SPECULARE GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Intensità speculare della luce *i*    |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>POSIZIONE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Posizione della luce *i*              |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | (0.0,0.0,1.0,0.0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>ATTENUAZIONE COSTANTE GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Fattore di attenuazione costante        |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 1.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>ATTENUAZIONE \_ \_ LINEARE GL</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Fattore di attenuazione lineare          |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>ATTENUAZIONE \_ QUADRATICA GL \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Fattore di attenuazione quadratica       |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>DIREZIONE DEI SPOT GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Direzione della luce in evidenza *i*   |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | (0.0,0.0,-1.0)                     |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL \_ SPOT \_ EXPONENT</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Esponente in evidenza della luce *i*    |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL \_ SPOT \_ CUTOFF</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Angolo in evidenza della luce *i*       |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 180.0                              |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ LIGHT *i*</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | True se la luce *è abilitata*          |
| Gruppo di attributi: | illuminazione/abilitazione                    |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>INDICI COLORI GL \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | *C (a)*, *C (d)* e *C (s) per l'illuminazione* dell'indice colori                         |
| Gruppo di attributi: | illuminazione/abilitazione                                                                |
| Valore iniziale:   | 0,1,1                                                                          |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




