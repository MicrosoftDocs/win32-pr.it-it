---
title: Round (Corecrt \_ Math. h)
description: Arrotonda il valore specificato all'intero più vicino.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- Round HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969396"
---
# <a name="round"></a><span data-ttu-id="11b70-104">round</span><span class="sxs-lookup"><span data-stu-id="11b70-104">round</span></span>

<span data-ttu-id="11b70-105">Arrotonda il valore specificato all'intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="11b70-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="11b70-106">La metà dei casi viene arrotondata al pari più vicino.</span><span class="sxs-lookup"><span data-stu-id="11b70-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="11b70-107">Round *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="11b70-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="11b70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="11b70-108">Parameters</span></span>



| <span data-ttu-id="11b70-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="11b70-109">Item</span></span>                                                   | <span data-ttu-id="11b70-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11b70-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="11b70-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="11b70-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="11b70-112">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="11b70-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="11b70-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11b70-113">Return Value</span></span>

<span data-ttu-id="11b70-114">Il parametro *x* , arrotondato all'intero più vicino all'interno di un tipo a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="11b70-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="11b70-115">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="11b70-115">Type Description</span></span>



| <span data-ttu-id="11b70-116">Nome</span><span class="sxs-lookup"><span data-stu-id="11b70-116">Name</span></span>  | [<span data-ttu-id="11b70-117">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="11b70-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="11b70-118">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="11b70-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="11b70-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="11b70-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="11b70-120">*x*</span><span class="sxs-lookup"><span data-stu-id="11b70-120">*x*</span></span>   | <span data-ttu-id="11b70-121">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="11b70-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="11b70-122">**float**</span><span class="sxs-lookup"><span data-stu-id="11b70-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="11b70-123">any</span><span class="sxs-lookup"><span data-stu-id="11b70-123">any</span></span>                            |
| <span data-ttu-id="11b70-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="11b70-124">*ret*</span></span> | <span data-ttu-id="11b70-125">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="11b70-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="11b70-126">**float**</span><span class="sxs-lookup"><span data-stu-id="11b70-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="11b70-127">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="11b70-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11b70-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="11b70-128">Minimum Shader Model</span></span>

<span data-ttu-id="11b70-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="11b70-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="11b70-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="11b70-130">Shader Model</span></span>                                                                       | <span data-ttu-id="11b70-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="11b70-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="11b70-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="11b70-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="11b70-133">sì</span><span class="sxs-lookup"><span data-stu-id="11b70-133">yes</span></span>                 |
| [<span data-ttu-id="11b70-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11b70-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="11b70-135">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="11b70-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="11b70-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11b70-136">Requirements</span></span>



| <span data-ttu-id="11b70-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="11b70-137">Requirement</span></span> | <span data-ttu-id="11b70-138">Valore</span><span class="sxs-lookup"><span data-stu-id="11b70-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="11b70-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11b70-139">Header</span></span><br/> | <dl> <span data-ttu-id="11b70-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="11b70-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11b70-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11b70-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b70-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="11b70-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

