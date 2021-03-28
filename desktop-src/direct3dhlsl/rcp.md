---
title: rcp
description: Calcola un reciproco rapido, approssimativo, per componente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- HLSL RCP
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728194"
---
# <a name="rcp"></a><span data-ttu-id="21c49-104">rcp</span><span class="sxs-lookup"><span data-stu-id="21c49-104">rcp</span></span>

<span data-ttu-id="21c49-105">Calcola un reciproco rapido, approssimativo, per componente.</span><span class="sxs-lookup"><span data-stu-id="21c49-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="21c49-106">RCP *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="21c49-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="21c49-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="21c49-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c49-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="21c49-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="21c49-109">\[nel \] valore di input.</span><span class="sxs-lookup"><span data-stu-id="21c49-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21c49-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21c49-110">Return Value</span></span>

<span data-ttu-id="21c49-111">Reciproco del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="21c49-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="21c49-112">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="21c49-112">Type Description</span></span>



| <span data-ttu-id="21c49-113">Nome</span><span class="sxs-lookup"><span data-stu-id="21c49-113">Name</span></span>  | [<span data-ttu-id="21c49-114">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="21c49-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="21c49-115">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="21c49-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="21c49-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="21c49-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="21c49-117">*x*</span><span class="sxs-lookup"><span data-stu-id="21c49-117">*x*</span></span>   | <span data-ttu-id="21c49-118">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="21c49-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="21c49-119">[**float**](/windows/desktop/WinProg/windows-data-types) o [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="21c49-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="21c49-120">any</span><span class="sxs-lookup"><span data-stu-id="21c49-120">any</span></span>                            |
| <span data-ttu-id="21c49-121">*RET*</span><span class="sxs-lookup"><span data-stu-id="21c49-121">*ret*</span></span> | <span data-ttu-id="21c49-122">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="21c49-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="21c49-123">[**float**](/windows/desktop/WinProg/windows-data-types) o [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="21c49-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="21c49-124">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="21c49-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="21c49-125">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="21c49-125">Minimum Shader Model</span></span>

<span data-ttu-id="21c49-126">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="21c49-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="21c49-127">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="21c49-127">Shader Model</span></span>                                                                | <span data-ttu-id="21c49-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="21c49-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="21c49-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="21c49-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="21c49-130">sì</span><span class="sxs-lookup"><span data-stu-id="21c49-130">yes</span></span>       |



 

<span data-ttu-id="21c49-131">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="21c49-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="21c49-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="21c49-132">Vertex</span></span> | <span data-ttu-id="21c49-133">Hull</span><span class="sxs-lookup"><span data-stu-id="21c49-133">Hull</span></span> | <span data-ttu-id="21c49-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="21c49-134">Domain</span></span> | <span data-ttu-id="21c49-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="21c49-135">Geometry</span></span> | <span data-ttu-id="21c49-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="21c49-136">Pixel</span></span> | <span data-ttu-id="21c49-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="21c49-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="21c49-138">x</span><span class="sxs-lookup"><span data-stu-id="21c49-138">x</span></span>      | <span data-ttu-id="21c49-139">x</span><span class="sxs-lookup"><span data-stu-id="21c49-139">x</span></span>    | <span data-ttu-id="21c49-140">x</span><span class="sxs-lookup"><span data-stu-id="21c49-140">x</span></span>      | <span data-ttu-id="21c49-141">x</span><span class="sxs-lookup"><span data-stu-id="21c49-141">x</span></span>        | <span data-ttu-id="21c49-142">x</span><span class="sxs-lookup"><span data-stu-id="21c49-142">x</span></span>     | <span data-ttu-id="21c49-143">x</span><span class="sxs-lookup"><span data-stu-id="21c49-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="21c49-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21c49-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c49-145">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="21c49-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="21c49-146">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="21c49-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 