---
title: tanh
description: Restituisce la tangente iperbolica del valore specificato.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- HLSL tanh
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c5312aaac6d6f164e940f99183e61688b393fbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046940"
---
# <a name="tanh"></a><span data-ttu-id="bc825-104">tanh</span><span class="sxs-lookup"><span data-stu-id="bc825-104">tanh</span></span>

<span data-ttu-id="bc825-105">Restituisce la tangente iperbolica del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="bc825-105">Returns the hyperbolic tangent of the specified value.</span></span>



| <span data-ttu-id="bc825-106">tanh *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="bc825-106">*ret* tanh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="bc825-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc825-107">Parameters</span></span>



| <span data-ttu-id="bc825-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc825-108">Item</span></span>                                                   | <span data-ttu-id="bc825-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc825-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="bc825-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bc825-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bc825-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="bc825-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bc825-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc825-112">Return Value</span></span>

<span data-ttu-id="bc825-113">Tangente iperbolica del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="bc825-113">The hyperbolic tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="bc825-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="bc825-114">Type Description</span></span>



| <span data-ttu-id="bc825-115">Nome</span><span class="sxs-lookup"><span data-stu-id="bc825-115">Name</span></span>  | [<span data-ttu-id="bc825-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="bc825-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bc825-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="bc825-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bc825-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="bc825-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bc825-119">*x*</span><span class="sxs-lookup"><span data-stu-id="bc825-119">*x*</span></span>   | <span data-ttu-id="bc825-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="bc825-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="bc825-121">**float**</span><span class="sxs-lookup"><span data-stu-id="bc825-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bc825-122">any</span><span class="sxs-lookup"><span data-stu-id="bc825-122">any</span></span>                            |
| <span data-ttu-id="bc825-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="bc825-123">*ret*</span></span> | <span data-ttu-id="bc825-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="bc825-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bc825-125">**float**</span><span class="sxs-lookup"><span data-stu-id="bc825-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bc825-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="bc825-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bc825-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="bc825-127">Minimum Shader Model</span></span>

<span data-ttu-id="bc825-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc825-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bc825-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="bc825-129">Shader Model</span></span>                                                                       | <span data-ttu-id="bc825-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="bc825-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="bc825-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="bc825-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bc825-132">sì</span><span class="sxs-lookup"><span data-stu-id="bc825-132">yes</span></span>                 |
| [<span data-ttu-id="bc825-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc825-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bc825-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="bc825-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bc825-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc825-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc825-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bc825-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

