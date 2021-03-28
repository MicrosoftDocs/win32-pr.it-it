---
title: log2 (Corecrt \_ Math. h)
description: Restituisce il logaritmo in base 2 del valore specificato.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- HLSL log2
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969500"
---
# <a name="log2"></a><span data-ttu-id="e20ce-104">log2</span><span class="sxs-lookup"><span data-stu-id="e20ce-104">log2</span></span>

<span data-ttu-id="e20ce-105">Restituisce il logaritmo in base 2 del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e20ce-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="e20ce-106">log2 *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="e20ce-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="e20ce-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e20ce-107">Parameters</span></span>



| <span data-ttu-id="e20ce-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e20ce-108">Item</span></span>                                                   | <span data-ttu-id="e20ce-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e20ce-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e20ce-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e20ce-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e20ce-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e20ce-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e20ce-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e20ce-112">Return Value</span></span>

<span data-ttu-id="e20ce-113">Logaritmo in base 2 del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="e20ce-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="e20ce-114">Se il parametro *x* è negativo, la funzione restituisce un valore indefinito.</span><span class="sxs-lookup"><span data-stu-id="e20ce-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="e20ce-115">Se il parametro *x* è 0, questa funzione restituisce + inf.</span><span class="sxs-lookup"><span data-stu-id="e20ce-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="e20ce-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="e20ce-116">Type Description</span></span>



| <span data-ttu-id="e20ce-117">Nome</span><span class="sxs-lookup"><span data-stu-id="e20ce-117">Name</span></span>  | [<span data-ttu-id="e20ce-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="e20ce-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="e20ce-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="e20ce-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e20ce-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e20ce-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="e20ce-121">*x*</span><span class="sxs-lookup"><span data-stu-id="e20ce-121">*x*</span></span>   | <span data-ttu-id="e20ce-122">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="e20ce-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="e20ce-123">**float**</span><span class="sxs-lookup"><span data-stu-id="e20ce-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e20ce-124">any</span><span class="sxs-lookup"><span data-stu-id="e20ce-124">any</span></span>                            |
| <span data-ttu-id="e20ce-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="e20ce-125">*ret*</span></span> | <span data-ttu-id="e20ce-126">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="e20ce-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="e20ce-127">**float**</span><span class="sxs-lookup"><span data-stu-id="e20ce-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e20ce-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="e20ce-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e20ce-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e20ce-129">Minimum Shader Model</span></span>

<span data-ttu-id="e20ce-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e20ce-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e20ce-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e20ce-131">Shader Model</span></span>                                                                       | <span data-ttu-id="e20ce-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="e20ce-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="e20ce-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="e20ce-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="e20ce-134">sì</span><span class="sxs-lookup"><span data-stu-id="e20ce-134">yes</span></span>                 |
| [<span data-ttu-id="e20ce-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e20ce-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="e20ce-136">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="e20ce-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e20ce-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e20ce-137">Requirements</span></span>



| <span data-ttu-id="e20ce-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e20ce-138">Requirement</span></span> | <span data-ttu-id="e20ce-139">Valore</span><span class="sxs-lookup"><span data-stu-id="e20ce-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e20ce-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e20ce-140">Header</span></span><br/> | <dl> <span data-ttu-id="e20ce-141"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20ce-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20ce-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e20ce-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20ce-143">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e20ce-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

