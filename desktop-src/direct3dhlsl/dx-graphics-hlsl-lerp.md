---
title: Lerp
description: Esegue un'interpolazione lineare.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- HLSL Lerp
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993432"
---
# <a name="lerp"></a><span data-ttu-id="f7be8-104">Lerp</span><span class="sxs-lookup"><span data-stu-id="f7be8-104">lerp</span></span>

<span data-ttu-id="f7be8-105">Esegue un'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="f7be8-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="f7be8-106">Lerp *ret* (*x*, *y*, *s*)</span><span class="sxs-lookup"><span data-stu-id="f7be8-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f7be8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7be8-107">Parameters</span></span>



| <span data-ttu-id="f7be8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7be8-108">Item</span></span>                                                   | <span data-ttu-id="f7be8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7be8-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7be8-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f7be8-111">\[nel \] primo valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="f7be8-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="f7be8-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="f7be8-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="f7be8-113">\[nel \] secondo valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="f7be8-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="f7be8-114"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="f7be8-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="f7be8-115">\[in \] un valore che esegue l'interpolazione lineare tra il parametro *x* e il parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="f7be8-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f7be8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7be8-116">Return Value</span></span>

<span data-ttu-id="f7be8-117">Risultato dell'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="f7be8-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="f7be8-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="f7be8-118">Type Description</span></span>



| <span data-ttu-id="f7be8-119">Nome</span><span class="sxs-lookup"><span data-stu-id="f7be8-119">Name</span></span>  | [<span data-ttu-id="f7be8-120">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="f7be8-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f7be8-121">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="f7be8-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f7be8-122">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f7be8-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f7be8-123">*x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-123">*x*</span></span>   | <span data-ttu-id="f7be8-124">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="f7be8-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f7be8-125">**float**</span><span class="sxs-lookup"><span data-stu-id="f7be8-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f7be8-126">any</span><span class="sxs-lookup"><span data-stu-id="f7be8-126">any</span></span>                            |
| <span data-ttu-id="f7be8-127">*y*</span><span class="sxs-lookup"><span data-stu-id="f7be8-127">*y*</span></span>   | <span data-ttu-id="f7be8-128">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f7be8-129">**float**</span><span class="sxs-lookup"><span data-stu-id="f7be8-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f7be8-130">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="f7be8-131">*s*</span><span class="sxs-lookup"><span data-stu-id="f7be8-131">*s*</span></span>   | <span data-ttu-id="f7be8-132">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f7be8-133">**float**</span><span class="sxs-lookup"><span data-stu-id="f7be8-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f7be8-134">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="f7be8-135">*RET*</span><span class="sxs-lookup"><span data-stu-id="f7be8-135">*ret*</span></span> | <span data-ttu-id="f7be8-136">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f7be8-137">**float**</span><span class="sxs-lookup"><span data-stu-id="f7be8-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f7be8-138">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="f7be8-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f7be8-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7be8-139">Remarks</span></span>

<span data-ttu-id="f7be8-140">L'interpolazione lineare è basata sulla formula seguente: x \* (1-s) + y \* s, che può essere scritta in modo equivalente come x + s (y-x).</span><span class="sxs-lookup"><span data-stu-id="f7be8-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f7be8-141">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f7be8-141">Minimum Shader Model</span></span>

<span data-ttu-id="f7be8-142">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7be8-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f7be8-143">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f7be8-143">Shader Model</span></span>                                                                       | <span data-ttu-id="f7be8-144">Supportato</span><span class="sxs-lookup"><span data-stu-id="f7be8-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="f7be8-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="f7be8-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f7be8-146">sì</span><span class="sxs-lookup"><span data-stu-id="f7be8-146">yes</span></span>                         |
| [<span data-ttu-id="f7be8-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7be8-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f7be8-148">Sì (vs \_ 1 \_ 1 e PS \_ 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="f7be8-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="f7be8-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7be8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7be8-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f7be8-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

