---
title: asin
description: Restituisce l'arcoseno del valore specificato.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- HLSL Asin
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047300"
---
# <a name="asin"></a><span data-ttu-id="bf15c-104">asin</span><span class="sxs-lookup"><span data-stu-id="bf15c-104">asin</span></span>

<span data-ttu-id="bf15c-105">Restituisce l'arcoseno del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="bf15c-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="bf15c-106">asin *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="bf15c-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="bf15c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf15c-107">Parameters</span></span>



| <span data-ttu-id="bf15c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf15c-108">Item</span></span>                                                   | <span data-ttu-id="bf15c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf15c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="bf15c-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bf15c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bf15c-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="bf15c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bf15c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf15c-112">Return Value</span></span>

<span data-ttu-id="bf15c-113">Arcoseno del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="bf15c-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf15c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf15c-114">Remarks</span></span>

<span data-ttu-id="bf15c-115">Ogni componente del parametro *x* deve essere compreso nell'intervallo tra-π/2 e π/2.</span><span class="sxs-lookup"><span data-stu-id="bf15c-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="bf15c-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="bf15c-116">Type Description</span></span>



| <span data-ttu-id="bf15c-117">Nome</span><span class="sxs-lookup"><span data-stu-id="bf15c-117">Name</span></span>  | [<span data-ttu-id="bf15c-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="bf15c-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bf15c-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="bf15c-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bf15c-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bf15c-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bf15c-121">*x*</span><span class="sxs-lookup"><span data-stu-id="bf15c-121">*x*</span></span>   | <span data-ttu-id="bf15c-122">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="bf15c-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bf15c-123">**float**</span><span class="sxs-lookup"><span data-stu-id="bf15c-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bf15c-124">any</span><span class="sxs-lookup"><span data-stu-id="bf15c-124">any</span></span>                            |
| <span data-ttu-id="bf15c-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="bf15c-125">*ret*</span></span> | <span data-ttu-id="bf15c-126">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="bf15c-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bf15c-127">**float**</span><span class="sxs-lookup"><span data-stu-id="bf15c-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bf15c-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="bf15c-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf15c-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bf15c-129">Minimum Shader Model</span></span>

<span data-ttu-id="bf15c-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf15c-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bf15c-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bf15c-131">Shader Model</span></span>                                                                       | <span data-ttu-id="bf15c-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="bf15c-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="bf15c-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="bf15c-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bf15c-134">sì</span><span class="sxs-lookup"><span data-stu-id="bf15c-134">yes</span></span>       |
| [<span data-ttu-id="bf15c-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf15c-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bf15c-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf15c-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="bf15c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf15c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf15c-138">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bf15c-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

