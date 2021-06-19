---
title: Intrinseci dei valori di sistema HLSL raytracing di Direct3D 12
description: Visualizzare i collegamenti ad articoli che descrivono funzioni intrinseche intrinseche del valore di sistema HLSL (High-Level Shader Language) che supportano la pipeline di raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396436"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="b708c-103">Intrinseci dei valori di sistema HLSL raytracing di Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b708c-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="b708c-104">I valori di sistema vengono recuperati usando funzioni intrinseche speciali, anziché includere parametri con semantica speciale nella firma della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="b708c-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="b708c-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b708c-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="b708c-106">Valori del sistema ray dispatch</span><span class="sxs-lookup"><span data-stu-id="b708c-106">Ray dispatch system values</span></span>

| <span data-ttu-id="b708c-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="b708c-107">Topic</span></span> | <span data-ttu-id="b708c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b708c-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="b708c-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="b708c-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="b708c-110">Ottiene la posizione x e y corrente all'interno della larghezza e dell'altezza ottenute con il valore di sistema **DispatchRaysDimensions** intrinseco.</span><span class="sxs-lookup"><span data-stu-id="b708c-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="b708c-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="b708c-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="b708c-112">Valori di larghezza, altezza e profondità della struttura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** specificata nella chiamata **DispatchRays di** origine.</span><span class="sxs-lookup"><span data-stu-id="b708c-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="b708c-113">Valori del sistema di raggi</span><span class="sxs-lookup"><span data-stu-id="b708c-113">Ray system values</span></span>

| <span data-ttu-id="b708c-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="b708c-114">Topic</span></span> | <span data-ttu-id="b708c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b708c-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="b708c-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="b708c-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="b708c-117">Origine dello spazio del mondo del raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="b708c-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="b708c-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="b708c-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="b708c-119">Direzione dello spazio del mondo per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="b708c-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="b708c-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="b708c-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="b708c-121">Valore float che rappresenta il punto iniziale parametrico corrente per il raggio.</span><span class="sxs-lookup"><span data-stu-id="b708c-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="b708c-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="b708c-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="b708c-123">Valore float che rappresenta il punto finale parametrico corrente per il raggio.</span><span class="sxs-lookup"><span data-stu-id="b708c-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="b708c-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="b708c-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="b708c-125">Intero senza segno contenente i **flag** ray_flag corrente.</span><span class="sxs-lookup"><span data-stu-id="b708c-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="b708c-126">Valori di sistema dello spazio degli oggetti/primitivi</span><span class="sxs-lookup"><span data-stu-id="b708c-126">Primitive/object space system values</span></span>

| <span data-ttu-id="b708c-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="b708c-127">Topic</span></span> | <span data-ttu-id="b708c-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b708c-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="b708c-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="b708c-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="b708c-130">Indice rigenerato automaticamente dell'istanza corrente nella struttura di accelerazione raytracing di primo livello.</span><span class="sxs-lookup"><span data-stu-id="b708c-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="b708c-131">**Instanceid**</span><span class="sxs-lookup"><span data-stu-id="b708c-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="b708c-132">Identificatore fornito dall'utente per l'istanza nell'istanza della struttura di accelerazione di livello inferiore all'interno della struttura di primo livello.</span><span class="sxs-lookup"><span data-stu-id="b708c-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="b708c-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="b708c-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="b708c-134">Indice rigenerato automaticamente della primitiva all'interno della geometria all'interno dell'istanza della struttura di accelerazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="b708c-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="b708c-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="b708c-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="b708c-136">Origine dello spazio oggetti per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="b708c-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="b708c-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="b708c-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="b708c-138">Direzione dello spazio oggetto per il raggio corrente.</span><span class="sxs-lookup"><span data-stu-id="b708c-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="b708c-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="b708c-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="b708c-140">Matrice per la trasformazione dallo spazio oggetti allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="b708c-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="b708c-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="b708c-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="b708c-142">Matrice per la trasformazione dallo spazio oggetti allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="b708c-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="b708c-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="b708c-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="b708c-144">Matrice per la trasformazione dallo spazio globale allo spazio oggetti</span><span class="sxs-lookup"><span data-stu-id="b708c-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="b708c-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="b708c-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="b708c-146">Matrice per la trasformazione dallo spazio globale allo spazio oggetti</span><span class="sxs-lookup"><span data-stu-id="b708c-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="b708c-147">Valori di sistema specifici dei hit</span><span class="sxs-lookup"><span data-stu-id="b708c-147">Hit-specific system values</span></span>

| <span data-ttu-id="b708c-148">Argomento</span><span class="sxs-lookup"><span data-stu-id="b708c-148">Topic</span></span> | <span data-ttu-id="b708c-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b708c-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="b708c-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="b708c-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="b708c-151">Restituisce il valore passato come parametro **HitKind** a [**ReportHit.**](reporthit-function.md)</span><span class="sxs-lookup"><span data-stu-id="b708c-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="b708c-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b708c-152">Related topics</span></span>

* [<span data-ttu-id="b708c-153">Informazioni di riferimento di base</span><span class="sxs-lookup"><span data-stu-id="b708c-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="b708c-154">Informazioni di riferimento su Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b708c-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
