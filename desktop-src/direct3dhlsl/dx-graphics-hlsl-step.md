---
title: step
description: Confronta due valori, restituendo 0 o 1 in base al valore maggiore.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- passaggio HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729527"
---
# <a name="step"></a><span data-ttu-id="0b04e-104">step</span><span class="sxs-lookup"><span data-stu-id="0b04e-104">step</span></span>

<span data-ttu-id="0b04e-105">Confronta due valori, restituendo 0 o 1 in base al valore maggiore.</span><span class="sxs-lookup"><span data-stu-id="0b04e-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="0b04e-106">passaggio *ret* (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="0b04e-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="0b04e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b04e-107">Parameters</span></span>



| <span data-ttu-id="0b04e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0b04e-108">Item</span></span>                                                   | <span data-ttu-id="0b04e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b04e-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0b04e-110"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="0b04e-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="0b04e-111">\[nel \] primo valore a virgola mobile da confrontare.</span><span class="sxs-lookup"><span data-stu-id="0b04e-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="0b04e-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0b04e-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0b04e-113">\[nel \] secondo valore a virgola mobile da confrontare.</span><span class="sxs-lookup"><span data-stu-id="0b04e-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0b04e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b04e-114">Return Value</span></span>

<span data-ttu-id="0b04e-115">1 se il parametro *x* è maggiore o uguale al parametro *y* ; in caso contrario, 0.</span><span class="sxs-lookup"><span data-stu-id="0b04e-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b04e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b04e-116">Remarks</span></span>

<span data-ttu-id="0b04e-117">Questa funzione utilizza la formula seguente: (*x*  >=  *y*)?</span><span class="sxs-lookup"><span data-stu-id="0b04e-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="0b04e-118">1:0.</span><span class="sxs-lookup"><span data-stu-id="0b04e-118">1 : 0.</span></span> <span data-ttu-id="0b04e-119">La funzione restituisce 0 o 1 a seconda che il parametro *x* sia maggiore o uguale al parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="0b04e-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="0b04e-120">Per calcolare un'interpolazione uniforme tra 0 e 1, usare la funzione intrinseca [**SmoothStep**](dx-graphics-hlsl-smoothstep.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="0b04e-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="0b04e-121">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="0b04e-121">Type Description</span></span>



| <span data-ttu-id="0b04e-122">Nome</span><span class="sxs-lookup"><span data-stu-id="0b04e-122">Name</span></span>  | [<span data-ttu-id="0b04e-123">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="0b04e-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0b04e-124">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="0b04e-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0b04e-125">Dimensione</span><span class="sxs-lookup"><span data-stu-id="0b04e-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0b04e-126">*y*</span><span class="sxs-lookup"><span data-stu-id="0b04e-126">*y*</span></span>   | <span data-ttu-id="0b04e-127">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="0b04e-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0b04e-128">**float**</span><span class="sxs-lookup"><span data-stu-id="0b04e-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b04e-129">any</span><span class="sxs-lookup"><span data-stu-id="0b04e-129">any</span></span>                            |
| <span data-ttu-id="0b04e-130">*x*</span><span class="sxs-lookup"><span data-stu-id="0b04e-130">*x*</span></span>   | <span data-ttu-id="0b04e-131">uguale all'input *y*</span><span class="sxs-lookup"><span data-stu-id="0b04e-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="0b04e-132">**float**</span><span class="sxs-lookup"><span data-stu-id="0b04e-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b04e-133">le stesse dimensioni di input *y*</span><span class="sxs-lookup"><span data-stu-id="0b04e-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="0b04e-134">*RET*</span><span class="sxs-lookup"><span data-stu-id="0b04e-134">*ret*</span></span> | <span data-ttu-id="0b04e-135">uguale all'input *y*</span><span class="sxs-lookup"><span data-stu-id="0b04e-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="0b04e-136">**float**</span><span class="sxs-lookup"><span data-stu-id="0b04e-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b04e-137">le stesse dimensioni di input *y*</span><span class="sxs-lookup"><span data-stu-id="0b04e-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b04e-138">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="0b04e-138">Minimum Shader Model</span></span>

<span data-ttu-id="0b04e-139">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b04e-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b04e-140">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="0b04e-140">Shader Model</span></span>                                                                       | <span data-ttu-id="0b04e-141">Supportato</span><span class="sxs-lookup"><span data-stu-id="0b04e-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="0b04e-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="0b04e-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0b04e-143">sì</span><span class="sxs-lookup"><span data-stu-id="0b04e-143">yes</span></span>                         |
| [<span data-ttu-id="0b04e-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b04e-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0b04e-145">Sì (vs \_ 1 \_ e PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="0b04e-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0b04e-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b04e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b04e-147">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0b04e-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

