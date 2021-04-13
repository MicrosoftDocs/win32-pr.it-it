---
title: ddy
description: Restituisce la derivazione parziale del valore specificato rispetto alla coordinata y dello spazio dello schermo.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- HLSL ddy
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399216"
---
# <a name="ddy"></a><span data-ttu-id="cb2fc-104">ddy</span><span class="sxs-lookup"><span data-stu-id="cb2fc-104">ddy</span></span>

<span data-ttu-id="cb2fc-105">Restituisce la derivazione parziale del valore specificato rispetto alla coordinata y dello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-105">Returns the partial derivative of the specified value with respect to the screen-space y-coordinate.</span></span>



| <span data-ttu-id="cb2fc-106">ddy *ret* (*x*)</span><span class="sxs-lookup"><span data-stu-id="cb2fc-106">*ret* ddy(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="cb2fc-107">Questa funzione calcola la derivazione parziale per quanto riguarda la coordinata y dello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-107">This function computes the partial derivative with respect to the screen-space y-coordinate.</span></span> <span data-ttu-id="cb2fc-108">Per calcolare la derivazione parziale per quanto riguarda la coordinata x dello spazio dello schermo, utilizzare la funzione [**DDX**](dx-graphics-hlsl-ddx.md) .</span><span class="sxs-lookup"><span data-stu-id="cb2fc-108">To compute the partial derivative with respect to the screen-space x-coordinate, use the [**ddx**](dx-graphics-hlsl-ddx.md) function.</span></span>

<span data-ttu-id="cb2fc-109">Questa funzione è supportata solo in pixel shader.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb2fc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb2fc-110">Parameters</span></span>



| <span data-ttu-id="cb2fc-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="cb2fc-111">Item</span></span>                                                   | <span data-ttu-id="cb2fc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb2fc-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="cb2fc-113"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="cb2fc-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="cb2fc-114">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="cb2fc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb2fc-115">Return Value</span></span>

<span data-ttu-id="cb2fc-116">Derivato parziale del parametro *x* .</span><span class="sxs-lookup"><span data-stu-id="cb2fc-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="cb2fc-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="cb2fc-117">Type Description</span></span>



| <span data-ttu-id="cb2fc-118">Nome</span><span class="sxs-lookup"><span data-stu-id="cb2fc-118">Name</span></span>  | [<span data-ttu-id="cb2fc-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="cb2fc-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="cb2fc-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="cb2fc-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="cb2fc-122">*x*</span><span class="sxs-lookup"><span data-stu-id="cb2fc-122">*x*</span></span>   | <span data-ttu-id="cb2fc-123">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="cb2fc-124">**float**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="cb2fc-125">any</span><span class="sxs-lookup"><span data-stu-id="cb2fc-125">any</span></span>                            |
| <span data-ttu-id="cb2fc-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="cb2fc-126">*ret*</span></span> | <span data-ttu-id="cb2fc-127">uguale all'input *x*</span><span class="sxs-lookup"><span data-stu-id="cb2fc-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="cb2fc-128">**float**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="cb2fc-129">le stesse dimensioni di input *x*</span><span class="sxs-lookup"><span data-stu-id="cb2fc-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cb2fc-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="cb2fc-130">Minimum Shader Model</span></span>

<span data-ttu-id="cb2fc-131">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cb2fc-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="cb2fc-132">Shader Model</span></span>                                                                | <span data-ttu-id="cb2fc-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="cb2fc-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="cb2fc-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="cb2fc-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="cb2fc-135">sì</span><span class="sxs-lookup"><span data-stu-id="cb2fc-135">yes</span></span>                                       |
| [<span data-ttu-id="cb2fc-136">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="cb2fc-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="cb2fc-137">sì</span><span class="sxs-lookup"><span data-stu-id="cb2fc-137">yes</span></span>                                       |
| [<span data-ttu-id="cb2fc-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb2fc-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="cb2fc-139">sì</span><span class="sxs-lookup"><span data-stu-id="cb2fc-139">yes</span></span>                                       |
| [<span data-ttu-id="cb2fc-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb2fc-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="cb2fc-141">Sì in PS \_ 2 \_ x; non supportato in PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="cb2fc-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="cb2fc-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb2fc-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="cb2fc-143">no</span><span class="sxs-lookup"><span data-stu-id="cb2fc-143">no</span></span>                                        |



 

<span data-ttu-id="cb2fc-144">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb2fc-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cb2fc-145">Vertice</span><span class="sxs-lookup"><span data-stu-id="cb2fc-145">Vertex</span></span> | <span data-ttu-id="cb2fc-146">Hull</span><span class="sxs-lookup"><span data-stu-id="cb2fc-146">Hull</span></span> | <span data-ttu-id="cb2fc-147">Dominio</span><span class="sxs-lookup"><span data-stu-id="cb2fc-147">Domain</span></span> | <span data-ttu-id="cb2fc-148">Geometria</span><span class="sxs-lookup"><span data-stu-id="cb2fc-148">Geometry</span></span> | <span data-ttu-id="cb2fc-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="cb2fc-149">Pixel</span></span> | <span data-ttu-id="cb2fc-150">Calcolo</span><span class="sxs-lookup"><span data-stu-id="cb2fc-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cb2fc-151">x</span><span class="sxs-lookup"><span data-stu-id="cb2fc-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="cb2fc-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb2fc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2fc-153">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="cb2fc-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

