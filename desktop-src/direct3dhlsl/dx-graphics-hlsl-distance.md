---
title: distance
description: Restituisce un valore scalare distanza tra due vettori.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- distanza HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338078"
---
# <a name="distance"></a><span data-ttu-id="b8c63-104">distance</span><span class="sxs-lookup"><span data-stu-id="b8c63-104">distance</span></span>

<span data-ttu-id="b8c63-105">Restituisce un valore scalare distanza tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="b8c63-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="b8c63-106">distanza *ret* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="b8c63-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b8c63-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8c63-107">Parameters</span></span>



| <span data-ttu-id="b8c63-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8c63-108">Item</span></span>                                                   | <span data-ttu-id="b8c63-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8c63-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b8c63-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b8c63-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b8c63-111">\[nel \] primo vettore a virgola mobile da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b8c63-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="b8c63-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="b8c63-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="b8c63-113">\[nel \] secondo vettore a virgola mobile da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b8c63-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b8c63-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8c63-114">Return Value</span></span>

<span data-ttu-id="b8c63-115">Valore scalare A virgola mobile che rappresenta la distanza tra il parametro *x* e il parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="b8c63-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b8c63-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="b8c63-116">Type Description</span></span>



| <span data-ttu-id="b8c63-117">Nome</span><span class="sxs-lookup"><span data-stu-id="b8c63-117">Name</span></span>  | [<span data-ttu-id="b8c63-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="b8c63-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b8c63-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="b8c63-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b8c63-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="b8c63-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b8c63-121">*x*</span><span class="sxs-lookup"><span data-stu-id="b8c63-121">*x*</span></span>   | [<span data-ttu-id="b8c63-122">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b8c63-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b8c63-123">**float**</span><span class="sxs-lookup"><span data-stu-id="b8c63-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b8c63-124">any</span><span class="sxs-lookup"><span data-stu-id="b8c63-124">any</span></span>                            |
| <span data-ttu-id="b8c63-125">*y*</span><span class="sxs-lookup"><span data-stu-id="b8c63-125">*y*</span></span>   | [<span data-ttu-id="b8c63-126">**vettore**</span><span class="sxs-lookup"><span data-stu-id="b8c63-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b8c63-127">**float**</span><span class="sxs-lookup"><span data-stu-id="b8c63-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b8c63-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="b8c63-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b8c63-129">*RET*</span><span class="sxs-lookup"><span data-stu-id="b8c63-129">*ret*</span></span> | [<span data-ttu-id="b8c63-130">**scalare**</span><span class="sxs-lookup"><span data-stu-id="b8c63-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b8c63-131">**float**</span><span class="sxs-lookup"><span data-stu-id="b8c63-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b8c63-132">1</span><span class="sxs-lookup"><span data-stu-id="b8c63-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b8c63-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="b8c63-133">Minimum Shader Model</span></span>

<span data-ttu-id="b8c63-134">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8c63-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b8c63-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="b8c63-135">Shader Model</span></span>                                                                       | <span data-ttu-id="b8c63-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="b8c63-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b8c63-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="b8c63-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b8c63-138">sì</span><span class="sxs-lookup"><span data-stu-id="b8c63-138">yes</span></span>       |
| [<span data-ttu-id="b8c63-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8c63-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b8c63-140">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b8c63-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="b8c63-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8c63-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c63-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b8c63-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

