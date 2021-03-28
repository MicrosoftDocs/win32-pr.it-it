---
title: dot
description: Restituisce il prodotto scalare di due vettori.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- HLSL punto
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963339"
---
# <a name="dot"></a><span data-ttu-id="d5adf-104">dot</span><span class="sxs-lookup"><span data-stu-id="d5adf-104">dot</span></span>

<span data-ttu-id="d5adf-105">Restituisce il prodotto scalare di due vettori.</span><span class="sxs-lookup"><span data-stu-id="d5adf-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="d5adf-106">punto *ret* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="d5adf-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="d5adf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5adf-107">Parameters</span></span>



| <span data-ttu-id="d5adf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d5adf-108">Item</span></span>                                                   | <span data-ttu-id="d5adf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5adf-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="d5adf-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d5adf-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d5adf-111">\[nel \] primo vettore.</span><span class="sxs-lookup"><span data-stu-id="d5adf-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="d5adf-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="d5adf-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="d5adf-113">\[nel \] secondo vettore.</span><span class="sxs-lookup"><span data-stu-id="d5adf-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d5adf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5adf-114">Return Value</span></span>

<span data-ttu-id="d5adf-115">Prodotto punto del parametro *x* e del parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="d5adf-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d5adf-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="d5adf-116">Type Description</span></span>



| <span data-ttu-id="d5adf-117">Nome</span><span class="sxs-lookup"><span data-stu-id="d5adf-117">Name</span></span>  | [<span data-ttu-id="d5adf-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="d5adf-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d5adf-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="d5adf-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="d5adf-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="d5adf-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="d5adf-121">*x*</span><span class="sxs-lookup"><span data-stu-id="d5adf-121">*x*</span></span>   | [<span data-ttu-id="d5adf-122">**vettore**</span><span class="sxs-lookup"><span data-stu-id="d5adf-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d5adf-123">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d5adf-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d5adf-124">any</span><span class="sxs-lookup"><span data-stu-id="d5adf-124">any</span></span>                             |
| <span data-ttu-id="d5adf-125">*y*</span><span class="sxs-lookup"><span data-stu-id="d5adf-125">*y*</span></span>   | [<span data-ttu-id="d5adf-126">**vettore**</span><span class="sxs-lookup"><span data-stu-id="d5adf-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d5adf-127">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d5adf-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d5adf-128">stesse dimensioni come input *x*</span><span class="sxs-lookup"><span data-stu-id="d5adf-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="d5adf-129">*RET*</span><span class="sxs-lookup"><span data-stu-id="d5adf-129">*ret*</span></span> | [<span data-ttu-id="d5adf-130">**scalare**</span><span class="sxs-lookup"><span data-stu-id="d5adf-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d5adf-131">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d5adf-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d5adf-132">1</span><span class="sxs-lookup"><span data-stu-id="d5adf-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5adf-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="d5adf-133">Minimum Shader Model</span></span>

<span data-ttu-id="d5adf-134">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5adf-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5adf-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="d5adf-135">Shader Model</span></span>                                                                       | <span data-ttu-id="d5adf-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="d5adf-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d5adf-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="d5adf-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d5adf-138">sì</span><span class="sxs-lookup"><span data-stu-id="d5adf-138">yes</span></span>       |
| [<span data-ttu-id="d5adf-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5adf-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d5adf-140">sì</span><span class="sxs-lookup"><span data-stu-id="d5adf-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5adf-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5adf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5adf-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d5adf-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

