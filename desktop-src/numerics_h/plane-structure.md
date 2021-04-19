---
title: struttura del piano (Windowsnumerics. h)
description: Questa struttura rappresenta un piano usando un vettore 3D normale e un valore di distanza.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- struttura del piano
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332790"
---
# <a name="plane-structure"></a><span data-ttu-id="794bb-104">struttura del piano</span><span class="sxs-lookup"><span data-stu-id="794bb-104">plane structure</span></span>

<span data-ttu-id="794bb-105">Questa struttura rappresenta un piano usando un vettore 3D normale e un valore di distanza.</span><span class="sxs-lookup"><span data-stu-id="794bb-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="794bb-106">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="794bb-106">This type is available only in C++.</span></span> <span data-ttu-id="794bb-107">Il relativo equivalente .NET è [System. Numerics. Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="794bb-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="794bb-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="794bb-108">Constructors</span></span>

| <span data-ttu-id="794bb-109">Nome</span><span class="sxs-lookup"><span data-stu-id="794bb-109">Name</span></span> | <span data-ttu-id="794bb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="794bb-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="794bb-111">Crea un piano non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="794bb-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="794bb-112">Crea un piano con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="794bb-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="794bb-113">Crea un piano da un float3 e da una distanza.</span><span class="sxs-lookup"><span data-stu-id="794bb-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="794bb-114">Crea un piano da un float4.</span><span class="sxs-lookup"><span data-stu-id="794bb-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="794bb-115">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Plane** in un piano.</span><span class="sxs-lookup"><span data-stu-id="794bb-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="794bb-116">Funzioni</span><span class="sxs-lookup"><span data-stu-id="794bb-116">Functions</span></span>

| <span data-ttu-id="794bb-117">Nome</span><span class="sxs-lookup"><span data-stu-id="794bb-117">Name</span></span> | <span data-ttu-id="794bb-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="794bb-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="794bb-119">Crea un piano da un set di tre posizioni del vertice, che devono essere tutte diverse e non in una linea retta.</span><span class="sxs-lookup"><span data-stu-id="794bb-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="794bb-120">Modifica i coefficienti del vettore normale di un piano per renderlo di lunghezza dell'unità.</span><span class="sxs-lookup"><span data-stu-id="794bb-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="794bb-121">Trasforma un piano normalizzato in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="794bb-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="794bb-122">Trasforma un piano normalizzato in base a una rotazione quaternione.</span><span class="sxs-lookup"><span data-stu-id="794bb-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="794bb-123">Calcola il prodotto a punti di un piano con un vettore.</span><span class="sxs-lookup"><span data-stu-id="794bb-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="794bb-124">Calcola il prodotto punto di un piano con una coordinata float3.</span><span class="sxs-lookup"><span data-stu-id="794bb-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="794bb-125">Diversamente dal punto \_ normale, questo calcolo include il valore del piano d.</span><span class="sxs-lookup"><span data-stu-id="794bb-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="794bb-126">Calcola il prodotto a punti di un piano con una normale float3.</span><span class="sxs-lookup"><span data-stu-id="794bb-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="794bb-127">A differenza \_ della coordinata del punto, questo calcolo ignora il valore del piano d.</span><span class="sxs-lookup"><span data-stu-id="794bb-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="794bb-128">Operatori</span><span class="sxs-lookup"><span data-stu-id="794bb-128">Operators</span></span>

| <span data-ttu-id="794bb-129">Nome</span><span class="sxs-lookup"><span data-stu-id="794bb-129">Name</span></span> | <span data-ttu-id="794bb-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="794bb-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="794bb-131">Determina se due istanze del piano sono uguali.</span><span class="sxs-lookup"><span data-stu-id="794bb-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="794bb-132">Determina se due istanze del piano non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="794bb-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="794bb-133">Converte un piano in un oggetto **Microsoft. graphics. Canvas. Numerics. Plane**.</span><span class="sxs-lookup"><span data-stu-id="794bb-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="794bb-134">Campi</span><span class="sxs-lookup"><span data-stu-id="794bb-134">Fields</span></span>

| <span data-ttu-id="794bb-135">Nome</span><span class="sxs-lookup"><span data-stu-id="794bb-135">Name</span></span> | <span data-ttu-id="794bb-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="794bb-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="794bb-137">Vettore normale del piano.</span><span class="sxs-lookup"><span data-stu-id="794bb-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="794bb-138">Distanza del piano lungo la normale dall'origine.</span><span class="sxs-lookup"><span data-stu-id="794bb-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="794bb-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="794bb-139">Requirements</span></span>

| <span data-ttu-id="794bb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="794bb-140">Requirement</span></span> | <span data-ttu-id="794bb-141">Valore</span><span class="sxs-lookup"><span data-stu-id="794bb-141">Value</span></span> |
|-|-|
| <span data-ttu-id="794bb-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="794bb-142">Namespace</span></span> | <span data-ttu-id="794bb-143">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="794bb-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="794bb-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="794bb-144">Header</span></span> | <dl> <span data-ttu-id="794bb-145"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="794bb-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="794bb-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="794bb-146">See also</span></span>

[<span data-ttu-id="794bb-147">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="794bb-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
