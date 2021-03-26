---
title: acos
description: Restituisce l'arcoseno del valore specificato.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- HLSL ARccOS
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118359"
---
# <a name="acos"></a><span data-ttu-id="fb6d1-104">acos</span><span class="sxs-lookup"><span data-stu-id="fb6d1-104">acos</span></span>

<span data-ttu-id="fb6d1-105">Restituisce l'arcoseno del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="fb6d1-106">ARccOS *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="fb6d1-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="fb6d1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb6d1-107">Parameters</span></span>



| <span data-ttu-id="fb6d1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="fb6d1-108">Item</span></span>                                                   | <span data-ttu-id="fb6d1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb6d1-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6d1-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="fb6d1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fb6d1-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-111">\[in\] The specified value.</span></span> <span data-ttu-id="fb6d1-112">Ogni componente deve essere un valore a virgola mobile compreso nell'intervallo compreso tra-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fb6d1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb6d1-113">Return Value</span></span>

<span data-ttu-id="fb6d1-114">Arcoseno del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="fb6d1-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="fb6d1-115">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="fb6d1-115">Type Description</span></span>



| <span data-ttu-id="fb6d1-116">Nome</span><span class="sxs-lookup"><span data-stu-id="fb6d1-116">Name</span></span>  | [<span data-ttu-id="fb6d1-117">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fb6d1-118">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fb6d1-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="fb6d1-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="fb6d1-120">*x*</span><span class="sxs-lookup"><span data-stu-id="fb6d1-120">*x*</span></span>   | <span data-ttu-id="fb6d1-121">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="fb6d1-122">**float**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fb6d1-123">any</span><span class="sxs-lookup"><span data-stu-id="fb6d1-123">any</span></span>                            |
| <span data-ttu-id="fb6d1-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="fb6d1-124">*ret*</span></span> | <span data-ttu-id="fb6d1-125">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="fb6d1-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="fb6d1-126">**float**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fb6d1-127">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="fb6d1-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fb6d1-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="fb6d1-128">Minimum Shader Model</span></span>

<span data-ttu-id="fb6d1-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fb6d1-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="fb6d1-130">Shader Model</span></span>                                                                       | <span data-ttu-id="fb6d1-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="fb6d1-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="fb6d1-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="fb6d1-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="fb6d1-133">sì</span><span class="sxs-lookup"><span data-stu-id="fb6d1-133">yes</span></span>           |
| [<span data-ttu-id="fb6d1-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb6d1-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="fb6d1-135">\_solo vs 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="fb6d1-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="fb6d1-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb6d1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6d1-137">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

