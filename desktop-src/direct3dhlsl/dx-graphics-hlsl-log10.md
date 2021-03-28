---
title: log10
description: Restituisce il logaritmo in base 10 del valore specificato.
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- HLSL log10
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d226dcc33da1aee6d55e21c6d97febc23577503
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338599"
---
# <a name="log10"></a><span data-ttu-id="bfc21-104">log10</span><span class="sxs-lookup"><span data-stu-id="bfc21-104">log10</span></span>

<span data-ttu-id="bfc21-105">Restituisce il logaritmo in base 10 del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="bfc21-105">Returns the base-10 logarithm of the specified value.</span></span>



| <span data-ttu-id="bfc21-106">log10 *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="bfc21-106">*ret* log10(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="bfc21-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfc21-107">Parameters</span></span>



| <span data-ttu-id="bfc21-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bfc21-108">Item</span></span>                                                   | <span data-ttu-id="bfc21-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfc21-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="bfc21-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bfc21-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bfc21-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="bfc21-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bfc21-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfc21-112">Return Value</span></span>

<span data-ttu-id="bfc21-113">Logaritmo in base 10 del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="bfc21-113">The base-10 logarithm of the *x* parameter.</span></span> <span data-ttu-id="bfc21-114">Se il parametro *x* è negativo, la funzione restituisce un valore indefinito.</span><span class="sxs-lookup"><span data-stu-id="bfc21-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="bfc21-115">Se *x* è 0, questa funzione restituisce-inf.</span><span class="sxs-lookup"><span data-stu-id="bfc21-115">If the *x* is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="bfc21-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="bfc21-116">Type Description</span></span>



| <span data-ttu-id="bfc21-117">Nome</span><span class="sxs-lookup"><span data-stu-id="bfc21-117">Name</span></span>  | [<span data-ttu-id="bfc21-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="bfc21-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bfc21-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="bfc21-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bfc21-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bfc21-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bfc21-121">*x*</span><span class="sxs-lookup"><span data-stu-id="bfc21-121">*x*</span></span>   | <span data-ttu-id="bfc21-122">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="bfc21-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bfc21-123">**float**</span><span class="sxs-lookup"><span data-stu-id="bfc21-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bfc21-124">any</span><span class="sxs-lookup"><span data-stu-id="bfc21-124">any</span></span>                            |
| <span data-ttu-id="bfc21-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="bfc21-125">*ret*</span></span> | <span data-ttu-id="bfc21-126">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="bfc21-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bfc21-127">**float**</span><span class="sxs-lookup"><span data-stu-id="bfc21-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bfc21-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="bfc21-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bfc21-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bfc21-129">Minimum Shader Model</span></span>

<span data-ttu-id="bfc21-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfc21-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bfc21-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bfc21-131">Shader Model</span></span>                                                                       | <span data-ttu-id="bfc21-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="bfc21-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="bfc21-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="bfc21-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bfc21-134">sì</span><span class="sxs-lookup"><span data-stu-id="bfc21-134">yes</span></span>                 |
| [<span data-ttu-id="bfc21-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfc21-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bfc21-136">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="bfc21-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bfc21-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfc21-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc21-138">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bfc21-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

