---
title: ldexp (Corecrt \_ Math. h)
description: Restituisce il risultato della moltiplicazione del valore specificato per due, elevato alla potenza dell'esponente specificato.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- HLSL ldexp
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886297"
---
# <a name="ldexp"></a><span data-ttu-id="2c325-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="2c325-104">ldexp</span></span>

<span data-ttu-id="2c325-105">Restituisce il risultato della moltiplicazione del valore specificato per due, elevato alla potenza dell'esponente specificato.</span><span class="sxs-lookup"><span data-stu-id="2c325-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="2c325-106">ldexp *ret* (*x*, *Exp*)</span><span class="sxs-lookup"><span data-stu-id="2c325-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="2c325-107">Questa funzione usa la formula seguente: *x* \* 2 <sup>Exp</sup></span><span class="sxs-lookup"><span data-stu-id="2c325-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="2c325-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c325-108">Parameters</span></span>



| <span data-ttu-id="2c325-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c325-109">Item</span></span>                                                         | <span data-ttu-id="2c325-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c325-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="2c325-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="2c325-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="2c325-112">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="2c325-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="2c325-113"><span id="exp"></span><span id="EXP"></span>*exp*</span><span class="sxs-lookup"><span data-stu-id="2c325-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="2c325-114">\[nell' \] esponente specificato.</span><span class="sxs-lookup"><span data-stu-id="2c325-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="2c325-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c325-115">Return Value</span></span>

<span data-ttu-id="2c325-116">Risultato della moltiplicazione del parametro *x* per due, elevato alla potenza del parametro *Exp* .</span><span class="sxs-lookup"><span data-stu-id="2c325-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="2c325-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="2c325-117">Type Description</span></span>



| <span data-ttu-id="2c325-118">Nome</span><span class="sxs-lookup"><span data-stu-id="2c325-118">Name</span></span>  | [<span data-ttu-id="2c325-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="2c325-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2c325-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="2c325-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2c325-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2c325-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="2c325-122">*x*</span><span class="sxs-lookup"><span data-stu-id="2c325-122">*x*</span></span>   | <span data-ttu-id="2c325-123">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="2c325-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2c325-124">**float**</span><span class="sxs-lookup"><span data-stu-id="2c325-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2c325-125">any</span><span class="sxs-lookup"><span data-stu-id="2c325-125">any</span></span>                            |
| <span data-ttu-id="2c325-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="2c325-126">*exp*</span></span> | <span data-ttu-id="2c325-127">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="2c325-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2c325-128">**float**</span><span class="sxs-lookup"><span data-stu-id="2c325-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2c325-129">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="2c325-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="2c325-130">*RET*</span><span class="sxs-lookup"><span data-stu-id="2c325-130">*ret*</span></span> | <span data-ttu-id="2c325-131">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="2c325-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="2c325-132">**float**</span><span class="sxs-lookup"><span data-stu-id="2c325-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="2c325-133">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="2c325-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c325-134">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="2c325-134">Minimum Shader Model</span></span>

<span data-ttu-id="2c325-135">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c325-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2c325-136">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="2c325-136">Shader Model</span></span>                                                                       | <span data-ttu-id="2c325-137">Supportato</span><span class="sxs-lookup"><span data-stu-id="2c325-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="2c325-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="2c325-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="2c325-139">sì</span><span class="sxs-lookup"><span data-stu-id="2c325-139">yes</span></span>                 |
| [<span data-ttu-id="2c325-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c325-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="2c325-141">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="2c325-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2c325-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c325-142">Requirements</span></span>



| <span data-ttu-id="2c325-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c325-143">Requirement</span></span> | <span data-ttu-id="2c325-144">Valore</span><span class="sxs-lookup"><span data-stu-id="2c325-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c325-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c325-145">Header</span></span><br/> | <dl> <span data-ttu-id="2c325-146"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c325-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c325-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c325-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c325-148">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="2c325-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

