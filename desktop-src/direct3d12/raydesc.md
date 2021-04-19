---
description: Passato alla funzione TraceRay per definire l'origine, la direzione e gli extent del raggio.
ms.assetid: ''
title: Struttura RayDesc
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305067"
---
# <a name="raydesc-structure"></a><span data-ttu-id="dc30d-103">Struttura RayDesc</span><span class="sxs-lookup"><span data-stu-id="dc30d-103">RayDesc structure</span></span>

<span data-ttu-id="dc30d-104">Passato alla funzione [**TraceRay**](traceray-function.md) per definire l'origine, la direzione e gli extent del raggio.</span><span class="sxs-lookup"><span data-stu-id="dc30d-104">Passed to the [**TraceRay**](traceray-function.md) function to define the origin, direction, and extents of the ray.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc30d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc30d-105">Syntax</span></span>


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a><span data-ttu-id="dc30d-106">Campi</span><span class="sxs-lookup"><span data-stu-id="dc30d-106">Fields</span></span>

<dl> <dt>

<span data-ttu-id="dc30d-107"><span id="Origin"></span><span id="origin"></span>**Origine**</span><span class="sxs-lookup"><span data-stu-id="dc30d-107"><span id="Origin"></span><span id="origin"></span>**Origin**</span></span>
</dt> <dd>

<span data-ttu-id="dc30d-108">Origine del raggio.</span><span class="sxs-lookup"><span data-stu-id="dc30d-108">The origin of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="dc30d-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span><span class="sxs-lookup"><span data-stu-id="dc30d-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span></span>
</dt> <dd>

<span data-ttu-id="dc30d-110">Extent minimo del raggio.</span><span class="sxs-lookup"><span data-stu-id="dc30d-110">The minimum extent of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="dc30d-111"><span id="Direction"></span><span id="direction"></span>**Direzione**</span><span class="sxs-lookup"><span data-stu-id="dc30d-111"><span id="Direction"></span><span id="direction"></span>**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="dc30d-112">Direzione del raggio.</span><span class="sxs-lookup"><span data-stu-id="dc30d-112">The direction of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="dc30d-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span><span class="sxs-lookup"><span data-stu-id="dc30d-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span></span>
</dt> <dd>

<span data-ttu-id="dc30d-114">Extent massimo del raggio.</span><span class="sxs-lookup"><span data-stu-id="dc30d-114">The maximum extent of the ray.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="dc30d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc30d-115">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="dc30d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc30d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc30d-117">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="dc30d-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




