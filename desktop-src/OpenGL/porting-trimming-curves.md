---
title: Porting delle curve di taglio
description: Le curve di trimming OpenGL sono molto simili alle curve di taglio GL di IRIS. La tabella seguente elenca le funzioni di IRIS GL per la definizione delle curve di taglio e delle funzioni OpenGL equivalenti.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Porting di IRIS GL, curve di taglio
- porting da IRIS GL, curve di taglio
- porting in OpenGL da IRIS GL, taglio delle curve
- Porting OpenGL da IRIS GL, curve di taglio
- taglio di curve
- curve
- Porting di IRIS GL, curve
- porting da IRIS GL, curve
- porting in OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221819"
---
# <a name="porting-trimming-curves"></a>Porting delle curve di taglio

Le curve di trimming OpenGL sono molto simili alle curve di taglio GL di IRIS. La tabella seguente elenca le funzioni di IRIS GL per la definizione delle curve di taglio e delle funzioni OpenGL equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                        | Significato                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Inizia la definizione della curva di taglio.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Definisce una curva lineare a tratti.    |
| **NurbsCurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Specifica gli attributi della curva di taglio. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Termina la definizione della curva di taglio.      |



 

??

 

 




