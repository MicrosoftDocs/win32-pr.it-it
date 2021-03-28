---
title: semifinito (Corecrt \_ Math. h)
description: Determina se il valore a virgola mobile specificato è finito.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- HLSL finito
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995876"
---
# <a name="isfinite"></a><span data-ttu-id="f05d0-104">isFinite</span><span class="sxs-lookup"><span data-stu-id="f05d0-104">isfinite</span></span>

<span data-ttu-id="f05d0-105">Determina se il valore a virgola mobile specificato è finito.</span><span class="sxs-lookup"><span data-stu-id="f05d0-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="f05d0-106">*ret* finito (*x*)</span><span class="sxs-lookup"><span data-stu-id="f05d0-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="f05d0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f05d0-107">Parameters</span></span>



| <span data-ttu-id="f05d0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f05d0-108">Item</span></span>                                                   | <span data-ttu-id="f05d0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f05d0-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f05d0-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f05d0-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f05d0-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f05d0-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f05d0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f05d0-112">Return Value</span></span>

<span data-ttu-id="f05d0-113">Restituisce un valore della stessa dimensione dell'input, con un valore impostato su **true** se il parametro *x* è finito; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f05d0-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="f05d0-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="f05d0-114">Type Description</span></span>



| <span data-ttu-id="f05d0-115">Nome</span><span class="sxs-lookup"><span data-stu-id="f05d0-115">Name</span></span>  | [<span data-ttu-id="f05d0-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="f05d0-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f05d0-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="f05d0-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f05d0-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f05d0-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="f05d0-119">*x*</span><span class="sxs-lookup"><span data-stu-id="f05d0-119">*x*</span></span>   | <span data-ttu-id="f05d0-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="f05d0-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f05d0-121">**float**</span><span class="sxs-lookup"><span data-stu-id="f05d0-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f05d0-122">any</span><span class="sxs-lookup"><span data-stu-id="f05d0-122">any</span></span>      |
| <span data-ttu-id="f05d0-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="f05d0-123">*ret*</span></span> | <span data-ttu-id="f05d0-124">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="f05d0-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f05d0-125">**bool**</span><span class="sxs-lookup"><span data-stu-id="f05d0-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="f05d0-126">come input</span><span class="sxs-lookup"><span data-stu-id="f05d0-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f05d0-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f05d0-127">Minimum Shader Model</span></span>

<span data-ttu-id="f05d0-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f05d0-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f05d0-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f05d0-129">Shader Model</span></span>                                                                       | <span data-ttu-id="f05d0-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="f05d0-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f05d0-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="f05d0-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f05d0-132">sì</span><span class="sxs-lookup"><span data-stu-id="f05d0-132">yes</span></span>                 |
| [<span data-ttu-id="f05d0-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f05d0-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f05d0-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="f05d0-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f05d0-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f05d0-135">Requirements</span></span>



| <span data-ttu-id="f05d0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05d0-136">Requirement</span></span> | <span data-ttu-id="f05d0-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f05d0-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f05d0-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f05d0-138">Header</span></span><br/> | <dl> <span data-ttu-id="f05d0-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05d0-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f05d0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f05d0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05d0-141">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f05d0-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

