---
title: pow
description: Restituisce il valore specificato elevato alla potenza specificata.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- HLSL POW
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474094"
---
# <a name="pow"></a><span data-ttu-id="00d97-104">pow</span><span class="sxs-lookup"><span data-stu-id="00d97-104">pow</span></span>

<span data-ttu-id="00d97-105">Restituisce il valore specificato elevato alla potenza specificata.</span><span class="sxs-lookup"><span data-stu-id="00d97-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="00d97-106">*ret* Pow (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="00d97-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="00d97-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00d97-107">Parameters</span></span>



| <span data-ttu-id="00d97-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="00d97-108">Item</span></span>                                                   | <span data-ttu-id="00d97-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00d97-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="00d97-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="00d97-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="00d97-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="00d97-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="00d97-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="00d97-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="00d97-113">\[nella \] potenza specificata.</span><span class="sxs-lookup"><span data-stu-id="00d97-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="00d97-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00d97-114">Return Value</span></span>

<span data-ttu-id="00d97-115">Parametro *x* elevato alla potenza del parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="00d97-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d97-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="00d97-116">Remarks</span></span>

<span data-ttu-id="00d97-117">La funzione intrinseca **POW** HLSL calcola *x*<sup>y</sup>.</span><span class="sxs-lookup"><span data-stu-id="00d97-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="00d97-118">X</span><span class="sxs-lookup"><span data-stu-id="00d97-118">X</span></span>      | <span data-ttu-id="00d97-119">Y</span><span class="sxs-lookup"><span data-stu-id="00d97-119">Y</span></span>      | <span data-ttu-id="00d97-120">Risultato</span><span class="sxs-lookup"><span data-stu-id="00d97-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="00d97-121">< 0</span><span class="sxs-lookup"><span data-stu-id="00d97-121">< 0</span></span> | <span data-ttu-id="00d97-122">any</span><span class="sxs-lookup"><span data-stu-id="00d97-122">any</span></span>    | <span data-ttu-id="00d97-123">NAN</span><span class="sxs-lookup"><span data-stu-id="00d97-123">NAN</span></span>                                                                         |
| <span data-ttu-id="00d97-124">> 0</span><span class="sxs-lookup"><span data-stu-id="00d97-124">> 0</span></span> | <span data-ttu-id="00d97-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="00d97-125">== 0</span></span>   | <span data-ttu-id="00d97-126">1</span><span class="sxs-lookup"><span data-stu-id="00d97-126">1</span></span>                                                                           |
| <span data-ttu-id="00d97-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="00d97-127">== 0</span></span>   | <span data-ttu-id="00d97-128">> 0</span><span class="sxs-lookup"><span data-stu-id="00d97-128">> 0</span></span> | <span data-ttu-id="00d97-129">0</span><span class="sxs-lookup"><span data-stu-id="00d97-129">0</span></span>                                                                           |
| <span data-ttu-id="00d97-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="00d97-130">== 0</span></span>   | <span data-ttu-id="00d97-131">< 0</span><span class="sxs-lookup"><span data-stu-id="00d97-131">< 0</span></span> | <span data-ttu-id="00d97-132">INF</span><span class="sxs-lookup"><span data-stu-id="00d97-132">inf</span></span>                                                                         |
| <span data-ttu-id="00d97-133">> 0</span><span class="sxs-lookup"><span data-stu-id="00d97-133">> 0</span></span> | <span data-ttu-id="00d97-134">< 0</span><span class="sxs-lookup"><span data-stu-id="00d97-134">< 0</span></span> | <span data-ttu-id="00d97-135">1/X<sup>-Y</sup></span><span class="sxs-lookup"><span data-stu-id="00d97-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="00d97-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="00d97-136">== 0</span></span>   | <span data-ttu-id="00d97-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="00d97-137">== 0</span></span>   | <span data-ttu-id="00d97-138">Dipende dal processore grafico specifico</span><span class="sxs-lookup"><span data-stu-id="00d97-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="00d97-139">0, 1 o NAN</span><span class="sxs-lookup"><span data-stu-id="00d97-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="00d97-140">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="00d97-140">Type Description</span></span>



| <span data-ttu-id="00d97-141">Nome</span><span class="sxs-lookup"><span data-stu-id="00d97-141">Name</span></span>  | [<span data-ttu-id="00d97-142">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="00d97-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="00d97-143">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="00d97-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="00d97-144">Dimensione</span><span class="sxs-lookup"><span data-stu-id="00d97-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="00d97-145">*x*</span><span class="sxs-lookup"><span data-stu-id="00d97-145">*x*</span></span>   | <span data-ttu-id="00d97-146">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="00d97-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="00d97-147">**float**</span><span class="sxs-lookup"><span data-stu-id="00d97-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="00d97-148">any</span><span class="sxs-lookup"><span data-stu-id="00d97-148">any</span></span>                            |
| <span data-ttu-id="00d97-149">*y*</span><span class="sxs-lookup"><span data-stu-id="00d97-149">*y*</span></span>   | <span data-ttu-id="00d97-150">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="00d97-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="00d97-151">**float**</span><span class="sxs-lookup"><span data-stu-id="00d97-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="00d97-152">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="00d97-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="00d97-153">*RET*</span><span class="sxs-lookup"><span data-stu-id="00d97-153">*ret*</span></span> | <span data-ttu-id="00d97-154">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="00d97-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="00d97-155">**float**</span><span class="sxs-lookup"><span data-stu-id="00d97-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="00d97-156">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="00d97-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="00d97-157">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="00d97-157">Minimum Shader Model</span></span>

<span data-ttu-id="00d97-158">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="00d97-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="00d97-159">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="00d97-159">Shader Model</span></span>                                                                       | <span data-ttu-id="00d97-160">Supportato</span><span class="sxs-lookup"><span data-stu-id="00d97-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="00d97-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="00d97-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="00d97-162">sì</span><span class="sxs-lookup"><span data-stu-id="00d97-162">yes</span></span>                 |
| [<span data-ttu-id="00d97-163">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00d97-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="00d97-164">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="00d97-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="00d97-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00d97-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d97-166">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="00d97-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

