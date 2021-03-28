---
title: max
description: Seleziona maggiore di x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- numero massimo di HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399464"
---
# <a name="max"></a><span data-ttu-id="bc6b9-104">max</span><span class="sxs-lookup"><span data-stu-id="bc6b9-104">max</span></span>

<span data-ttu-id="bc6b9-105">Seleziona maggiore di x e y.</span><span class="sxs-lookup"><span data-stu-id="bc6b9-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="bc6b9-106">RET Max (x, y)</span><span class="sxs-lookup"><span data-stu-id="bc6b9-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="bc6b9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc6b9-107">Parameters</span></span>



| <span data-ttu-id="bc6b9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc6b9-108">Item</span></span>                                                   | <span data-ttu-id="bc6b9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc6b9-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="bc6b9-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bc6b9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bc6b9-111">\[nel \] valore di input x.</span><span class="sxs-lookup"><span data-stu-id="bc6b9-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="bc6b9-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="bc6b9-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="bc6b9-113">\[nel \] valore di input y.</span><span class="sxs-lookup"><span data-stu-id="bc6b9-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bc6b9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc6b9-114">Return Value</span></span>

<span data-ttu-id="bc6b9-115">Il parametro *x* o *y* , a seconda del valore più grande.</span><span class="sxs-lookup"><span data-stu-id="bc6b9-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="bc6b9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc6b9-116">Remarks</span></span>

<span data-ttu-id="bc6b9-117">I denormalizzati vengono gestiti come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="bc6b9-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="bc6b9-118">src1 src0-></span><span class="sxs-lookup"><span data-stu-id="bc6b9-118">src0 src1-></span></span> | <span data-ttu-id="bc6b9-119">-inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-119">-inf</span></span> | <span data-ttu-id="bc6b9-120">F</span><span class="sxs-lookup"><span data-stu-id="bc6b9-120">F</span></span>             | <span data-ttu-id="bc6b9-121">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-121">+inf</span></span> | <span data-ttu-id="bc6b9-122">NAN</span><span class="sxs-lookup"><span data-stu-id="bc6b9-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="bc6b9-123">-inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-123">-inf</span></span>        | <span data-ttu-id="bc6b9-124">-inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-124">-inf</span></span> | <span data-ttu-id="bc6b9-125">src1</span><span class="sxs-lookup"><span data-stu-id="bc6b9-125">src1</span></span>          | <span data-ttu-id="bc6b9-126">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-126">+inf</span></span> | <span data-ttu-id="bc6b9-127">-inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-127">-inf</span></span> |
| <span data-ttu-id="bc6b9-128">F</span><span class="sxs-lookup"><span data-stu-id="bc6b9-128">F</span></span>           | <span data-ttu-id="bc6b9-129">src0</span><span class="sxs-lookup"><span data-stu-id="bc6b9-129">src0</span></span> | <span data-ttu-id="bc6b9-130">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="bc6b9-130">src0 or src1</span></span>  | <span data-ttu-id="bc6b9-131">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-131">+inf</span></span> | <span data-ttu-id="bc6b9-132">src0</span><span class="sxs-lookup"><span data-stu-id="bc6b9-132">src0</span></span> |
| <span data-ttu-id="bc6b9-133">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-133">+inf</span></span>        | <span data-ttu-id="bc6b9-134">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-134">+inf</span></span> | <span data-ttu-id="bc6b9-135">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-135">+inf</span></span>          | <span data-ttu-id="bc6b9-136">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-136">+inf</span></span> | <span data-ttu-id="bc6b9-137">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-137">+inf</span></span> |
| <span data-ttu-id="bc6b9-138">NaN</span><span class="sxs-lookup"><span data-stu-id="bc6b9-138">NaN</span></span>         | <span data-ttu-id="bc6b9-139">-inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-139">-inf</span></span> | <span data-ttu-id="bc6b9-140">src1</span><span class="sxs-lookup"><span data-stu-id="bc6b9-140">src1</span></span>          | <span data-ttu-id="bc6b9-141">+inf</span><span class="sxs-lookup"><span data-stu-id="bc6b9-141">+inf</span></span> | <span data-ttu-id="bc6b9-142">NaN</span><span class="sxs-lookup"><span data-stu-id="bc6b9-142">NaN</span></span>  |

<span data-ttu-id="bc6b9-143">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="bc6b9-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="bc6b9-144">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="bc6b9-144">Type Description</span></span>

| <span data-ttu-id="bc6b9-145">Nome</span><span class="sxs-lookup"><span data-stu-id="bc6b9-145">Name</span></span> | <span data-ttu-id="bc6b9-146">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="bc6b9-146">In/Out</span></span>      | [<span data-ttu-id="bc6b9-147">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="bc6b9-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bc6b9-148">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="bc6b9-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="bc6b9-149">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bc6b9-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="bc6b9-150">x</span><span class="sxs-lookup"><span data-stu-id="bc6b9-150">x</span></span>    | <span data-ttu-id="bc6b9-151">in ingresso</span><span class="sxs-lookup"><span data-stu-id="bc6b9-151">in</span></span>          | <span data-ttu-id="bc6b9-152">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="bc6b9-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="bc6b9-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bc6b9-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="bc6b9-154">any</span><span class="sxs-lookup"><span data-stu-id="bc6b9-154">any</span></span>                          |
| <span data-ttu-id="bc6b9-155">y</span><span class="sxs-lookup"><span data-stu-id="bc6b9-155">y</span></span>    | <span data-ttu-id="bc6b9-156">in ingresso</span><span class="sxs-lookup"><span data-stu-id="bc6b9-156">in</span></span>          | <span data-ttu-id="bc6b9-157">uguale all'input x</span><span class="sxs-lookup"><span data-stu-id="bc6b9-157">same as input x</span></span>                                                                                                | <span data-ttu-id="bc6b9-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bc6b9-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="bc6b9-159">le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="bc6b9-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="bc6b9-160">RET</span><span class="sxs-lookup"><span data-stu-id="bc6b9-160">ret</span></span>  | <span data-ttu-id="bc6b9-161">tipo restituito</span><span class="sxs-lookup"><span data-stu-id="bc6b9-161">return type</span></span> | <span data-ttu-id="bc6b9-162">uguale all'input x</span><span class="sxs-lookup"><span data-stu-id="bc6b9-162">same as input x</span></span>                                                                                                | <span data-ttu-id="bc6b9-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bc6b9-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="bc6b9-164">le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="bc6b9-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bc6b9-165">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bc6b9-165">Minimum Shader Model</span></span>

<span data-ttu-id="bc6b9-166">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc6b9-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bc6b9-167">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bc6b9-167">Shader Model</span></span>                                                                       | <span data-ttu-id="bc6b9-168">Supportato</span><span class="sxs-lookup"><span data-stu-id="bc6b9-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="bc6b9-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="bc6b9-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bc6b9-170">sì</span><span class="sxs-lookup"><span data-stu-id="bc6b9-170">yes</span></span>                         |
| [<span data-ttu-id="bc6b9-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc6b9-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bc6b9-172">Sì (vs \_ 1 \_ e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="bc6b9-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bc6b9-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc6b9-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6b9-174">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bc6b9-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="bc6b9-175">**Specifica funzionale DirectX**</span><span class="sxs-lookup"><span data-stu-id="bc6b9-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
