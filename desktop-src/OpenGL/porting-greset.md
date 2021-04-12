---
title: Portabilità del porting
description: OpenGL sostituisce la funzione IRIS GL, il Grest, con le funzioni glPushAttrib e glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Porting di IRIS GL, variabili di stato
- porting da IRIS GL, variabili di stato
- porting in OpenGL da IRIS GL, variabili di stato
- Porting OpenGL da IRIS GL, variabili di stato
- variabili di stato
- Porting di IRIS GL, funzione Grest
- porting da IRIS GL, funzione Grest
- porting in OpenGL da IRIS GL, funzione Grest
- Porting OpenGL da IRIS GL, funzione Grest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396346"
---
# <a name="porting-greset"></a>Portabilità del porting

OpenGL sostituisce la funzione IRIS GL, il **Grest**, con le funzioni [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md). Usare queste funzioni per salvare e ripristinare i gruppi di variabili di stato. Ad esempio,

``` syntax
void glPushAttrib( GLbitfield mask );
```

Questo esempio accetta un operatore OR bit per bit di costanti simboliche, che indica i gruppi di variabili di stato da inserire nello stack di attributi. Ogni costante fa riferimento a un gruppo di variabili di stato. Nella tabella seguente vengono illustrati i gruppi di attributi con i nomi di costanti simbolici equivalenti. Per un elenco completo delle variabili di stato OpenGL associate a ogni costante, vedere [**glPushAttrib**](glpushattrib.md).



| Attributo                       | Costante                  |
|---------------------------------|---------------------------|
| valore Clear buffer accumulo | \_bit del buffer di accut GL \_ \_    |
| buffer dei colori                    | \_bit del \_ buffer dei colori GL \_    |
| corrente                         | \_bit corrente \_ GL          |
| buffer profondità                    | \_ \_ bit buffer di profondità GL \_    |
| abilitare                          | \_bit di abilitazione GL \_           |
| analizzatori                      | EGL \_ Val \_ bit             |
| nebbia                             | \_bit di nebbia GL \_              |
| \_ \_ Impostazione base elenco GL          | \_bit elenco \_ GL             |
| variabili hint                  | \_bit suggerimento \_ GL             |
| variabili di illuminazione              | \_bit di illuminazione GL \_         |
| modalità di disegno linea               | \_bit linea \_ GL             |
| variabili in modalità pixel            | \_bit in \_ modalità GL pixel \_      |
| variabili punto                 | \_bit punto \_ GL            |
| polygon                         | \_bit poligono GL \_          |
| poligono stipple                 | \_bit stipple poligono GL \_ \_ |
| ritaglio                         | \_bit a forbice GL \_          |
| buffer stencil                  | \_ \_ bit buffer dello stencil GL \_  |
| trama                         | \_bit trama \_ GL          |
| trasformazione                       | \_bit di trasformazione GL \_        |
| riquadro di visualizzazione                        | \_bit del viewport GL \_         |
|                                 | \_tutti i \_ \_ bit attrib (GL)     |



 

Per ripristinare i valori delle variabili di stato in quelli salvati con l'ultimo [**glPushAttrib**](glpushattrib.md), è sufficiente chiamare [**glPopAttrib**](glpopattrib.md). Le variabili non salvate rimarranno invariate. Lo stack degli attributi ha una profondità finita di almeno 16.

 

 




