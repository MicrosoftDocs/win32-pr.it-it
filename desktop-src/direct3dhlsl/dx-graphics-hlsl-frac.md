---
title: Frac
description: Restituisce la parte frazionaria (o decimale) di x; che è maggiore o uguale a 0 e minore di 1.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- HLSL frac
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474110"
---
# <a name="frac"></a><span data-ttu-id="018e2-104">Frac</span><span class="sxs-lookup"><span data-stu-id="018e2-104">frac</span></span>

<span data-ttu-id="018e2-105">Restituisce la parte frazionaria (o decimale) di x; che è maggiore o uguale a 0 e minore di 1.</span><span class="sxs-lookup"><span data-stu-id="018e2-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="018e2-106">Vedere anche [Tronca](./dx-graphics-hlsl-trunc.md).</span><span class="sxs-lookup"><span data-stu-id="018e2-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="018e2-107">Frac *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="018e2-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="018e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="018e2-108">Parameters</span></span>



| <span data-ttu-id="018e2-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="018e2-109">Item</span></span>                                                   | <span data-ttu-id="018e2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="018e2-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="018e2-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="018e2-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="018e2-112">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="018e2-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="018e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="018e2-113">Return Value</span></span>

<span data-ttu-id="018e2-114">Parte frazionaria del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="018e2-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="018e2-115">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="018e2-115">Type Description</span></span>



| <span data-ttu-id="018e2-116">Nome</span><span class="sxs-lookup"><span data-stu-id="018e2-116">Name</span></span>  | [<span data-ttu-id="018e2-117">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="018e2-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="018e2-118">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="018e2-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="018e2-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="018e2-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="018e2-120">*x*</span><span class="sxs-lookup"><span data-stu-id="018e2-120">*x*</span></span>   | <span data-ttu-id="018e2-121">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="018e2-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="018e2-122">**float**</span><span class="sxs-lookup"><span data-stu-id="018e2-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="018e2-123">any</span><span class="sxs-lookup"><span data-stu-id="018e2-123">any</span></span>                            |
| <span data-ttu-id="018e2-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="018e2-124">*ret*</span></span> | <span data-ttu-id="018e2-125">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="018e2-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="018e2-126">**float**</span><span class="sxs-lookup"><span data-stu-id="018e2-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="018e2-127">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="018e2-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="018e2-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="018e2-128">Minimum Shader Model</span></span>

<span data-ttu-id="018e2-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="018e2-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="018e2-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="018e2-130">Shader Model</span></span>                                                                       | <span data-ttu-id="018e2-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="018e2-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="018e2-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="018e2-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="018e2-133">sì</span><span class="sxs-lookup"><span data-stu-id="018e2-133">yes</span></span>       |
| [<span data-ttu-id="018e2-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="018e2-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="018e2-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="018e2-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="018e2-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="018e2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018e2-137">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="018e2-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

