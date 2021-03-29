---
title: isinf (Corecrt \_ Math. h)
description: Determina se il valore specificato è infinito.
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- HLSL isinf
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4df738438d62d5a66dd3b08ad769d475df562d5f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235086"
---
# <a name="isinf"></a><span data-ttu-id="8a417-104">isinf</span><span class="sxs-lookup"><span data-stu-id="8a417-104">isinf</span></span>

<span data-ttu-id="8a417-105">Determina se il valore specificato è infinito.</span><span class="sxs-lookup"><span data-stu-id="8a417-105">Determines if the specified value is infinite.</span></span>



| <span data-ttu-id="8a417-106">isinf *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="8a417-106">*ret* isinf(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="8a417-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a417-107">Parameters</span></span>



| <span data-ttu-id="8a417-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a417-108">Item</span></span>                                                   | <span data-ttu-id="8a417-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a417-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8a417-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8a417-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8a417-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="8a417-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8a417-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a417-112">Return Value</span></span>

<span data-ttu-id="8a417-113">Restituisce un valore della stessa dimensione dell'input, con un valore impostato su **true** se il parametro *x* è + inf o-inf.</span><span class="sxs-lookup"><span data-stu-id="8a417-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is +INF or -INF.</span></span> <span data-ttu-id="8a417-114">In caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8a417-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="8a417-115">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="8a417-115">Type Description</span></span>



| <span data-ttu-id="8a417-116">Nome</span><span class="sxs-lookup"><span data-stu-id="8a417-116">Name</span></span>  | [<span data-ttu-id="8a417-117">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="8a417-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8a417-118">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="8a417-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8a417-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8a417-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="8a417-120">*x*</span><span class="sxs-lookup"><span data-stu-id="8a417-120">*x*</span></span>   | <span data-ttu-id="8a417-121">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="8a417-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8a417-122">**float**</span><span class="sxs-lookup"><span data-stu-id="8a417-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8a417-123">any</span><span class="sxs-lookup"><span data-stu-id="8a417-123">any</span></span>      |
| <span data-ttu-id="8a417-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="8a417-124">*ret*</span></span> | <span data-ttu-id="8a417-125">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="8a417-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8a417-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="8a417-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="8a417-127">come input</span><span class="sxs-lookup"><span data-stu-id="8a417-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8a417-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8a417-128">Minimum Shader Model</span></span>

<span data-ttu-id="8a417-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8a417-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8a417-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8a417-130">Shader Model</span></span>                                                                       | <span data-ttu-id="8a417-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="8a417-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="8a417-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="8a417-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8a417-133">sì</span><span class="sxs-lookup"><span data-stu-id="8a417-133">yes</span></span>                 |
| [<span data-ttu-id="8a417-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a417-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8a417-135">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="8a417-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8a417-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a417-136">Requirements</span></span>



| <span data-ttu-id="8a417-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a417-137">Requirement</span></span> | <span data-ttu-id="8a417-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8a417-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a417-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a417-139">Header</span></span><br/> | <dl> <span data-ttu-id="8a417-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a417-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a417-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a417-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a417-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8a417-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

