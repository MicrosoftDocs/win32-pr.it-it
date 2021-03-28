---
title: cosh
description: Restituisce il coseno iperbolico del valore specificato.
ms.assetid: ed68c461-de91-4ce4-a424-8ab28ee43f23
keywords:
- HLSL cosh
topic_type:
- apiref
api_name:
- cosh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bd6cad2b79e849d8f20bbaf5baa6cfc7db0b702
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993584"
---
# <a name="cosh"></a><span data-ttu-id="8255d-104">cosh</span><span class="sxs-lookup"><span data-stu-id="8255d-104">cosh</span></span>

<span data-ttu-id="8255d-105">Restituisce il coseno iperbolico del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="8255d-105">Returns the hyperbolic cosine of the specified value.</span></span>



| <span data-ttu-id="8255d-106">cosh *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="8255d-106">*ret* cosh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8255d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8255d-107">Parameters</span></span>



| <span data-ttu-id="8255d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8255d-108">Item</span></span>                                                   | <span data-ttu-id="8255d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8255d-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="8255d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8255d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8255d-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="8255d-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8255d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8255d-112">Return Value</span></span>

<span data-ttu-id="8255d-113">Coseno iperbolico del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="8255d-113">The hyperbolic cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8255d-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="8255d-114">Type Description</span></span>



| <span data-ttu-id="8255d-115">Nome</span><span class="sxs-lookup"><span data-stu-id="8255d-115">Name</span></span>  | [<span data-ttu-id="8255d-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="8255d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8255d-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="8255d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8255d-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8255d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8255d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8255d-119">*x*</span></span>   | <span data-ttu-id="8255d-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="8255d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8255d-121">**float**</span><span class="sxs-lookup"><span data-stu-id="8255d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8255d-122">any</span><span class="sxs-lookup"><span data-stu-id="8255d-122">any</span></span>                            |
| <span data-ttu-id="8255d-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="8255d-123">*ret*</span></span> | <span data-ttu-id="8255d-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="8255d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8255d-125">**float**</span><span class="sxs-lookup"><span data-stu-id="8255d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8255d-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="8255d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8255d-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8255d-127">Minimum Shader Model</span></span>

<span data-ttu-id="8255d-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8255d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8255d-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8255d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8255d-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="8255d-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8255d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="8255d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8255d-132">sì</span><span class="sxs-lookup"><span data-stu-id="8255d-132">yes</span></span>       |
| [<span data-ttu-id="8255d-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8255d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8255d-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8255d-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="8255d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8255d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8255d-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8255d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

