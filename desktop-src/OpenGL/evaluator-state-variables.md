---
title: Variabili di stato dell'analizzatore
description: Variabili di stato dell'analizzatore
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- Variabili di stato dell'analizzatore OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 615e7cde4a8f82c3f4a9a95791912c5dc3f77ff3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955960"
---
# <a name="evaluator-state-variables"></a>Variabili di stato dell'analizzatore

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>\_ordine GL</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descrizione:     | ordine mappa 1-D                  |
| Gruppo di attributi: |                                |
| Valore iniziale:   | 1                              |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>\_ordine GL</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descrizione:     | ordini Mappa 2D                 |
| Gruppo di attributi: |                                |
| Valore iniziale:   | 1, 1                            |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>\_Coeff GL</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descrizione:     | punti di controllo 1-D             |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>\_Coeff GL</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descrizione:     | punti di controllo 2D             |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>\_dominio GL</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descrizione:     | endpoint del dominio 1-D           |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>\_dominio GL</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descrizione:     | endpoint del dominio 2D           |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ Mappa1 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | la mappa 1-D Abilita: *x* è il tipo di mappa   |
| Gruppo di attributi: | EVAL/Enable                        |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ map2 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | la mappa 2D Abilita: *x* è il tipo di mappa   |
| Gruppo di attributi: | EVAL/Enable                        |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>\_Dominio della \_ griglia GL Mappa1 \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | endpoint della griglia da 1 a D                                                             |
| Gruppo di attributi: | eval                                                                           |
| Valore iniziale:   | 0, 1                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>\_Dominio della \_ griglia GL map2 \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | endpoint della griglia 2D                                                             |
| Gruppo di attributi: | eval                                                                           |
| Valore iniziale:   | 0, 1; 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>\_ \_ Segmenti griglia GL \_ Mappa1</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | divisioni della griglia da 1 a D                 |
| Gruppo di attributi: | eval                               |
| Valore iniziale:   | 1                                  |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>\_ \_ Segmenti griglia GL \_ Mappa1</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | segmenti griglia 2D                                                              |
| Gruppo di attributi: | eval                                                                           |
| Valore iniziale:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ auto \_ normale</dt> <dd> 

|                  |                                             |
|------------------|---------------------------------------------|
| Descrizione:     | True se la generazione automatica normale è abilitata |
| Gruppo di attributi: | eval                                        |
| Valore iniziale:   | GL \_ false                                   |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




