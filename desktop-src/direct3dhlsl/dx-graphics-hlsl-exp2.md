---
title: exp2 (Corecrt \_ Math. h)
description: Restituisce l'esponenziale in base 2, o 2x, del valore specificato.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- HLSL exp2
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982187"
---
# <a name="exp2"></a><span data-ttu-id="5d2e6-104">exp2</span><span class="sxs-lookup"><span data-stu-id="5d2e6-104">exp2</span></span>

<span data-ttu-id="5d2e6-105">Restituisce l'esponenziale in base 2, o 2<sup>x</sup>, del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="5d2e6-106">exp2 *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="5d2e6-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="5d2e6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d2e6-107">Parameters</span></span>



| <span data-ttu-id="5d2e6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5d2e6-108">Item</span></span>                                                   | <span data-ttu-id="5d2e6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d2e6-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="5d2e6-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="5d2e6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5d2e6-111">\[nel \] valore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5d2e6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d2e6-112">Return Value</span></span>

<span data-ttu-id="5d2e6-113">Esponenziale in base 2 del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="5d2e6-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="5d2e6-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="5d2e6-114">Type Description</span></span>



| <span data-ttu-id="5d2e6-115">Nome</span><span class="sxs-lookup"><span data-stu-id="5d2e6-115">Name</span></span>  | [<span data-ttu-id="5d2e6-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5d2e6-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5d2e6-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5d2e6-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5d2e6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="5d2e6-119">*x*</span></span>   | <span data-ttu-id="5d2e6-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="5d2e6-121">**float**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5d2e6-122">any</span><span class="sxs-lookup"><span data-stu-id="5d2e6-122">any</span></span>                            |
| <span data-ttu-id="5d2e6-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="5d2e6-123">*ret*</span></span> | <span data-ttu-id="5d2e6-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="5d2e6-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5d2e6-125">**float**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5d2e6-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="5d2e6-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5d2e6-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5d2e6-127">Minimum Shader Model</span></span>

<span data-ttu-id="5d2e6-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5d2e6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5d2e6-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5d2e6-129">Shader Model</span></span>                                                                       | <span data-ttu-id="5d2e6-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="5d2e6-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5d2e6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="5d2e6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5d2e6-132">sì</span><span class="sxs-lookup"><span data-stu-id="5d2e6-132">yes</span></span>       |
| [<span data-ttu-id="5d2e6-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d2e6-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5d2e6-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5d2e6-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="5d2e6-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d2e6-135">Requirements</span></span>



| <span data-ttu-id="5d2e6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d2e6-136">Requirement</span></span> | <span data-ttu-id="5d2e6-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5d2e6-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2e6-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d2e6-138">Header</span></span><br/> | <dl> <span data-ttu-id="5d2e6-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2e6-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2e6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d2e6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2e6-141">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5d2e6-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

