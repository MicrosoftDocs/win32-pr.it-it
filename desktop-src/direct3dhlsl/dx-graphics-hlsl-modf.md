---
title: modf (Corecrt \_ Math. h)
description: Suddivide il valore x in parti frazionarie e intere, ognuna delle quali ha lo stesso segno di x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- HLSL modf
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079549e70414f8237fd33a5e263dd8f17dcb9e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969397"
---
# <a name="modf"></a><span data-ttu-id="57f78-104">modf</span><span class="sxs-lookup"><span data-stu-id="57f78-104">modf</span></span>

<span data-ttu-id="57f78-105">Suddivide il valore x in parti frazionarie e intere, ognuna delle quali ha lo stesso segno di x.</span><span class="sxs-lookup"><span data-stu-id="57f78-105">Splits the value x into fractional and integer parts, each of which has the same sign as x.</span></span>



| <span data-ttu-id="57f78-106">RET modf (x, out IP)</span><span class="sxs-lookup"><span data-stu-id="57f78-106">ret modf(x, out ip)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="57f78-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="57f78-107">Parameters</span></span>



| <span data-ttu-id="57f78-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="57f78-108">Item</span></span>                                                      | <span data-ttu-id="57f78-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57f78-109">Description</span></span>                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="57f78-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="57f78-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>    | <span data-ttu-id="57f78-111">\[nel \] valore di input x.</span><span class="sxs-lookup"><span data-stu-id="57f78-111">\[in\] The x input value.</span></span><br/>           |
| <span data-ttu-id="57f78-112"><span id="ip"></span><span id="IP"></span>*IP*</span><span class="sxs-lookup"><span data-stu-id="57f78-112"><span id="ip"></span><span id="IP"></span>*ip*</span></span><br/> | <span data-ttu-id="57f78-113">\[\]parte intera di *x*.</span><span class="sxs-lookup"><span data-stu-id="57f78-113">\[out\] The integer portion of *x*.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="57f78-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57f78-114">Return Value</span></span>

<span data-ttu-id="57f78-115">Parte della x con segno frazionario.</span><span class="sxs-lookup"><span data-stu-id="57f78-115">The signed-fractional portion of x.</span></span>

## <a name="type-description"></a><span data-ttu-id="57f78-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="57f78-116">Type Description</span></span>



| <span data-ttu-id="57f78-117">Nome</span><span class="sxs-lookup"><span data-stu-id="57f78-117">Name</span></span> | <span data-ttu-id="57f78-118">Ingresso/Uscita</span><span class="sxs-lookup"><span data-stu-id="57f78-118">In/Out</span></span> | [<span data-ttu-id="57f78-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="57f78-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="57f78-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="57f78-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="57f78-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="57f78-121">Size</span></span>                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="57f78-122">x</span><span class="sxs-lookup"><span data-stu-id="57f78-122">x</span></span>    | <span data-ttu-id="57f78-123">in ingresso</span><span class="sxs-lookup"><span data-stu-id="57f78-123">in</span></span>     | <span data-ttu-id="57f78-124">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="57f78-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="57f78-125">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="57f78-125">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="57f78-126">any</span><span class="sxs-lookup"><span data-stu-id="57f78-126">any</span></span>                          |
| <span data-ttu-id="57f78-127">IP</span><span class="sxs-lookup"><span data-stu-id="57f78-127">ip</span></span>   | <span data-ttu-id="57f78-128">in uscita</span><span class="sxs-lookup"><span data-stu-id="57f78-128">out</span></span>    | <span data-ttu-id="57f78-129">uguale all'input x</span><span class="sxs-lookup"><span data-stu-id="57f78-129">same as input x</span></span>                                                                                                | <span data-ttu-id="57f78-130">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="57f78-130">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="57f78-131">le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="57f78-131">same dimension(s) as input x</span></span> |
| <span data-ttu-id="57f78-132">RET</span><span class="sxs-lookup"><span data-stu-id="57f78-132">ret</span></span>  | <span data-ttu-id="57f78-133">in uscita</span><span class="sxs-lookup"><span data-stu-id="57f78-133">out</span></span>    | <span data-ttu-id="57f78-134">uguale all'input x</span><span class="sxs-lookup"><span data-stu-id="57f78-134">same as input x</span></span>                                                                                                | <span data-ttu-id="57f78-135">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="57f78-135">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="57f78-136">le stesse dimensioni di input x</span><span class="sxs-lookup"><span data-stu-id="57f78-136">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="57f78-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="57f78-137">Minimum Shader Model</span></span>

<span data-ttu-id="57f78-138">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="57f78-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="57f78-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="57f78-139">Shader Model</span></span>                                                                       | <span data-ttu-id="57f78-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="57f78-140">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="57f78-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="57f78-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="57f78-142">sì</span><span class="sxs-lookup"><span data-stu-id="57f78-142">yes</span></span>                 |
| [<span data-ttu-id="57f78-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57f78-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="57f78-144">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="57f78-144">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="57f78-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57f78-145">Requirements</span></span>



| <span data-ttu-id="57f78-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="57f78-146">Requirement</span></span> | <span data-ttu-id="57f78-147">Valore</span><span class="sxs-lookup"><span data-stu-id="57f78-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="57f78-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57f78-148">Header</span></span><br/> | <dl> <span data-ttu-id="57f78-149"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="57f78-149"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f78-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57f78-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f78-151">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="57f78-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

