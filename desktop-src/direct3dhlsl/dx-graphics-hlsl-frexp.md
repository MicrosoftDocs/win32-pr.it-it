---
title: frexp (Corecrt \_ Math. h)
description: Restituisce mantissa ed esponente del valore a virgola mobile specificato.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- HLSL frexp
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969348"
---
# <a name="frexp"></a><span data-ttu-id="e1494-104">frexp</span><span class="sxs-lookup"><span data-stu-id="e1494-104">frexp</span></span>

<span data-ttu-id="e1494-105">Restituisce mantissa ed esponente del valore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="e1494-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="e1494-106">frexp *ret* (*x*, *Exp*)</span><span class="sxs-lookup"><span data-stu-id="e1494-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="e1494-107">Il valore restituito è mantissa e il valore restituito dal parametro *Exp* è l'esponente.</span><span class="sxs-lookup"><span data-stu-id="e1494-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1494-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1494-108">Parameters</span></span>



| <span data-ttu-id="e1494-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1494-109">Item</span></span>                                                         | <span data-ttu-id="e1494-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1494-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1494-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e1494-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="e1494-112">\[nel \] valore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="e1494-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="e1494-113">Se il parametro *x* è 0, questa funzione restituisce 0 sia per mantissa che per l'esponente.</span><span class="sxs-lookup"><span data-stu-id="e1494-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="e1494-114"><span id="exp"></span><span id="EXP"></span>*exp*</span><span class="sxs-lookup"><span data-stu-id="e1494-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="e1494-115">\[\]esponente restituito del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="e1494-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="e1494-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1494-116">Return Value</span></span>

<span data-ttu-id="e1494-117">Mantissa del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="e1494-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="e1494-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="e1494-118">Type Description</span></span>



| <span data-ttu-id="e1494-119">Nome</span><span class="sxs-lookup"><span data-stu-id="e1494-119">Name</span></span>  | [<span data-ttu-id="e1494-120">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="e1494-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e1494-121">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="e1494-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e1494-122">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e1494-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e1494-123">*x*</span><span class="sxs-lookup"><span data-stu-id="e1494-123">*x*</span></span>   | <span data-ttu-id="e1494-124">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="e1494-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e1494-125">**float**</span><span class="sxs-lookup"><span data-stu-id="e1494-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e1494-126">any</span><span class="sxs-lookup"><span data-stu-id="e1494-126">any</span></span>                            |
| <span data-ttu-id="e1494-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="e1494-127">*exp*</span></span> | <span data-ttu-id="e1494-128">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="e1494-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e1494-129">**float**</span><span class="sxs-lookup"><span data-stu-id="e1494-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e1494-130">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="e1494-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="e1494-131">*RET*</span><span class="sxs-lookup"><span data-stu-id="e1494-131">*ret*</span></span> | <span data-ttu-id="e1494-132">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="e1494-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e1494-133">**float**</span><span class="sxs-lookup"><span data-stu-id="e1494-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e1494-134">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="e1494-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e1494-135">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e1494-135">Minimum Shader Model</span></span>

<span data-ttu-id="e1494-136">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1494-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e1494-137">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e1494-137">Shader Model</span></span>                                                                       | <span data-ttu-id="e1494-138">Supportato</span><span class="sxs-lookup"><span data-stu-id="e1494-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e1494-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="e1494-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="e1494-140">sì</span><span class="sxs-lookup"><span data-stu-id="e1494-140">yes</span></span>                 |
| [<span data-ttu-id="e1494-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1494-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="e1494-142">Sì ( \_ solo PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="e1494-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="e1494-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1494-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e1494-144">no</span><span class="sxs-lookup"><span data-stu-id="e1494-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="e1494-145">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e1494-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e1494-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1494-146">Requirements</span></span>



| <span data-ttu-id="e1494-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1494-147">Requirement</span></span> | <span data-ttu-id="e1494-148">Valore</span><span class="sxs-lookup"><span data-stu-id="e1494-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1494-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1494-149">Header</span></span><br/> | <dl> <span data-ttu-id="e1494-150"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1494-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1494-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1494-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1494-152">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e1494-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

