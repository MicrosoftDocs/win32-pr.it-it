---
title: AsFloat
description: Interpreta lo schema di bit di x come numero a virgola mobile.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- HLSL AsFloat
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993533"
---
# <a name="asfloat"></a><span data-ttu-id="4c34a-104">AsFloat</span><span class="sxs-lookup"><span data-stu-id="4c34a-104">asfloat</span></span>

<span data-ttu-id="4c34a-105">Interpreta lo schema di bit di *x* come numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="4c34a-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="4c34a-106">AsFloat RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="4c34a-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="4c34a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c34a-107">Parameters</span></span>



| <span data-ttu-id="4c34a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c34a-108">Item</span></span>                                                   | <span data-ttu-id="4c34a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c34a-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="4c34a-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4c34a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4c34a-111">\[nel \] valore di input.</span><span class="sxs-lookup"><span data-stu-id="4c34a-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4c34a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c34a-112">Return Value</span></span>

<span data-ttu-id="4c34a-113">Input interpretato come numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="4c34a-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="4c34a-114">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="4c34a-114">Type Description</span></span>



| <span data-ttu-id="4c34a-115">Nome</span><span class="sxs-lookup"><span data-stu-id="4c34a-115">Name</span></span>  | [<span data-ttu-id="4c34a-116">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="4c34a-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4c34a-117">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="4c34a-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="4c34a-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="4c34a-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4c34a-119">*x*</span><span class="sxs-lookup"><span data-stu-id="4c34a-119">*x*</span></span>   | <span data-ttu-id="4c34a-120">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="4c34a-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="4c34a-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4c34a-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="4c34a-122">any</span><span class="sxs-lookup"><span data-stu-id="4c34a-122">any</span></span>                            |
| <span data-ttu-id="4c34a-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="4c34a-123">*ret*</span></span> | <span data-ttu-id="4c34a-124">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="4c34a-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4c34a-125">**float**</span><span class="sxs-lookup"><span data-stu-id="4c34a-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="4c34a-126">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="4c34a-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="4c34a-127">Overload di funzioni</span><span class="sxs-lookup"><span data-stu-id="4c34a-127">Function Overloads</span></span>

<dl> <span data-ttu-id="4c34a-128">' float <x> AsFloat ( <x> valore float); `  
` float <x> AsFloat ( <x> valore int); `  
` float <x> AsFloat ( <x> valore uint);'</span><span class="sxs-lookup"><span data-stu-id="4c34a-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="4c34a-129">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4c34a-129">Minimum Shader Model</span></span>

<span data-ttu-id="4c34a-130">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c34a-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4c34a-131">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4c34a-131">Shader Model</span></span>                                                        | <span data-ttu-id="4c34a-132">Supportato</span><span class="sxs-lookup"><span data-stu-id="4c34a-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="4c34a-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="4c34a-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="4c34a-134">sì</span><span class="sxs-lookup"><span data-stu-id="4c34a-134">yes</span></span>       |
| [<span data-ttu-id="4c34a-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c34a-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="4c34a-136">no</span><span class="sxs-lookup"><span data-stu-id="4c34a-136">no</span></span>        |
| [<span data-ttu-id="4c34a-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c34a-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="4c34a-138">no</span><span class="sxs-lookup"><span data-stu-id="4c34a-138">no</span></span>        |
| [<span data-ttu-id="4c34a-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c34a-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="4c34a-140">no</span><span class="sxs-lookup"><span data-stu-id="4c34a-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="4c34a-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c34a-141">Remarks</span></span>

<span data-ttu-id="4c34a-142">I compilatori meno recenti non sono consentiti correttamente `asfloat(bool)` , ma si noti che gli input bool non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="4c34a-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c34a-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c34a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c34a-144">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4c34a-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

