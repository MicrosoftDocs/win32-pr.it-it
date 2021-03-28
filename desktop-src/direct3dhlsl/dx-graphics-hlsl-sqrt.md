---
title: sqrt
description: Restituisce la radice quadrata del valore a virgola mobile specificato, per componente.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- HLSL sqrt
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399056"
---
# <a name="sqrt"></a><span data-ttu-id="4f20e-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="4f20e-104">sqrt</span></span>

<span data-ttu-id="4f20e-105">Restituisce la radice quadrata del valore a virgola mobile specificato, per componente.</span><span class="sxs-lookup"><span data-stu-id="4f20e-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="4f20e-106">sqrt *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="4f20e-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="4f20e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f20e-107">Parameters</span></span>



| <span data-ttu-id="4f20e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4f20e-108">Item</span></span>                                                   | <span data-ttu-id="4f20e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f20e-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="4f20e-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4f20e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4f20e-111">\[nel \] valore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="4f20e-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4f20e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f20e-112">Return Value</span></span>

<span data-ttu-id="4f20e-113">Radice quadrata del parametro *x* , per componente.</span><span class="sxs-lookup"><span data-stu-id="4f20e-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="4f20e-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="4f20e-114">Type Description</span></span>



| <span data-ttu-id="4f20e-115">Nome</span><span class="sxs-lookup"><span data-stu-id="4f20e-115">Name</span></span>  | [<span data-ttu-id="4f20e-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="4f20e-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4f20e-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="4f20e-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4f20e-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4f20e-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4f20e-119">*x*</span><span class="sxs-lookup"><span data-stu-id="4f20e-119">*x*</span></span>   | <span data-ttu-id="4f20e-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="4f20e-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4f20e-121">**float**</span><span class="sxs-lookup"><span data-stu-id="4f20e-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4f20e-122">any</span><span class="sxs-lookup"><span data-stu-id="4f20e-122">any</span></span>                            |
| <span data-ttu-id="4f20e-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="4f20e-123">*ret*</span></span> | <span data-ttu-id="4f20e-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="4f20e-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4f20e-125">**float**</span><span class="sxs-lookup"><span data-stu-id="4f20e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4f20e-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="4f20e-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4f20e-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4f20e-127">Minimum Shader Model</span></span>

<span data-ttu-id="4f20e-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f20e-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4f20e-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4f20e-129">Shader Model</span></span>                                                                       | <span data-ttu-id="4f20e-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="4f20e-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4f20e-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="4f20e-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="4f20e-132">sì</span><span class="sxs-lookup"><span data-stu-id="4f20e-132">yes</span></span>                 |
| [<span data-ttu-id="4f20e-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4f20e-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4f20e-134">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="4f20e-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4f20e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f20e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f20e-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4f20e-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

