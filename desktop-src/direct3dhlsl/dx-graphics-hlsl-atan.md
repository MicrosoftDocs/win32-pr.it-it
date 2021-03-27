---
title: atan
description: Restituisce l'arcotangente del valore specificato.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- HLSL Atan
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727866"
---
# <a name="atan"></a><span data-ttu-id="3888c-104">atan</span><span class="sxs-lookup"><span data-stu-id="3888c-104">atan</span></span>

<span data-ttu-id="3888c-105">Restituisce l'arcotangente del valore specificato.</span><span class="sxs-lookup"><span data-stu-id="3888c-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="3888c-106">atan *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="3888c-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="3888c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3888c-107">Parameters</span></span>



| <span data-ttu-id="3888c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3888c-108">Item</span></span>                                                   | <span data-ttu-id="3888c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3888c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="3888c-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="3888c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3888c-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="3888c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3888c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3888c-112">Return Value</span></span>

<span data-ttu-id="3888c-113">Arcotangente del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="3888c-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="3888c-114">Questo valore è compreso nell'intervallo tra-π/2 e π/2.</span><span class="sxs-lookup"><span data-stu-id="3888c-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="3888c-115">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="3888c-115">Type Description</span></span>



| <span data-ttu-id="3888c-116">Nome</span><span class="sxs-lookup"><span data-stu-id="3888c-116">Name</span></span>  | [<span data-ttu-id="3888c-117">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="3888c-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3888c-118">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="3888c-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3888c-119">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3888c-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3888c-120">*x*</span><span class="sxs-lookup"><span data-stu-id="3888c-120">*x*</span></span>   | <span data-ttu-id="3888c-121">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="3888c-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3888c-122">**float**</span><span class="sxs-lookup"><span data-stu-id="3888c-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3888c-123">any</span><span class="sxs-lookup"><span data-stu-id="3888c-123">any</span></span>                            |
| <span data-ttu-id="3888c-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="3888c-124">*ret*</span></span> | <span data-ttu-id="3888c-125">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="3888c-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3888c-126">**float**</span><span class="sxs-lookup"><span data-stu-id="3888c-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3888c-127">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="3888c-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3888c-128">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="3888c-128">Minimum Shader Model</span></span>

<span data-ttu-id="3888c-129">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="3888c-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3888c-130">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="3888c-130">Shader Model</span></span>                                                                       | <span data-ttu-id="3888c-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="3888c-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3888c-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="3888c-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3888c-133">sì</span><span class="sxs-lookup"><span data-stu-id="3888c-133">yes</span></span>       |
| [<span data-ttu-id="3888c-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3888c-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3888c-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3888c-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="3888c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3888c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3888c-137">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3888c-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

