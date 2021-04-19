---
title: struttura float4 (Windowsnumerics. h)
description: Vettore con quattro componenti.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- struttura float4
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332792"
---
# <a name="float4-structure"></a><span data-ttu-id="fad5a-104">struttura float4</span><span class="sxs-lookup"><span data-stu-id="fad5a-104">float4 structure</span></span>

<span data-ttu-id="fad5a-105">Vettore con quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="fad5a-105">A vector with four components.</span></span>

<span data-ttu-id="fad5a-106">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="fad5a-106">This type is available only in C++.</span></span> <span data-ttu-id="fad5a-107">Il relativo equivalente .NET è [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="fad5a-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="fad5a-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="fad5a-108">Constructors</span></span>

| <span data-ttu-id="fad5a-109">Nome</span><span class="sxs-lookup"><span data-stu-id="fad5a-109">Name</span></span> | <span data-ttu-id="fad5a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad5a-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="fad5a-111">Crea un float4 non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="fad5a-112">Crea un float4 con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="fad5a-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="fad5a-113">Crea una float4 con x e y copiata da un float2 più i valori z e w specificati.</span><span class="sxs-lookup"><span data-stu-id="fad5a-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="fad5a-114">Crea un float4 con x, y e z copiati da un float3 più il valore w specificato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="fad5a-115">Crea un float4 con tutti i set di impostazioni com. ent impostati sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="fad5a-116">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Vector4** in un float4.</span><span class="sxs-lookup"><span data-stu-id="fad5a-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="fad5a-117">Funzioni</span><span class="sxs-lookup"><span data-stu-id="fad5a-117">Functions</span></span>

| <span data-ttu-id="fad5a-118">Nome</span><span class="sxs-lookup"><span data-stu-id="fad5a-118">Name</span></span> | <span data-ttu-id="fad5a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad5a-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="fad5a-120">Calcola la lunghezza o la distanza euclidea del vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="fad5a-121">Calcola la lunghezza o la distanza euclidea del vettore quadrato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-122">Calcola la distanza euclidea tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-123">Calcola la distanza euclidea tra due vettori quadrati.</span><span class="sxs-lookup"><span data-stu-id="fad5a-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="fad5a-124">Calcola il prodotto a punti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="fad5a-125">Crea un vettore di unità dal vettore specificato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-126">Restituisce un vettore che contiene il valore più basso di ogni coppia di componenti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fad5a-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-127">Restituisce un vettore che contiene il valore massimo di ogni coppia di componenti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fad5a-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="fad5a-128">Limita un valore all'interno di un intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="fad5a-129">Esegue un'interpolazione lineare tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="fad5a-130">Trasforma un float4 in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="fad5a-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="fad5a-131">Trasforma un float3 in base alla matrice specificata, restituendo un float4.</span><span class="sxs-lookup"><span data-stu-id="fad5a-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="fad5a-132">Trasforma un float2 in base alla matrice specificata, restituendo un float4.</span><span class="sxs-lookup"><span data-stu-id="fad5a-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="fad5a-133">Trasforma un float4 in base al quaternione specificato.</span><span class="sxs-lookup"><span data-stu-id="fad5a-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="fad5a-134">Trasforma un float3 in base al quaternione specificato, restituendo un float4.</span><span class="sxs-lookup"><span data-stu-id="fad5a-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="fad5a-135">Trasforma un float2 in base al quaternione specificato, restituendo un float4.</span><span class="sxs-lookup"><span data-stu-id="fad5a-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="fad5a-136">Metodi</span><span class="sxs-lookup"><span data-stu-id="fad5a-136">Methods</span></span>

| <span data-ttu-id="fad5a-137">Nome</span><span class="sxs-lookup"><span data-stu-id="fad5a-137">Name</span></span> | <span data-ttu-id="fad5a-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad5a-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="fad5a-139">Restituisce un float4 con tutti i relativi componenti impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="fad5a-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="fad5a-140">Restituisce un float4 con tutti i relativi componenti impostati su uno.</span><span class="sxs-lookup"><span data-stu-id="fad5a-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="fad5a-141">Restituisce float4 (1, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="fad5a-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="fad5a-142">Restituisce float4 (0, 1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="fad5a-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="fad5a-143">Restituisce float4 (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="fad5a-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="fad5a-144">Restituisce float4 (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="fad5a-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="fad5a-145">Operatori</span><span class="sxs-lookup"><span data-stu-id="fad5a-145">Operators</span></span>

| <span data-ttu-id="fad5a-146">Nome</span><span class="sxs-lookup"><span data-stu-id="fad5a-146">Name</span></span> | <span data-ttu-id="fad5a-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad5a-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-148">Aggiunge due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-149">Sottrae un vettore da un vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-150">Moltiplica i componenti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="fad5a-151">Moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="fad5a-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="fad5a-152">Moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="fad5a-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-153">Divide i componenti di un vettore in base ai componenti di un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="fad5a-154">Divide un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="fad5a-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="fad5a-155">Restituisce un vettore che punta nella direzione opposta.</span><span class="sxs-lookup"><span data-stu-id="fad5a-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="fad5a-156">Sul posto vengono aggiunti due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="fad5a-157">Il sul posto sottrae un vettore da un vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="fad5a-158">Sul posto moltiplica i componenti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="fad5a-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="fad5a-159">Sul posto moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="fad5a-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="fad5a-160">Sul posto divide i componenti di un vettore in base ai componenti di un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="fad5a-161">Sul posto divide un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="fad5a-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-162">Determina se due istanze di float4 sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fad5a-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="fad5a-163">Determina se due istanze di float4 non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fad5a-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="fad5a-164">Converte un float4 in un oggetto **Microsoft. graphics. Canvas. Numerics. Vector4**.</span><span class="sxs-lookup"><span data-stu-id="fad5a-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="fad5a-165">Campi</span><span class="sxs-lookup"><span data-stu-id="fad5a-165">Fields</span></span>

| <span data-ttu-id="fad5a-166">Nome</span><span class="sxs-lookup"><span data-stu-id="fad5a-166">Name</span></span> | <span data-ttu-id="fad5a-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad5a-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="fad5a-168">Componente X del vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="fad5a-169">Componente Y del vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="fad5a-170">Componente Z del vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="fad5a-171">Componente W del vettore.</span><span class="sxs-lookup"><span data-stu-id="fad5a-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="fad5a-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fad5a-172">Requirements</span></span>

| <span data-ttu-id="fad5a-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad5a-173">Requirement</span></span> | <span data-ttu-id="fad5a-174">Valore</span><span class="sxs-lookup"><span data-stu-id="fad5a-174">Value</span></span> |
|-|-|
| <span data-ttu-id="fad5a-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fad5a-175">Namespace</span></span> | <span data-ttu-id="fad5a-176">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="fad5a-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="fad5a-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fad5a-177">Header</span></span> | <dl> <span data-ttu-id="fad5a-178"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad5a-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="fad5a-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fad5a-179">See also</span></span>

[<span data-ttu-id="fad5a-180">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="fad5a-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
