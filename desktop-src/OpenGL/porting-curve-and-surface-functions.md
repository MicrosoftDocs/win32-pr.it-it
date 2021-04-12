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
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="50f0c-113">Curva di porting e funzioni di superficie</span><span class="sxs-lookup"><span data-stu-id="50f0c-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="50f0c-114">OpenGL non supporta gli equivalenti alle funzioni di IRIS GL per le curve e le patch della superficie.</span><span class="sxs-lookup"><span data-stu-id="50f0c-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="50f0c-115">È necessario riscrivere il codice se include una delle chiamate seguenti:</span><span class="sxs-lookup"><span data-stu-id="50f0c-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="50f0c-116">**defbasis**</span><span class="sxs-lookup"><span data-stu-id="50f0c-116">**defbasis**</span></span>
-   <span data-ttu-id="50f0c-117">**curvebasis**, **curveprecision**, **CRV**, **legato vanadio**, **rcrv**, **rcrvn** e **curveit**</span><span class="sxs-lookup"><span data-stu-id="50f0c-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="50f0c-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch** e **rpatch**</span><span class="sxs-lookup"><span data-stu-id="50f0c-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="50f0c-119">Questo argomento include informazioni sui seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="50f0c-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="50f0c-120">Porting di oggetti NURBS</span><span class="sxs-lookup"><span data-stu-id="50f0c-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="50f0c-121">Porting di curve NURBS</span><span class="sxs-lookup"><span data-stu-id="50f0c-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="50f0c-122">Porting delle curve di taglio</span><span class="sxs-lookup"><span data-stu-id="50f0c-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="50f0c-123">Porting di superfici NURBS</span><span class="sxs-lookup"><span data-stu-id="50f0c-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 




