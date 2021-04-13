---
title: cos
description: Restituisce il coseno del valore specificato.
ms.assetid: 96c15702-98be-45bc-9abc-60ccc3c217b6
keywords:
- HLSL cos
topic_type:
- apiref
api_name:
- cos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f5c0f4f071d47102c673301a397bfe3ecf178e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399670"
---
# <a name="cos"></a><span data-ttu-id="256bb-104">cos</span><span class="sxs-lookup"><span data-stu-id="256bb-104">cos</span></span>

<span data-ttu-id="256bb-105">Restituisce il coseno del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="256bb-105">Returns the cosine of the specified value.</span></span>



| <span data-ttu-id="256bb-106">cos *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="256bb-106">*ret* cos(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="256bb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="256bb-107">Parameters</span></span>



| <span data-ttu-id="256bb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="256bb-108">Item</span></span>                                                   | <span data-ttu-id="256bb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="256bb-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="256bb-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="256bb-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="256bb-111">\[nel \] valore specificato, in radianti.</span><span class="sxs-lookup"><span data-stu-id="256bb-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="256bb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="256bb-112">Return Value</span></span>

<span data-ttu-id="256bb-113">Coseno del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="256bb-113">The cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="256bb-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="256bb-114">Type Description</span></span>



| <span data-ttu-id="256bb-115">Nome</span><span class="sxs-lookup"><span data-stu-id="256bb-115">Name</span></span>  | [<span data-ttu-id="256bb-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="256bb-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="256bb-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="256bb-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="256bb-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="256bb-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="256bb-119">*x*</span><span class="sxs-lookup"><span data-stu-id="256bb-119">*x*</span></span>   | <span data-ttu-id="256bb-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="256bb-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="256bb-121">**float**</span><span class="sxs-lookup"><span data-stu-id="256bb-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="256bb-122">any</span><span class="sxs-lookup"><span data-stu-id="256bb-122">any</span></span>                            |
| <span data-ttu-id="256bb-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="256bb-123">*ret*</span></span> | <span data-ttu-id="256bb-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="256bb-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="256bb-125">**float**</span><span class="sxs-lookup"><span data-stu-id="256bb-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="256bb-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="256bb-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="256bb-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="256bb-127">Minimum Shader Model</span></span>

<span data-ttu-id="256bb-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="256bb-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="256bb-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="256bb-129">Shader Model</span></span>                                                                       | <span data-ttu-id="256bb-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="256bb-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="256bb-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="256bb-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="256bb-132">sì</span><span class="sxs-lookup"><span data-stu-id="256bb-132">yes</span></span>       |
| [<span data-ttu-id="256bb-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="256bb-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="256bb-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="256bb-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="256bb-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="256bb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256bb-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="256bb-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

