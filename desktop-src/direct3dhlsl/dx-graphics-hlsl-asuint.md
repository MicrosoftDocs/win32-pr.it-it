---
title: asuint
description: Interpreta lo schema di bit di x come Unsigned Integer.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- HLSL asuint
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976799"
---
# <a name="asuint"></a><span data-ttu-id="47bda-104">asuint</span><span class="sxs-lookup"><span data-stu-id="47bda-104">asuint</span></span>

<span data-ttu-id="47bda-105">Interpreta lo schema di bit di *x* come Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="47bda-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="47bda-106">asuint RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="47bda-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="47bda-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="47bda-107">Parameters</span></span>



| <span data-ttu-id="47bda-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="47bda-108">Item</span></span>                                                   | <span data-ttu-id="47bda-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47bda-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="47bda-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="47bda-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="47bda-111">\[nel \] valore di input.</span><span class="sxs-lookup"><span data-stu-id="47bda-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="47bda-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47bda-112">Return Value</span></span>

<span data-ttu-id="47bda-113">Input interpretato come Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="47bda-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="47bda-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="47bda-114">Type Description</span></span>



| <span data-ttu-id="47bda-115">Nome</span><span class="sxs-lookup"><span data-stu-id="47bda-115">Name</span></span>  | [<span data-ttu-id="47bda-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="47bda-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="47bda-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="47bda-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="47bda-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="47bda-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="47bda-119">*x*</span><span class="sxs-lookup"><span data-stu-id="47bda-119">*x*</span></span>   | <span data-ttu-id="47bda-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="47bda-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="47bda-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="47bda-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="47bda-122">any</span><span class="sxs-lookup"><span data-stu-id="47bda-122">any</span></span>                            |
| <span data-ttu-id="47bda-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="47bda-123">*ret*</span></span> | <span data-ttu-id="47bda-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="47bda-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="47bda-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="47bda-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="47bda-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="47bda-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47bda-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="47bda-127">Minimum Shader Model</span></span>

<span data-ttu-id="47bda-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="47bda-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="47bda-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="47bda-129">Shader Model</span></span>                                                        | <span data-ttu-id="47bda-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="47bda-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="47bda-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="47bda-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="47bda-132">sì</span><span class="sxs-lookup"><span data-stu-id="47bda-132">yes</span></span>       |
| [<span data-ttu-id="47bda-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47bda-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="47bda-134">no</span><span class="sxs-lookup"><span data-stu-id="47bda-134">no</span></span>        |
| [<span data-ttu-id="47bda-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47bda-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="47bda-136">no</span><span class="sxs-lookup"><span data-stu-id="47bda-136">no</span></span>        |
| [<span data-ttu-id="47bda-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47bda-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="47bda-138">no</span><span class="sxs-lookup"><span data-stu-id="47bda-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="47bda-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47bda-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47bda-140">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="47bda-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

