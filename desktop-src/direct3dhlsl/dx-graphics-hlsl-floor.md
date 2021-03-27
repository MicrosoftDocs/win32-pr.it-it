---
title: Floor (Corecrt \_ Math. h)
description: Restituisce l'intero più grande che è minore o uguale al valore specificato.
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- HLSL Floor
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982184"
---
# <a name="floor"></a><span data-ttu-id="a37b1-104">floor</span><span class="sxs-lookup"><span data-stu-id="a37b1-104">floor</span></span>

<span data-ttu-id="a37b1-105">Restituisce l'intero più grande che è minore o uguale al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="a37b1-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="a37b1-106">*ret* Floor (*x*)</span><span class="sxs-lookup"><span data-stu-id="a37b1-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="a37b1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a37b1-107">Parameters</span></span>



| <span data-ttu-id="a37b1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a37b1-108">Item</span></span>                                                   | <span data-ttu-id="a37b1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a37b1-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a37b1-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a37b1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a37b1-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="a37b1-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a37b1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a37b1-112">Return Value</span></span>

<span data-ttu-id="a37b1-113">Il valore integer più grande (restituito come tipo a virgola mobile) minore o uguale al parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="a37b1-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="a37b1-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="a37b1-114">Type Description</span></span>



| <span data-ttu-id="a37b1-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a37b1-115">Name</span></span>  | [<span data-ttu-id="a37b1-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="a37b1-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a37b1-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="a37b1-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a37b1-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a37b1-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a37b1-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a37b1-119">*x*</span></span>   | <span data-ttu-id="a37b1-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="a37b1-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a37b1-121">**float**</span><span class="sxs-lookup"><span data-stu-id="a37b1-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a37b1-122">any</span><span class="sxs-lookup"><span data-stu-id="a37b1-122">any</span></span>                            |
| <span data-ttu-id="a37b1-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="a37b1-123">*ret*</span></span> | <span data-ttu-id="a37b1-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="a37b1-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a37b1-125">**float**</span><span class="sxs-lookup"><span data-stu-id="a37b1-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a37b1-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="a37b1-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a37b1-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a37b1-127">Minimum Shader Model</span></span>

<span data-ttu-id="a37b1-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="a37b1-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a37b1-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a37b1-129">Shader Model</span></span>                                                                       | <span data-ttu-id="a37b1-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="a37b1-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a37b1-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="a37b1-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a37b1-132">sì</span><span class="sxs-lookup"><span data-stu-id="a37b1-132">yes</span></span>       |
| [<span data-ttu-id="a37b1-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a37b1-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a37b1-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a37b1-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="a37b1-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a37b1-135">Requirements</span></span>



| <span data-ttu-id="a37b1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a37b1-136">Requirement</span></span> | <span data-ttu-id="a37b1-137">Valore</span><span class="sxs-lookup"><span data-stu-id="a37b1-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a37b1-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a37b1-138">Header</span></span><br/> | <dl> <span data-ttu-id="a37b1-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a37b1-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a37b1-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a37b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a37b1-141">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a37b1-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

