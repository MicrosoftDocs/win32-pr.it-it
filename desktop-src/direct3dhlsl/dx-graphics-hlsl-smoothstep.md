---
title: SmoothStep
description: Restituisce un'interpolazione dell'eremita smussata tra 0 e 1, se x è compreso nell'intervallo \ min, max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- HLSL SmoothStep
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976671"
---
# <a name="smoothstep"></a><span data-ttu-id="60081-104">SmoothStep</span><span class="sxs-lookup"><span data-stu-id="60081-104">smoothstep</span></span>

<span data-ttu-id="60081-105">Restituisce un'interpolazione dell'eremita smussata tra 0 e 1, se *x* è compreso nell'intervallo \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="60081-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="60081-106">SmoothStep *ret* (*min*, *Max*, *x*)</span><span class="sxs-lookup"><span data-stu-id="60081-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="60081-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="60081-107">Parameters</span></span>



| <span data-ttu-id="60081-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="60081-108">Item</span></span>                                                         | <span data-ttu-id="60081-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60081-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="60081-110"><span id="min"></span><span id="MIN"></span>*min*</span><span class="sxs-lookup"><span data-stu-id="60081-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="60081-111">\[nell' \] intervallo minimo del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="60081-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="60081-112"><span id="max"></span><span id="MAX"></span>*Max*</span><span class="sxs-lookup"><span data-stu-id="60081-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="60081-113">\[nell' \] intervallo massimo del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="60081-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="60081-114"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="60081-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="60081-115">\[nel \] valore specificato da interpolare.</span><span class="sxs-lookup"><span data-stu-id="60081-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="60081-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60081-116">Return Value</span></span>

<span data-ttu-id="60081-117">Restituisce 0 se *x* è minore di *min*; 1 se *x* è maggiore di *Max*; in caso contrario, un valore compreso tra 0 e 1 se *x* è compreso nell'intervallo \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="60081-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="60081-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="60081-118">Remarks</span></span>

<span data-ttu-id="60081-119">Usare la funzione intrinseca **SmoothStep** HLSL per creare una transizione uniforme tra due valori.</span><span class="sxs-lookup"><span data-stu-id="60081-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="60081-120">Ad esempio, è possibile usare questa funzione per unire due colori in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="60081-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="60081-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="60081-121">Type Description</span></span>



| <span data-ttu-id="60081-122">Nome</span><span class="sxs-lookup"><span data-stu-id="60081-122">Name</span></span>  | [<span data-ttu-id="60081-123">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="60081-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="60081-124">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="60081-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="60081-125">Dimensione</span><span class="sxs-lookup"><span data-stu-id="60081-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="60081-126">*x*</span><span class="sxs-lookup"><span data-stu-id="60081-126">*x*</span></span>   | <span data-ttu-id="60081-127">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="60081-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="60081-128">**float**</span><span class="sxs-lookup"><span data-stu-id="60081-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="60081-129">any</span><span class="sxs-lookup"><span data-stu-id="60081-129">any</span></span>                            |
| <span data-ttu-id="60081-130">*min*</span><span class="sxs-lookup"><span data-stu-id="60081-130">*min*</span></span> | <span data-ttu-id="60081-131">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="60081-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="60081-132">**float**</span><span class="sxs-lookup"><span data-stu-id="60081-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="60081-133">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="60081-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="60081-134">*max*</span><span class="sxs-lookup"><span data-stu-id="60081-134">*max*</span></span> | <span data-ttu-id="60081-135">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="60081-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="60081-136">**float**</span><span class="sxs-lookup"><span data-stu-id="60081-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="60081-137">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="60081-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="60081-138">*RET*</span><span class="sxs-lookup"><span data-stu-id="60081-138">*ret*</span></span> | <span data-ttu-id="60081-139">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="60081-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="60081-140">**float**</span><span class="sxs-lookup"><span data-stu-id="60081-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="60081-141">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="60081-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60081-142">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="60081-142">Minimum Shader Model</span></span>

<span data-ttu-id="60081-143">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="60081-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="60081-144">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="60081-144">Shader Model</span></span>                                                                       | <span data-ttu-id="60081-145">Supportato</span><span class="sxs-lookup"><span data-stu-id="60081-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="60081-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="60081-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="60081-147">sì</span><span class="sxs-lookup"><span data-stu-id="60081-147">yes</span></span>                 |
| [<span data-ttu-id="60081-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60081-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="60081-149">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="60081-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="60081-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60081-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60081-151">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="60081-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

