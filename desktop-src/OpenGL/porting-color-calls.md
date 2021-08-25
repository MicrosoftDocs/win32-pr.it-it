---
title: Porting di chiamate a colori
description: La tabella seguente elenca le funzioni di colore IRIS GL e le funzioni OpenGL equivalenti.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Portabilità IRIS GL, colore
- porting from IRIS GL,color
- porting to OpenGL from IRIS GL,color
- Portabilità OpenGL da IRIS GL, colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e15774f66964c11527955b57651e69db26f6f3d3704d114fdfa4de9a0d5b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777051"
---
# <a name="porting-color-calls"></a>Porting di chiamate a colori

La tabella seguente elenca le funzioni di colore IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                  | Funzione OpenGL                                                                                                                               | Significato                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Imposta il colore RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Imposta l'indice dei colori.                                |
| **getcolor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ CURRENT \_ INDEX )                                               | Restituisce l'indice dei colori corrente.                     |
| **getmcolor**                     |                                                                                                                                               | Ottiene una copia dei valori RGB per una voce della mappa colori. |
| **gRGBcolor**                     | **glGet**( GL \_ CURRENT \_ COLOR )                                                                                                               | Ottiene i valori di colore RGB correnti.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **Colore RGB**                      | **glColor**                                                                                                                                   | Imposta il colore RGB.                                      |
| **maschera di scrittura**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Imposta la maschera colori della modalità indice colori.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Imposta la maschera della modalità colore RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ COLOR \_ WRITEMASK )**glGet**( GL \_ INDEX \_ WRITEMASK )<br/> | Ottiene la maschera di colore.                                 |
| **gRGBmask**                      | **glGet**( GL \_ COLOR \_ WRITEMASK )                                                                                                             | Ottiene la maschera di colore.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Prestare attenzione quando si **sostituisce zwritemask** [**con glDepthMask**](gldepthmask.md); **glDepthMask** accetta un argomento booleano, mentre **zwritemask** accetta un campo di bit.

 

Se si vogliono usare più mappe colori, è necessario usare le funzioni appropriate Windows mappa colori. Pertanto, **multimap**, **onemap**, **getcmmode**, **setmap** e **getmap** non hanno equivalenti OpenGL.

 

 





