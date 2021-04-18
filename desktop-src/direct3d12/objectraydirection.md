---
description: Direzione dello spazio dell'oggetto per il raggio corrente.
ms.assetid: ''
title: ObjectRayDirection
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayDirection
api_type:
- NA
ms.openlocfilehash: 1cc291a33f91bf7fc0565596bdd075a86e193246
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304706"
---
# <a name="objectraydirection"></a><span data-ttu-id="cc575-103">ObjectRayDirection</span><span class="sxs-lookup"><span data-stu-id="cc575-103">ObjectRayDirection</span></span>

<span data-ttu-id="cc575-104">Direzione dello spazio dell'oggetto per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="cc575-104">The object-space direction for the current ray.</span></span> <span data-ttu-id="cc575-105">Oggetto-spazio si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.</span><span class="sxs-lookup"><span data-stu-id="cc575-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc575-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc575-106">Syntax</span></span>

```
float3 ObjectRayDirection();

```



## <a name="remarks"></a><span data-ttu-id="cc575-107">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="cc575-107">Remarks</span></span>

<span data-ttu-id="cc575-108">Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:</span><span class="sxs-lookup"><span data-stu-id="cc575-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="cc575-109">**Qualsiasi hit shader**</span><span class="sxs-lookup"><span data-stu-id="cc575-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="cc575-110">**Hit shader più vicino**</span><span class="sxs-lookup"><span data-stu-id="cc575-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="cc575-111">**Intersezione shader**</span><span class="sxs-lookup"><span data-stu-id="cc575-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="cc575-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc575-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc575-113">Guida di riferimento a Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="cc575-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




