---
title: Oggetti intrinseci del valore di sistema di Direct3D 12 raytracing HLSL
description: Gli shader HLSL seguenti supportano la pipeline raytracing di Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "106300642"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="c1637-103">Oggetti intrinseci del valore di sistema di Direct3D 12 raytracing HLSL</span><span class="sxs-lookup"><span data-stu-id="c1637-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="c1637-104">I valori di sistema vengono recuperati usando funzioni intrinseche speciali, anziché includere parametri con semantica speciale nella firma della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="c1637-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="c1637-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c1637-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="c1637-106">Valori del sistema ray dispatch</span><span class="sxs-lookup"><span data-stu-id="c1637-106">Ray dispatch system values</span></span>

| <span data-ttu-id="c1637-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="c1637-107">Topic</span></span> | <span data-ttu-id="c1637-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1637-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="c1637-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="c1637-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="c1637-110">Ottiene la posizione x e y corrente all'interno della larghezza e dell'altezza ottenuta con il valore intrinseco di sistema **DispatchRaysDimensions** .</span><span class="sxs-lookup"><span data-stu-id="c1637-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="c1637-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="c1637-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="c1637-112">I valori di larghezza, altezza e profondità della struttura **D3D12 di \_ distribuzione dei \_ raggi \_** di recapito specificata nella chiamata **DispatchRays** di origine.</span><span class="sxs-lookup"><span data-stu-id="c1637-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="c1637-113">Valori del sistema ray</span><span class="sxs-lookup"><span data-stu-id="c1637-113">Ray system values</span></span>

| <span data-ttu-id="c1637-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="c1637-114">Topic</span></span> | <span data-ttu-id="c1637-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1637-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="c1637-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="c1637-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="c1637-117">Origine dello spazio globale del raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="c1637-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="c1637-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="c1637-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="c1637-119">Direzione dello spazio globale per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="c1637-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="c1637-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="c1637-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="c1637-121">Float che rappresenta il punto di partenza parametrico corrente per il raggio.</span><span class="sxs-lookup"><span data-stu-id="c1637-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="c1637-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="c1637-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="c1637-123">Valore float che rappresenta il punto finale parametrico corrente per il raggio.</span><span class="sxs-lookup"><span data-stu-id="c1637-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="c1637-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="c1637-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="c1637-125">Unsigned Integer contenente i flag di **ray_flag** correnti.</span><span class="sxs-lookup"><span data-stu-id="c1637-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="c1637-126">Valori di sistema per spazio oggetti/primitivi</span><span class="sxs-lookup"><span data-stu-id="c1637-126">Primitive/object space system values</span></span>

| <span data-ttu-id="c1637-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="c1637-127">Topic</span></span> | <span data-ttu-id="c1637-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1637-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="c1637-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="c1637-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="c1637-130">Indice generato automaticamente dell'istanza corrente nella struttura di accelerazione raytracing di primo livello.</span><span class="sxs-lookup"><span data-stu-id="c1637-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="c1637-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1637-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="c1637-132">Identificatore fornito dall'utente per l'istanza nell'istanza della struttura di accelerazione di livello inferiore all'interno della struttura di primo livello.</span><span class="sxs-lookup"><span data-stu-id="c1637-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="c1637-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="c1637-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="c1637-134">Indice generato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="c1637-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="c1637-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="c1637-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="c1637-136">Origine dello spazio oggetto per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="c1637-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="c1637-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="c1637-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="c1637-138">Direzione dello spazio dell'oggetto per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="c1637-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="c1637-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="c1637-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="c1637-140">Matrice per la trasformazione dallo spazio oggetto allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="c1637-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="c1637-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="c1637-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="c1637-142">Matrice per la trasformazione dallo spazio oggetto allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="c1637-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="c1637-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="c1637-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="c1637-144">Matrice per la trasformazione da spazio globale a oggetto-spazio</span><span class="sxs-lookup"><span data-stu-id="c1637-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="c1637-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="c1637-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="c1637-146">Matrice per la trasformazione da spazio globale a oggetto-spazio</span><span class="sxs-lookup"><span data-stu-id="c1637-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="c1637-147">Valori di sistema specifici di hit</span><span class="sxs-lookup"><span data-stu-id="c1637-147">Hit-specific system values</span></span>

| <span data-ttu-id="c1637-148">Argomento</span><span class="sxs-lookup"><span data-stu-id="c1637-148">Topic</span></span> | <span data-ttu-id="c1637-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1637-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="c1637-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="c1637-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="c1637-151">Restituisce il valore passato come parametro **HitKind** a [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c1637-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="c1637-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1637-152">Related topics</span></span>

* [<span data-ttu-id="c1637-153">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="c1637-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="c1637-154">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c1637-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
