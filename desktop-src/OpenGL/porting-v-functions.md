---
title: Funzioni di porting v
description: In IRIS GL si usano le variazioni sulla funzione v per specificare i vertici. La funzione OpenGL equivalente è glVertex di seguito sono riportati esempi di glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Porting di IRIS GL, vertici
- porting da IRIS GL, vertici
- porting in OpenGL da IRIS GL, vertici
- Porting OpenGL da IRIS GL, vertici
- funzioni di disegno, vertici
- vertici, porting da IRIS GL
- Porting di IRIS GL, funzioni v
- porting da IRIS GL, v Functions
- porting in OpenGL dalle funzioni di IRIS GL, v
- Porting OpenGL dalle funzioni di IRIS GL, v
- funzioni di disegno, funzioni v
- funzioni v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329420"
---
# <a name="porting-v-functions"></a>Funzioni di porting v

In IRIS GL si usano le variazioni sulla funzione **v** per specificare i vertici. La funzione OpenGL equivalente è [glVertex](glvertex-functions.md): di seguito sono riportati alcuni esempi di **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

La funzione **glVertex** accetta suffissi allo stesso modo di altre chiamate di OpenGL. Le versioni vettoriali della chiamata accettano matrici di dimensioni appropriate come argomenti. Nella versione 2D, z = 0 e w = 1. Nella versione 3D, w = 1.

 

 




