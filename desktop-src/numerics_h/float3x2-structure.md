---
title: struttura float3x2 (Windowsnumerics. h)
description: Matrice 3x2 utilizzata per le trasformazioni 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- struttura float3x2
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332803"
---
# <a name="float3x2-structure"></a><span data-ttu-id="7a925-104">struttura float3x2</span><span class="sxs-lookup"><span data-stu-id="7a925-104">float3x2 structure</span></span>

<span data-ttu-id="7a925-105">Matrice 3x2 utilizzata per le trasformazioni 2D.</span><span class="sxs-lookup"><span data-stu-id="7a925-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="7a925-106">Questo tipo di matrice utilizza un layout vettoriale di riga.</span><span class="sxs-lookup"><span data-stu-id="7a925-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="7a925-107">Le x e y del vettore di traduzione della matrice corrispondono ai campi M31, M32.</span><span class="sxs-lookup"><span data-stu-id="7a925-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="7a925-108">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="7a925-108">This type is available only in C++.</span></span> <span data-ttu-id="7a925-109">Il relativo equivalente .NET è [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="7a925-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="7a925-110">Costruttori</span><span class="sxs-lookup"><span data-stu-id="7a925-110">Constructors</span></span>

| <span data-ttu-id="7a925-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7a925-111">Name</span></span> | <span data-ttu-id="7a925-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a925-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="7a925-113">Crea un float3x2 non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="7a925-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="7a925-114">Crea un float3x2 con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="7a925-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="7a925-115">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Matrix3x2** in un float3x2.</span><span class="sxs-lookup"><span data-stu-id="7a925-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="7a925-116">Funzioni</span><span class="sxs-lookup"><span data-stu-id="7a925-116">Functions</span></span>

| <span data-ttu-id="7a925-117">Nome</span><span class="sxs-lookup"><span data-stu-id="7a925-117">Name</span></span> | <span data-ttu-id="7a925-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a925-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="7a925-119">Crea una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="7a925-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="7a925-120">Crea una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="7a925-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="7a925-121">Crea una matrice di scala, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="7a925-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="7a925-122">Crea una matrice di scala, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a925-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="7a925-123">Crea una matrice di scala, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="7a925-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="7a925-124">Crea una matrice di scala, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a925-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="7a925-125">Crea una matrice di scala, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="7a925-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="7a925-126">Crea una matrice di scala, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a925-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="7a925-127">Crea una matrice di inclinazione, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="7a925-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="7a925-128">Crea una matrice di inclinazione, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a925-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="7a925-129">Crea una matrice di rotazione, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="7a925-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="7a925-130">Crea una matrice di rotazione, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="7a925-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="7a925-131">Verifica se si tratta di una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="7a925-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="7a925-132">Calcola il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="7a925-133">Ottiene il vettore di traslazione della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="7a925-134">Calcola l'inverso di una matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="7a925-135">Restituisce true se la matrice può essere invertita; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="7a925-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="7a925-136">Esegue l'interpolazione lineare tra i valori corrispondenti di due matrici.</span><span class="sxs-lookup"><span data-stu-id="7a925-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="7a925-137">Metodi</span><span class="sxs-lookup"><span data-stu-id="7a925-137">Methods</span></span>

| <span data-ttu-id="7a925-138">Nome</span><span class="sxs-lookup"><span data-stu-id="7a925-138">Name</span></span> | <span data-ttu-id="7a925-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a925-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="7a925-140">Restituisce un'istanza della matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="7a925-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="7a925-141">Operatori</span><span class="sxs-lookup"><span data-stu-id="7a925-141">Operators</span></span>

| <span data-ttu-id="7a925-142">Nome</span><span class="sxs-lookup"><span data-stu-id="7a925-142">Name</span></span> | <span data-ttu-id="7a925-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a925-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-144">Aggiunge ogni componente di una matrice a un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-145">Sottrae ogni componente di una matrice da un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-146">Moltiplica una matrice per un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="7a925-147">Questo ha l'effetto di concatenare due trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="7a925-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="7a925-148">Moltiplica ogni componente di una matrice in base a un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="7a925-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="7a925-149">Nega ogni componente di una matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-150">Sul posto aggiunge ogni componente di una matrice a un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-151">Il sul posto sottrae ogni componente di una matrice da un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-152">Sul posto viene moltiplicata una matrice da un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="7a925-153">Questo ha l'effetto di concatenare due trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="7a925-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="7a925-154">Sul posto moltiplica ogni componente di una matrice per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="7a925-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-155">Determina se due istanze di float3x2 sono uguali.</span><span class="sxs-lookup"><span data-stu-id="7a925-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7a925-156">Determina se due istanze di float3x2 non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="7a925-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="7a925-157">Converte un float3x2 in un oggetto **Microsoft. graphics. Canvas. Numerics. Matrix3x2**.</span><span class="sxs-lookup"><span data-stu-id="7a925-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="7a925-158">Campi</span><span class="sxs-lookup"><span data-stu-id="7a925-158">Fields</span></span>

| <span data-ttu-id="7a925-159">Nome</span><span class="sxs-lookup"><span data-stu-id="7a925-159">Name</span></span> | <span data-ttu-id="7a925-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a925-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="7a925-161">Valore alla riga 1 colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="7a925-162">Valore alla riga 1 colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="7a925-163">Valore alla riga 2 colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="7a925-164">Valore alla riga 2 colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="7a925-165">Valore alla riga 3 della colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="7a925-166">Valore alla riga 3 colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="7a925-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="7a925-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a925-167">Requirements</span></span>

| <span data-ttu-id="7a925-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a925-168">Requirement</span></span> | <span data-ttu-id="7a925-169">Valore</span><span class="sxs-lookup"><span data-stu-id="7a925-169">Value</span></span> |
|-|-|
| <span data-ttu-id="7a925-170">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7a925-170">Namespace</span></span> | <span data-ttu-id="7a925-171">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="7a925-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="7a925-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a925-172">Header</span></span> | <dl> <span data-ttu-id="7a925-173"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a925-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="7a925-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a925-174">See also</span></span>

[<span data-ttu-id="7a925-175">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="7a925-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
