---
description: Float che rappresenta il punto di partenza parametrico corrente per il raggio.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305063"
---
# <a name="raytmin"></a><span data-ttu-id="47491-103">RayTMin</span><span class="sxs-lookup"><span data-stu-id="47491-103">RayTMin</span></span>

<span data-ttu-id="47491-104">Float che rappresenta il punto di partenza parametrico corrente per il raggio.</span><span class="sxs-lookup"><span data-stu-id="47491-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="47491-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47491-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="47491-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="47491-106">Remarks</span></span>

<span data-ttu-id="47491-107">**RayTMin** definisce il punto iniziale del raggio in base alla formula seguente: Origin + (Direction \* RayTMin).</span><span class="sxs-lookup"><span data-stu-id="47491-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="47491-108">L' *origine* e la *direzione* possono trovarsi nel mondo o nello spazio degli oggetti, il che comporta il punto di partenza di un mondo o uno spazio oggetti.</span><span class="sxs-lookup"><span data-stu-id="47491-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="47491-109">**RayTMin** viene specificato nella chiamata a [**TraceRay**](traceray-function.md)ed è costante per la durata della chiamata.</span><span class="sxs-lookup"><span data-stu-id="47491-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="47491-110">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="47491-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="47491-111">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="47491-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="47491-112">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="47491-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="47491-113">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="47491-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="47491-114">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="47491-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="47491-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47491-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47491-116">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="47491-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




