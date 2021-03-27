---
title: tan
description: Restituisce la tangente del valore specificato.
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- HLSL Tan
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf9451a2bf1a5759470e87343f1b4a15583b470a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728207"
---
# <a name="tan"></a><span data-ttu-id="c85d6-104">tan</span><span class="sxs-lookup"><span data-stu-id="c85d6-104">tan</span></span>

<span data-ttu-id="c85d6-105">Restituisce la tangente del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="c85d6-105">Returns the tangent of the specified value.</span></span>



| <span data-ttu-id="c85d6-106">*ret* Tan (*x*)</span><span class="sxs-lookup"><span data-stu-id="c85d6-106">*ret* tan(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="c85d6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c85d6-107">Parameters</span></span>



| <span data-ttu-id="c85d6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c85d6-108">Item</span></span>                                                   | <span data-ttu-id="c85d6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c85d6-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="c85d6-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="c85d6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c85d6-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="c85d6-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c85d6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c85d6-112">Return Value</span></span>

<span data-ttu-id="c85d6-113">Tangente del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="c85d6-113">The tangent of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="c85d6-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="c85d6-114">Type Description</span></span>



| <span data-ttu-id="c85d6-115">Nome</span><span class="sxs-lookup"><span data-stu-id="c85d6-115">Name</span></span>  | [<span data-ttu-id="c85d6-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="c85d6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c85d6-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="c85d6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c85d6-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c85d6-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c85d6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c85d6-119">*x*</span></span>   | <span data-ttu-id="c85d6-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="c85d6-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c85d6-121">**float**</span><span class="sxs-lookup"><span data-stu-id="c85d6-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c85d6-122">any</span><span class="sxs-lookup"><span data-stu-id="c85d6-122">any</span></span>                            |
| <span data-ttu-id="c85d6-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="c85d6-123">*ret*</span></span> | <span data-ttu-id="c85d6-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="c85d6-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c85d6-125">**float**</span><span class="sxs-lookup"><span data-stu-id="c85d6-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c85d6-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="c85d6-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c85d6-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c85d6-127">Minimum Shader Model</span></span>

<span data-ttu-id="c85d6-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c85d6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c85d6-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c85d6-129">Shader Model</span></span>                                                                       | <span data-ttu-id="c85d6-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="c85d6-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c85d6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="c85d6-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c85d6-132">sì</span><span class="sxs-lookup"><span data-stu-id="c85d6-132">yes</span></span>                 |
| [<span data-ttu-id="c85d6-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c85d6-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c85d6-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c85d6-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c85d6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c85d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85d6-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c85d6-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

