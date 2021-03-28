---
title: fwidth
description: Restituisce il valore assoluto dei derivati parziali del valore specificato.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- HLSL fWidth
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118155"
---
# <a name="fwidth"></a><span data-ttu-id="f6320-104">fwidth</span><span class="sxs-lookup"><span data-stu-id="f6320-104">fwidth</span></span>

<span data-ttu-id="f6320-105">Restituisce il valore assoluto dei derivati parziali del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f6320-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="f6320-106">fWidth *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="f6320-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="f6320-107">Questa funzione calcola quanto segue: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span><span class="sxs-lookup"><span data-stu-id="f6320-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="f6320-108">Questa funzione è supportata solo in pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f6320-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6320-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6320-109">Parameters</span></span>



| <span data-ttu-id="f6320-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6320-110">Item</span></span>                                                   | <span data-ttu-id="f6320-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6320-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f6320-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f6320-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f6320-113">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f6320-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f6320-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6320-114">Return Value</span></span>

<span data-ttu-id="f6320-115">Valore assoluto dei derivati parziali del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="f6320-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="f6320-116">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="f6320-116">Type Description</span></span>



| <span data-ttu-id="f6320-117">Nome</span><span class="sxs-lookup"><span data-stu-id="f6320-117">Name</span></span>  | [<span data-ttu-id="f6320-118">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="f6320-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f6320-119">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="f6320-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f6320-120">Dimensione</span><span class="sxs-lookup"><span data-stu-id="f6320-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f6320-121">*x*</span><span class="sxs-lookup"><span data-stu-id="f6320-121">*x*</span></span>   | <span data-ttu-id="f6320-122">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="f6320-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f6320-123">**float**</span><span class="sxs-lookup"><span data-stu-id="f6320-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f6320-124">any</span><span class="sxs-lookup"><span data-stu-id="f6320-124">any</span></span>                            |
| <span data-ttu-id="f6320-125">*RET*</span><span class="sxs-lookup"><span data-stu-id="f6320-125">*ret*</span></span> | <span data-ttu-id="f6320-126">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="f6320-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f6320-127">**float**</span><span class="sxs-lookup"><span data-stu-id="f6320-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f6320-128">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="f6320-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f6320-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f6320-129">Minimum Shader Model</span></span>

<span data-ttu-id="f6320-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6320-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f6320-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="f6320-131">Shader Model</span></span>                                                                       | <span data-ttu-id="f6320-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="f6320-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f6320-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="f6320-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="f6320-134">sì</span><span class="sxs-lookup"><span data-stu-id="f6320-134">yes</span></span>                 |
| [<span data-ttu-id="f6320-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6320-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="f6320-136">Sì ( \_ solo PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="f6320-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="f6320-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6320-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f6320-138">no</span><span class="sxs-lookup"><span data-stu-id="f6320-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="f6320-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6320-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6320-140">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f6320-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

