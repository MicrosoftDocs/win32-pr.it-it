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
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857398"
---
# <a name="lighting-state-variables"></a>Variabili di stato di illuminazione

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_illuminazione GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | True se l'illuminazione è abilitata        |
| Gruppo di attributi: | illuminazione/abilitazione                    |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_materiale colore \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | True se è abilitata la verifica dei colori  |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_parametro del \_ materiale \_ colore GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Proprietà materiali che verificano il colore corrente                                       |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | \_ambiente GL \_ e \_ diffusa                                                        |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_ \_ aspetto materiale colore \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Visi interessati dal rilevamento dei colori                                                 |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | \_primo \_ e \_ indietro GL                                                             |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Colore materiale ambiente                   |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.2, 0.2, 0.2, 1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ diffuse</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Colore materiale diffuso                   |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.8, 0.8, 0.8, 1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_speculare GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Colore materiale speculare                  |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.0, 0.0, 0.0, 1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_emissione GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Colore materiale emissivo                  |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | (0.0, 0.0, 0.0, 1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_lucentezza GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descrizione:     | Esponente speculare del materiale            |
| Gruppo di attributi: | illuminazione                                 |
| Valore iniziale:   | 0,0                                      |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ \_ ambiente modello di luce GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Colore della scena ambiente                                                            |
| Gruppo di attributi: | illuminazione                                                                       |
| Valore iniziale:   | (0.2, 0.2, 0.2, 1.0)                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ Visualizzatore locale del modello GL Light \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Visualizzatore locale                                                                  |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | GL \_ false                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_modello GL Light \_ Two- \_ \_ Side</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | USA illuminazione a due lati                                                           |
| Gruppo di attributi: | illuminazione                                                                         |
| Valore iniziale:   | GL \_ false                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Intensità di ambiente della luce *i*     |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | (0.0, 0.0, 0.0, 1.0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ diffuse</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Intensità diffusa della luce *i*     |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_speculare GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Intensità speculare della luce *i*    |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_posizione GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Posizione della luce *i*              |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | (0,0, 0.0, 1.0, 0,0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_ \_ attenuazione costante GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Fattore di attenuazione costante        |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 1.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_ \_ attenuazione lineare GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Fattore di attenuazione lineare          |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_attenuazione quadratica GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Fattore di attenuazione quadratica       |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_direzione spot \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Direzione Spotlight della luce *i*   |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | (0,0, 0,0,-1,0)                     |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>\_esponente spot GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Esponente Spotlight della luce *i*    |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>\_taglio GL spot \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Angolo in primo piano della luce *i*       |
| Gruppo di attributi: | illuminazione                           |
| Valore iniziale:   | 180,0                              |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ Light *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | True se la *luce è* abilitata          |
| Gruppo di attributi: | illuminazione/abilitazione                    |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>indici di \_ colore GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | *C (a)*, *c (d)* e *c (s* ) per l'illuminazione degli indici dei colori                         |
| Gruppo di attributi: | illuminazione/abilitazione                                                                |
| Valore iniziale:   | 0, 1, 1                                                                          |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




