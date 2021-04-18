---
description: Ottiene la posizione corrente entro la larghezza, l'altezza e la profondità ottenute con il valore intrinseco di sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) .
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "106300640"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="1d9ca-103">DispatchRaysIndex </span><span class="sxs-lookup"><span data-stu-id="1d9ca-103">DispatchRaysIndex</span></span>

<span data-ttu-id="1d9ca-104">Ottiene la posizione corrente entro la larghezza, l'altezza e la profondità ottenute con il valore intrinseco di sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) .</span><span class="sxs-lookup"><span data-stu-id="1d9ca-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d9ca-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="1d9ca-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="1d9ca-106">Remarks</span></span>

<span data-ttu-id="1d9ca-107">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing.</span><span class="sxs-lookup"><span data-stu-id="1d9ca-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="1d9ca-108">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="1d9ca-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="1d9ca-109">**Richiamabile shader**</span><span class="sxs-lookup"><span data-stu-id="1d9ca-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="1d9ca-110">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="1d9ca-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="1d9ca-111">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="1d9ca-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="1d9ca-112">**Lo shader manca**</span><span class="sxs-lookup"><span data-stu-id="1d9ca-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="1d9ca-113">**Shader di generazione del Ray**</span><span class="sxs-lookup"><span data-stu-id="1d9ca-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="1d9ca-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d9ca-114">See also</span></span>

* [<span data-ttu-id="1d9ca-115">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="1d9ca-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
