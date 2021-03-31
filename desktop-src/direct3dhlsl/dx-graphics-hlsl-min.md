---
title: min
description: Seleziona il minore di x e y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- min HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474099"
---
# <a name="min"></a><span data-ttu-id="aa469-104">min</span><span class="sxs-lookup"><span data-stu-id="aa469-104">min</span></span>

<span data-ttu-id="aa469-105">Seleziona il minore di x e y.</span><span class="sxs-lookup"><span data-stu-id="aa469-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="aa469-106">RET min (x, y)</span><span class="sxs-lookup"><span data-stu-id="aa469-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="aa469-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa469-107">Parameters</span></span>



| <span data-ttu-id="aa469-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa469-108">Item</span></span>                                                   | <span data-ttu-id="aa469-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa469-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="aa469-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="aa469-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="aa469-111">\[nel \] valore di input x.</span><span class="sxs-lookup"><span data-stu-id="aa469-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="aa469-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="aa469-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="aa469-113">\[nel \] valore di input y.</span><span class="sxs-lookup"><span data-stu-id="aa469-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="aa469-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa469-114">Return Value</span></span>

<span data-ttu-id="aa469-115">Il parametro *x* o *y* , a seconda del valore più piccolo.</span><span class="sxs-lookup"><span data-stu-id="aa469-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="aa469-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa469-116">Remarks</span></span>

<span data-ttu-id="aa469-117">I denormalizzati vengono gestiti come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="aa469-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="aa469-118">src1 src0-></span><span class="sxs-lookup"><span data-stu-id="aa469-118">src0 src1-></span></span> | <span data-ttu-id="aa469-119">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-119">-inf</span></span> | <span data-ttu-id="aa469-120">F</span><span class="sxs-lookup"><span data-stu-id="aa469-120">F</span></span>             | <span data-ttu-id="aa469-121">+inf</span><span class="sxs-lookup"><span data-stu-id="aa469-121">+inf</span></span> | <span data-ttu-id="aa469-122">NAN</span><span class="sxs-lookup"><span data-stu-id="aa469-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="aa469-123">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-123">-inf</span></span>        | <span data-ttu-id="aa469-124">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-124">-inf</span></span> | <span data-ttu-id="aa469-125">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-125">-inf</span></span>          | <span data-ttu-id="aa469-126">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-126">-inf</span></span> | <span data-ttu-id="aa469-127">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-127">-inf</span></span> |
| <span data-ttu-id="aa469-128">F</span><span class="sxs-lookup"><span data-stu-id="aa469-128">F</span></span>           | <span data-ttu-id="aa469-129">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-129">-inf</span></span> | <span data-ttu-id="aa469-130">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="aa469-130">src0 or src1</span></span>  | <span data-ttu-id="aa469-131">src0</span><span class="sxs-lookup"><span data-stu-id="aa469-131">src0</span></span> | <span data-ttu-id="aa469-132">src0</span><span class="sxs-lookup"><span data-stu-id="aa469-132">src0</span></span> |
| <span data-ttu-id="aa469-133">+inf</span><span class="sxs-lookup"><span data-stu-id="aa469-133">+inf</span></span>        | <span data-ttu-id="aa469-134">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-134">-inf</span></span> | <span data-ttu-id="aa469-135">src1</span><span class="sxs-lookup"><span data-stu-id="aa469-135">src1</span></span>          | <span data-ttu-id="aa469-136">+inf</span><span class="sxs-lookup"><span data-stu-id="aa469-136">+inf</span></span> | <span data-ttu-id="aa469-137">+inf</span><span class="sxs-lookup"><span data-stu-id="aa469-137">+inf</span></span> |
| <span data-ttu-id="aa469-138">NaN</span><span class="sxs-lookup"><span data-stu-id="aa469-138">NaN</span></span>         | <span data-ttu-id="aa469-139">-inf</span><span class="sxs-lookup"><span data-stu-id="aa469-139">-inf</span></span> | <span data-ttu-id="aa469-140">src1</span><span class="sxs-lookup"><span data-stu-id="aa469-140">src1</span></span>          | <span data-ttu-id="aa469-141">+inf</span><span class="sxs-lookup"><span data-stu-id="aa469-141">+inf</span></span> | <span data-ttu-id="aa469-142">NaN</span><span class="sxs-lookup"><span data-stu-id="aa469-142">NaN</span></span>  |

<span data-ttu-id="aa469-143">F indica un numero reale finito.</span><span class="sxs-lookup"><span data-stu-id="aa469-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="aa469-144">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="aa469-144">Type Description</span></span>

| <span data-ttu-id="aa469-145">Nome</span><span class="sxs-lookup"><span data-stu-id="aa469-145">Name</span></span> | <span data-ttu-id="aa469-146">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="aa469-146">In/Out</span></span>      | [<span data-ttu-id="aa469-147">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="aa469-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="aa469-148">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="aa469-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="aa469-149">Dimensione</span><span class="sxs-lookup"><span data-stu-id="aa469-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="aa469-150">x</span><span class="sxs-lookup"><span data-stu-id="aa469-150">x</span></span>    | <span data-ttu-id="aa469-151">in ingresso</span><span class="sxs-lookup"><span data-stu-id="aa469-151">in</span></span>          | <span data-ttu-id="aa469-152">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="aa469-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="aa469-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="aa469-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="aa469-154">any</span><span class="sxs-lookup"><span data-stu-id="aa469-154">any</span></span>                          |
| <span data-ttu-id="aa469-155">y</span><span class="sxs-lookup"><span data-stu-id="aa469-155">y</span></span>    | <span data-ttu-id="aa469-156">in ingresso</span><span class="sxs-lookup"><span data-stu-id="aa469-156">in</span></span>          | <span data-ttu-id="aa469-157">uguale all'input x</span><span class="sxs-lookup"><span data-stu-id="aa469-157">same as input x</span></span>                                                                                                | <span data-ttu-id="aa469-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="aa469-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="aa469-159">le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="aa469-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="aa469-160">RET</span><span class="sxs-lookup"><span data-stu-id="aa469-160">ret</span></span>  | <span data-ttu-id="aa469-161">tipo restituito</span><span class="sxs-lookup"><span data-stu-id="aa469-161">return type</span></span> | <span data-ttu-id="aa469-162">uguale all'input x</span><span class="sxs-lookup"><span data-stu-id="aa469-162">same as input x</span></span>                                                                                                | <span data-ttu-id="aa469-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="aa469-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="aa469-164">le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="aa469-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa469-165">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="aa469-165">Minimum Shader Model</span></span>

<span data-ttu-id="aa469-166">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="aa469-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa469-167">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="aa469-167">Shader Model</span></span>                                                                       | <span data-ttu-id="aa469-168">Supportato</span><span class="sxs-lookup"><span data-stu-id="aa469-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="aa469-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="aa469-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="aa469-170">sì</span><span class="sxs-lookup"><span data-stu-id="aa469-170">yes</span></span>                         |
| [<span data-ttu-id="aa469-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa469-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="aa469-172">Sì (vs \_ 1 \_ e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="aa469-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="aa469-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa469-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa469-174">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="aa469-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="aa469-175">**Specifica funzionale DirectX**</span><span class="sxs-lookup"><span data-stu-id="aa469-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)