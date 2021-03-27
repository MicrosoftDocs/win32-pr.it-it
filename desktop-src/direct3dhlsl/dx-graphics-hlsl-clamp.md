---
title: morsetto
description: Consente di bloccare il valore specificato nell'intervallo minimo e massimo specificato.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- blocca HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729543"
---
# <a name="clamp"></a><span data-ttu-id="d1e10-104">morsetto</span><span class="sxs-lookup"><span data-stu-id="d1e10-104">clamp</span></span>

<span data-ttu-id="d1e10-105">Consente di bloccare il valore specificato nell'intervallo minimo e massimo specificato.</span><span class="sxs-lookup"><span data-stu-id="d1e10-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="d1e10-106">morsetto *ret* (*x*, *min*, *Max*)</span><span class="sxs-lookup"><span data-stu-id="d1e10-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d1e10-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1e10-107">Parameters</span></span>



| <span data-ttu-id="d1e10-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d1e10-108">Item</span></span>                                                         | <span data-ttu-id="d1e10-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1e10-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="d1e10-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="d1e10-111">\[in \] un valore da bloccare.</span><span class="sxs-lookup"><span data-stu-id="d1e10-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="d1e10-112"><span id="min"></span><span id="MIN"></span>*min*</span><span class="sxs-lookup"><span data-stu-id="d1e10-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="d1e10-113">\[nell' \] intervallo minimo specificato.</span><span class="sxs-lookup"><span data-stu-id="d1e10-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="d1e10-114"><span id="max"></span><span id="MAX"></span>*Max*</span><span class="sxs-lookup"><span data-stu-id="d1e10-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="d1e10-115">\[nell' \] intervallo massimo specificato.</span><span class="sxs-lookup"><span data-stu-id="d1e10-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d1e10-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1e10-116">Return Value</span></span>

<span data-ttu-id="d1e10-117">Valore premuto per il parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="d1e10-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e10-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1e10-118">Remarks</span></span>

<span data-ttu-id="d1e10-119">Per i valori di-INF o INF, il morsetto si comporterà come previsto.</span><span class="sxs-lookup"><span data-stu-id="d1e10-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="d1e10-120">Per i valori NaN, tuttavia, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="d1e10-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="d1e10-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="d1e10-121">Type Description</span></span>



| <span data-ttu-id="d1e10-122">Nome</span><span class="sxs-lookup"><span data-stu-id="d1e10-122">Name</span></span>  | [<span data-ttu-id="d1e10-123">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="d1e10-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d1e10-124">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="d1e10-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="d1e10-125">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d1e10-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d1e10-126">*x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-126">*x*</span></span>   | <span data-ttu-id="d1e10-127">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="d1e10-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="d1e10-128">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d1e10-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d1e10-129">any</span><span class="sxs-lookup"><span data-stu-id="d1e10-129">any</span></span>                            |
| <span data-ttu-id="d1e10-130">*min*</span><span class="sxs-lookup"><span data-stu-id="d1e10-130">*min*</span></span> | <span data-ttu-id="d1e10-131">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="d1e10-132">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d1e10-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d1e10-133">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d1e10-134">*max*</span><span class="sxs-lookup"><span data-stu-id="d1e10-134">*max*</span></span> | <span data-ttu-id="d1e10-135">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="d1e10-136">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d1e10-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d1e10-137">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d1e10-138">*RET*</span><span class="sxs-lookup"><span data-stu-id="d1e10-138">*ret*</span></span> | <span data-ttu-id="d1e10-139">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="d1e10-140">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d1e10-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d1e10-141">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="d1e10-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d1e10-142">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d1e10-142">Minimum Shader Model</span></span>

<span data-ttu-id="d1e10-143">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1e10-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d1e10-144">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d1e10-144">Shader Model</span></span>                                                                       | <span data-ttu-id="d1e10-145">Supportato</span><span class="sxs-lookup"><span data-stu-id="d1e10-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="d1e10-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="d1e10-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d1e10-147">sì</span><span class="sxs-lookup"><span data-stu-id="d1e10-147">yes</span></span>                   |
| [<span data-ttu-id="d1e10-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d1e10-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d1e10-149">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d1e10-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d1e10-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1e10-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e10-151">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d1e10-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

