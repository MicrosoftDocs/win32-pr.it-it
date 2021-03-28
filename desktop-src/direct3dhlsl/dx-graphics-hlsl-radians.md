---
title: radianti
description: Converte il valore specificato da gradi in radianti.
ms.assetid: 6fc6b1f8-b686-49ba-93ea-2b2470b3fc72
keywords:
- radianti HLSL
topic_type:
- apiref
api_name:
- radians
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 029c0ffe2838cdcc997e47cae4e0adafede4411d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399667"
---
# <a name="radians"></a><span data-ttu-id="efe9d-104">radianti</span><span class="sxs-lookup"><span data-stu-id="efe9d-104">radians</span></span>

<span data-ttu-id="efe9d-105">Converte il valore specificato da gradi in radianti.</span><span class="sxs-lookup"><span data-stu-id="efe9d-105">Converts the specified value from degrees to radians.</span></span>



| <span data-ttu-id="efe9d-106">in radianti *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="efe9d-106">*ret* radians(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="efe9d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="efe9d-107">Parameters</span></span>



| <span data-ttu-id="efe9d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="efe9d-108">Item</span></span>                                                   | <span data-ttu-id="efe9d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efe9d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="efe9d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="efe9d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="efe9d-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="efe9d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="efe9d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efe9d-112">Return Value</span></span>

<span data-ttu-id="efe9d-113">Parametro *x* convertito da gradi a radianti.</span><span class="sxs-lookup"><span data-stu-id="efe9d-113">The *x* parameter converted from degrees to radians.</span></span>

## <a name="type-description"></a><span data-ttu-id="efe9d-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="efe9d-114">Type Description</span></span>



| <span data-ttu-id="efe9d-115">Nome</span><span class="sxs-lookup"><span data-stu-id="efe9d-115">Name</span></span>  | [<span data-ttu-id="efe9d-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="efe9d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="efe9d-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="efe9d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="efe9d-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="efe9d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="efe9d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="efe9d-119">*x*</span></span>   | <span data-ttu-id="efe9d-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="efe9d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="efe9d-121">**float**</span><span class="sxs-lookup"><span data-stu-id="efe9d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="efe9d-122">any</span><span class="sxs-lookup"><span data-stu-id="efe9d-122">any</span></span>                            |
| <span data-ttu-id="efe9d-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="efe9d-123">*ret*</span></span> | <span data-ttu-id="efe9d-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="efe9d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="efe9d-125">**float**</span><span class="sxs-lookup"><span data-stu-id="efe9d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="efe9d-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="efe9d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efe9d-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="efe9d-127">Minimum Shader Model</span></span>

<span data-ttu-id="efe9d-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="efe9d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="efe9d-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="efe9d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="efe9d-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="efe9d-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="efe9d-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="efe9d-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="efe9d-132">sì</span><span class="sxs-lookup"><span data-stu-id="efe9d-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="efe9d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efe9d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe9d-134">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="efe9d-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

