---
title: Uso di curve e superfici NURBS
description: Le funzioni NURBS B-spline (NURBS) non uniformi forniscono descrizioni generali e potenti di curve e superfici in due e tre dimensioni, convertendo le curve e le superfici negli analizzatori OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilità OpenGL (GLU), B-spline razionale non uniforme (NURBS)
- GLU (utilità OpenGL), B-spline razionale non uniforme (NURBS)
- OpenGL B-spline (NURBS) non uniforme
- OpenGL (non-Uniform Rational B-spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329199"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Uso di curve e superfici NURBS

Le funzioni NURBS B-spline (NURBS) non uniformi forniscono descrizioni generali e potenti di curve e superfici in due e tre dimensioni, convertendo le curve e le superfici negli analizzatori OpenGL. Le funzioni NURBS possono rappresentare la geometria in molti sistemi di progettazione meccanica computerizzati. Possono eseguire il rendering di curve e superfici in un'ampia gamma di stili e possono gestire automaticamente la suddivisione adattiva che tessellates il dominio in triangoli più piccoli in aree di curvatura elevata e bordi vicino alla silhouette. Le funzioni NURBS rientrano nelle categorie seguenti.

Per gestire un oggetto NURBS, usare:

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (crea un oggetto NURBS)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (Elimina un oggetto NURBS)
-   [*gluNurbsCallback*](glunurbs.md) (stabilisce una funzione di gestione degli errori)

Per specificare le curve desiderate, usare:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Per specificare le superfici desiderate, usare:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

È anche possibile specificare un'area di trimming, che definisce un subset del dominio della superficie NURBS da valutare, in modo da poter creare superfici con limiti smussati o che contengono buchi.

Per specificare l'area di trimming, usare:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Come per gli oggetti quadrica, è possibile controllare la modalità di rendering delle curve e delle superfici NURBS. È possibile determinare:

-   Indica se rimuovere una curva o una superficie il cui poliedro di controllo si trova al di fuori del viewport corrente.
-   Lunghezza massima (in pixel) dei bordi dei poligoni utilizzati per il rendering di curve e superfici.
-   Sia che si tratti della matrice di proiezione, della matrice Modelview e del viewport dal server OpenGL o di fornire loro esplicitamente con [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Usare [**gluNurbsProperty**](glunurbsproperty.md) per impostare queste proprietà o usare i valori predefiniti. È possibile eseguire una query su un oggetto NURBS sullo stile di rendering con [**gluGetNurbsProperty**](glugetnurbsproperty.md).

 

 




