---
title: cross
description: Restituisce il prodotto incrociato di due vettori 3D a virgola mobile.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- Cross HLSL
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993581"
---
# <a name="cross"></a><span data-ttu-id="89507-104">cross</span><span class="sxs-lookup"><span data-stu-id="89507-104">cross</span></span>

<span data-ttu-id="89507-105">Restituisce il prodotto incrociato di due vettori 3D a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="89507-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="89507-106">incrociato *ret* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="89507-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="89507-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="89507-107">Parameters</span></span>



| <span data-ttu-id="89507-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="89507-108">Item</span></span>                                                   | <span data-ttu-id="89507-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89507-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="89507-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="89507-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="89507-111">\[nel \] primo vettore 3D a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="89507-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="89507-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="89507-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="89507-113">\[nel \] secondo vettore 3D a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="89507-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="89507-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89507-114">Return Value</span></span>

<span data-ttu-id="89507-115">Prodotto incrociato del parametro *x* e del parametro *y* .</span><span class="sxs-lookup"><span data-stu-id="89507-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="89507-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="89507-116">Type Description</span></span>



| <span data-ttu-id="89507-117">Nome</span><span class="sxs-lookup"><span data-stu-id="89507-117">Name</span></span>  | [<span data-ttu-id="89507-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="89507-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="89507-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="89507-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="89507-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="89507-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="89507-121">*x*</span><span class="sxs-lookup"><span data-stu-id="89507-121">*x*</span></span>   | [<span data-ttu-id="89507-122">**vettore**</span><span class="sxs-lookup"><span data-stu-id="89507-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="89507-123">**float**</span><span class="sxs-lookup"><span data-stu-id="89507-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="89507-124">3</span><span class="sxs-lookup"><span data-stu-id="89507-124">3</span></span>    |
| <span data-ttu-id="89507-125">*y*</span><span class="sxs-lookup"><span data-stu-id="89507-125">*y*</span></span>   | [<span data-ttu-id="89507-126">**vettore**</span><span class="sxs-lookup"><span data-stu-id="89507-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="89507-127">**float**</span><span class="sxs-lookup"><span data-stu-id="89507-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="89507-128">3</span><span class="sxs-lookup"><span data-stu-id="89507-128">3</span></span>    |
| <span data-ttu-id="89507-129">*RET*</span><span class="sxs-lookup"><span data-stu-id="89507-129">*ret*</span></span> | [<span data-ttu-id="89507-130">**vettore**</span><span class="sxs-lookup"><span data-stu-id="89507-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="89507-131">**float**</span><span class="sxs-lookup"><span data-stu-id="89507-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="89507-132">3</span><span class="sxs-lookup"><span data-stu-id="89507-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="89507-133">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="89507-133">Minimum Shader Model</span></span>

<span data-ttu-id="89507-134">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="89507-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="89507-135">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="89507-135">Shader Model</span></span>                                                                       | <span data-ttu-id="89507-136">Supportato</span><span class="sxs-lookup"><span data-stu-id="89507-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="89507-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="89507-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="89507-138">sì</span><span class="sxs-lookup"><span data-stu-id="89507-138">yes</span></span>                   |
| [<span data-ttu-id="89507-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="89507-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="89507-140">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="89507-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="89507-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89507-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89507-142">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="89507-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

