---
title: sinh
description: Restituisce il seno iperbolico del valore specificato.
ms.assetid: 8a9e11a3-582f-4680-a5bd-ecde90560db3
keywords:
- HLSL di
topic_type:
- apiref
api_name:
- sinh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbf6c5e04eb248c81782ba236010298ebb9564db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047219"
---
# <a name="sinh"></a><span data-ttu-id="49150-104">sinh</span><span class="sxs-lookup"><span data-stu-id="49150-104">sinh</span></span>

<span data-ttu-id="49150-105">Restituisce il seno iperbolico del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="49150-105">Returns the hyperbolic sine of the specified value.</span></span>



| <span data-ttu-id="49150-106">per *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="49150-106">*ret* sinh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="49150-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49150-107">Parameters</span></span>



| <span data-ttu-id="49150-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="49150-108">Item</span></span>                                                   | <span data-ttu-id="49150-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49150-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="49150-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="49150-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="49150-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="49150-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="49150-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49150-112">Return Value</span></span>

<span data-ttu-id="49150-113">Seno iperbolico del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="49150-113">The hyperbolic sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="49150-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="49150-114">Type Description</span></span>



| <span data-ttu-id="49150-115">Nome</span><span class="sxs-lookup"><span data-stu-id="49150-115">Name</span></span>  | [<span data-ttu-id="49150-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="49150-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="49150-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="49150-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="49150-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="49150-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="49150-119">*x*</span><span class="sxs-lookup"><span data-stu-id="49150-119">*x*</span></span>   | <span data-ttu-id="49150-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="49150-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="49150-121">**float**</span><span class="sxs-lookup"><span data-stu-id="49150-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="49150-122">any</span><span class="sxs-lookup"><span data-stu-id="49150-122">any</span></span>                            |
| <span data-ttu-id="49150-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="49150-123">*ret*</span></span> | <span data-ttu-id="49150-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="49150-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="49150-125">**float**</span><span class="sxs-lookup"><span data-stu-id="49150-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="49150-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="49150-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="49150-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="49150-127">Minimum Shader Model</span></span>

<span data-ttu-id="49150-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="49150-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="49150-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="49150-129">Shader Model</span></span>                                                                       | <span data-ttu-id="49150-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="49150-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="49150-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="49150-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="49150-132">sì</span><span class="sxs-lookup"><span data-stu-id="49150-132">yes</span></span>                 |
| [<span data-ttu-id="49150-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49150-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="49150-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="49150-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="49150-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49150-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49150-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="49150-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

