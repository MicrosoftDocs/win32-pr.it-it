---
title: AsInt
description: Interpreta lo schema di bit di x come valore integer.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- AsInt HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047134"
---
# <a name="asint"></a><span data-ttu-id="c9160-104">AsInt</span><span class="sxs-lookup"><span data-stu-id="c9160-104">asint</span></span>

<span data-ttu-id="c9160-105">Interpreta lo schema di bit di *x* come valore integer.</span><span class="sxs-lookup"><span data-stu-id="c9160-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="c9160-106">asina RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="c9160-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="c9160-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9160-107">Parameters</span></span>



| <span data-ttu-id="c9160-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9160-108">Item</span></span>                                                   | <span data-ttu-id="c9160-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9160-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="c9160-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="c9160-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c9160-111">\[nel \] valore di input.</span><span class="sxs-lookup"><span data-stu-id="c9160-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c9160-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9160-112">Return Value</span></span>

<span data-ttu-id="c9160-113">Input interpretato come Integer.</span><span class="sxs-lookup"><span data-stu-id="c9160-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="c9160-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="c9160-114">Type Description</span></span>



| <span data-ttu-id="c9160-115">Nome</span><span class="sxs-lookup"><span data-stu-id="c9160-115">Name</span></span>  | [<span data-ttu-id="c9160-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="c9160-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c9160-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="c9160-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="c9160-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="c9160-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c9160-119">*x*</span><span class="sxs-lookup"><span data-stu-id="c9160-119">*x*</span></span>   | <span data-ttu-id="c9160-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="c9160-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="c9160-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c9160-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c9160-122">any</span><span class="sxs-lookup"><span data-stu-id="c9160-122">any</span></span>                            |
| <span data-ttu-id="c9160-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="c9160-123">*ret*</span></span> | <span data-ttu-id="c9160-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="c9160-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c9160-125">**INT**</span><span class="sxs-lookup"><span data-stu-id="c9160-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="c9160-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="c9160-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9160-127">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c9160-127">Minimum Shader Model</span></span>

<span data-ttu-id="c9160-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9160-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9160-129">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c9160-129">Shader Model</span></span>                                                        | <span data-ttu-id="c9160-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="c9160-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="c9160-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="c9160-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="c9160-132">sì</span><span class="sxs-lookup"><span data-stu-id="c9160-132">yes</span></span>       |
| [<span data-ttu-id="c9160-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9160-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="c9160-134">no</span><span class="sxs-lookup"><span data-stu-id="c9160-134">no</span></span>        |
| [<span data-ttu-id="c9160-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9160-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="c9160-136">no</span><span class="sxs-lookup"><span data-stu-id="c9160-136">no</span></span>        |
| [<span data-ttu-id="c9160-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9160-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="c9160-138">no</span><span class="sxs-lookup"><span data-stu-id="c9160-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="c9160-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9160-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9160-140">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c9160-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

