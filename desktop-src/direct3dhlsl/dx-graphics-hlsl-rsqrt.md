---
title: rsqrt
description: Restituisce il reciproco della radice quadrata del valore specificato.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- HLSL rsqrt
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993429"
---
# <a name="rsqrt"></a><span data-ttu-id="653c1-104">rsqrt</span><span class="sxs-lookup"><span data-stu-id="653c1-104">rsqrt</span></span>

<span data-ttu-id="653c1-105">Restituisce il reciproco della radice quadrata del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="653c1-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="653c1-106">rsqrt *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="653c1-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="653c1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="653c1-107">Parameters</span></span>



| <span data-ttu-id="653c1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="653c1-108">Item</span></span>                                                   | <span data-ttu-id="653c1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="653c1-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="653c1-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="653c1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="653c1-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="653c1-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="653c1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="653c1-112">Return Value</span></span>

<span data-ttu-id="653c1-113">Il reciproco della radice quadrata del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="653c1-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="653c1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="653c1-114">Remarks</span></span>

<span data-ttu-id="653c1-115">Questa funzione usa la formula seguente: 1/ **Sqrt**(*x*).</span><span class="sxs-lookup"><span data-stu-id="653c1-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="653c1-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="653c1-116">Type Description</span></span>



| <span data-ttu-id="653c1-117">Nome</span><span class="sxs-lookup"><span data-stu-id="653c1-117">Name</span></span>  | [<span data-ttu-id="653c1-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="653c1-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="653c1-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="653c1-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="653c1-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="653c1-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="653c1-121">*x*</span><span class="sxs-lookup"><span data-stu-id="653c1-121">*x*</span></span>   | <span data-ttu-id="653c1-122">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="653c1-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="653c1-123">**float**</span><span class="sxs-lookup"><span data-stu-id="653c1-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="653c1-124">any</span><span class="sxs-lookup"><span data-stu-id="653c1-124">any</span></span>                            |
| <span data-ttu-id="653c1-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="653c1-125">*ret*</span></span> | <span data-ttu-id="653c1-126">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="653c1-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="653c1-127">**float**</span><span class="sxs-lookup"><span data-stu-id="653c1-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="653c1-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="653c1-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="653c1-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="653c1-129">Minimum Shader Model</span></span>

<span data-ttu-id="653c1-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="653c1-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="653c1-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="653c1-131">Shader Model</span></span>                                                                       | <span data-ttu-id="653c1-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="653c1-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="653c1-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="653c1-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="653c1-134">sì</span><span class="sxs-lookup"><span data-stu-id="653c1-134">yes</span></span>                 |
| [<span data-ttu-id="653c1-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="653c1-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="653c1-136">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="653c1-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="653c1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="653c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653c1-138">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="653c1-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

