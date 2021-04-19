---
title: struttura float4x4 (Windowsnumerics. h)
description: Matrice 4x4 usata per le trasformazioni 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- struttura float4x4
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332791"
---
# <a name="float4x4-structure"></a><span data-ttu-id="cbc4b-104">struttura float4x4</span><span class="sxs-lookup"><span data-stu-id="cbc4b-104">float4x4 structure</span></span>

<span data-ttu-id="cbc4b-105">Matrice 4x4 usata per le trasformazioni 3D.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-105">A 4x4 matrix, used for 3D transforms.</span></span>

<span data-ttu-id="cbc4b-106">Questo tipo di matrice utilizza un layout vettoriale di riga.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="cbc4b-107">X, y e z del vettore di conversione della matrice corrispondono ai campi M41, M42, M43.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-107">The x, y, and z of this matrix's translation vector correspond to the fields m41, m42, m43.</span></span>

<span data-ttu-id="cbc4b-108">Questo tipo è disponibile solo in C++.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-108">This type is available only in C++.</span></span> <span data-ttu-id="cbc4b-109">Il relativo equivalente .NET è [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="cbc4b-109">Its .NET equivalent is [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="cbc4b-110">Costruttori</span><span class="sxs-lookup"><span data-stu-id="cbc4b-110">Constructors</span></span>

| <span data-ttu-id="cbc4b-111">Nome</span><span class="sxs-lookup"><span data-stu-id="cbc4b-111">Name</span></span> | <span data-ttu-id="cbc4b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbc4b-112">Description</span></span> |
|-|-|
| `float4x4()` | <span data-ttu-id="cbc4b-113">Crea un float4x4 non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-113">Creates an uninitialized float4x4.</span></span> |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | <span data-ttu-id="cbc4b-114">Crea un float4x4 con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-114">Creates a float4x4 with the specified values.</span></span> |
| `explicit float4x4(float3x2 value)` | <span data-ttu-id="cbc4b-115">Crea un float4x4 da un float3x2.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-115">Creates a float4x4 from a float3x2.</span></span> |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | <span data-ttu-id="cbc4b-116">Converte un oggetto **Microsoft. graphics. Canvas. Numerics. Matrix4x4** in un float4x4.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** to a float4x4.</span></span> |

## <a name="functions"></a><span data-ttu-id="cbc4b-117">Funzioni</span><span class="sxs-lookup"><span data-stu-id="cbc4b-117">Functions</span></span>

