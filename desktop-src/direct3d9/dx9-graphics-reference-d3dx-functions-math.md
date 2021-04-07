---
description: La libreria Math fornita dalla libreria di utilità D3DX fornisce funzioni per calcolare le operazioni matematiche 3D.
ms.assetid: 00f0f943-64fa-45e3-8bd3-ca61c8b87e1a
title: Funzioni matematiche (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069b0de6a40806a4461fa68ba00e456b1d3b9dfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746551"
---
# <a name="math-functions-direct3d-9-graphics"></a><span data-ttu-id="aef75-103">Funzioni matematiche (grafica Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aef75-103">Math Functions (Direct3D 9 Graphics)</span></span>

> [!Note]  
> <span data-ttu-id="aef75-104">Le funzioni matematiche della libreria di utilità D3DX sono deprecate per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aef75-104">The math functions of the D3DX utility library are deprecated for Windows 8.</span></span> <span data-ttu-id="aef75-105">È invece consigliabile usare [DirectXMath](../dxmath/directxmath-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="aef75-105">We recommend that you use [DirectXMath](../dxmath/directxmath-portal.md) instead.</span></span>

 

<span data-ttu-id="aef75-106">La libreria Math fornita dalla libreria di utilità D3DX fornisce funzioni per calcolare le operazioni matematiche 3D.</span><span class="sxs-lookup"><span data-stu-id="aef75-106">The math library provided by the D3DX utility library supplies functions to compute 3D mathematical operations.</span></span> <span data-ttu-id="aef75-107">Ognuna delle funzioni può assumere lo stesso oggetto del passato \[ \] e restituire i \[ \] parametri.</span><span class="sxs-lookup"><span data-stu-id="aef75-107">Each of the functions can take the same object as the passed \[in\] and returned \[out\] parameters.</span></span> <span data-ttu-id="aef75-108">Inoltre, i parametri out vengono in genere restituiti come valori restituiti, in modo che l'output di una funzione matematica possa essere utilizzato come parametro per un'altra funzione matematica.</span><span class="sxs-lookup"><span data-stu-id="aef75-108">Also, out parameters are typically returned as return values, so that the output of one math function can be used as a parameter for another math function.</span></span>

<span data-ttu-id="aef75-109">Molte delle funzioni sono implementate in d3dx9math. inl.</span><span class="sxs-lookup"><span data-stu-id="aef75-109">Many of the functions are implemented in d3dx9math.inl.</span></span>

<span data-ttu-id="aef75-110">Le funzioni dell'applicazione Math 3D possono essere organizzate nei gruppi seguenti.</span><span class="sxs-lookup"><span data-stu-id="aef75-110">The 3D math application functions can be organized into the following groups.</span></span>

## <a name="functions"></a><span data-ttu-id="aef75-111">Funzioni</span><span class="sxs-lookup"><span data-stu-id="aef75-111">Functions</span></span>

-   [<span data-ttu-id="aef75-112">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="aef75-112">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
-   [<span data-ttu-id="aef75-113">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="aef75-113">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
-   [<span data-ttu-id="aef75-114">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="aef75-114">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
-   [<span data-ttu-id="aef75-115">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="aef75-115">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
-   [<span data-ttu-id="aef75-116">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="aef75-116">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
-   [<span data-ttu-id="aef75-117">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="aef75-117">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
-   [<span data-ttu-id="aef75-118">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="aef75-118">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
-   [<span data-ttu-id="aef75-119">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="aef75-119">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
-   [<span data-ttu-id="aef75-120">**D3DXCreateMatrixStack**</span><span class="sxs-lookup"><span data-stu-id="aef75-120">**D3DXCreateMatrixStack**</span></span>](d3dxcreatematrixstack.md)
-   [<span data-ttu-id="aef75-121">**D3DXFloat16To32Array**</span><span class="sxs-lookup"><span data-stu-id="aef75-121">**D3DXFloat16To32Array**</span></span>](d3dxfloat16to32array.md)
-   [<span data-ttu-id="aef75-122">**D3DXFloat32To16Array**</span><span class="sxs-lookup"><span data-stu-id="aef75-122">**D3DXFloat32To16Array**</span></span>](d3dxfloat32to16array.md)
-   [<span data-ttu-id="aef75-123">**D3DXFresnelTerm**</span><span class="sxs-lookup"><span data-stu-id="aef75-123">**D3DXFresnelTerm**</span></span>](d3dxfresnelterm.md)
-   [<span data-ttu-id="aef75-124">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="aef75-124">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
-   [<span data-ttu-id="aef75-125">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="aef75-125">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
-   [<span data-ttu-id="aef75-126">**D3DXMatrixDecompose**</span><span class="sxs-lookup"><span data-stu-id="aef75-126">**D3DXMatrixDecompose**</span></span>](d3dxmatrixdecompose.md)
-   [<span data-ttu-id="aef75-127">**D3DXMatrixDeterminant**</span><span class="sxs-lookup"><span data-stu-id="aef75-127">**D3DXMatrixDeterminant**</span></span>](d3dxmatrixdeterminant.md)
-   [<span data-ttu-id="aef75-128">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="aef75-128">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
-   [<span data-ttu-id="aef75-129">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="aef75-129">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
-   [<span data-ttu-id="aef75-130">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="aef75-130">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
-   [<span data-ttu-id="aef75-131">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="aef75-131">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
-   [<span data-ttu-id="aef75-132">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="aef75-132">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
-   [<span data-ttu-id="aef75-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="aef75-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
-   [<span data-ttu-id="aef75-134">**D3DXMatrixMultiplyTranspose**</span><span class="sxs-lookup"><span data-stu-id="aef75-134">**D3DXMatrixMultiplyTranspose**</span></span>](d3dxmatrixmultiplytranspose.md)
-   [<span data-ttu-id="aef75-135">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="aef75-135">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
-   [<span data-ttu-id="aef75-136">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="aef75-136">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
-   [<span data-ttu-id="aef75-137">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="aef75-137">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
-   [<span data-ttu-id="aef75-138">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="aef75-138">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
-   [<span data-ttu-id="aef75-139">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="aef75-139">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="aef75-140">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="aef75-140">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="aef75-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="aef75-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="aef75-142">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="aef75-142">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="aef75-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="aef75-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
-   [<span data-ttu-id="aef75-144">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="aef75-144">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="aef75-145">**D3DXMatrixReflect**</span><span class="sxs-lookup"><span data-stu-id="aef75-145">**D3DXMatrixReflect**</span></span>](d3dxmatrixreflect.md)
-   [<span data-ttu-id="aef75-146">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="aef75-146">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
-   [<span data-ttu-id="aef75-147">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="aef75-147">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
-   [<span data-ttu-id="aef75-148">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="aef75-148">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
-   [<span data-ttu-id="aef75-149">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="aef75-149">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
-   [<span data-ttu-id="aef75-150">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="aef75-150">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
-   [<span data-ttu-id="aef75-151">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="aef75-151">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
-   [<span data-ttu-id="aef75-152">**D3DXMatrixScaling**</span><span class="sxs-lookup"><span data-stu-id="aef75-152">**D3DXMatrixScaling**</span></span>](d3dxmatrixscaling.md)
-   [<span data-ttu-id="aef75-153">**D3DXMatrixShadow**</span><span class="sxs-lookup"><span data-stu-id="aef75-153">**D3DXMatrixShadow**</span></span>](d3dxmatrixshadow.md)
-   [<span data-ttu-id="aef75-154">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="aef75-154">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
-   [<span data-ttu-id="aef75-155">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="aef75-155">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
-   [<span data-ttu-id="aef75-156">**D3DXMatrixTranslation**</span><span class="sxs-lookup"><span data-stu-id="aef75-156">**D3DXMatrixTranslation**</span></span>](d3dxmatrixtranslation.md)
-   [<span data-ttu-id="aef75-157">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="aef75-157">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
-   [<span data-ttu-id="aef75-158">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="aef75-158">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
-   [<span data-ttu-id="aef75-159">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="aef75-159">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
-   [<span data-ttu-id="aef75-160">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="aef75-160">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
-   [<span data-ttu-id="aef75-161">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="aef75-161">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
-   [<span data-ttu-id="aef75-162">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="aef75-162">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
-   [<span data-ttu-id="aef75-163">**D3DXPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="aef75-163">**D3DXPlaneIntersectLine**</span></span>](d3dxplaneintersectline.md)
-   [<span data-ttu-id="aef75-164">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="aef75-164">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
-   [<span data-ttu-id="aef75-165">**D3DXPlaneScale**</span><span class="sxs-lookup"><span data-stu-id="aef75-165">**D3DXPlaneScale**</span></span>](d3dxplanescale.md)
-   [<span data-ttu-id="aef75-166">**D3DXPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="aef75-166">**D3DXPlaneTransform**</span></span>](d3dxplanetransform.md)
-   [<span data-ttu-id="aef75-167">**D3DXPlaneTransformArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-167">**D3DXPlaneTransformArray**</span></span>](d3dxplanetransformarray.md)
-   [<span data-ttu-id="aef75-168">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="aef75-168">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="aef75-169">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="aef75-169">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="aef75-170">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="aef75-170">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="aef75-171">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="aef75-171">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="aef75-172">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="aef75-172">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="aef75-173">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="aef75-173">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="aef75-174">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="aef75-174">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="aef75-175">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="aef75-175">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="aef75-176">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="aef75-176">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="aef75-177">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="aef75-177">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="aef75-178">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="aef75-178">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="aef75-179">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="aef75-179">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="aef75-180">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="aef75-180">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="aef75-181">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="aef75-181">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="aef75-182">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="aef75-182">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="aef75-183">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="aef75-183">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="aef75-184">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="aef75-184">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="aef75-185">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="aef75-185">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
-   [<span data-ttu-id="aef75-186">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="aef75-186">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)
-   [<span data-ttu-id="aef75-187">**D3DXSHAdd**</span><span class="sxs-lookup"><span data-stu-id="aef75-187">**D3DXSHAdd**</span></span>](d3dxshadd.md)
-   [<span data-ttu-id="aef75-188">**D3DXSHDot**</span><span class="sxs-lookup"><span data-stu-id="aef75-188">**D3DXSHDot**</span></span>](d3dxshdot.md)
-   [<span data-ttu-id="aef75-189">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="aef75-189">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)
-   [<span data-ttu-id="aef75-190">**D3DXSHEvalDirection**</span><span class="sxs-lookup"><span data-stu-id="aef75-190">**D3DXSHEvalDirection**</span></span>](d3dxshevaldirection.md)
-   [<span data-ttu-id="aef75-191">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="aef75-191">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md)
-   [<span data-ttu-id="aef75-192">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="aef75-192">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)
-   [<span data-ttu-id="aef75-193">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="aef75-193">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)
-   [<span data-ttu-id="aef75-194">**D3DXSHProjectCubeMap**</span><span class="sxs-lookup"><span data-stu-id="aef75-194">**D3DXSHProjectCubeMap**</span></span>](d3dxshprojectcubemap.md)
-   [<span data-ttu-id="aef75-195">**D3DXSHRotate**</span><span class="sxs-lookup"><span data-stu-id="aef75-195">**D3DXSHRotate**</span></span>](d3dxshrotate.md)
-   [<span data-ttu-id="aef75-196">**D3DXSHRotateZ**</span><span class="sxs-lookup"><span data-stu-id="aef75-196">**D3DXSHRotateZ**</span></span>](d3dxshrotatez.md)
-   [<span data-ttu-id="aef75-197">**D3DXSHScale**</span><span class="sxs-lookup"><span data-stu-id="aef75-197">**D3DXSHScale**</span></span>](d3dxshscale.md)
-   [<span data-ttu-id="aef75-198">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="aef75-198">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
-   [<span data-ttu-id="aef75-199">**D3DXVec2BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="aef75-199">**D3DXVec2BaryCentric**</span></span>](d3dxvec2barycentric.md)
-   [<span data-ttu-id="aef75-200">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="aef75-200">**D3DXVec2CatmullRom**</span></span>](d3dxvec2catmullrom.md)
-   [<span data-ttu-id="aef75-201">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="aef75-201">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
-   [<span data-ttu-id="aef75-202">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="aef75-202">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
-   [<span data-ttu-id="aef75-203">**D3DXVec2Hermite**</span><span class="sxs-lookup"><span data-stu-id="aef75-203">**D3DXVec2Hermite**</span></span>](d3dxvec2hermite.md)
-   [<span data-ttu-id="aef75-204">**D3DXVec2Length**</span><span class="sxs-lookup"><span data-stu-id="aef75-204">**D3DXVec2Length**</span></span>](d3dxvec2length.md)
-   [<span data-ttu-id="aef75-205">**D3DXVec2LengthSq**</span><span class="sxs-lookup"><span data-stu-id="aef75-205">**D3DXVec2LengthSq**</span></span>](d3dxvec2lengthsq.md)
-   [<span data-ttu-id="aef75-206">**D3DXVec2Lerp**</span><span class="sxs-lookup"><span data-stu-id="aef75-206">**D3DXVec2Lerp**</span></span>](d3dxvec2lerp.md)
-   [<span data-ttu-id="aef75-207">**D3DXVec2Maximize**</span><span class="sxs-lookup"><span data-stu-id="aef75-207">**D3DXVec2Maximize**</span></span>](d3dxvec2maximize.md)
-   [<span data-ttu-id="aef75-208">**D3DXVec2Minimize**</span><span class="sxs-lookup"><span data-stu-id="aef75-208">**D3DXVec2Minimize**</span></span>](d3dxvec2minimize.md)
-   [<span data-ttu-id="aef75-209">**D3DXVec2Normalize**</span><span class="sxs-lookup"><span data-stu-id="aef75-209">**D3DXVec2Normalize**</span></span>](d3dxvec2normalize.md)
-   [<span data-ttu-id="aef75-210">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="aef75-210">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
-   [<span data-ttu-id="aef75-211">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="aef75-211">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
-   [<span data-ttu-id="aef75-212">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="aef75-212">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
-   [<span data-ttu-id="aef75-213">**D3DXVec2TransformArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-213">**D3DXVec2TransformArray**</span></span>](d3dxvec2transformarray.md)
-   [<span data-ttu-id="aef75-214">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="aef75-214">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
-   [<span data-ttu-id="aef75-215">**D3DXVec2TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-215">**D3DXVec2TransformCoordArray**</span></span>](d3dxvec2transformcoordarray.md)
-   [<span data-ttu-id="aef75-216">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="aef75-216">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
-   [<span data-ttu-id="aef75-217">**D3DXVec2TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-217">**D3DXVec2TransformNormalArray**</span></span>](d3dxvec2transformnormalarray.md)
-   [<span data-ttu-id="aef75-218">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="aef75-218">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="aef75-219">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="aef75-219">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="aef75-220">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="aef75-220">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="aef75-221">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="aef75-221">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="aef75-222">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="aef75-222">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="aef75-223">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="aef75-223">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="aef75-224">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="aef75-224">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="aef75-225">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="aef75-225">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="aef75-226">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="aef75-226">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="aef75-227">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="aef75-227">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="aef75-228">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="aef75-228">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="aef75-229">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="aef75-229">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="aef75-230">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="aef75-230">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="aef75-231">**D3DXVec3ProjectArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-231">**D3DXVec3ProjectArray**</span></span>](d3dxvec3projectarray.md)
-   [<span data-ttu-id="aef75-232">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="aef75-232">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="aef75-233">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="aef75-233">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="aef75-234">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="aef75-234">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="aef75-235">**D3DXVec3TransformArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-235">**D3DXVec3TransformArray**</span></span>](d3dxvec3transformarray.md)
-   [<span data-ttu-id="aef75-236">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="aef75-236">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="aef75-237">**D3DXVec3TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-237">**D3DXVec3TransformCoordArray**</span></span>](d3dxvec3transformcoordarray.md)
-   [<span data-ttu-id="aef75-238">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="aef75-238">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="aef75-239">**D3DXVec3TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-239">**D3DXVec3TransformNormalArray**</span></span>](d3dxvec3transformnormalarray.md)
-   [<span data-ttu-id="aef75-240">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="aef75-240">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
-   [<span data-ttu-id="aef75-241">**D3DXVec3UnprojectArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-241">**D3DXVec3UnprojectArray**</span></span>](d3dxvec3unprojectarray.md)
-   [<span data-ttu-id="aef75-242">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="aef75-242">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
-   [<span data-ttu-id="aef75-243">**D3DXVec4BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="aef75-243">**D3DXVec4BaryCentric**</span></span>](d3dxvec4barycentric.md)
-   [<span data-ttu-id="aef75-244">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="aef75-244">**D3DXVec4CatmullRom**</span></span>](d3dxvec4catmullrom.md)
-   [<span data-ttu-id="aef75-245">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="aef75-245">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
-   [<span data-ttu-id="aef75-246">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="aef75-246">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
-   [<span data-ttu-id="aef75-247">**D3DXVec4Hermite**</span><span class="sxs-lookup"><span data-stu-id="aef75-247">**D3DXVec4Hermite**</span></span>](d3dxvec4hermite.md)
-   [<span data-ttu-id="aef75-248">**D3DXVec4Length**</span><span class="sxs-lookup"><span data-stu-id="aef75-248">**D3DXVec4Length**</span></span>](d3dxvec4length.md)
-   [<span data-ttu-id="aef75-249">**D3DXVec4LengthSq**</span><span class="sxs-lookup"><span data-stu-id="aef75-249">**D3DXVec4LengthSq**</span></span>](d3dxvec4lengthsq.md)
-   [<span data-ttu-id="aef75-250">**D3DXVec4Lerp**</span><span class="sxs-lookup"><span data-stu-id="aef75-250">**D3DXVec4Lerp**</span></span>](d3dxvec4lerp.md)
-   [<span data-ttu-id="aef75-251">**D3DXVec4Maximize**</span><span class="sxs-lookup"><span data-stu-id="aef75-251">**D3DXVec4Maximize**</span></span>](d3dxvec4maximize.md)
-   [<span data-ttu-id="aef75-252">**D3DXVec4Minimize**</span><span class="sxs-lookup"><span data-stu-id="aef75-252">**D3DXVec4Minimize**</span></span>](d3dxvec4minimize.md)
-   [<span data-ttu-id="aef75-253">**D3DXVec4Normalize**</span><span class="sxs-lookup"><span data-stu-id="aef75-253">**D3DXVec4Normalize**</span></span>](d3dxvec4normalize.md)
-   [<span data-ttu-id="aef75-254">**D3DXVec4Scale**</span><span class="sxs-lookup"><span data-stu-id="aef75-254">**D3DXVec4Scale**</span></span>](d3dxvec4scale.md)
-   [<span data-ttu-id="aef75-255">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="aef75-255">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
-   [<span data-ttu-id="aef75-256">**D3DXVec4Transform**</span><span class="sxs-lookup"><span data-stu-id="aef75-256">**D3DXVec4Transform**</span></span>](d3dxvec4transform.md)
-   [<span data-ttu-id="aef75-257">**D3DXVec4TransformArray**</span><span class="sxs-lookup"><span data-stu-id="aef75-257">**D3DXVec4TransformArray**</span></span>](d3dxvec4transformarray.md)

## <a name="related-topics"></a><span data-ttu-id="aef75-258">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aef75-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aef75-259">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="aef75-259">D3DX Functions</span></span>](dx9-graphics-reference-d3dx-functions.md)
</dt> </dl>

 

 
