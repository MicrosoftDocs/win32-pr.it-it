---
title: dcl_resource RAW (SM5-ASM)
description: Dichiarare un input di risorsa shader e assegnarlo a un registro segnaposto t \-a per la risorsa. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234748"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="58d80-104">\_risorsa DCL RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="58d80-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="58d80-105">Dichiarare un input di risorsa dello shader e assegnarlo a un \# Registro di segnaposto t-a per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="58d80-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="58d80-106">\_dstSRV RAW delle risorse DCL \_</span><span class="sxs-lookup"><span data-stu-id="58d80-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="58d80-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="58d80-107">Item</span></span>                                                                                           | <span data-ttu-id="58d80-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58d80-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d80-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="58d80-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="58d80-110">\[in \] un \# Registro t dichiarato come riferimento a un ShaderResourceView di un buffer non elaborato.</span><span class="sxs-lookup"><span data-stu-id="58d80-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58d80-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="58d80-111">Remarks</span></span>

<span data-ttu-id="58d80-112">Il contenuto della struttura non è di tipo; le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.</span><span class="sxs-lookup"><span data-stu-id="58d80-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="58d80-113">Le istruzioni che fanno riferimento a una t non elaborata \# accettano un indirizzo 1D, un valore senza segno a 32 bit che specifica l'offset dei byte a una posizione allineata a 32 bit nel buffer.</span><span class="sxs-lookup"><span data-stu-id="58d80-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="58d80-114">L'indirizzo deve essere un multiplo di 4 (byte).</span><span class="sxs-lookup"><span data-stu-id="58d80-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="58d80-115">Le visualizzazioni vincolate a t \# dichiarate come RAW devono avere un valore RAW specificato durante la creazione; in caso contrario, il comportamento quando si accede da uno shader non è definito.</span><span class="sxs-lookup"><span data-stu-id="58d80-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="58d80-116">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="58d80-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="58d80-117">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="58d80-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="58d80-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="58d80-118">Vertex</span></span> | <span data-ttu-id="58d80-119">Hull</span><span class="sxs-lookup"><span data-stu-id="58d80-119">Hull</span></span> | <span data-ttu-id="58d80-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="58d80-120">Domain</span></span> | <span data-ttu-id="58d80-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="58d80-121">Geometry</span></span> | <span data-ttu-id="58d80-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="58d80-122">Pixel</span></span> | <span data-ttu-id="58d80-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="58d80-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="58d80-124">X</span><span class="sxs-lookup"><span data-stu-id="58d80-124">X</span></span>      | <span data-ttu-id="58d80-125">X</span><span class="sxs-lookup"><span data-stu-id="58d80-125">X</span></span>    | <span data-ttu-id="58d80-126">X</span><span class="sxs-lookup"><span data-stu-id="58d80-126">X</span></span>      | <span data-ttu-id="58d80-127">X</span><span class="sxs-lookup"><span data-stu-id="58d80-127">X</span></span>        | <span data-ttu-id="58d80-128">X</span><span class="sxs-lookup"><span data-stu-id="58d80-128">X</span></span>     | <span data-ttu-id="58d80-129">X</span><span class="sxs-lookup"><span data-stu-id="58d80-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="58d80-130">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="58d80-130">Minimum Shader Model</span></span>

<span data-ttu-id="58d80-131">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="58d80-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="58d80-132">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="58d80-132">Shader Model</span></span>                                              | <span data-ttu-id="58d80-133">Supportato</span><span class="sxs-lookup"><span data-stu-id="58d80-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="58d80-134">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="58d80-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="58d80-135">sì</span><span class="sxs-lookup"><span data-stu-id="58d80-135">yes</span></span>       |
| [<span data-ttu-id="58d80-136">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="58d80-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="58d80-137">no</span><span class="sxs-lookup"><span data-stu-id="58d80-137">no</span></span>        |
| [<span data-ttu-id="58d80-138">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="58d80-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="58d80-139">no</span><span class="sxs-lookup"><span data-stu-id="58d80-139">no</span></span>        |
| [<span data-ttu-id="58d80-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58d80-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="58d80-141">no</span><span class="sxs-lookup"><span data-stu-id="58d80-141">no</span></span>        |
| [<span data-ttu-id="58d80-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58d80-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="58d80-143">no</span><span class="sxs-lookup"><span data-stu-id="58d80-143">no</span></span>        |
| [<span data-ttu-id="58d80-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58d80-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="58d80-145">no</span><span class="sxs-lookup"><span data-stu-id="58d80-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="58d80-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58d80-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d80-147">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="58d80-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





