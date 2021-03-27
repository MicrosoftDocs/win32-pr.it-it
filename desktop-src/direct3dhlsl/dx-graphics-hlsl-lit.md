---
title: acceso
description: Restituisce un vettore di coefficienti di illuminazione.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL illuminato
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872541"
---
# <a name="lit"></a><span data-ttu-id="344c6-104">acceso</span><span class="sxs-lookup"><span data-stu-id="344c6-104">lit</span></span>

<span data-ttu-id="344c6-105">Restituisce un vettore di coefficienti di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="344c6-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="344c6-106">*ret* lit (*n \_ punto \_ l*, *n \_ punto \_ h*, *m*)</span><span class="sxs-lookup"><span data-stu-id="344c6-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="344c6-107">Questa funzione restituisce un vettore di coefficienti di illuminazione (ambiente, diffuso, speculare, 1) in cui:</span><span class="sxs-lookup"><span data-stu-id="344c6-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="344c6-108">ambiente = 1</span><span class="sxs-lookup"><span data-stu-id="344c6-108">ambient = 1</span></span>
-   <span data-ttu-id="344c6-109">diffusa = n · l < 0?</span><span class="sxs-lookup"><span data-stu-id="344c6-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="344c6-110">0: n · l</span><span class="sxs-lookup"><span data-stu-id="344c6-110">0 : n · l</span></span>
-   <span data-ttu-id="344c6-111">speculare = n · l < 0 \| \| n · h < 0?</span><span class="sxs-lookup"><span data-stu-id="344c6-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="344c6-112">0: (n · h) ^ m</span><span class="sxs-lookup"><span data-stu-id="344c6-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="344c6-113">Dove Vector n è il vettore normale, l è la direzione della luce e h è il vettore mezzo.</span><span class="sxs-lookup"><span data-stu-id="344c6-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="344c6-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="344c6-114">Parameters</span></span>



| <span data-ttu-id="344c6-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="344c6-115">Item</span></span>                                                                       | <span data-ttu-id="344c6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="344c6-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="344c6-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ punto \_ l*</span><span class="sxs-lookup"><span data-stu-id="344c6-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="344c6-118">\[nel \] prodotto a punti della superficie normalizzata normale e del vettore chiaro.</span><span class="sxs-lookup"><span data-stu-id="344c6-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="344c6-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punto \_ h*</span><span class="sxs-lookup"><span data-stu-id="344c6-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="344c6-120">\[nel \] prodotto a virgola del vettore a metà angolo e della normale della superficie.</span><span class="sxs-lookup"><span data-stu-id="344c6-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="344c6-121"><span id="m"></span><span id="M"></span>*m*</span><span class="sxs-lookup"><span data-stu-id="344c6-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="344c6-122">\[in \] un esponente speculare.</span><span class="sxs-lookup"><span data-stu-id="344c6-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="344c6-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="344c6-123">Return Value</span></span>

<span data-ttu-id="344c6-124">Vettore di coefficiente di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="344c6-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="344c6-125">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="344c6-125">Type Description</span></span>



| <span data-ttu-id="344c6-126">Nome</span><span class="sxs-lookup"><span data-stu-id="344c6-126">Name</span></span>        | [<span data-ttu-id="344c6-127">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="344c6-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="344c6-128">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="344c6-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="344c6-129">Dimensione</span><span class="sxs-lookup"><span data-stu-id="344c6-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="344c6-130">*n \_ punto \_ l*</span><span class="sxs-lookup"><span data-stu-id="344c6-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="344c6-131">**scalare**</span><span class="sxs-lookup"><span data-stu-id="344c6-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="344c6-132">**float**</span><span class="sxs-lookup"><span data-stu-id="344c6-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="344c6-133">1</span><span class="sxs-lookup"><span data-stu-id="344c6-133">1</span></span>    |
| <span data-ttu-id="344c6-134">*n \_ punto \_ h*</span><span class="sxs-lookup"><span data-stu-id="344c6-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="344c6-135">**scalare**</span><span class="sxs-lookup"><span data-stu-id="344c6-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="344c6-136">**float**</span><span class="sxs-lookup"><span data-stu-id="344c6-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="344c6-137">1</span><span class="sxs-lookup"><span data-stu-id="344c6-137">1</span></span>    |
| <span data-ttu-id="344c6-138">*m*</span><span class="sxs-lookup"><span data-stu-id="344c6-138">*m*</span></span>         | [<span data-ttu-id="344c6-139">**scalare**</span><span class="sxs-lookup"><span data-stu-id="344c6-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="344c6-140">**float**</span><span class="sxs-lookup"><span data-stu-id="344c6-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="344c6-141">1</span><span class="sxs-lookup"><span data-stu-id="344c6-141">1</span></span>    |
| <span data-ttu-id="344c6-142">*RET*</span><span class="sxs-lookup"><span data-stu-id="344c6-142">*ret*</span></span>       | [<span data-ttu-id="344c6-143">**vettore**</span><span class="sxs-lookup"><span data-stu-id="344c6-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="344c6-144">**float**</span><span class="sxs-lookup"><span data-stu-id="344c6-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="344c6-145">4</span><span class="sxs-lookup"><span data-stu-id="344c6-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="344c6-146">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="344c6-146">Minimum Shader Model</span></span>

<span data-ttu-id="344c6-147">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="344c6-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="344c6-148">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="344c6-148">Shader Model</span></span>                                                                       | <span data-ttu-id="344c6-149">Supportato</span><span class="sxs-lookup"><span data-stu-id="344c6-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="344c6-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="344c6-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="344c6-151">sì</span><span class="sxs-lookup"><span data-stu-id="344c6-151">yes</span></span>                 |
| [<span data-ttu-id="344c6-152">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="344c6-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="344c6-153">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="344c6-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="344c6-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="344c6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344c6-155">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="344c6-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

