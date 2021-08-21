---
title: Porting di curve NURBS
description: Le funzioni OpenGL per il disegno di curve NURBS sono molto simili alle funzioni IRIS GL. È possibile specificare sequenze di nodi e punti di controllo usando una funzione gluNurbsCurve, che deve essere contenuta in una coppia gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Porting IRIS GL, curve NURBS
- porting da curve IRIS GL,NURBS
- porting in OpenGL da curve IRIS GL,NURBS
- Porting OpenGL da curve IRIS GL,NURBS
- Curve NURBS
- curve
- porting IRIS GL, curve
- porting da IRIS GL, curve
- porting a OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
- NURBS (B-Spline razionale non uniforme)
- B-Spline razionale non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9aa43bcc40c2b6a93eb5690abe4265f792a58a2520e579d536a08520ca4f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132400"
---
# <a name="porting-nurbs-curves"></a>Porting di curve NURBS

Le funzioni OpenGL per il disegno di curve NURBS sono molto simili alle funzioni IRIS GL. È possibile specificare sequenze di nodi e punti di controllo usando una [**funzione gluNurbsCurve,**](glunurbscurve.md) che deve essere contenuta in una coppia [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve.**](gluendcurve.md)

Nella tabella seguente sono elencate le funzioni IRIS GL per il disegno di curve NURBS e le funzioni OpenGL equivalenti.



| Funzione GL IRIS | Funzione OpenGL                        | Significato                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Avvia una definizione di curva.  |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Specifica gli attributi della curva. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Termina una definizione di curva.    |



 

Associare le coordinate di posizione, trama e colore presentando ognuna come **gluNurbsCurve** separata all'interno della coppia inizio/fine. Non è possibile effettuare più di una chiamata a **gluNurbsCurve** per ogni parte di dati di colore, posizione e trama all'interno di una singola coppia **gluBeginCurve/gluEndCurve.** È necessario effettuare esattamente una chiamata per descrivere la posizione della curva (descrizione \_ \_ VERTEX 3 o GL \_ \_ MAP1 \_ VERTEX \_ 4). Quando si chiama **gluEndCurve**, la curva viene suddivisa in segmenti di linea e quindi sottoposta a rendering.

La tabella seguente elenca i tipi di curva IRIS GL e OpenGL NURBS.



| Tipo GL IRIS | Tipo OpenGL                  | Significato                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | VERTICE \_ \_ 3 GL MAP1 \_          | Curva polinomiale.                       |
| N \_ V3DR      | VERTICE \_ \_ 4 GL MAP1 \_          | Curva razionale.                         |
|              | GL \_ MAP1 \_ TEXTURE \_ COORD\_\* | I punti di controllo sono coordinate di trama. |
|              | GL \_ MAP1 \_ NORMAL             | I punti di controllo sono normali.             |



 

Per altre informazioni sui tipi di analizzatore disponibili, vedere [**glMap1**](glmap1.md).

??

 

 




