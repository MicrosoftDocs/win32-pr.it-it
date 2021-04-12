---
title: Curva di porting e funzioni di superficie
description: Curva di porting e funzioni di superficie
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Porting di IRIS GL, curve
- porting da IRIS GL, curve
- porting in OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
- Porting di IRIS GL, patch della superficie
- porting da IRIS GL, patch Surface
- porting in OpenGL da IRIS GL, patch della superficie
- Porting OpenGL da IRIS GL, patch della superficie
- curve
- patch della superficie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328828"
---
# <a name="porting-curve-and-surface-functions"></a>Curva di porting e funzioni di superficie

OpenGL non supporta gli equivalenti alle funzioni di IRIS GL per le curve e le patch della superficie. È necessario riscrivere il codice se include una delle chiamate seguenti:

-   **defbasis**
-   **curvebasis**, **curveprecision**, **CRV**, **legato vanadio**, **rcrv**, **rcrvn** e **curveit**
-   **patchbasis**, **patchcurves**, **patchprecision**, **patch** e **rpatch**

Questo argomento include informazioni sui seguenti elementi.

-   [Porting di oggetti NURBS](porting-nurbs-objects.md)
-   [Porting di curve NURBS](porting-nurbs-curves.md)
-   [Porting delle curve di taglio](porting-trimming-curves.md)
-   [Porting di superfici NURBS](porting-nurbs-surfaces.md)

 

 




