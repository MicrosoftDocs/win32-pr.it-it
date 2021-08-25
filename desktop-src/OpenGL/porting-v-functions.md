---
title: Porting v Functions
description: In IRIS GL si usano le variazioni nella funzione v per specificare i vertici. La funzione OpenGL equivalente è glVertex Di seguito sono riportati esempi di glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- porting IRIS GL, vertici
- porting da IRIS GL, vertici
- porting in OpenGL da IRIS GL, vertici
- Porting OpenGL da IRIS GL, vertici
- funzioni di disegno, vertici
- vertici, porting da IRIS GL
- Porting IRIS GL,funzioni v
- porting da funzioni IRIS GL,v
- porting in OpenGL da funzioni IRIS GL,v
- Porting OpenGL da funzioni IRIS GL,v
- funzioni di disegno,funzioni v
- Funzioni v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e84fd5eb036afaf5291902ab00f91f3b155f7507d8fce7135dc8030323c1a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888071"
---
# <a name="porting-v-functions"></a>Porting v Functions

In IRIS GL si usano le variazioni nella **funzione v** per specificare i vertici. La funzione OpenGL equivalente è [glVertex](glvertex-functions.md): di seguito sono riportati esempi di **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

La **funzione glVertex** accetta suffissi nello stesso modo delle altre chiamate OpenGL. Le versioni vettoriali della chiamata accettano matrici delle dimensioni appropriate come argomenti. Nella versione 2D, z=0 e w=1. Nella versione 3D, w=1.

 

 




