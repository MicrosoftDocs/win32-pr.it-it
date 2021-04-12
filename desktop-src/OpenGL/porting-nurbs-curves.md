---
title: Porting di curve NURBS
description: Le funzioni OpenGL per il disegno di curve NURBS sono molto simili alle funzioni GL di IRIS. È possibile specificare sequenze di nodi e punti di controllo utilizzando una funzione gluNurbsCurve, che deve essere contenuta all'interno di una coppia gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Porting di IRIS GL, curve NURBS
- porting da IRIS GL, curve NURBS
- porting in OpenGL da IRIS GL, curve NURBS
- Porting OpenGL da IRIS GL, curve NURBS
- Curve NURBS
- curve
- Porting di IRIS GL, curve
- porting da IRIS GL, curve
- porting in OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
- NURBS (B-spline razionale non uniforme)
- B-spline razionale non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396335"
---
# <a name="porting-nurbs-curves"></a>Porting di curve NURBS

Le funzioni OpenGL per il disegno di curve NURBS sono molto simili alle funzioni GL di IRIS. È possibile specificare sequenze di nodi e punti di controllo utilizzando una funzione [**gluNurbsCurve**](glunurbscurve.md) , che deve essere contenuta all'interno di una [](glubegincurve.md)  /  coppia [**gluEndCurve**](gluendcurve.md) gluBeginCurve.

La tabella seguente elenca le funzioni di IRIS GL per la creazione di curve NURBS e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                        | Significato                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Inizia una definizione della curva.  |
| **NurbsCurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Specifica gli attributi della curva. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Termina una definizione di curva.    |



 

Associare le coordinate della posizione, della trama e del colore presentando ognuno come **gluNurbsCurve** separato all'interno della coppia di inizio/fine. È possibile non eseguire più di una chiamata a **gluNurbsCurve** per ogni parte dei dati di colore, posizione e trama all'interno di una singola coppia **gluBeginCurve/gluEndCurve** . È necessario effettuare esattamente una chiamata per descrivere la posizione della curva (una descrizione di GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Vertex \_ 4). Quando si chiama **gluEndCurve**, la curva è tassellati in segmenti di linea e viene quindi sottoposta a rendering.

La tabella seguente elenca i tipi di curve NURBS IRIS e OpenGL.



| Tipo GL IRIS | Tipo OpenGL                  | Significato                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | \_Vertice GL \_ Mappa1 \_ 3          | Curva polinomiale.                       |
| N \_ V3DR      | \_Mappa1 \_ Vertex \_ 4          | Curva razionale.                         |
|              | \_ \_ Coord trama GL \_ Mappa1\_\* | I punti di controllo sono coordinate di trama. |
|              | \_Normale MAPPA1 \_ GL             | I punti di controllo sono normali.             |



 

Per ulteriori informazioni sui tipi di analizzatore disponibili, vedere [**glMap1**](glmap1.md).

??

 

 




