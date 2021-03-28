---
title: sin
description: Restituisce il seno del valore specificato.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- HLSL sin
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399569"
---
# <a name="sin"></a><span data-ttu-id="69477-104">sin</span><span class="sxs-lookup"><span data-stu-id="69477-104">sin</span></span>

<span data-ttu-id="69477-105">Restituisce il seno del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="69477-105">Returns the sine of the specified value.</span></span>



| <span data-ttu-id="69477-106">sin *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="69477-106">*ret* sin(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="69477-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="69477-107">Parameters</span></span>



| <span data-ttu-id="69477-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="69477-108">Item</span></span>                                                   | <span data-ttu-id="69477-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69477-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="69477-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="69477-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="69477-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="69477-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="69477-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69477-112">Return Value</span></span>

<span data-ttu-id="69477-113">Seno del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="69477-113">The sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="69477-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="69477-114">Type Description</span></span>



| <span data-ttu-id="69477-115">Nome</span><span class="sxs-lookup"><span data-stu-id="69477-115">Name</span></span>  | [<span data-ttu-id="69477-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="69477-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="69477-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="69477-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="69477-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="69477-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="69477-119">*x*</span><span class="sxs-lookup"><span data-stu-id="69477-119">*x*</span></span>   | <span data-ttu-id="69477-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="69477-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="69477-121">**float**</span><span class="sxs-lookup"><span data-stu-id="69477-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="69477-122">any</span><span class="sxs-lookup"><span data-stu-id="69477-122">any</span></span>                            |
| <span data-ttu-id="69477-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="69477-123">*ret*</span></span> | <span data-ttu-id="69477-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="69477-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="69477-125">**float**</span><span class="sxs-lookup"><span data-stu-id="69477-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="69477-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="69477-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="69477-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="69477-127">Minimum Shader Model</span></span>

<span data-ttu-id="69477-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="69477-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69477-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="69477-129">Shader Model</span></span>                                                                       | <span data-ttu-id="69477-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="69477-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="69477-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="69477-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="69477-132">sì</span><span class="sxs-lookup"><span data-stu-id="69477-132">yes</span></span>                 |
| [<span data-ttu-id="69477-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69477-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="69477-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="69477-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="69477-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69477-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69477-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="69477-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

