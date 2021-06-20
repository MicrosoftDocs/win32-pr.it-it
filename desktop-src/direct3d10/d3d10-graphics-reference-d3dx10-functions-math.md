---
description: Informazioni sulla libreria matematica fornita dalla libreria di utilità D3DX in Direct3D 10 Graphics. La libreria fornisce funzioni per calcolare operazioni matematiche 3D.
ms.assetid: 6e180c12-8cbe-4013-8bb4-3ac5bb9c65f1
title: Funzioni matematiche (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b47aec382f8b21d8769722afab51cb69a7452e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408044"
---
# <a name="math-functions-direct3d-10-graphics"></a><span data-ttu-id="3b190-104">Funzioni matematiche (grafica Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3b190-104">Math Functions (Direct3D 10 Graphics)</span></span>

> [!Note]  
> <span data-ttu-id="3b190-105">Le funzioni matematiche della libreria di utilità D3DX sono deprecate per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3b190-105">The math functions of the D3DX utility library are deprecated for Windows 8.</span></span> <span data-ttu-id="3b190-106">In alternativa, è [consigliabile usare DirectXMath.](../dxmath/directxmath-portal.md)</span><span class="sxs-lookup"><span data-stu-id="3b190-106">We recommend that you use [DirectXMath](../dxmath/directxmath-portal.md) instead.</span></span>

 

<span data-ttu-id="3b190-107">La libreria matematica fornita dalla libreria di utilità D3DX fornisce funzioni per calcolare operazioni matematiche 3D.</span><span class="sxs-lookup"><span data-stu-id="3b190-107">The math library provided by the D3DX utility library supplies functions to compute 3D mathematical operations.</span></span> <span data-ttu-id="3b190-108">Ognuna delle funzioni può assumere lo stesso oggetto dei parametri passati \[ e \] \[ \] restituiti.</span><span class="sxs-lookup"><span data-stu-id="3b190-108">Each of the functions can take the same object as the passed \[in\] and returned \[out\] parameters.</span></span> <span data-ttu-id="3b190-109">Inoltre, i parametri out vengono in genere restituiti come valori restituiti, in modo che l'output di una funzione matematica possa essere usato come parametro per un'altra funzione matematica.</span><span class="sxs-lookup"><span data-stu-id="3b190-109">Also, out parameters are typically returned as return values, so that the output of one math function can be used as a parameter for another math function.</span></span>

-   [<span data-ttu-id="3b190-110">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="3b190-110">**D3DXColorAdjustContrast**</span></span>](d3d10-d3dxcoloradjustcontrast.md)
-   [<span data-ttu-id="3b190-111">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="3b190-111">**D3DXColorAdjustSaturation**</span></span>](d3d10-d3dxcoloradjustsaturation.md)
-   [<span data-ttu-id="3b190-112">**D3DXCreateMatrixStack**</span><span class="sxs-lookup"><span data-stu-id="3b190-112">**D3DXCreateMatrixStack**</span></span>](d3d10-d3dxcreatematrixstack.md)
-   [<span data-ttu-id="3b190-113">**D3DXCpuOptimizations**</span><span class="sxs-lookup"><span data-stu-id="3b190-113">**D3DXCpuOptimizations**</span></span>](d3d10-d3dxcpuoptimizations.md)
-   [<span data-ttu-id="3b190-114">**D3DXFloat16To32Array**</span><span class="sxs-lookup"><span data-stu-id="3b190-114">**D3DXFloat16To32Array**</span></span>](d3d10-d3dxfloat16to32array.md)
-   [<span data-ttu-id="3b190-115">**D3DXFloat32To16Array**</span><span class="sxs-lookup"><span data-stu-id="3b190-115">**D3DXFloat32To16Array**</span></span>](d3d10-d3dxfloat32to16array.md)
-   [<span data-ttu-id="3b190-116">**D3DXFresnelTerm**</span><span class="sxs-lookup"><span data-stu-id="3b190-116">**D3DXFresnelTerm**</span></span>](d3d10-d3dxfresnelterm.md)
-   [<span data-ttu-id="3b190-117">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="3b190-117">**D3DXMatrixAffineTransformation**</span></span>](d3d10-d3dxmatrixaffinetransformation.md)
-   [<span data-ttu-id="3b190-118">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="3b190-118">**D3DXMatrixAffineTransformation2D**</span></span>](d3d10-d3dxmatrixaffinetransformation2d.md)
-   [<span data-ttu-id="3b190-119">**D3DXMatrixDecompose**</span><span class="sxs-lookup"><span data-stu-id="3b190-119">**D3DXMatrixDecompose**</span></span>](d3d10-d3dxmatrixdecompose.md)
-   [<span data-ttu-id="3b190-120">**D3DXMatrixDeterminant**</span><span class="sxs-lookup"><span data-stu-id="3b190-120">**D3DXMatrixDeterminant**</span></span>](d3d10-d3dxmatrixdeterminant.md)
-   [<span data-ttu-id="3b190-121">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="3b190-121">**D3DXMatrixInverse**</span></span>](d3d10-d3dxmatrixinverse.md)
-   [<span data-ttu-id="3b190-122">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="3b190-122">**D3DXMatrixLookAtLH**</span></span>](d3d10-d3dxmatrixlookatlh.md)
-   [<span data-ttu-id="3b190-123">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="3b190-123">**D3DXMatrixLookAtRH**</span></span>](d3d10-d3dxmatrixlookatrh.md)
-   [<span data-ttu-id="3b190-124">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="3b190-124">**D3DXMatrixMultiply**</span></span>](d3d10-d3dxmatrixmultiply.md)
-   [<span data-ttu-id="3b190-125">**D3DXMatrixMultiplyTranspose**</span><span class="sxs-lookup"><span data-stu-id="3b190-125">**D3DXMatrixMultiplyTranspose**</span></span>](d3d10-d3dxmatrixmultiplytranspose.md)
-   [<span data-ttu-id="3b190-126">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="3b190-126">**D3DXMatrixOrthoLH**</span></span>](d3d10-d3dxmatrixortholh.md)
-   [<span data-ttu-id="3b190-127">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="3b190-127">**D3DXMatrixOrthoRH**</span></span>](d3d10-d3dxmatrixorthorh.md)
-   [<span data-ttu-id="3b190-128">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="3b190-128">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3d10-d3dxmatrixorthooffcenterlh.md)
-   [<span data-ttu-id="3b190-129">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="3b190-129">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3d10-d3dxmatrixorthooffcenterrh.md)
-   [<span data-ttu-id="3b190-130">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="3b190-130">**D3DXMatrixPerspectiveFovLH**</span></span>](d3d10-d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="3b190-131">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="3b190-131">**D3DXMatrixPerspectiveFovRH**</span></span>](d3d10-d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="3b190-132">**D3DXMatrixReflect**</span><span class="sxs-lookup"><span data-stu-id="3b190-132">**D3DXMatrixReflect**</span></span>](d3d10-d3dxmatrixreflect.md)
-   [<span data-ttu-id="3b190-133">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="3b190-133">**D3DXMatrixRotationAxis**</span></span>](d3d10-d3dxmatrixrotationaxis.md)
-   [<span data-ttu-id="3b190-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="3b190-134">**D3DXMatrixRotationX**</span></span>](d3d10-d3dxmatrixrotationx.md)
-   [<span data-ttu-id="3b190-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="3b190-135">**D3DXMatrixRotationY**</span></span>](d3d10-d3dxmatrixrotationy.md)
-   [<span data-ttu-id="3b190-136">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="3b190-136">**D3DXMatrixRotationZ**</span></span>](d3d10-d3dxmatrixrotationz.md)
-   [<span data-ttu-id="3b190-137">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="3b190-137">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3d10-d3dxmatrixrotationyawpitchroll.md)
-   [<span data-ttu-id="3b190-138">**D3DXMatrixScaling**</span><span class="sxs-lookup"><span data-stu-id="3b190-138">**D3DXMatrixScaling**</span></span>](d3d10-d3dxmatrixscaling.md)
-   [<span data-ttu-id="3b190-139">**D3DXMatrixShadow**</span><span class="sxs-lookup"><span data-stu-id="3b190-139">**D3DXMatrixShadow**</span></span>](d3d10-d3dxmatrixshadow.md)
-   [<span data-ttu-id="3b190-140">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="3b190-140">**D3DXMatrixTransformation**</span></span>](d3d10-d3dxmatrixtransformation.md)
-   [<span data-ttu-id="3b190-141">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="3b190-141">**D3DXMatrixTransformation2D**</span></span>](d3d10-d3dxmatrixtransformation2d.md)
-   [<span data-ttu-id="3b190-142">**D3DXMatrixTranslation**</span><span class="sxs-lookup"><span data-stu-id="3b190-142">**D3DXMatrixTranslation**</span></span>](d3d10-d3dxmatrixtranslation.md)
-   [<span data-ttu-id="3b190-143">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="3b190-143">**D3DXMatrixTranspose**</span></span>](d3d10-d3dxmatrixtranspose.md)
-   [<span data-ttu-id="3b190-144">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="3b190-144">**D3DXPlaneFromPointNormal**</span></span>](d3d10-d3dxplanefrompointnormal.md)
-   [<span data-ttu-id="3b190-145">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="3b190-145">**D3DXPlaneFromPoints**</span></span>](d3d10-d3dxplanefrompoints.md)
-   [<span data-ttu-id="3b190-146">**D3DXPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="3b190-146">**D3DXPlaneIntersectLine**</span></span>](d3d10-d3dxplaneintersectline.md)
-   [<span data-ttu-id="3b190-147">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="3b190-147">**D3DXPlaneNormalize**</span></span>](d3d10-d3dxplanenormalize.md)
-   [<span data-ttu-id="3b190-148">**D3DXPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="3b190-148">**D3DXPlaneTransform**</span></span>](d3d10-d3dxplanetransform.md)
-   [<span data-ttu-id="3b190-149">**D3DXPlaneTransformArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-149">**D3DXPlaneTransformArray**</span></span>](d3d10-d3dxplanetransformarray.md)
-   [<span data-ttu-id="3b190-150">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="3b190-150">**D3DXQuaternionBaryCentric**</span></span>](d3d10-d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="3b190-151">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="3b190-151">**D3DXQuaternionExp**</span></span>](d3d10-d3dxquaternionexp.md)
-   [<span data-ttu-id="3b190-152">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="3b190-152">**D3DXQuaternionInverse**</span></span>](d3d10-d3dxquaternioninverse.md)
-   [<span data-ttu-id="3b190-153">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="3b190-153">**D3DXQuaternionLn**</span></span>](d3d10-d3dxquaternionln.md)
-   [<span data-ttu-id="3b190-154">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="3b190-154">**D3DXQuaternionMultiply**</span></span>](d3d10-d3dxquaternionmultiply.md)
-   [<span data-ttu-id="3b190-155">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="3b190-155">**D3DXQuaternionNormalize**</span></span>](d3d10-d3dxquaternionnormalize.md)
-   [<span data-ttu-id="3b190-156">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="3b190-156">**D3DXQuaternionRotationAxis**</span></span>](d3d10-d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="3b190-157">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="3b190-157">**D3DXQuaternionRotationMatrix**</span></span>](d3d10-d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="3b190-158">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="3b190-158">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3d10-d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="3b190-159">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="3b190-159">**D3DXQuaternionSlerp**</span></span>](d3d10-d3dxquaternionslerp.md)
-   [<span data-ttu-id="3b190-160">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="3b190-160">**D3DXQuaternionSquad**</span></span>](d3d10-d3dxquaternionsquad.md)
-   [<span data-ttu-id="3b190-161">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="3b190-161">**D3DXQuaternionSquadSetup**</span></span>](d3d10-d3dxquaternionsquadsetup.md)
-   [<span data-ttu-id="3b190-162">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="3b190-162">**D3DXQuaternionToAxisAngle**</span></span>](d3d10-d3dxquaterniontoaxisangle.md)
-   [<span data-ttu-id="3b190-163">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="3b190-163">**D3DXSHEvalConeLight**</span></span>](d3d10-d3dxshevalconelight.md)
-   [<span data-ttu-id="3b190-164">**D3DXSHEvalDirection**</span><span class="sxs-lookup"><span data-stu-id="3b190-164">**D3DXSHEvalDirection**</span></span>](d3d10-d3dxshevaldirection.md)
-   [<span data-ttu-id="3b190-165">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="3b190-165">**D3DXSHEvalDirectionalLight**</span></span>](d3d10-d3dxshevaldirectionallight.md)
-   [<span data-ttu-id="3b190-166">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="3b190-166">**D3DXSHEvalHemisphereLight**</span></span>](d3d10-d3dxshevalhemispherelight.md)
-   [<span data-ttu-id="3b190-167">**D3DXSHMultiply2**</span><span class="sxs-lookup"><span data-stu-id="3b190-167">**D3DXSHMultiply2**</span></span>](d3d10-d3dxshmultiply2.md)
-   [<span data-ttu-id="3b190-168">**D3DXSHMultiply3**</span><span class="sxs-lookup"><span data-stu-id="3b190-168">**D3DXSHMultiply3**</span></span>](d3d10-d3dxshmultiply3.md)
-   [<span data-ttu-id="3b190-169">**D3DXSHMultiply4**</span><span class="sxs-lookup"><span data-stu-id="3b190-169">**D3DXSHMultiply4**</span></span>](d3d10-d3dxshmultiply4.md)
-   [<span data-ttu-id="3b190-170">**D3DXSHMultiply5**</span><span class="sxs-lookup"><span data-stu-id="3b190-170">**D3DXSHMultiply5**</span></span>](d3d10-d3dxshmultiply5.md)
-   [<span data-ttu-id="3b190-171">**D3DXSHMultiply6**</span><span class="sxs-lookup"><span data-stu-id="3b190-171">**D3DXSHMultiply6**</span></span>](d3d10-d3dxshmultiply6.md)
-   [<span data-ttu-id="3b190-172">**D3DX10SHProjectCubeMap**</span><span class="sxs-lookup"><span data-stu-id="3b190-172">**D3DX10SHProjectCubeMap**</span></span>](d3dx10shprojectcubemap.md)
-   [<span data-ttu-id="3b190-173">**D3DXSHRotate**</span><span class="sxs-lookup"><span data-stu-id="3b190-173">**D3DXSHRotate**</span></span>](d3d10-d3dxshrotate.md)
-   [<span data-ttu-id="3b190-174">**D3DXSHRotatez**</span><span class="sxs-lookup"><span data-stu-id="3b190-174">**D3DXSHRotateZ**</span></span>](d3d10-d3dxshrotatez.md)
-   [<span data-ttu-id="3b190-175">**D3DXSHScale**</span><span class="sxs-lookup"><span data-stu-id="3b190-175">**D3DXSHScale**</span></span>](d3d10-d3dxshscale.md)
-   [<span data-ttu-id="3b190-176">**D3DXVec2BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="3b190-176">**D3DXVec2BaryCentric**</span></span>](d3d10-d3dxvec2barycentric.md)
-   [<span data-ttu-id="3b190-177">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="3b190-177">**D3DXVec2CatmullRom**</span></span>](d3d10-d3dxvec2catmullrom.md)
-   [<span data-ttu-id="3b190-178">**D3DXVec2Hermite**</span><span class="sxs-lookup"><span data-stu-id="3b190-178">**D3DXVec2Hermite**</span></span>](d3d10-d3dxvec2hermite.md)
-   [<span data-ttu-id="3b190-179">**D3DXVec2Normalize**</span><span class="sxs-lookup"><span data-stu-id="3b190-179">**D3DXVec2Normalize**</span></span>](d3d10-d3dxvec2normalize.md)
-   [<span data-ttu-id="3b190-180">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="3b190-180">**D3DXVec2Transform**</span></span>](d3d10-d3dxvec2transform.md)
-   [<span data-ttu-id="3b190-181">**D3DXVec2TransformArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-181">**D3DXVec2TransformArray**</span></span>](d3d10-d3dxvec2transformarray.md)
-   [<span data-ttu-id="3b190-182">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="3b190-182">**D3DXVec2TransformCoord**</span></span>](d3d10-d3dxvec2transformcoord.md)
-   [<span data-ttu-id="3b190-183">**D3DXVec2TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-183">**D3DXVec2TransformCoordArray**</span></span>](d3d10-d3dxvec2transformcoordarray.md)
-   [<span data-ttu-id="3b190-184">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="3b190-184">**D3DXVec2TransformNormal**</span></span>](d3d10-d3dxvec2transformnormal.md)
-   [<span data-ttu-id="3b190-185">**D3DXVec2TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-185">**D3DXVec2TransformNormalArray**</span></span>](d3d10-d3dxvec2transformnormalarray.md)
-   [<span data-ttu-id="3b190-186">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="3b190-186">**D3DXVec3BaryCentric**</span></span>](d3d10-d3dxvec3barycentric.md)
-   [<span data-ttu-id="3b190-187">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="3b190-187">**D3DXVec3CatmullRom**</span></span>](d3d10-d3dxvec3catmullrom.md)
-   [<span data-ttu-id="3b190-188">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="3b190-188">**D3DXVec3Hermite**</span></span>](d3d10-d3dxvec3hermite.md)
-   [<span data-ttu-id="3b190-189">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="3b190-189">**D3DXVec3Normalize**</span></span>](d3d10-d3dxvec3normalize.md)
-   [<span data-ttu-id="3b190-190">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="3b190-190">**D3DXVec3Project**</span></span>](d3d10-d3dxvec3project.md)
-   [<span data-ttu-id="3b190-191">**D3DXVec3ProjectArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-191">**D3DXVec3ProjectArray**</span></span>](d3d10-d3dxvec3projectarray.md)
-   [<span data-ttu-id="3b190-192">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="3b190-192">**D3DXVec3Transform**</span></span>](d3d10-d3dxvec3transform.md)
-   [<span data-ttu-id="3b190-193">**D3DXVec3TransformArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-193">**D3DXVec3TransformArray**</span></span>](d3d10-d3dxvec3transformarray.md)
-   [<span data-ttu-id="3b190-194">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="3b190-194">**D3DXVec3TransformCoord**</span></span>](d3d10-d3dxvec3transformcoord.md)
-   [<span data-ttu-id="3b190-195">**D3DXVec3TransformCoordArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-195">**D3DXVec3TransformCoordArray**</span></span>](d3d10-d3dxvec3transformcoordarray.md)
-   [<span data-ttu-id="3b190-196">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="3b190-196">**D3DXVec3TransformNormal**</span></span>](d3d10-d3dxvec3transformnormal.md)
-   [<span data-ttu-id="3b190-197">**D3DXVec3TransformNormalArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-197">**D3DXVec3TransformNormalArray**</span></span>](d3d10-d3dxvec3transformnormalarray.md)
-   [<span data-ttu-id="3b190-198">**D3DXVec4BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="3b190-198">**D3DXVec4BaryCentric**</span></span>](d3d10-d3dxvec4barycentric.md)
-   [<span data-ttu-id="3b190-199">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="3b190-199">**D3DXVec4CatmullRom**</span></span>](d3d10-d3dxvec4catmullrom.md)
-   [<span data-ttu-id="3b190-200">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="3b190-200">**D3DXVec4Cross**</span></span>](d3d10-d3dxvec4cross.md)
-   [<span data-ttu-id="3b190-201">**D3DXVec4Hermite**</span><span class="sxs-lookup"><span data-stu-id="3b190-201">**D3DXVec4Hermite**</span></span>](d3d10-d3dxvec4hermite.md)
-   [<span data-ttu-id="3b190-202">**D3DXVec4Normalize**</span><span class="sxs-lookup"><span data-stu-id="3b190-202">**D3DXVec4Normalize**</span></span>](d3d10-d3dxvec4normalize.md)
-   [<span data-ttu-id="3b190-203">**D3DXVec4Transform**</span><span class="sxs-lookup"><span data-stu-id="3b190-203">**D3DXVec4Transform**</span></span>](d3d10-d3dxvec4transform.md)
-   [<span data-ttu-id="3b190-204">**D3DXVec4TransformArray**</span><span class="sxs-lookup"><span data-stu-id="3b190-204">**D3DXVec4TransformArray**</span></span>](d3d10-d3dxvec4transformarray.md)

## <a name="resolving-link-errors-with-d3dx-math-functions"></a><span data-ttu-id="3b190-205">Risoluzione degli errori di collegamento con le funzioni matematiche D3DX</span><span class="sxs-lookup"><span data-stu-id="3b190-205">Resolving Link Errors with D3DX Math Functions</span></span>

<span data-ttu-id="3b190-206">Le funzioni matematiche D3DX vengono implementate in modo identico in D3DX10 (D3DX10math.h) e D3DX9 (D3DX9math.h).</span><span class="sxs-lookup"><span data-stu-id="3b190-206">The D3DX math functions are implemented identically in D3DX10 (D3DX10math.h) and D3DX9 (D3DX9math.h).</span></span> <span data-ttu-id="3b190-207">Ciò può causare errori di collegamento se un progetto implementa sia codice DirectX 9 che DirectX 10 e tenta di collegare una funzione da un'intestazione alla libreria opposta.</span><span class="sxs-lookup"><span data-stu-id="3b190-207">This can cause link errors if a project implements both DirectX 9 and DirectX 10 code, and attempts to link a function from one header with the opposite library.</span></span>

<span data-ttu-id="3b190-208">Per eliminare il problema dell'inclusione di entrambe le intestazioni, D3DX10math.h include la definizione \# seguente:</span><span class="sxs-lookup"><span data-stu-id="3b190-208">To eliminate the problem of including both headers, D3DX10math.h includes the following \#define:</span></span>


```
#ifndef __D3DX9MATH_H__
#define __D3DX9MATH_H__
```



<span data-ttu-id="3b190-209">Per eliminare possibili errori di collegamento, gli esempi di DX SDK si collegano prima alle librerie D3DX9 (D3DX9d.lib e D3DX9.lib) e quindi alle librerie D3DX10 (D3DX10d.lib e D3DX10.lib).</span><span class="sxs-lookup"><span data-stu-id="3b190-209">To eliminate possible link errors, the DX SDK samples link to D3DX9 libraries first (D3DX9d.lib and D3DX9.lib) and then the D3DX10 libraries second (D3DX10d.lib and D3DX10.lib).</span></span> <span data-ttu-id="3b190-210">Queste impostazioni sono disponibili in Progetto/Proprietà se si usa Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3b190-210">These settings are under Project/Properties if you are using Visual Studio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b190-211">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b190-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b190-212">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="3b190-212">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
