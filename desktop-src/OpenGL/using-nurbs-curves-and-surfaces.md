---
title: Uso di curve e superfici NURBS
description: Le funzioni NURBS (Non-Uniform Rational B-Spline) forniscono descrizioni generali e potenti di curve e superfici in due e tre dimensioni, convertendo le curve e le superfici in analizzatori OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- OpenGL Utility (GLU),Non-Uniform Rational B-Spline (NURBS)
- GLU (utilità OpenGL),NuRBS (Non-Uniform Rational B-Spline)
- OpenGL (Non-Uniform Rational B-Spline) (NURBS)
- NURBS (Non-Uniform Rational B-Spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1b366571be7a9210576e78540c77970667aca2f37ec8a092de07edb97493d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932771"
---
# <a name="using-nurbs-curves-and-surfaces"></a>Uso di curve e superfici NURBS

Le funzioni NURBS (Non-Uniform Rational B-Spline) forniscono descrizioni generali e potenti di curve e superfici in due e tre dimensioni, convertendo le curve e le superfici in analizzatori OpenGL. Le funzioni NURBS possono rappresentare la geometria in molti sistemi di progettazione meccanica computer-aided. Possono eseguire il rendering di curve e superfici in un'ampia gamma di stili e possono gestire automaticamente la suddivisione adattiva che snoda il dominio in triangoli più piccoli in aree con curvatura elevata e in prossimità dei bordi del triangolo. Le funzioni NURBS rientrano nelle categorie seguenti.

Per gestire un oggetto NURBS, usare:

-   [**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (creare un oggetto NURBS)
-   [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (elimina un oggetto NURBS)
-   [*gluNurbsCallback*](glunurbs.md) (stabilisce una funzione di gestione degli errori)

Per specificare le curve desiderate, usare:

-   [**gluBeginCurve**](glubegincurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndCurve**](gluendcurve.md)

Per specificare le superfici desiderate, usare:

-   [**gluBeginSurface**](glubeginsurface.md)
-   [**gluNurbsSurface**](glunurbssurface.md)
-   [**gluEndSurface**](gluendsurface.md)

È anche possibile specificare un'area di taglio, che definisce un subset del dominio della superficie NURBS da valutare in modo da creare superfici con limiti uniformi o che contengono fori.

Per specificare l'area di taglio, usare:

-   [**gluBeginTrim**](glubegintrim.md)
-   [**gluPwlCurve**](glupwlcurve.md)
-   [**gluNurbsCurve**](glunurbscurve.md)
-   [**gluEndTrim**](gluendtrim.md)

Come per gli oggetti quadric, è possibile controllare la modalità di rendering delle curve e delle superfici NURBS. È possibile determinare:

-   Indica se eliminare una curva o una superficie il cui poliedro di controllo si trova all'esterno del viewport corrente.
-   Lunghezza massima (in pixel) dei bordi dei poligoni usata per eseguire il rendering di curve e superfici.
-   Se la matrice di proiezione, la matrice della visualizzazione modello e il riquadro di visualizzazione verranno accettati dal server OpenGL o forniti esplicitamente con [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).

Usare [**gluNurbsProperty**](glunurbsproperty.md) per impostare queste proprietà o usare i valori predefiniti. È possibile eseguire una query su un oggetto NURBS sul relativo stile di rendering [**con gluGetNurbsProperty.**](glugetnurbsproperty.md)

 

 




