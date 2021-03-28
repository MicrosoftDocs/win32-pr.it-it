---
title: rifrangono
description: Restituisce un vettore di rifrazione usando un raggio di immissione, una normale della superficie e un indice di rifrazione.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- HLSL di rifrazione
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993568"
---
# <a name="refract"></a><span data-ttu-id="3e15e-104">rifrangono</span><span class="sxs-lookup"><span data-stu-id="3e15e-104">refract</span></span>

<span data-ttu-id="3e15e-105">Restituisce un vettore di rifrazione usando un raggio di immissione, una normale della superficie e un indice di rifrazione.</span><span class="sxs-lookup"><span data-stu-id="3e15e-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="3e15e-106">rifrazione *ret* (*i*, *n*,?)</span><span class="sxs-lookup"><span data-stu-id="3e15e-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3e15e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e15e-107">Parameters</span></span>



| <span data-ttu-id="3e15e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3e15e-108">Item</span></span>                                                   | <span data-ttu-id="3e15e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e15e-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="3e15e-110"><span id="i"></span><span id="I"></span>*i*</span><span class="sxs-lookup"><span data-stu-id="3e15e-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="3e15e-111">\[in \] un vettore a virgola mobile e direzione raggio.</span><span class="sxs-lookup"><span data-stu-id="3e15e-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="3e15e-112"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="3e15e-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="3e15e-113">\[in \] un vettore a virgola mobile, superficie normale.</span><span class="sxs-lookup"><span data-stu-id="3e15e-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="3e15e-114">*?*</span><span class="sxs-lookup"><span data-stu-id="3e15e-114">*?*</span></span><br/>                                         | <span data-ttu-id="3e15e-115">\[in \] una virgola mobile, indice rifrazione scalare.</span><span class="sxs-lookup"><span data-stu-id="3e15e-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3e15e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e15e-116">Return Value</span></span>

<span data-ttu-id="3e15e-117">Vettore di rifrazione A virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3e15e-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="3e15e-118">Se l'angolo tra il raggio i e la normale della superficie n è troppo grande per un indice di rifrazione specificato, il valore restituito è (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="3e15e-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="3e15e-119">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="3e15e-119">Type Description</span></span>



| <span data-ttu-id="3e15e-120">Nome</span><span class="sxs-lookup"><span data-stu-id="3e15e-120">Name</span></span>              | [<span data-ttu-id="3e15e-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="3e15e-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="3e15e-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="3e15e-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3e15e-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3e15e-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3e15e-124">*i*</span><span class="sxs-lookup"><span data-stu-id="3e15e-124">*i*</span></span>               | [<span data-ttu-id="3e15e-125">**vettore**</span><span class="sxs-lookup"><span data-stu-id="3e15e-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3e15e-126">**float**</span><span class="sxs-lookup"><span data-stu-id="3e15e-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3e15e-127">any</span><span class="sxs-lookup"><span data-stu-id="3e15e-127">any</span></span>                            |
| <span data-ttu-id="3e15e-128">*n*</span><span class="sxs-lookup"><span data-stu-id="3e15e-128">*n*</span></span>               | [<span data-ttu-id="3e15e-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="3e15e-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3e15e-130">**float**</span><span class="sxs-lookup"><span data-stu-id="3e15e-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3e15e-131">le stesse dimensioni di input *i*</span><span class="sxs-lookup"><span data-stu-id="3e15e-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="3e15e-132">?</span><span class="sxs-lookup"><span data-stu-id="3e15e-132">?</span></span>                 | [<span data-ttu-id="3e15e-133">**scalare**</span><span class="sxs-lookup"><span data-stu-id="3e15e-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3e15e-134">**float**</span><span class="sxs-lookup"><span data-stu-id="3e15e-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3e15e-135">1</span><span class="sxs-lookup"><span data-stu-id="3e15e-135">1</span></span>                              |
| <span data-ttu-id="3e15e-136">vettore di rifrazione</span><span class="sxs-lookup"><span data-stu-id="3e15e-136">refraction vector</span></span> | [<span data-ttu-id="3e15e-137">**vettore**</span><span class="sxs-lookup"><span data-stu-id="3e15e-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3e15e-138">**float**</span><span class="sxs-lookup"><span data-stu-id="3e15e-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3e15e-139">le stesse dimensioni di input *i*</span><span class="sxs-lookup"><span data-stu-id="3e15e-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3e15e-140">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3e15e-140">Minimum Shader Model</span></span>

<span data-ttu-id="3e15e-141">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e15e-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3e15e-142">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3e15e-142">Shader Model</span></span>                                                                       | <span data-ttu-id="3e15e-143">Supportato</span><span class="sxs-lookup"><span data-stu-id="3e15e-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="3e15e-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="3e15e-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3e15e-145">sì</span><span class="sxs-lookup"><span data-stu-id="3e15e-145">yes</span></span>                 |
| [<span data-ttu-id="3e15e-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3e15e-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3e15e-147">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="3e15e-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3e15e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e15e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e15e-149">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3e15e-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

