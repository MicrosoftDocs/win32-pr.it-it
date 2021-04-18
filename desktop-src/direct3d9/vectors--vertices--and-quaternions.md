---
description: In Direct3D, i vertici descrivono la posizione e l'orientamento. Ogni vertice in una primitiva viene descritto da un vettore che fornisce la posizione, il colore, le coordinate di trama e un vettore normale che ne dà l'orientamento.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vettori, vertici e quaternioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521162"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a><span data-ttu-id="bc36e-104">Vettori, vertici e quaternioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc36e-104">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>

<span data-ttu-id="bc36e-105">In Direct3D, i vertici descrivono la posizione e l'orientamento.</span><span class="sxs-lookup"><span data-stu-id="bc36e-105">Throughout Direct3D, vertices describe position and orientation.</span></span> <span data-ttu-id="bc36e-106">Ogni vertice in una primitiva viene descritto da un vettore che fornisce la posizione, il colore, le coordinate di trama e un vettore normale che ne dà l'orientamento.</span><span class="sxs-lookup"><span data-stu-id="bc36e-106">Each vertex in a primitive is described by a vector that gives its position, color, texture coordinates, and a normal vector that gives its orientation.</span></span>

<span data-ttu-id="bc36e-107">I quaternioni aggiungono un quarto elemento ai \[ valori x, y, z \] che definiscono un vettore a tre componenti.</span><span class="sxs-lookup"><span data-stu-id="bc36e-107">Quaternions add a fourth element to the \[x, y, z\] values that define a three-component-vector.</span></span> <span data-ttu-id="bc36e-108">I quaternioni rappresentano un'alternativa ai metodi della matrice che vengono in genere usati per le rotazioni 3D.</span><span class="sxs-lookup"><span data-stu-id="bc36e-108">Quaternions are an alternative to the matrix methods that are typically used for 3D rotations.</span></span> <span data-ttu-id="bc36e-109">Un quaternione rappresenta un asse nello spazio 3D e una rotazione intorno a tale asse.</span><span class="sxs-lookup"><span data-stu-id="bc36e-109">A quaternion represents an axis in 3D space and a rotation around that axis.</span></span> <span data-ttu-id="bc36e-110">Ad esempio, un quaternione può rappresentare un asse (1, 1, 2) e una rotazione di 1 radiante.</span><span class="sxs-lookup"><span data-stu-id="bc36e-110">For example, a quaternion might represent a (1,1,2) axis and a rotation of 1 radian.</span></span> <span data-ttu-id="bc36e-111">I quaternioni contengono informazioni importanti, ma la loro vera potenza deriva dalle due operazioni che è possibile eseguire su di essi: composizione e interpolazione.</span><span class="sxs-lookup"><span data-stu-id="bc36e-111">Quaternions carry valuable information, but their true power comes from the two operations that you can perform on them: composition and interpolation.</span></span>

<span data-ttu-id="bc36e-112">L'esecuzione della composizione nei quaternioni è simile alla combinazione di tali elementi.</span><span class="sxs-lookup"><span data-stu-id="bc36e-112">Performing composition on quaternions is similar to combining them.</span></span> <span data-ttu-id="bc36e-113">La composizione di due quaternioni è nota come la figura seguente.</span><span class="sxs-lookup"><span data-stu-id="bc36e-113">The composition of two quaternions is notated like the following illustration.</span></span>

![illustrazione della notazione Quaternion](images/quateq.png)

<span data-ttu-id="bc36e-115">La composizione di due quaternioni applicati a una geometria significa "ruotare la geometria intorno all'asse ₂ per rotazione ₂, quindi ruotarla attorno all'asse ₁ per rotazione ₁".</span><span class="sxs-lookup"><span data-stu-id="bc36e-115">The composition of two quaternions applied to a geometry means "rotate the geometry around axis₂ by rotation₂, then rotate it around axis₁ by rotation₁."</span></span> <span data-ttu-id="bc36e-116">In questo caso, Q rappresenta una rotazione intorno a un singolo asse risultante dall'applicazione di q ₂, quindi da q ₁ alla geometria.</span><span class="sxs-lookup"><span data-stu-id="bc36e-116">In this case, Q represents a rotation around a single axis that is the result of applying q₂, then q₁ to the geometry.</span></span>

<span data-ttu-id="bc36e-117">Utilizzando l'interpolazione quaternione, un'applicazione può calcolare un percorso uniforme e ragionevole da un asse e un orientamento a un altro.</span><span class="sxs-lookup"><span data-stu-id="bc36e-117">Using quaternion interpolation, an application can calculate a smooth and reasonable path from one axis and orientation to another.</span></span> <span data-ttu-id="bc36e-118">Di conseguenza, l'interpolazione tra q ₁ e q ₂ fornisce un modo semplice per animare da un orientamento a un altro.</span><span class="sxs-lookup"><span data-stu-id="bc36e-118">Therefore, interpolation between q₁ and q₂ provides a simple way to animate from one orientation to another.</span></span>

