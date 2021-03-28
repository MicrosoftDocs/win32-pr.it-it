---
title: normalizzare
description: Normalizza il vettore a virgola mobile specificato in base alla x/lunghezza (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- Normalizza HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963425"
---
# <a name="normalize"></a><span data-ttu-id="5c0de-104">normalizzare</span><span class="sxs-lookup"><span data-stu-id="5c0de-104">normalize</span></span>

<span data-ttu-id="5c0de-105">Normalizza il vettore a virgola mobile specificato in base alla x/lunghezza (x).</span><span class="sxs-lookup"><span data-stu-id="5c0de-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="5c0de-106">normalizzazione *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="5c0de-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="5c0de-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c0de-107">Parameters</span></span>



| <span data-ttu-id="5c0de-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c0de-108">Item</span></span>                                                   | <span data-ttu-id="5c0de-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c0de-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="5c0de-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="5c0de-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5c0de-111">\[nel \] vettore a virgola mobile specificato.</span><span class="sxs-lookup"><span data-stu-id="5c0de-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5c0de-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c0de-112">Return Value</span></span>

<span data-ttu-id="5c0de-113">Parametro *x* normalizzato.</span><span class="sxs-lookup"><span data-stu-id="5c0de-113">The normalized *x* parameter.</span></span> <span data-ttu-id="5c0de-114">Se la lunghezza del parametro *x* è 0, il risultato è indefinito.</span><span class="sxs-lookup"><span data-stu-id="5c0de-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c0de-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c0de-115">Remarks</span></span>

<span data-ttu-id="5c0de-116">La funzione intrinseca HLSL **Normalize** usa la formula seguente: *x*  /  [**length**](dx-graphics-hlsl-length.md)(*x*).</span><span class="sxs-lookup"><span data-stu-id="5c0de-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="5c0de-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="5c0de-117">Type Description</span></span>



| <span data-ttu-id="5c0de-118">Nome</span><span class="sxs-lookup"><span data-stu-id="5c0de-118">Name</span></span>  | [<span data-ttu-id="5c0de-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="5c0de-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="5c0de-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="5c0de-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5c0de-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="5c0de-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5c0de-122">*x*</span><span class="sxs-lookup"><span data-stu-id="5c0de-122">*x*</span></span>   | [<span data-ttu-id="5c0de-123">**vettore**</span><span class="sxs-lookup"><span data-stu-id="5c0de-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5c0de-124">**float**</span><span class="sxs-lookup"><span data-stu-id="5c0de-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5c0de-125">any</span><span class="sxs-lookup"><span data-stu-id="5c0de-125">any</span></span>                            |
| <span data-ttu-id="5c0de-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="5c0de-126">*ret*</span></span> | <span data-ttu-id="5c0de-127">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="5c0de-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="5c0de-128">**float**</span><span class="sxs-lookup"><span data-stu-id="5c0de-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5c0de-129">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="5c0de-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c0de-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5c0de-130">Minimum Shader Model</span></span>

<span data-ttu-id="5c0de-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5c0de-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5c0de-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5c0de-132">Shader Model</span></span>                                                                       | <span data-ttu-id="5c0de-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="5c0de-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="5c0de-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati</span><span class="sxs-lookup"><span data-stu-id="5c0de-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5c0de-135">sì</span><span class="sxs-lookup"><span data-stu-id="5c0de-135">yes</span></span>                 |
| [<span data-ttu-id="5c0de-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c0de-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5c0de-137">Sì ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="5c0de-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="5c0de-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c0de-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c0de-139">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5c0de-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

