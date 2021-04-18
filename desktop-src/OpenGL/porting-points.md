---
title: Punti di porting
description: OpenGL non ha alcun comando per creare un singolo punto. In caso contrario, le funzioni del punto di porting sono semplici. La tabella seguente elenca le funzioni di IRIS GL per i punti di disegno e le relative funzioni OpenGL equivalenti.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Porting di IRIS GL, punti
- porting da IRIS GL, punti
- porting in OpenGL da IRIS GL, punti
- Porting OpenGL da IRIS GL, punti
- disegno di funzioni, punti
- punti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298538"
---
# <a name="porting-points"></a>Punti di porting

OpenGL non ha alcun comando per creare un singolo punto. In caso contrario, le funzioni del punto di porting sono semplici. La tabella seguente elenca le funzioni di IRIS GL per i punti di disegno e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL           | OpenGL (funzione)                                                   | Significato                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PNT**                    |                                                                   | Disegna un singolo punto.                                                                                                                                |
| **bgnpoint**, **endpoint** | [**glBegin**](glbegin.md) ( \_ punti GL), [ **glEnd**](glend.md) | Interpreta i vertici come punti.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Imposta la dimensione del punto in pixel.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( \_ punto GL \_ smussato)                | Attiva l'anti-aliasing del punto. Per ulteriori informazioni sull'anti-aliasing dei punti, vedere [porting anti-aliasing Functions](porting-antialiasing-functions.md). |



 

Per informazioni sulle funzioni Get correlate, vedere [**glPointSize**](glpointsize.md).

??

 

 




