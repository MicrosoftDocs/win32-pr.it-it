---
title: SinCos
description: Restituisce il seno e il coseno di x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- HLSL SinCos
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993541"
---
# <a name="sincos"></a><span data-ttu-id="e4a11-104">SinCos</span><span class="sxs-lookup"><span data-stu-id="e4a11-104">sincos</span></span>

<span data-ttu-id="e4a11-105">Restituisce il seno e il coseno di x.</span><span class="sxs-lookup"><span data-stu-id="e4a11-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="e4a11-106">SinCos (*x*, out *s*, out *c*)</span><span class="sxs-lookup"><span data-stu-id="e4a11-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="e4a11-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4a11-107">Parameters</span></span>



| <span data-ttu-id="e4a11-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e4a11-108">Item</span></span>                                                   | <span data-ttu-id="e4a11-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4a11-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="e4a11-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e4a11-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e4a11-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="e4a11-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="e4a11-112"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="e4a11-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="e4a11-113">\[out \] restituisce il seno di x.</span><span class="sxs-lookup"><span data-stu-id="e4a11-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="e4a11-114"><span id="c"></span><span id="C"></span>*c*</span><span class="sxs-lookup"><span data-stu-id="e4a11-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="e4a11-115">\[out \] restituisce il coseno di x.</span><span class="sxs-lookup"><span data-stu-id="e4a11-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="e4a11-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4a11-116">Return Value</span></span>

<span data-ttu-id="e4a11-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="e4a11-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="e4a11-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="e4a11-118">Type Description</span></span>



| <span data-ttu-id="e4a11-119">Nome</span><span class="sxs-lookup"><span data-stu-id="e4a11-119">Name</span></span> | [<span data-ttu-id="e4a11-120">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="e4a11-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e4a11-121">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="e4a11-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e4a11-122">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e4a11-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e4a11-123">*x*</span><span class="sxs-lookup"><span data-stu-id="e4a11-123">*x*</span></span>  | <span data-ttu-id="e4a11-124">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="e4a11-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e4a11-125">**float**</span><span class="sxs-lookup"><span data-stu-id="e4a11-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e4a11-126">any</span><span class="sxs-lookup"><span data-stu-id="e4a11-126">any</span></span>                            |
| <span data-ttu-id="e4a11-127">*s*</span><span class="sxs-lookup"><span data-stu-id="e4a11-127">*s*</span></span>  | <span data-ttu-id="e4a11-128">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="e4a11-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e4a11-129">**float**</span><span class="sxs-lookup"><span data-stu-id="e4a11-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e4a11-130">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="e4a11-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="e4a11-131">c</span><span class="sxs-lookup"><span data-stu-id="e4a11-131">c</span></span>    | <span data-ttu-id="e4a11-132">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="e4a11-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e4a11-133">**float**</span><span class="sxs-lookup"><span data-stu-id="e4a11-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e4a11-134">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="e4a11-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e4a11-135">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e4a11-135">Minimum Shader Model</span></span>

<span data-ttu-id="e4a11-136">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4a11-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e4a11-137">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e4a11-137">Shader Model</span></span>                                                                       | <span data-ttu-id="e4a11-138">Supportato</span><span class="sxs-lookup"><span data-stu-id="e4a11-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e4a11-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="e4a11-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e4a11-140">sì</span><span class="sxs-lookup"><span data-stu-id="e4a11-140">yes</span></span>                 |
| [<span data-ttu-id="e4a11-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4a11-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e4a11-142">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="e4a11-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e4a11-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4a11-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a11-144">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e4a11-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

