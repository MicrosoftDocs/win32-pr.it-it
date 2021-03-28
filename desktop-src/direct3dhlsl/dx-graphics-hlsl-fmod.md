---
title: fmod (Corecrt \_ Math. h)
description: Restituisce il resto a virgola mobile di x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- HLSL fmod
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354739"
---
# <a name="fmod"></a><span data-ttu-id="5613b-104">fmod</span><span class="sxs-lookup"><span data-stu-id="5613b-104">fmod</span></span>

<span data-ttu-id="5613b-105">Restituisce il resto a virgola mobile di x/y.</span><span class="sxs-lookup"><span data-stu-id="5613b-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="5613b-106">fmod *ret* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="5613b-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="5613b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5613b-107">Parameters</span></span>



| <span data-ttu-id="5613b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5613b-108">Item</span></span>                                                   | <span data-ttu-id="5613b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5613b-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="5613b-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="5613b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5613b-111">\[nel \] dividendo a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="5613b-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="5613b-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="5613b-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="5613b-113">\[nel \] divisore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="5613b-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="5613b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5613b-114">Return Value</span></span>

<span data-ttu-id="5613b-115">Resto a virgola mobile del parametro *x* diviso per il parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="5613b-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="5613b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5613b-116">Remarks</span></span>

<span data-ttu-id="5613b-117">Il resto a virgola mobile viene calcolato in modo tale che x = i \* y + f, dove i è un numero intero, f ha lo stesso segno di x e il valore assoluto di f è minore del valore assoluto di y.</span><span class="sxs-lookup"><span data-stu-id="5613b-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="5613b-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="5613b-118">Type Description</span></span>



| <span data-ttu-id="5613b-119">Nome</span><span class="sxs-lookup"><span data-stu-id="5613b-119">Name</span></span>  | [<span data-ttu-id="5613b-120">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="5613b-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5613b-121">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="5613b-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5613b-122">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5613b-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5613b-123">*x*</span><span class="sxs-lookup"><span data-stu-id="5613b-123">*x*</span></span>   | <span data-ttu-id="5613b-124">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="5613b-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="5613b-125">**float**</span><span class="sxs-lookup"><span data-stu-id="5613b-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5613b-126">any</span><span class="sxs-lookup"><span data-stu-id="5613b-126">any</span></span>                            |
| <span data-ttu-id="5613b-127">*y*</span><span class="sxs-lookup"><span data-stu-id="5613b-127">*y*</span></span>   | <span data-ttu-id="5613b-128">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="5613b-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5613b-129">**float**</span><span class="sxs-lookup"><span data-stu-id="5613b-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5613b-130">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="5613b-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="5613b-131">*RET*</span><span class="sxs-lookup"><span data-stu-id="5613b-131">*ret*</span></span> | <span data-ttu-id="5613b-132">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="5613b-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5613b-133">**float**</span><span class="sxs-lookup"><span data-stu-id="5613b-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5613b-134">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="5613b-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5613b-135">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5613b-135">Minimum Shader Model</span></span>

<span data-ttu-id="5613b-136">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5613b-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5613b-137">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5613b-137">Shader Model</span></span>                                                                       | <span data-ttu-id="5613b-138">Supportato</span><span class="sxs-lookup"><span data-stu-id="5613b-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5613b-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="5613b-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5613b-140">sì</span><span class="sxs-lookup"><span data-stu-id="5613b-140">yes</span></span>       |
| [<span data-ttu-id="5613b-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5613b-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5613b-142">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5613b-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="5613b-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5613b-143">Requirements</span></span>



| <span data-ttu-id="5613b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5613b-144">Requirement</span></span> | <span data-ttu-id="5613b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="5613b-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5613b-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5613b-146">Header</span></span><br/> | <dl> <span data-ttu-id="5613b-147"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5613b-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5613b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5613b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5613b-149">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5613b-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

