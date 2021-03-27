---
title: log
description: Restituisce il logaritmo in base e del valore specificato.
ms.assetid: 443e7aa7-7219-40ad-aafc-4bce09c8f596
keywords:
- HLSL log
topic_type:
- apiref
api_name:
- log
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdd08fe178925406145476b3250e8d256b263c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729162"
---
# <a name="log"></a><span data-ttu-id="f7ad4-104">log</span><span class="sxs-lookup"><span data-stu-id="f7ad4-104">log</span></span>

<span data-ttu-id="f7ad4-105">Restituisce il logaritmo in base e del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ad4-105">Returns the base-e logarithm of the specified value.</span></span>



| <span data-ttu-id="f7ad4-106">log *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="f7ad4-106">*ret* log(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="f7ad4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7ad4-107">Parameters</span></span>



| <span data-ttu-id="f7ad4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7ad4-108">Item</span></span>                                                   | <span data-ttu-id="f7ad4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7ad4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f7ad4-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f7ad4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f7ad4-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ad4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f7ad4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7ad4-112">Return Value</span></span>

<span data-ttu-id="f7ad4-113">Logaritmo in base e del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="f7ad4-113">The base-e logarithm of the *x* parameter.</span></span> <span data-ttu-id="f7ad4-114">Se il parametro *x* è negativo, la funzione restituisce un valore indefinito.</span><span class="sxs-lookup"><span data-stu-id="f7ad4-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="f7ad4-115">Se il parametro *x* è 0, questa funzione restituisce-inf.</span><span class="sxs-lookup"><span data-stu-id="f7ad4-115">If the *x* parameter is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="f7ad4-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="f7ad4-116">Type Description</span></span>



| <span data-ttu-id="f7ad4-117">Nome</span><span class="sxs-lookup"><span data-stu-id="f7ad4-117">Name</span></span>  | [<span data-ttu-id="f7ad4-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="f7ad4-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f7ad4-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="f7ad4-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f7ad4-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f7ad4-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f7ad4-121">*x*</span><span class="sxs-lookup"><span data-stu-id="f7ad4-121">*x*</span></span>   | <span data-ttu-id="f7ad4-122">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="f7ad4-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f7ad4-123">**float**</span><span class="sxs-lookup"><span data-stu-id="f7ad4-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f7ad4-124">any</span><span class="sxs-lookup"><span data-stu-id="f7ad4-124">any</span></span>                            |
| <span data-ttu-id="f7ad4-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="f7ad4-125">*ret*</span></span> | <span data-ttu-id="f7ad4-126">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="f7ad4-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f7ad4-127">**float**</span><span class="sxs-lookup"><span data-stu-id="f7ad4-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f7ad4-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="f7ad4-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f7ad4-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f7ad4-129">Minimum Shader Model</span></span>

<span data-ttu-id="f7ad4-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7ad4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f7ad4-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f7ad4-131">Shader Model</span></span>                                                                       | <span data-ttu-id="f7ad4-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="f7ad4-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f7ad4-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="f7ad4-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f7ad4-134">sì</span><span class="sxs-lookup"><span data-stu-id="f7ad4-134">yes</span></span>                 |
| [<span data-ttu-id="f7ad4-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7ad4-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f7ad4-136">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="f7ad4-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="f7ad4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7ad4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ad4-138">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f7ad4-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

