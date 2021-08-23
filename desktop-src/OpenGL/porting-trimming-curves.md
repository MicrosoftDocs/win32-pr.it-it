---
title: Porting di curve di taglio
description: Le curve di taglio OpenGL sono molto simili alle curve di taglio IRIS GL. Nella tabella seguente sono elencate le funzioni IRIS GL per definire le curve di taglio e le funzioni OpenGL equivalenti.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Porting IRIS GL, curve di taglio
- porting da IRIS GL, taglio di curve
- porting a OpenGL da IRIS GL, taglio delle curve
- Porting OpenGL da IRIS GL, curve di taglio
- taglio di curve
- curve
- Porting IRIS GL, curve
- porting da IRIS GL, curve
- porting in OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad544431adaa7f0b049341ec7314e3e53ae60752d633a48c760ca09334f79d33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553861"
---
# <a name="porting-trimming-curves"></a>Porting di curve di taglio

Le curve di taglio OpenGL sono molto simili alle curve di taglio IRIS GL. Nella tabella seguente sono elencate le funzioni IRIS GL per definire le curve di taglio e le funzioni OpenGL equivalenti.



| Funzione GL IRIS | Funzione OpenGL                        | Significato                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Inizia la definizione della curva di taglio.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Definisce una curva lineare a punti.    |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Specifica gli attributi trimming-curve. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Termina la definizione della curva di taglio.      |



 

??

 

 




