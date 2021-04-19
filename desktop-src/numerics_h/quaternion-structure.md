---
title: struttura Quaternion (Windowsnumerics. h)
description: Vettore a quattro dimensioni, usato per rappresentare una rotazione.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- struttura Quaternion
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332789"
---
# <a name="quaternion-structure"></a><span data-ttu-id="50a58-104">Struttura Quaternion</span><span class="sxs-lookup"><span data-stu-id="50a58-104">quaternion Structure</span></span>

<span data-ttu-id="50a58-105">Vettore a quattro dimensioni, usato per rappresentare una rotazione.</span><span class="sxs-lookup"><span data-stu-id="50a58-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="50a58-106">Un quaternione può ruotare in modo efficiente un oggetto relativo al vettore (x, y, z) in base all'angolo theta, dove w = cos (theta/2).</span><span class="sxs-lookup"><span data-stu-id="50a58-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="50a58-107">I quaternioni vengono in genere usati per l'interpolazione uniforme tra due angoli e per evitare il problema di blocco del cardano che può verificarsi con gli angoli di Eulero.</span><span class="sxs-lookup"><span data-stu-id="50a58-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="50a58-108">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="50a58-108">This type is available only in C++.</span></span> <span data-ttu-id="50a58-109">Il relativo equivalente .NET è [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="50a58-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="50a58-110">Costruttori</span><span class="sxs-lookup"><span data-stu-id="50a58-110">Constructors</span></span>

| <span data-ttu-id="50a58-111">Nome</span><span class="sxs-lookup"><span data-stu-id="50a58-111">Name</span></span> | <span data-ttu-id="50a58-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a58-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="50a58-113">Crea un quaternione non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="50a58-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="50a58-114">Crea un quaternione con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="50a58-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="50a58-115">Crea un quaternione da un float3 e scalare.</span><span class="sxs-lookup"><span data-stu-id="50a58-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="50a58-116">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Quaternion** in un quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="50a58-117">Funzioni</span><span class="sxs-lookup"><span data-stu-id="50a58-117">Functions</span></span>

| <span data-ttu-id="50a58-118">Nome</span><span class="sxs-lookup"><span data-stu-id="50a58-118">Name</span></span> | <span data-ttu-id="50a58-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a58-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="50a58-120">Crea un quaternione da un vettore e un angolo per la rotazione intorno al vettore.</span><span class="sxs-lookup"><span data-stu-id="50a58-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="50a58-121">Crea un quaternione dagli angoli specificati per l'imbardata, il pitch e il roll.</span><span class="sxs-lookup"><span data-stu-id="50a58-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="50a58-122">Crea un quaternione da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="50a58-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="50a58-123">Verifica se si tratta di un quaternione Identity (nessuna rotazione).</span><span class="sxs-lookup"><span data-stu-id="50a58-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="50a58-124">Calcola la lunghezza di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="50a58-125">Calcola la lunghezza quadrata di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="50a58-126">Calcola il prodotto scalare di due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="50a58-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="50a58-127">Divide ogni componente di un quaternione per la lunghezza del quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="50a58-128">Calcola il coniugato di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="50a58-129">Calcola l'inverso di un quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="50a58-130">Esegue l'interpolazione tra due quaternioni usando l'interpolazione lineare sferica.</span><span class="sxs-lookup"><span data-stu-id="50a58-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="50a58-131">Interpolazione lineare tra due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="50a58-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-132">Concatena due quaternioni; il risultato rappresenta la prima rotazione seguita dalla seconda rotazione.</span><span class="sxs-lookup"><span data-stu-id="50a58-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="50a58-133">Metodi</span><span class="sxs-lookup"><span data-stu-id="50a58-133">Methods</span></span>

| <span data-ttu-id="50a58-134">Nome</span><span class="sxs-lookup"><span data-stu-id="50a58-134">Name</span></span> | <span data-ttu-id="50a58-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a58-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="50a58-136">Restituisce un'istanza del quaternione di identità.</span><span class="sxs-lookup"><span data-stu-id="50a58-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="50a58-137">Operatori</span><span class="sxs-lookup"><span data-stu-id="50a58-137">Operators</span></span>

| <span data-ttu-id="50a58-138">Nome</span><span class="sxs-lookup"><span data-stu-id="50a58-138">Name</span></span> | <span data-ttu-id="50a58-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a58-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-140">Aggiunge due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="50a58-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-141">Sottrae un quaternione da un altro quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-142">Moltiplica un quaternione per un altro quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="50a58-143">Moltiplica un quaternione per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="50a58-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-144">Divide un quaternione da un altro quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="50a58-145">Capovolge il segno di ogni componente del quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="50a58-146">Sul posto vengono aggiunti due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="50a58-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="50a58-147">Il sul posto sottrae un quaternione da un altro quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="50a58-148">Sul posto moltiplica un quaternione per un altro quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="50a58-149">Nultiplies sul posto di un quaternione da un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="50a58-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="50a58-150">Sul posto divide un quaternione da un altro quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-151">Determina se due istanze del quaternione sono uguali.</span><span class="sxs-lookup"><span data-stu-id="50a58-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="50a58-152">Determina se due istanze di Quaternion non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="50a58-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="50a58-153">Converte un quaternione in un oggetto **Microsoft. graphics. Canvas. Numerics. Quaternion**.</span><span class="sxs-lookup"><span data-stu-id="50a58-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="50a58-154">Campi</span><span class="sxs-lookup"><span data-stu-id="50a58-154">Fields</span></span>

| <span data-ttu-id="50a58-155">Nome</span><span class="sxs-lookup"><span data-stu-id="50a58-155">Name</span></span> | <span data-ttu-id="50a58-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a58-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="50a58-157">Valore X del componente Vector del quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="50a58-158">Valore Y del componente Vector del quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="50a58-159">Valore Z del componente Vector del quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="50a58-160">Componente di rotazione del quaternione.</span><span class="sxs-lookup"><span data-stu-id="50a58-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="50a58-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50a58-161">Requirements</span></span>

| <span data-ttu-id="50a58-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="50a58-162">Requirement</span></span> | <span data-ttu-id="50a58-163">Valore</span><span class="sxs-lookup"><span data-stu-id="50a58-163">Value</span></span> |
|-|-|
| <span data-ttu-id="50a58-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50a58-164">Namespace</span></span> | <span data-ttu-id="50a58-165">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="50a58-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="50a58-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50a58-166">Header</span></span> | <dl> <span data-ttu-id="50a58-167"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a58-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="50a58-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50a58-168">See also</span></span>

[<span data-ttu-id="50a58-169">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="50a58-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
