---
title: struttura float3 (Windowsnumerics. h)
description: Vettore con tre componenti.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- struttura float3
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332804"
---
# <a name="float3-structure"></a><span data-ttu-id="eee46-104">struttura float3</span><span class="sxs-lookup"><span data-stu-id="eee46-104">float3 structure</span></span>

<span data-ttu-id="eee46-105">Vettore con tre componenti.</span><span class="sxs-lookup"><span data-stu-id="eee46-105">A vector with three components.</span></span>

<span data-ttu-id="eee46-106">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="eee46-106">This type is available only in C++.</span></span> <span data-ttu-id="eee46-107">Il relativo equivalente .NET è [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="eee46-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="eee46-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="eee46-108">Constructors</span></span>

| <span data-ttu-id="eee46-109">Nome</span><span class="sxs-lookup"><span data-stu-id="eee46-109">Name</span></span> | <span data-ttu-id="eee46-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee46-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="eee46-111">Crea un float3 non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="eee46-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="eee46-112">Crea un float3 con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="eee46-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="eee46-113">Crea una float3 con x e y copiata da un float2 più il valore z specificato.</span><span class="sxs-lookup"><span data-stu-id="eee46-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="eee46-114">Crea un float3 con tutti i componenti impostati sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="eee46-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="eee46-115">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Vector3** in un float3.</span><span class="sxs-lookup"><span data-stu-id="eee46-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="eee46-116">Funzioni</span><span class="sxs-lookup"><span data-stu-id="eee46-116">Functions</span></span>

| <span data-ttu-id="eee46-117">Nome</span><span class="sxs-lookup"><span data-stu-id="eee46-117">Name</span></span> | <span data-ttu-id="eee46-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee46-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="eee46-119">Calcola la lunghezza o la distanza euclidea del vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="eee46-120">Calcola la lunghezza o la distanza euclidea del vettore quadrato.</span><span class="sxs-lookup"><span data-stu-id="eee46-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-121">Calcola la distanza euclidea tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-122">Calcola la distanza euclidea tra due vettori quadrati.</span><span class="sxs-lookup"><span data-stu-id="eee46-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="eee46-123">Calcola il prodotto a punti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="eee46-124">Crea un vettore di unità dal vettore specificato.</span><span class="sxs-lookup"><span data-stu-id="eee46-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="eee46-125">Calcola il prodotto incrociato di due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="eee46-126">Determina il vettore di reflection del vettore specificato e il normale.</span><span class="sxs-lookup"><span data-stu-id="eee46-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-127">Restituisce un vettore che contiene il valore più basso di ogni coppia di componenti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="eee46-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-128">Restituisce un vettore che contiene il valore massimo di ogni coppia di componenti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="eee46-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="eee46-129">Limita un valore all'interno di un intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="eee46-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="eee46-130">Esegue un'interpolazione lineare tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="eee46-131">Trasforma il vettore (x, y, z,1) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="eee46-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="eee46-132">Trasforma il vettore normale (x, y, z, 0) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="eee46-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="eee46-133">Trasforma un float3 in base al quaternione specificato.</span><span class="sxs-lookup"><span data-stu-id="eee46-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="eee46-134">Metodi</span><span class="sxs-lookup"><span data-stu-id="eee46-134">Methods</span></span>

| <span data-ttu-id="eee46-135">Nome</span><span class="sxs-lookup"><span data-stu-id="eee46-135">Name</span></span> | <span data-ttu-id="eee46-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee46-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="eee46-137">Restituisce un float3 con tutti i relativi componenti impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="eee46-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="eee46-138">Restituisce un float3 con tutti i relativi componenti impostati su uno.</span><span class="sxs-lookup"><span data-stu-id="eee46-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="eee46-139">Restituisce float3 (1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="eee46-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="eee46-140">Restituisce float3 (0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="eee46-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="eee46-141">Restituisce float3 (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="eee46-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="eee46-142">Operatori</span><span class="sxs-lookup"><span data-stu-id="eee46-142">Operators</span></span>

| <span data-ttu-id="eee46-143">Nome</span><span class="sxs-lookup"><span data-stu-id="eee46-143">Name</span></span> | <span data-ttu-id="eee46-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee46-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-145">Aggiunge due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-146">Sottrae un vettore da un vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-147">Moltiplica i componenti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="eee46-148">Moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="eee46-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="eee46-149">Moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="eee46-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-150">Divide i componenti di un vettore in base ai componenti di un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="eee46-151">Divide un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="eee46-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="eee46-152">Restituisce un vettore che punta nella direzione opposta.</span><span class="sxs-lookup"><span data-stu-id="eee46-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="eee46-153">Sul posto vengono aggiunti due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="eee46-154">Il sul posto sottrae un vettore da un vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="eee46-155">Sul posto moltiplica i componenti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="eee46-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="eee46-156">Sul posto moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="eee46-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="eee46-157">Sul posto divide i componenti di un vettore in base ai componenti di un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="eee46-158">Sul posto divide un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="eee46-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-159">Determina se due istanze di float3 sono uguali.</span><span class="sxs-lookup"><span data-stu-id="eee46-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="eee46-160">Determina se due istanze di float3 non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="eee46-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="eee46-161">Converte un float3 in un oggetto **Microsoft. graphics. Canvas. Numerics. Vector3**.</span><span class="sxs-lookup"><span data-stu-id="eee46-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="eee46-162">Campi</span><span class="sxs-lookup"><span data-stu-id="eee46-162">Fields</span></span>

| <span data-ttu-id="eee46-163">Nome</span><span class="sxs-lookup"><span data-stu-id="eee46-163">Name</span></span> | <span data-ttu-id="eee46-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee46-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="eee46-165">Componente X del vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="eee46-166">Componente Y del vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="eee46-167">Componente Z del vettore.</span><span class="sxs-lookup"><span data-stu-id="eee46-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="eee46-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eee46-168">Requirements</span></span>

| <span data-ttu-id="eee46-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee46-169">Requirement</span></span> | <span data-ttu-id="eee46-170">Valore</span><span class="sxs-lookup"><span data-stu-id="eee46-170">Value</span></span> |
|-|-|
| <span data-ttu-id="eee46-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eee46-171">Namespace</span></span> | <span data-ttu-id="eee46-172">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="eee46-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="eee46-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eee46-173">Header</span></span> | <dl> <span data-ttu-id="eee46-174"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee46-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="eee46-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eee46-175">See also</span></span>

[<span data-ttu-id="eee46-176">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="eee46-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
