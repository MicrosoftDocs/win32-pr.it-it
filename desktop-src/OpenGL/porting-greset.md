---
title: Porting greset
description: OpenGL sostituisce la funzione IRIS GL, greset, con le funzioni glPushAttrib e glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Portabilità IRIS GL, variabili di stato
- porting from IRIS GL,state variables
- porting to OpenGL from IRIS GL,state variables
- Portabilità OpenGL da IRIS GL, variabili di stato
- variabili di stato
- Portabilità IRIS GL, funzione greset
- porting from IRIS GL,greset function
- porting to OpenGL from IRIS GL,greset function
- Portabilità OpenGL da IRIS GL, funzione greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5a48c09e7078f3eccd316de9cb86872d61343aabfa0faf60fbe5af2bef218c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936149"
---
# <a name="porting-greset"></a>Porting greset

OpenGL sostituisce la funzione IRIS GL, **greset**, con le funzioni [**glPushAttrib**](glpushattrib.md) [**e glPopAttrib**](glpopattrib.md). Usare queste funzioni per salvare e ripristinare gruppi di variabili di stato. Ad esempio,

``` syntax
void glPushAttrib( GLbitfield mask );
```

In questo esempio viene accettata un'operazione OR bit per bit di costanti simboliche, che indica i gruppi di variabili di stato da inserire in uno stack di attributi. Ogni costante fa riferimento a un gruppo di variabili di stato. Nella tabella seguente vengono illustrati i gruppi di attributi con i nomi delle costanti simboliche equivalenti. Per un elenco completo delle variabili di stato OpenGL associate a ogni costante, vedere [**glPushAttrib.**](glpushattrib.md)



| Attributo                       | Costante                  |
|---------------------------------|---------------------------|
| valore di cancellazione buffer di accumulo | GL \_ ACCUM \_ BUFFER \_ BIT    |
| buffer dei colori                    | BIT BUFFER COLORE GL \_ \_ \_    |
| corrente                         | GL \_ CURRENT \_ BIT          |
| buffer di profondità                    | BIT \_ BUFFER \_ DI PROFONDITÀ GL \_    |
| abilitare                          | GL \_ ENABLE \_ BIT           |
| Valutatori                      | EGL \_ VAL \_ BIT             |
| Nebbia                             | GL \_ FOG \_ BIT              |
| Impostazione \_ GL LIST \_ BASE          | GL \_ LIST \_ BIT             |
| variabili hint                  | GL \_ HINT \_ BIT             |
| variabili di illuminazione              | BIT DI ILLUMINAZIONE GL \_ \_         |
| modalità di disegno di linee               | GL \_ LINE \_ BIT             |
| Variabili della modalità pixel            | BIT MODALITÀ PIXEL GL \_ \_ \_      |
| Variabili point                 | BIT DEL PUNTO GL \_ \_            |
| polygon                         | BIT \_ POLIGONO GL \_          |
| stipple poligono                 | GL \_ POLYGON \_ STIPPLE \_ BIT |
| Forbice                         | GL \_ SCISSOR \_ BIT          |
| stencil buffer                  | GL \_ STENCIL \_ BUFFER \_ BIT  |
| trama                         | BIT DI TRAMA GL \_ \_          |
| trasformazione                       | BIT DI TRASFORMAZIONE GL \_ \_        |
| riquadro di visualizzazione                        | GL \_ VIEWPORT \_ BIT         |
|                                 | GL \_ ALL \_ ATTRIB \_ BITS     |



 

Per ripristinare i valori delle variabili di stato a quelli salvati con l'ultimo [**glPushAttrib,**](glpushattrib.md)è sufficiente [**chiamare glPopAttrib**](glpopattrib.md). Le variabili non salvate rimarranno invariate. Lo stack di attributi ha una profondità limitata di almeno 16.

 

 




