---
description: I valori di larghezza, altezza e profondità dalla struttura D3D12_DISPATCH_RAYS_DESC specificata nella chiamata DispatchRays di origine.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305311"
---
# <a name="dispatchraysdimensions"></a><span data-ttu-id="d0cf4-103">DispatchRaysDimensions</span><span class="sxs-lookup"><span data-stu-id="d0cf4-103">DispatchRaysDimensions</span></span>

<span data-ttu-id="d0cf4-104">I valori di larghezza, altezza e profondità della struttura **D3D12 di \_ distribuzione dei \_ raggi \_** di recapito specificata nella chiamata [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) di origine.</span><span class="sxs-lookup"><span data-stu-id="d0cf4-104">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0cf4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0cf4-105">Syntax</span></span>

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a><span data-ttu-id="d0cf4-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d0cf4-106">Remarks</span></span>

<span data-ttu-id="d0cf4-107">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="d0cf4-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="d0cf4-108">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="d0cf4-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="d0cf4-109">**Richiamabile shader**</span><span class="sxs-lookup"><span data-stu-id="d0cf4-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="d0cf4-110">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="d0cf4-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="d0cf4-111">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="d0cf4-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="d0cf4-112">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="d0cf4-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="d0cf4-113">**Shader di generazione del Ray**</span><span class="sxs-lookup"><span data-stu-id="d0cf4-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="d0cf4-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0cf4-114">See also</span></span>

* [<span data-ttu-id="d0cf4-115">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="d0cf4-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
