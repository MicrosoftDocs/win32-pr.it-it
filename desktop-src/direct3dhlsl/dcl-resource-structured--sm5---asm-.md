---
title: struttura dcl_resource (SM5-ASM)
description: Dichiarare un input di risorsa shader e assegnarlo a un registro segnaposto t \-a per la risorsa. | struttura dcl_resource (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234685"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="a3640-104">\_struttura della risorsa DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a3640-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="a3640-105">Dichiarare un input di risorsa dello shader e assegnarlo a un \# Registro di segnaposto t-a per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a3640-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="a3640-106">\_ \_ dstSRV strutturato delle risorse DCL, structByteStride</span><span class="sxs-lookup"><span data-stu-id="a3640-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="a3640-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a3640-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="a3640-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3640-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3640-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="a3640-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="a3640-110">\[in \] un \# Registro t dichiarato come riferimento a un ShaderResourceView di un buffer strutturato con lo stride specificato che deve essere associato allo slot SRV \# nell'API.</span><span class="sxs-lookup"><span data-stu-id="a3640-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="a3640-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="a3640-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="a3640-112">\[in \] un uint che specifica la dimensione della struttura in byte nel buffer dichiarato.</span><span class="sxs-lookup"><span data-stu-id="a3640-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="a3640-113">Il valore deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="a3640-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="a3640-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3640-114">Remarks</span></span>

<span data-ttu-id="a3640-115">Il contenuto della struttura non è di tipo; le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.</span><span class="sxs-lookup"><span data-stu-id="a3640-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="a3640-116">Le istruzioni che fanno riferimento a un'istruzione t strutturata \# accettano un indirizzo 2D, dove il primo componente sceglie lo \[ struct \] e il secondo componente sceglie \[ offset all'interno dello struct, più di 32 bit \] .</span><span class="sxs-lookup"><span data-stu-id="a3640-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="a3640-117">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="a3640-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="a3640-118">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3640-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a3640-119">Vertice</span><span class="sxs-lookup"><span data-stu-id="a3640-119">Vertex</span></span> | <span data-ttu-id="a3640-120">Hull</span><span class="sxs-lookup"><span data-stu-id="a3640-120">Hull</span></span> | <span data-ttu-id="a3640-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="a3640-121">Domain</span></span> | <span data-ttu-id="a3640-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="a3640-122">Geometry</span></span> | <span data-ttu-id="a3640-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="a3640-123">Pixel</span></span> | <span data-ttu-id="a3640-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a3640-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a3640-125">X</span><span class="sxs-lookup"><span data-stu-id="a3640-125">X</span></span>      | <span data-ttu-id="a3640-126">X</span><span class="sxs-lookup"><span data-stu-id="a3640-126">X</span></span>    | <span data-ttu-id="a3640-127">X</span><span class="sxs-lookup"><span data-stu-id="a3640-127">X</span></span>      | <span data-ttu-id="a3640-128">X</span><span class="sxs-lookup"><span data-stu-id="a3640-128">X</span></span>        | <span data-ttu-id="a3640-129">X</span><span class="sxs-lookup"><span data-stu-id="a3640-129">X</span></span>     | <span data-ttu-id="a3640-130">X</span><span class="sxs-lookup"><span data-stu-id="a3640-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a3640-131">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="a3640-131">Minimum Shader Model</span></span>

<span data-ttu-id="a3640-132">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3640-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a3640-133">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="a3640-133">Shader Model</span></span>                                              | <span data-ttu-id="a3640-134">Supportato</span><span class="sxs-lookup"><span data-stu-id="a3640-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a3640-135">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="a3640-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a3640-136">sì</span><span class="sxs-lookup"><span data-stu-id="a3640-136">yes</span></span>       |
| [<span data-ttu-id="a3640-137">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="a3640-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a3640-138">no</span><span class="sxs-lookup"><span data-stu-id="a3640-138">no</span></span>        |
| [<span data-ttu-id="a3640-139">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="a3640-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a3640-140">no</span><span class="sxs-lookup"><span data-stu-id="a3640-140">no</span></span>        |
| [<span data-ttu-id="a3640-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a3640-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a3640-142">no</span><span class="sxs-lookup"><span data-stu-id="a3640-142">no</span></span>        |
| [<span data-ttu-id="a3640-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a3640-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a3640-144">no</span><span class="sxs-lookup"><span data-stu-id="a3640-144">no</span></span>        |
| [<span data-ttu-id="a3640-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a3640-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a3640-146">no</span><span class="sxs-lookup"><span data-stu-id="a3640-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a3640-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3640-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3640-148">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a3640-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





