---
title: faceforward
description: Capovolge la superficie normale, se necessario, in una direzione opposta a i; Restituisce il risultato in n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- HLSL faceforward
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117934"
---
# <a name="faceforward"></a><span data-ttu-id="30867-104">faceforward</span><span class="sxs-lookup"><span data-stu-id="30867-104">faceforward</span></span>

<span data-ttu-id="30867-105">Capovolge la superficie normale, se necessario, in una direzione opposta a i; Restituisce il risultato in n.</span><span class="sxs-lookup"><span data-stu-id="30867-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="30867-106">faceforward *ret* (*n*, *i*, *ng*)</span><span class="sxs-lookup"><span data-stu-id="30867-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="30867-107">Questa funzione usa la formula seguente:-*n*  Sign (dot (*i*, *ng*)).</span><span class="sxs-lookup"><span data-stu-id="30867-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="30867-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30867-108">Parameters</span></span>



| <span data-ttu-id="30867-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="30867-109">Item</span></span>                                                      | <span data-ttu-id="30867-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30867-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30867-111"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="30867-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="30867-112">\[nella \] superficie a virgola mobile risultante, vector normale.</span><span class="sxs-lookup"><span data-stu-id="30867-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="30867-113"><span id="i"></span><span id="I"></span>*i*</span><span class="sxs-lookup"><span data-stu-id="30867-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="30867-114">\[in \] un vettore di evento imprevisto a virgola mobile che punta dalla posizione di visualizzazione alla posizione di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="30867-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="30867-115"><span id="ng"></span><span id="NG"></span>*ng*</span><span class="sxs-lookup"><span data-stu-id="30867-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="30867-116">\[in \] una superficie a virgola mobile-vettore normale.</span><span class="sxs-lookup"><span data-stu-id="30867-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="30867-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30867-117">Return Value</span></span>

<span data-ttu-id="30867-118">Vettore normale della superficie A virgola mobile che si trova verso la direzione della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="30867-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="30867-119">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="30867-119">Type Description</span></span>



| <span data-ttu-id="30867-120">Nome</span><span class="sxs-lookup"><span data-stu-id="30867-120">Name</span></span>  | [<span data-ttu-id="30867-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="30867-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="30867-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="30867-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="30867-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="30867-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="30867-124">*n*</span><span class="sxs-lookup"><span data-stu-id="30867-124">*n*</span></span>   | [<span data-ttu-id="30867-125">**vettore**</span><span class="sxs-lookup"><span data-stu-id="30867-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30867-126">**float**</span><span class="sxs-lookup"><span data-stu-id="30867-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="30867-127">any</span><span class="sxs-lookup"><span data-stu-id="30867-127">any</span></span>                            |
| <span data-ttu-id="30867-128">*i*</span><span class="sxs-lookup"><span data-stu-id="30867-128">*i*</span></span>   | [<span data-ttu-id="30867-129">**vettore**</span><span class="sxs-lookup"><span data-stu-id="30867-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30867-130">**float**</span><span class="sxs-lookup"><span data-stu-id="30867-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="30867-131">le stesse dimensioni di input *n*</span><span class="sxs-lookup"><span data-stu-id="30867-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="30867-132">*ng*</span><span class="sxs-lookup"><span data-stu-id="30867-132">*ng*</span></span>  | [<span data-ttu-id="30867-133">**vettore**</span><span class="sxs-lookup"><span data-stu-id="30867-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30867-134">**float**</span><span class="sxs-lookup"><span data-stu-id="30867-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="30867-135">stesse dimensioni dell'input *n*</span><span class="sxs-lookup"><span data-stu-id="30867-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="30867-136">*RET*</span><span class="sxs-lookup"><span data-stu-id="30867-136">*ret*</span></span> | [<span data-ttu-id="30867-137">**vettore**</span><span class="sxs-lookup"><span data-stu-id="30867-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="30867-138">**float**</span><span class="sxs-lookup"><span data-stu-id="30867-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="30867-139">stesse dimensioni dell'input *n*</span><span class="sxs-lookup"><span data-stu-id="30867-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="30867-140">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="30867-140">Minimum Shader Model</span></span>

<span data-ttu-id="30867-141">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="30867-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="30867-142">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="30867-142">Shader Model</span></span>                                                                       | <span data-ttu-id="30867-143">Supportato</span><span class="sxs-lookup"><span data-stu-id="30867-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="30867-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="30867-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="30867-145">sì</span><span class="sxs-lookup"><span data-stu-id="30867-145">yes</span></span>                   |
| [<span data-ttu-id="30867-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="30867-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="30867-147">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="30867-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="30867-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30867-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30867-149">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="30867-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