<span data-ttu-id="bc36e-119">Quando si usano insieme la composizione e l'interpolazione, fornisce un modo semplice per modificare una geometria in modo che appaia complesso.</span><span class="sxs-lookup"><span data-stu-id="bc36e-119">When you use composition and interpolation together, they provide you with a simple way to manipulate a geometry in a manner that appears complex.</span></span> <span data-ttu-id="bc36e-120">Si supponga, ad esempio, di disporre di una geometria che si desidera ruotare a un determinato orientamento.</span><span class="sxs-lookup"><span data-stu-id="bc36e-120">For example, imagine that you have a geometry that you want to rotate to a given orientation.</span></span> <span data-ttu-id="bc36e-121">Si è certi che si vuole ruotarlo r ₂ gradi intorno all'asse ₂, quindi ruotarlo r ₁ gradi intorno all'asse ₁, ma non si conosce il quaternione finale.</span><span class="sxs-lookup"><span data-stu-id="bc36e-121">You know that you want to rotate it r₂ degrees around axis₂, then rotate it r₁ degrees around axis₁, but you don't know the final quaternion.</span></span> <span data-ttu-id="bc36e-122">Usando Composition, è possibile combinare le due rotazioni sulla geometria per ottenere un singolo quaternione che è il risultato.</span><span class="sxs-lookup"><span data-stu-id="bc36e-122">By using composition, you could combine the two rotations on the geometry to get a single quaternion that is the result.</span></span> <span data-ttu-id="bc36e-123">Quindi, è possibile eseguire l'interpolazione dal quaternione originale al quaternione composto per ottenere una transizione uniforme da uno all'altro.</span><span class="sxs-lookup"><span data-stu-id="bc36e-123">Then, you could interpolate from the original to the composed quaternion to achieve a smooth transition from one to the other.</span></span>

<span data-ttu-id="bc36e-124">La libreria di utilità D3DX include funzioni che consentono di lavorare con i quaternioni.</span><span class="sxs-lookup"><span data-stu-id="bc36e-124">The D3DX utility library includes functions that help you work with quaternions.</span></span> <span data-ttu-id="bc36e-125">Ad esempio, la funzione [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) aggiunge un valore di rotazione a un vettore che definisce un asse di rotazione e restituisce il risultato in un quaternione definito da una struttura [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="bc36e-125">For example, the [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) function adds a rotation value to a vector that defines an axis of rotation, and returns the result in a quaternion defined by a [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span> <span data-ttu-id="bc36e-126">Inoltre, la funzione [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) compone i quaternioni e [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) esegue l'interpolazione lineare sferica tra due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="bc36e-126">Additionally, the [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) function composes quaternions and the [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) performs spherical linear interpolation between two quaternions.</span></span>

<span data-ttu-id="bc36e-127">Le applicazioni Direct3D possono utilizzare le funzioni seguenti per semplificare l'attività di utilizzo dei quaternioni.</span><span class="sxs-lookup"><span data-stu-id="bc36e-127">Direct3D applications can use the following functions to simplify the task of working with quaternions.</span></span>

-   [<span data-ttu-id="bc36e-128">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="bc36e-128">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="bc36e-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="bc36e-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="bc36e-130">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="bc36e-130">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="bc36e-131">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="bc36e-131">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="bc36e-132">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="bc36e-132">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="bc36e-133">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="bc36e-133">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="bc36e-134">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="bc36e-134">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="bc36e-135">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="bc36e-135">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="bc36e-136">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="bc36e-136">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="bc36e-137">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="bc36e-137">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="bc36e-138">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="bc36e-138">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="bc36e-139">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="bc36e-139">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="bc36e-140">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="bc36e-140">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="bc36e-141">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="bc36e-141">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="bc36e-142">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="bc36e-142">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="bc36e-143">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="bc36e-143">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="bc36e-144">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="bc36e-144">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="bc36e-145">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="bc36e-145">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)

<span data-ttu-id="bc36e-146">Le applicazioni Direct3D possono utilizzare le funzioni seguenti per semplificare l'attività di utilizzo di vettori a tre componenti.</span><span class="sxs-lookup"><span data-stu-id="bc36e-146">Direct3D applications can use the following functions to simplify the task of working with three-component-vectors.</span></span>

-   [<span data-ttu-id="bc36e-147">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="bc36e-147">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="bc36e-148">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="bc36e-148">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="bc36e-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="bc36e-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="bc36e-150">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="bc36e-150">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="bc36e-151">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="bc36e-151">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="bc36e-152">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="bc36e-152">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="bc36e-153">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="bc36e-153">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="bc36e-154">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="bc36e-154">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="bc36e-155">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="bc36e-155">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="bc36e-156">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="bc36e-156">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="bc36e-157">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="bc36e-157">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="bc36e-158">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="bc36e-158">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="bc36e-159">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="bc36e-159">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="bc36e-160">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="bc36e-160">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="bc36e-161">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="bc36e-161">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="bc36e-162">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="bc36e-162">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="bc36e-163">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="bc36e-163">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="bc36e-164">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="bc36e-164">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="bc36e-165">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="bc36e-165">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)

<span data-ttu-id="bc36e-166">Molte funzioni aggiuntive che semplificano le attività usando i vettori a due e quattro componenti sono incluse tra le [funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md) fornite dalla libreria di utilità D3DX.</span><span class="sxs-lookup"><span data-stu-id="bc36e-166">Many additional functions that simplify tasks using two- and four-component-vectors are included among the [Math Functions](dx9-graphics-reference-d3dx-functions-math.md) supplied by the D3DX utility library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc36e-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc36e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc36e-168">Sistemi di coordinate e geometria</span><span class="sxs-lookup"><span data-stu-id="bc36e-168">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



