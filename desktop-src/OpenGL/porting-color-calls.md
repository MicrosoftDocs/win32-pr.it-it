---
title: Chiamate di colore di porting
description: Nella tabella seguente sono elencate le funzioni dei colori IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Porting di IRIS GL, colore
- porting da IRIS GL, color
- porting in OpenGL da IRIS GL, colore
- Porting OpenGL da IRIS GL, colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708464"
---
# <a name="porting-color-calls"></a>Chiamate di colore di porting

Nella tabella seguente sono elencate le funzioni dei colori IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                  | OpenGL (funzione)                                                                                                                               | Significato                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Imposta il colore RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Imposta l'indice dei colori.                                |
| **GetColor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ indice corrente GL \_ )                                               | Restituisce l'indice dei colori corrente.                     |
| **getmcolor**                     |                                                                                                                                               | Ottiene una copia dei valori RGB per una voce della mappa colori. |
| **gRGBcolor**                     | **glGet**( \_ colore corrente GL \_ )                                                                                                               | Ottiene i valori dei colori RGB correnti.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBcolor**                      | **glColor**                                                                                                                                   | Imposta il colore RGB.                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Imposta la maschera colori della modalità di indice dei colori.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Imposta la maschera della modalità colori RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Color \_ WRITEMASK)**glGet**(GL \_ index \_ WRITEMASK)<br/> | Ottiene la maschera dei colori.                                 |
| **gRGBmask**                      | **glGet**(GL \_ Color \_ WRITEMASK)                                                                                                             | Ottiene la maschera dei colori.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Prestare attenzione quando si sostituisce **zwritemask** con [**glDepthMask**](gldepthmask.md); **glDepthMask** accetta un argomento booleano, mentre **zwritemask** accetta un campo di bit.

 

Se si desidera utilizzare più mappe a colori, è necessario utilizzare le funzioni mappa colori di Windows appropriate. Pertanto, **multimap**, **OneMap**, **getcmmode**, **setmap** e **GetMap** non dispongono di equivalenti OpenGL.

 

 





