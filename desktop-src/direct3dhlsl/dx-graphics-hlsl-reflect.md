---
title: riflettere
description: Restituisce un vettore di reflection utilizzando un raggio di evento imprevisto e una normale della superficie.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- riflette HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729927"
---
# <a name="reflect"></a><span data-ttu-id="15e46-104">riflettere</span><span class="sxs-lookup"><span data-stu-id="15e46-104">reflect</span></span>

<span data-ttu-id="15e46-105">Restituisce un vettore di reflection utilizzando un raggio di evento imprevisto e una normale della superficie.</span><span class="sxs-lookup"><span data-stu-id="15e46-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="15e46-106">reflection *ret* (*i*, *n*)</span><span class="sxs-lookup"><span data-stu-id="15e46-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="15e46-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="15e46-107">Parameters</span></span>



| <span data-ttu-id="15e46-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="15e46-108">Item</span></span>                                                   | <span data-ttu-id="15e46-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15e46-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15e46-110"><span id="i"></span><span id="I"></span>*i*</span><span class="sxs-lookup"><span data-stu-id="15e46-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="15e46-111">\[in \] un vettore di evento imprevisto a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="15e46-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="15e46-112"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="15e46-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="15e46-113">\[in \] un vettore a virgola mobile normale.</span><span class="sxs-lookup"><span data-stu-id="15e46-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="15e46-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15e46-114">Return Value</span></span>

<span data-ttu-id="15e46-115">Vettore di Reflection A virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="15e46-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="15e46-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="15e46-116">Remarks</span></span>

<span data-ttu-id="15e46-117">Questa funzione calcola il vettore di Reflection usando la formula seguente: v = i-2 \* n \* dot (i n).</span><span class="sxs-lookup"><span data-stu-id="15e46-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="15e46-118">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="15e46-118">Type Description</span></span>



| <span data-ttu-id="15e46-119">Nome</span><span class="sxs-lookup"><span data-stu-id="15e46-119">Name</span></span>  | [<span data-ttu-id="15e46-120">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="15e46-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="15e46-121">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="15e46-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="15e46-122">Dimensione</span><span class="sxs-lookup"><span data-stu-id="15e46-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="15e46-123">*i*</span><span class="sxs-lookup"><span data-stu-id="15e46-123">*i*</span></span>   | [<span data-ttu-id="15e46-124">**vettore**</span><span class="sxs-lookup"><span data-stu-id="15e46-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="15e46-125">**float**</span><span class="sxs-lookup"><span data-stu-id="15e46-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="15e46-126">any</span><span class="sxs-lookup"><span data-stu-id="15e46-126">any</span></span>                            |
| <span data-ttu-id="15e46-127">*n*</span><span class="sxs-lookup"><span data-stu-id="15e46-127">*n*</span></span>   | [<span data-ttu-id="15e46-128">**vettore**</span><span class="sxs-lookup"><span data-stu-id="15e46-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="15e46-129">**float**</span><span class="sxs-lookup"><span data-stu-id="15e46-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="15e46-130">le stesse dimensioni di input *i*</span><span class="sxs-lookup"><span data-stu-id="15e46-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="15e46-131">*RET*</span><span class="sxs-lookup"><span data-stu-id="15e46-131">*ret*</span></span> | [<span data-ttu-id="15e46-132">**vettore**</span><span class="sxs-lookup"><span data-stu-id="15e46-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="15e46-133">**float**</span><span class="sxs-lookup"><span data-stu-id="15e46-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="15e46-134">le stesse dimensioni di input *i*</span><span class="sxs-lookup"><span data-stu-id="15e46-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="15e46-135">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="15e46-135">Minimum Shader Model</span></span>

<span data-ttu-id="15e46-136">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="15e46-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="15e46-137">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="15e46-137">Shader Model</span></span>                                                                       | <span data-ttu-id="15e46-138">Supportato</span><span class="sxs-lookup"><span data-stu-id="15e46-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="15e46-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="15e46-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="15e46-140">sì</span><span class="sxs-lookup"><span data-stu-id="15e46-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="15e46-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15e46-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e46-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="15e46-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