| <span data-ttu-id="cbc4b-118">Nome</span><span class="sxs-lookup"><span data-stu-id="cbc4b-118">Name</span></span> | <span data-ttu-id="cbc4b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbc4b-119">Description</span></span> |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | <span data-ttu-id="cbc4b-120">Crea un tabellone sferico che ruota intorno a una posizione di oggetto specificata, usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-120">Creates a spherical billboard that rotates around a specified object position, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | <span data-ttu-id="cbc4b-121">Crea un tabellone cilindrico che ruota intorno a un asse specificato, usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-121">Creates a cylindrical billboard that rotates around a specified axis, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_translation(float3 const& position)` | <span data-ttu-id="cbc4b-122">Crea una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-122">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | <span data-ttu-id="cbc4b-123">Crea una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-123">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | <span data-ttu-id="cbc4b-124">Crea una matrice di scala, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-124">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | <span data-ttu-id="cbc4b-125">Crea una matrice di scala, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-125">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales)` | <span data-ttu-id="cbc4b-126">Crea una matrice di scala, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-126">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | <span data-ttu-id="cbc4b-127">Crea una matrice di scala, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-127">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float scale)` | <span data-ttu-id="cbc4b-128">Crea una matrice di scala, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-128">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | <span data-ttu-id="cbc4b-129">Crea una matrice di scala, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-129">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians)` | <span data-ttu-id="cbc4b-130">Crea una matrice di rotazione dell'asse x, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-130">Creates an x-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | <span data-ttu-id="cbc4b-131">Crea una matrice di rotazione dell'asse x, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-131">Creates an x-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians)` | <span data-ttu-id="cbc4b-132">Crea una matrice di rotazione dell'asse y, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-132">Creates a y-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | <span data-ttu-id="cbc4b-133">Crea una matrice di rotazione dell'asse y, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-133">Creates a y-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians)` | <span data-ttu-id="cbc4b-134">Crea una matrice di rotazione dell'asse z, centrata sull'origine.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-134">Creates a z-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | <span data-ttu-id="cbc4b-135">Crea una matrice di rotazione dell'asse z, centrata sul punto specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-135">Creates a z-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="cbc4b-136">Crea una matrice che ruota intorno a un vettore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-136">Creates a matrix that rotates around an arbitrary vector.</span></span> |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="cbc4b-137">Crea una matrice di proiezione prospettica in base a un campo di visualizzazione, usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-137">Creates a perspective projection matrix based on a field of view, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="cbc4b-138">Crea una matrice di proiezione prospettica usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-138">Creates a perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="cbc4b-139">Crea una matrice di proiezione prospettica personalizzata, usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-139">Creates a customized perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | <span data-ttu-id="cbc4b-140">Crea una matrice di proiezione ortogonale usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-140">Creates an orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | <span data-ttu-id="cbc4b-141">Crea una matrice di proiezione ortogonale personalizzata, usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-141">Creates a customized orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | <span data-ttu-id="cbc4b-142">Crea una matrice di visualizzazione utilizzando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-142">Creates a view matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | <span data-ttu-id="cbc4b-143">Crea una matrice globale, usando un sistema di coordinate di destra.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-143">Creates a world matrix, using a right handed coordinate system.</span></span> <span data-ttu-id="cbc4b-144">Può essere usato per posizionare gli oggetti nello spazio 3D.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-144">This can be used to position objects in 3D space.</span></span> |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | <span data-ttu-id="cbc4b-145">Crea una matrice di rotazione da un quaternione.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-145">Creates a rotation matrix from a quaternion.</span></span> |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="cbc4b-146">Crea una matrice di rotazione da un'imbardata, un passo e un rullo specificati.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-146">Creates a rotation matrix from a specified yaw, pitch, and roll.</span></span> |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | <span data-ttu-id="cbc4b-147">Crea una matrice che appiattisce la geometria in un piano specificato come se si proiettasse un'ombra da una sorgente di luce specificata.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-147">Creates a matrix that flattens geometry into a specified plane as if casting a shadow from a specified light source.</span></span> |
| `float4x4 make_float4x4_reflection(plane const& value)` | <span data-ttu-id="cbc4b-148">Crea una matrice che crea un sistema di coordinate speculare rispetto a un piano specificato.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-148">Creates a matrix that reflects the coordinate system about a specified plane.</span></span> |
| `bool is_identity(float4x4 const& value)` | <span data-ttu-id="cbc4b-149">Verifica se si tratta di una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-149">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float4x4 const& value)` | <span data-ttu-id="cbc4b-150">Calcola il determinante della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-150">Calculates the determinant of the matrix.</span></span> |
| `float3 translation(float4x4 const& value)` | <span data-ttu-id="cbc4b-151">Ottiene il vettore di traslazione della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-151">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | <span data-ttu-id="cbc4b-152">Calcola l'inverso di una matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-152">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="cbc4b-153">Restituisce true se la matrice può essere invertita; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-153">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | <span data-ttu-id="cbc4b-154">Estrae i componenti scalari, di traslazione e di rotazione da una matrice 3D Scale/Rotate/Translate (SRT).</span><span class="sxs-lookup"><span data-stu-id="cbc4b-154">Extracts the scalar, translation, and rotation components from a 3D scale/rotate/translate (SRT) matrix.</span></span> <span data-ttu-id="cbc4b-155">Restituisce true se la matrice può essere scomposta; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-155">Returns true if the matrix can be decomposed; false otherwise.</span></span> |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | <span data-ttu-id="cbc4b-156">Trasforma una matrice applicando una rotazione quaternione.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-156">Transforms a matrix by applying a quaternion rotation.</span></span> |
| `float4x4 transpose(float4x4 const& matrix)` | <span data-ttu-id="cbc4b-157">Traspone i componenti di una matrice lungo la diagonale.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-157">Transposes the components of a matrix along its diagonal.</span></span> |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | <span data-ttu-id="cbc4b-158">Esegue l'interpolazione lineare tra i valori corrispondenti di due matrici.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-158">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="cbc4b-159">Metodi</span><span class="sxs-lookup"><span data-stu-id="cbc4b-159">Methods</span></span>

| <span data-ttu-id="cbc4b-160">Nome</span><span class="sxs-lookup"><span data-stu-id="cbc4b-160">Name</span></span> | <span data-ttu-id="cbc4b-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbc4b-161">Description</span></span> |
|-|-|
| `static float4x4 identity()` | <span data-ttu-id="cbc4b-162">Restituisce un'istanza della matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-162">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="cbc4b-163">Operatori</span><span class="sxs-lookup"><span data-stu-id="cbc4b-163">Operators</span></span>

