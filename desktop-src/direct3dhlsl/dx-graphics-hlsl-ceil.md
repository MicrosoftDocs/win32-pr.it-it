---
title: cella (Corecrt \_ Math. h)
description: Restituisce il più piccolo valore integer maggiore o uguale al valore specificato.
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- HLSL di cella
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995846"
---
# <a name="ceil"></a><span data-ttu-id="3acc4-104">ceil</span><span class="sxs-lookup"><span data-stu-id="3acc4-104">ceil</span></span>

<span data-ttu-id="3acc4-105">Restituisce il più piccolo valore integer maggiore o uguale al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="3acc4-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="3acc4-106">cella *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="3acc4-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="3acc4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3acc4-107">Parameters</span></span>



| <span data-ttu-id="3acc4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3acc4-108">Item</span></span>                                                   | <span data-ttu-id="3acc4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3acc4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="3acc4-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="3acc4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3acc4-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="3acc4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3acc4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3acc4-112">Return Value</span></span>

<span data-ttu-id="3acc4-113">Valore integer più piccolo (restituito come tipo a virgola mobile) maggiore o uguale al parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="3acc4-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="3acc4-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="3acc4-114">Type Description</span></span>



| <span data-ttu-id="3acc4-115">Nome</span><span class="sxs-lookup"><span data-stu-id="3acc4-115">Name</span></span>  | [<span data-ttu-id="3acc4-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="3acc4-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3acc4-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="3acc4-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3acc4-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3acc4-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3acc4-119">*x*</span><span class="sxs-lookup"><span data-stu-id="3acc4-119">*x*</span></span>   | <span data-ttu-id="3acc4-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="3acc4-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3acc4-121">**float**</span><span class="sxs-lookup"><span data-stu-id="3acc4-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3acc4-122">any</span><span class="sxs-lookup"><span data-stu-id="3acc4-122">any</span></span>                            |
| <span data-ttu-id="3acc4-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="3acc4-123">*ret*</span></span> | <span data-ttu-id="3acc4-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="3acc4-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3acc4-125">**float**</span><span class="sxs-lookup"><span data-stu-id="3acc4-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3acc4-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="3acc4-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3acc4-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3acc4-127">Minimum Shader Model</span></span>

<span data-ttu-id="3acc4-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3acc4-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3acc4-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3acc4-129">Shader Model</span></span>                                                                       | <span data-ttu-id="3acc4-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="3acc4-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3acc4-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="3acc4-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3acc4-132">sì</span><span class="sxs-lookup"><span data-stu-id="3acc4-132">yes</span></span>       |
| [<span data-ttu-id="3acc4-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3acc4-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3acc4-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3acc4-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="3acc4-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3acc4-135">Requirements</span></span>



| <span data-ttu-id="3acc4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3acc4-136">Requirement</span></span> | <span data-ttu-id="3acc4-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3acc4-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3acc4-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3acc4-138">Header</span></span><br/> | <dl> <span data-ttu-id="3acc4-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3acc4-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3acc4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3acc4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3acc4-141">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3acc4-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

