---
title: exp
description: Restituisce l'esponenziale in base e, o ex, del valore specificato.
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- HLSL exp
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727858"
---
# <a name="exp"></a><span data-ttu-id="ffbaf-104">exp</span><span class="sxs-lookup"><span data-stu-id="ffbaf-104">exp</span></span>

<span data-ttu-id="ffbaf-105">Restituisce l'esponenziale in base e la<sup>x</sup>e il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="ffbaf-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="ffbaf-106">exp *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="ffbaf-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="ffbaf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffbaf-107">Parameters</span></span>



| <span data-ttu-id="ffbaf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffbaf-108">Item</span></span>                                                   | <span data-ttu-id="ffbaf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffbaf-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ffbaf-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ffbaf-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ffbaf-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="ffbaf-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ffbaf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffbaf-112">Return Value</span></span>

<span data-ttu-id="ffbaf-113">Esponenziale in base e del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="ffbaf-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ffbaf-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="ffbaf-114">Type Description</span></span>



| <span data-ttu-id="ffbaf-115">Nome</span><span class="sxs-lookup"><span data-stu-id="ffbaf-115">Name</span></span>  | [<span data-ttu-id="ffbaf-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="ffbaf-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ffbaf-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="ffbaf-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ffbaf-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="ffbaf-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ffbaf-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ffbaf-119">*x*</span></span>   | <span data-ttu-id="ffbaf-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="ffbaf-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ffbaf-121">**float**</span><span class="sxs-lookup"><span data-stu-id="ffbaf-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ffbaf-122">any</span><span class="sxs-lookup"><span data-stu-id="ffbaf-122">any</span></span>                            |
| <span data-ttu-id="ffbaf-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="ffbaf-123">*ret*</span></span> | <span data-ttu-id="ffbaf-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="ffbaf-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ffbaf-125">**float**</span><span class="sxs-lookup"><span data-stu-id="ffbaf-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ffbaf-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="ffbaf-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ffbaf-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="ffbaf-127">Minimum Shader Model</span></span>

<span data-ttu-id="ffbaf-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ffbaf-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ffbaf-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ffbaf-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ffbaf-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="ffbaf-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ffbaf-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="ffbaf-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ffbaf-132">sì</span><span class="sxs-lookup"><span data-stu-id="ffbaf-132">yes</span></span>       |
| [<span data-ttu-id="ffbaf-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffbaf-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ffbaf-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ffbaf-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="ffbaf-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffbaf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbaf-136">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ffbaf-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

