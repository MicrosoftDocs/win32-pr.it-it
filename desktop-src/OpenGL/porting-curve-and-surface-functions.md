---
title: Funzioni curve e surface di portabilità
description: Funzioni curve e surface di portabilità
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Portabilità IRIS GL, curve
- porting from IRIS GL,curves
- porting to OpenGL from IRIS GL,curves
- Portabilità OpenGL da IRIS GL, curve
- Portabilità IRIS GL, patch di superficie
- porting da IRIS GL, patch di superficie
- porting to OpenGL from IRIS GL,surface patches
- Portabilità OpenGL da IRIS GL, patch di superficie
- curve
- patch di superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed76109bb0067996c26acf48bff7a58773220ad1eb87e13d617bddedeb6d62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777041"
---
# <a name="porting-curve-and-surface-functions"></a>Funzioni curve e surface di portabilità

OpenGL non supporta equivalenti alle funzioni IRIS GL per curve e patch di superficie. Sarà necessario riscrivere il codice se include una delle chiamate seguenti:

-   **defbasis**
-   **curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn** e **curveit**
-   **patchbasis,** **patchcurves,** **patchprecision,** **patch** e **rpatch**

Questo argomento include informazioni sugli argomenti seguenti.

-   [Portabilità di oggetti NURBS](porting-nurbs-objects.md)
-   [Porting di curve NURBS](porting-nurbs-curves.md)
-   [Porting di curve di taglio](porting-trimming-curves.md)
-   [Porting di superfici NURBS](porting-nurbs-surfaces.md)

 

 




