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
ms.openlocfilehash: f2895f773721f7c900003cbaa0f070c277a0e260
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909259"
---
# <a name="evaluator-state-variables"></a>Variabili di stato dell'analizzatore

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>ORDINE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------|
| Descrizione:     | Ordine mappa 1D                  |
| Gruppo di attributi: |                                |
| Valore iniziale:   | 1                              |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>ORDINE \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------|
| Descrizione:     | Ordini mappa 2D                 |
| Gruppo di attributi: |                                |
| Valore iniziale:   | 1,1                            |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------|
| Descrizione:     | Punti di controllo 1D             |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------|
| Descrizione:     | Punti di controllo 2D             |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMINIO \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------|
| Descrizione:     | Endpoint di dominio 1D           |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMINIO \_ GL</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------|
| Descrizione:     | Endpoint di dominio 2D           |
| Gruppo di attributi: |                                |
| Valore iniziale:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | La mappa 1D abilita: *x* è il tipo di mappa   |
| Gruppo di attributi: | eval/enable                        |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ MAP2 \_ x</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | La mappa 2D abilita: *x* è il tipo di mappa   |
| Gruppo di attributi: | eval/enable                        |
| Valore iniziale:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>DOMINIO \_ DELLA GRIGLIA GL MAP1 \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Endpoint griglia 1D                                                             |
| Gruppo di attributi: | eval                                                                           |
| Valore iniziale:   | 0,1                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>DOMINIO \_ GRIGLIA GL MAP2 \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Endpoint della griglia 2D                                                             |
| Gruppo di attributi: | eval                                                                           |
| Valore iniziale:   | 0, 1; 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>SEGMENTI \_ DELLA GRIGLIA GL MAP1 \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|------------------------------------|
| Descrizione:     | Divisioni griglia 1D                 |
| Gruppo di attributi: | eval                               |
| Valore iniziale:   | 1                                  |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>SEGMENTI \_ DELLA GRIGLIA GL MAP1 \_ \_</dt> <dd> 

| Proprietà | Valore |
|------------------|--------------------------------------------------------------------------------|
| Descrizione:     | Segmenti di griglia 2D                                                              |
| Gruppo di attributi: | eval                                                                           |
| Valore iniziale:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ AUTO \_ NORMAL</dt> <dd> 

| Proprietà | Valore |
|------------------|---------------------------------------------|
| Descrizione:     | True se la generazione normale automatica è abilitata |
| Gruppo di attributi: | eval                                        |
| Valore iniziale:   | GL \_ FALSE                                   |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