| <span data-ttu-id="cbc4b-164">Nome</span><span class="sxs-lookup"><span data-stu-id="cbc4b-164">Name</span></span> | <span data-ttu-id="cbc4b-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbc4b-165">Description</span></span> |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-166">Aggiunge ogni componente di una matrice a un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-166">Adds each component of a matrix to another matrix.</span></span> |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-167">Sottrae ogni componente di una matrice da un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-167">Subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-168">Moltiplica una matrice per un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-168">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="cbc4b-169">Questo ha l'effetto di concatenare due trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-169">This has the effect of concatenating two transforms.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float value2)` | <span data-ttu-id="cbc4b-170">Moltiplica ogni componente di una matrice in base a un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-170">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float4x4 operator- (float4x4 const& value)` | <span data-ttu-id="cbc4b-171">Nega ogni componente di una matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-171">Negates each component of a matrix.</span></span> |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-172">Sul posto aggiunge ogni componente di una matrice a un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-172">In-place adds each component of a matrix to another matrix.</span></span> |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-173">Il sul posto sottrae ogni componente di una matrice da un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-173">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-174">Sul posto viene moltiplicata una matrice da un'altra matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-174">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="cbc4b-175">Questo ha l'effetto di concatenare due trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-175">This has the effect of concatenating two transforms.</span></span> |
| `float4x4& operator*= (float4x4& value1, float value2)` | <span data-ttu-id="cbc4b-176">Sul posto moltiplica ogni componente di una matrice per un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-176">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-177">Determina se due istanze di float4x4 sono uguali.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-177">Determines whether two instances of float4x4 are equal.</span></span> |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="cbc4b-178">Determina se due istanze di float4x4 non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-178">Determines whether two instances of float4x4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | <span data-ttu-id="cbc4b-179">Converte un float4x4 in un oggetto **Microsoft. graphics. Canvas. Numerics. Matrix4x4**.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-179">Converts a float4x4 to a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="cbc4b-180">Campi</span><span class="sxs-lookup"><span data-stu-id="cbc4b-180">Fields</span></span>

| <span data-ttu-id="cbc4b-181">Nome</span><span class="sxs-lookup"><span data-stu-id="cbc4b-181">Name</span></span> | <span data-ttu-id="cbc4b-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbc4b-182">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="cbc4b-183">Valore alla riga 1 colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-183">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="cbc4b-184">Valore alla riga 1 colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-184">Value at row 1 column 2 of the matrix.</span></span> |
| `float m13` | <span data-ttu-id="cbc4b-185">Valore alla riga 1 colonna 3 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-185">Value at row 1 column 3 of the matrix.</span></span> |
| `float m14` | <span data-ttu-id="cbc4b-186">Valore alla riga 1 colonna 4 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-186">Value at row 1 column 4 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="cbc4b-187">Valore alla riga 2 colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-187">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="cbc4b-188">Valore alla riga 2 colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-188">Value at row 2 column 2 of the matrix.</span></span> |
| `float m23` | <span data-ttu-id="cbc4b-189">Valore alla riga 2 colonna 3 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-189">Value at row 2 column 3 of the matrix.</span></span> |
| `float m24` | <span data-ttu-id="cbc4b-190">Valore alla riga 2 colonna 4 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-190">Value at row 2 column 4 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="cbc4b-191">Valore alla riga 3 della colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-191">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="cbc4b-192">Valore alla riga 3 colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-192">Value at row 3 column 2 of the matrix.</span></span> |
| `float m33` | <span data-ttu-id="cbc4b-193">Valore alla riga 3 colonna 3 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-193">Value at row 3 column 3 of the matrix.</span></span> |
| `float m34` | <span data-ttu-id="cbc4b-194">Valore alla riga 3 colonna 4 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-194">Value at row 3 column 4 of the matrix.</span></span> |
| `float m41` | <span data-ttu-id="cbc4b-195">Valore alla riga 4 della colonna 1 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-195">Value at row 4 column 1 of the matrix.</span></span> |
| `float m42` | <span data-ttu-id="cbc4b-196">Valore alla riga 4 della colonna 2 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-196">Value at row 4 column 2 of the matrix.</span></span> |
| `float m43` | <span data-ttu-id="cbc4b-197">Valore alla riga 4 colonna 3 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-197">Value at row 4 column 3 of the matrix.</span></span> |
| `float m44` | <span data-ttu-id="cbc4b-198">Valore alla riga 4 della colonna 4 della matrice.</span><span class="sxs-lookup"><span data-stu-id="cbc4b-198">Value at row 4 column 4 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="cbc4b-199">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbc4b-199">Requirements</span></span>

| <span data-ttu-id="cbc4b-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc4b-200">Requirement</span></span> | <span data-ttu-id="cbc4b-201">Valore</span><span class="sxs-lookup"><span data-stu-id="cbc4b-201">Value</span></span> |
|-|-|
| <span data-ttu-id="cbc4b-202">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cbc4b-202">Namespace</span></span> | <span data-ttu-id="cbc4b-203">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="cbc4b-203">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="cbc4b-204">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbc4b-204">Header</span></span> | <dl> <span data-ttu-id="cbc4b-205"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc4b-205"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="cbc4b-206">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbc4b-206">See also</span></span>

[<span data-ttu-id="cbc4b-207">API windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="cbc4b-207">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
