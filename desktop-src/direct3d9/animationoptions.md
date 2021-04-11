---
description: Consente di impostare le opzioni di animazione.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127130"
---
# <a name="animationoptions"></a><span data-ttu-id="e815e-103">AnimationOptions</span><span class="sxs-lookup"><span data-stu-id="e815e-103">AnimationOptions</span></span>

<span data-ttu-id="e815e-104">Consente di impostare le opzioni di animazione.</span><span class="sxs-lookup"><span data-stu-id="e815e-104">Enables you to set animation options.</span></span>

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

<span data-ttu-id="e815e-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="e815e-105">Where:</span></span>

-   <span data-ttu-id="e815e-106">openclosed: usare 0 per un'animazione chiusa o 1 per un'animazione aperta.</span><span class="sxs-lookup"><span data-stu-id="e815e-106">openclosed - Use 0 for a closed animation, or 1 for an open animation.</span></span> <span data-ttu-id="e815e-107">Per impostazione predefinita, un'animazione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="e815e-107">By default, an animation is closed.</span></span>
-   <span data-ttu-id="e815e-108">positionquality: impostare la qualità della posizione per le chiavi di posizione specificate.</span><span class="sxs-lookup"><span data-stu-id="e815e-108">positionquality - Set the position quality for any position keys specified.</span></span> <span data-ttu-id="e815e-109">Usare 0 per le posizioni spline o 1 per le posizioni lineari.</span><span class="sxs-lookup"><span data-stu-id="e815e-109">Use 0 for spline positions or 1 for linear positions.</span></span>

## <a name="see-also"></a><span data-ttu-id="e815e-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e815e-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e815e-111">Modelli</span><span class="sxs-lookup"><span data-stu-id="e815e-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



