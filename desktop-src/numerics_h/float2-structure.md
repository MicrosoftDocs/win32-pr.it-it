---
title: struttura float2 (Windowsnumerics. h)
description: Vettore con due componenti.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- struttura float2
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332805"
---
# <a name="float2-structure"></a><span data-ttu-id="bf53f-104">struttura float2</span><span class="sxs-lookup"><span data-stu-id="bf53f-104">float2 structure</span></span>

<span data-ttu-id="bf53f-105">Vettore con due componenti.</span><span class="sxs-lookup"><span data-stu-id="bf53f-105">A vector with two components.</span></span>

<span data-ttu-id="bf53f-106">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="bf53f-106">This type is available only in C++.</span></span> <span data-ttu-id="bf53f-107">L'equivalente .NET è [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="bf53f-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="bf53f-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="bf53f-108">Constructors</span></span>

| <span data-ttu-id="bf53f-109">Nome</span><span class="sxs-lookup"><span data-stu-id="bf53f-109">Name</span></span> | <span data-ttu-id="bf53f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf53f-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="bf53f-111">Crea un float2 non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="bf53f-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="bf53f-112">Crea un float2 con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="bf53f-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="bf53f-113">Crea un float2 con tutti i componenti impostati sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="bf53f-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="bf53f-114">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Vector2** in un float2.</span><span class="sxs-lookup"><span data-stu-id="bf53f-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="bf53f-115">Converte un oggetto [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) in un float2.</span><span class="sxs-lookup"><span data-stu-id="bf53f-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="bf53f-116">Converte un oggetto [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) in un float2.</span><span class="sxs-lookup"><span data-stu-id="bf53f-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="bf53f-117">Funzioni</span><span class="sxs-lookup"><span data-stu-id="bf53f-117">Functions</span></span>

| <span data-ttu-id="bf53f-118">Nome</span><span class="sxs-lookup"><span data-stu-id="bf53f-118">Name</span></span> | <span data-ttu-id="bf53f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf53f-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="bf53f-120">Calcola la lunghezza o la distanza euclidea del vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="bf53f-121">Calcola la lunghezza o la distanza euclidea del vettore quadrato.</span><span class="sxs-lookup"><span data-stu-id="bf53f-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-122">Calcola la distanza euclidea tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-123">Calcola la distanza euclidea tra due vettori quadrati.</span><span class="sxs-lookup"><span data-stu-id="bf53f-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-124">Calcola il prodotto a punti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="bf53f-125">Crea un vettore di unità dal vettore specificato.</span><span class="sxs-lookup"><span data-stu-id="bf53f-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="bf53f-126">Determina il vettore di reflection del vettore specificato e il normale.</span><span class="sxs-lookup"><span data-stu-id="bf53f-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-127">Restituisce un vettore che contiene il valore più basso di ogni coppia di componenti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bf53f-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-128">Restituisce un vettore che contiene il valore massimo di ogni coppia di componenti corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bf53f-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="bf53f-129">Limita un valore all'interno di un intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="bf53f-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="bf53f-130">Esegue un'interpolazione lineare tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="bf53f-131">Trasforma il vettore (x, y, 0, 1) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="bf53f-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="bf53f-132">Trasforma il vettore (x, y, 0, 1) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="bf53f-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="bf53f-133">Trasforma il vettore normale (x, y, 0, 0) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="bf53f-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="bf53f-134">Trasforma il vettore normale (x, y, 0, 0) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="bf53f-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="bf53f-135">Trasforma un float2 in base al quaternione specificato.</span><span class="sxs-lookup"><span data-stu-id="bf53f-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="bf53f-136">Metodi</span><span class="sxs-lookup"><span data-stu-id="bf53f-136">Methods</span></span>

| <span data-ttu-id="bf53f-137">Nome</span><span class="sxs-lookup"><span data-stu-id="bf53f-137">Name</span></span> | <span data-ttu-id="bf53f-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf53f-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="bf53f-139">Restituisce un float2 con tutti i relativi componenti impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="bf53f-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="bf53f-140">Restituisce un float2 con tutti i relativi componenti impostati su uno.</span><span class="sxs-lookup"><span data-stu-id="bf53f-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="bf53f-141">Restituisce float2 (1,0).</span><span class="sxs-lookup"><span data-stu-id="bf53f-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="bf53f-142">Restituisce float2 (0, 1).</span><span class="sxs-lookup"><span data-stu-id="bf53f-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="bf53f-143">Operatori</span><span class="sxs-lookup"><span data-stu-id="bf53f-143">Operators</span></span>

| <span data-ttu-id="bf53f-144">Nome</span><span class="sxs-lookup"><span data-stu-id="bf53f-144">Name</span></span> | <span data-ttu-id="bf53f-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf53f-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="bf53f-146">Converte un float2 in un oggetto [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point).</span><span class="sxs-lookup"><span data-stu-id="bf53f-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="bf53f-147">Converte un float2 in un oggetto [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size).</span><span class="sxs-lookup"><span data-stu-id="bf53f-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-148">Aggiunge due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-149">Sottrae un vettore da un vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-150">Moltiplica i componenti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="bf53f-151">Moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="bf53f-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="bf53f-152">Moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="bf53f-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-153">Divide i componenti di un vettore in base ai componenti di un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="bf53f-154">Divide un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="bf53f-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="bf53f-155">Restituisce un vettore che punta nella direzione opposta.</span><span class="sxs-lookup"><span data-stu-id="bf53f-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="bf53f-156">Sul posto vengono aggiunti due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="bf53f-157">Il sul posto sottrae un vettore da un vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="bf53f-158">Sul posto moltiplica i componenti di due vettori.</span><span class="sxs-lookup"><span data-stu-id="bf53f-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="bf53f-159">Sul posto moltiplica un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="bf53f-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="bf53f-160">Sul posto divide i componenti di un vettore in base ai componenti di un altro vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="bf53f-161">Sul posto divide un vettore per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="bf53f-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-162">Determina se due istanze di float2 sono uguali.</span><span class="sxs-lookup"><span data-stu-id="bf53f-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="bf53f-163">Determina se due istanze di float2 non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="bf53f-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="bf53f-164">Converte un float2 in un oggetto **Microsoft. graphics. Canvas. Numerics. Vector2**.</span><span class="sxs-lookup"><span data-stu-id="bf53f-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="bf53f-165">Campi</span><span class="sxs-lookup"><span data-stu-id="bf53f-165">Fields</span></span>

| <span data-ttu-id="bf53f-166">Nome</span><span class="sxs-lookup"><span data-stu-id="bf53f-166">Name</span></span> | <span data-ttu-id="bf53f-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf53f-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="bf53f-168">Componente X del vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="bf53f-169">Componente Y del vettore.</span><span class="sxs-lookup"><span data-stu-id="bf53f-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="bf53f-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf53f-170">Requirements</span></span>

| <span data-ttu-id="bf53f-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf53f-171">Requirement</span></span> | <span data-ttu-id="bf53f-172">Valore</span><span class="sxs-lookup"><span data-stu-id="bf53f-172">Value</span></span> |
|-|-|
| <span data-ttu-id="bf53f-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf53f-173">Namespace</span></span> | <span data-ttu-id="bf53f-174">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="bf53f-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="bf53f-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf53f-175">Header</span></span> | <dl> <span data-ttu-id="bf53f-176"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf53f-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="bf53f-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf53f-177">See also</span></span>

[<span data-ttu-id="bf53f-178">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="bf53f-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
