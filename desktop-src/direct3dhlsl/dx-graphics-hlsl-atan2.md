---
title: atan2 (Corecrt \_ Math. h)
description: Restituisce l'arcotangente di due valori (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- HLSL atan2
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235008"
---
# <a name="atan2"></a><span data-ttu-id="bbe8e-104">atan2</span><span class="sxs-lookup"><span data-stu-id="bbe8e-104">atan2</span></span>

<span data-ttu-id="bbe8e-105">Restituisce l'arcotangente di due valori (x, y).</span><span class="sxs-lookup"><span data-stu-id="bbe8e-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="bbe8e-106">atan2 *ret* (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="bbe8e-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="bbe8e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bbe8e-107">Parameters</span></span>



| <span data-ttu-id="bbe8e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bbe8e-108">Item</span></span>                                                   | <span data-ttu-id="bbe8e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbe8e-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bbe8e-110"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="bbe8e-111">\[nel \] valore y.</span><span class="sxs-lookup"><span data-stu-id="bbe8e-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="bbe8e-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bbe8e-113">\[nel \] valore x.</span><span class="sxs-lookup"><span data-stu-id="bbe8e-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bbe8e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bbe8e-114">Return Value</span></span>

<span data-ttu-id="bbe8e-115">Arcotangente di (y, x).</span><span class="sxs-lookup"><span data-stu-id="bbe8e-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe8e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbe8e-116">Remarks</span></span>

<span data-ttu-id="bbe8e-117">I segni dei parametri *x* e *y* vengono utilizzati per determinare il quadrante dei valori restituiti nell'intervallo compreso tra-π e π.</span><span class="sxs-lookup"><span data-stu-id="bbe8e-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="bbe8e-118">La funzione intrinseca HLSL **Atan2** è ben definita per ogni punto diverso dall'origine, anche se *y* è uguale a 0 e *x* non è uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="bbe8e-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="bbe8e-119">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="bbe8e-119">Type Description</span></span>



| <span data-ttu-id="bbe8e-120">Nome</span><span class="sxs-lookup"><span data-stu-id="bbe8e-120">Name</span></span>  | [<span data-ttu-id="bbe8e-121">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bbe8e-122">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bbe8e-123">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bbe8e-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bbe8e-124">*y*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-124">*y*</span></span>   | <span data-ttu-id="bbe8e-125">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bbe8e-126">**float**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bbe8e-127">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="bbe8e-128">*x*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-128">*x*</span></span>   | <span data-ttu-id="bbe8e-129">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bbe8e-130">**float**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bbe8e-131">any</span><span class="sxs-lookup"><span data-stu-id="bbe8e-131">any</span></span>                            |
| <span data-ttu-id="bbe8e-132">*RET*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-132">*ret*</span></span> | <span data-ttu-id="bbe8e-133">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bbe8e-134">**float**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bbe8e-135">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="bbe8e-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bbe8e-136">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bbe8e-136">Minimum Shader Model</span></span>

<span data-ttu-id="bbe8e-137">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bbe8e-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bbe8e-138">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bbe8e-138">Shader Model</span></span>                                                                       | <span data-ttu-id="bbe8e-139">Supportato</span><span class="sxs-lookup"><span data-stu-id="bbe8e-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bbe8e-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="bbe8e-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bbe8e-141">sì</span><span class="sxs-lookup"><span data-stu-id="bbe8e-141">yes</span></span>       |
| [<span data-ttu-id="bbe8e-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bbe8e-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bbe8e-143">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bbe8e-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="bbe8e-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbe8e-144">Requirements</span></span>



| <span data-ttu-id="bbe8e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe8e-145">Requirement</span></span> | <span data-ttu-id="bbe8e-146">Valore</span><span class="sxs-lookup"><span data-stu-id="bbe8e-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe8e-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbe8e-147">Header</span></span><br/> | <dl> <span data-ttu-id="bbe8e-148"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe8e-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe8e-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbe8e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe8e-150">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bbe8e-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

