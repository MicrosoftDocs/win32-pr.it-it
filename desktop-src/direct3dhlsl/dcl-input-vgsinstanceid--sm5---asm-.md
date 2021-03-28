---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Abilita le istanze di Geometry shader.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335644"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="13fa3-103">\_vGSInstanceID di input DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="13fa3-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="13fa3-104">Abilita le istanze di Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="13fa3-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="13fa3-105">\_input DCL vGSInstanceID, instanceCount</span><span class="sxs-lookup"><span data-stu-id="13fa3-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="13fa3-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="13fa3-106">Item</span></span>                                                                                                                       | <span data-ttu-id="13fa3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13fa3-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="13fa3-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span><span class="sxs-lookup"><span data-stu-id="13fa3-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="13fa3-109">\[nell' \] ID istanza.</span><span class="sxs-lookup"><span data-stu-id="13fa3-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="13fa3-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="13fa3-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="13fa3-111">\[nel \] conteggio delle istanze.</span><span class="sxs-lookup"><span data-stu-id="13fa3-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13fa3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="13fa3-112">Remarks</span></span>

<span data-ttu-id="13fa3-113">Il parametro *instanceCount* della dichiarazione specifica il numero di istanze che il geometry shader deve eseguire per ogni primitiva di input.</span><span class="sxs-lookup"><span data-stu-id="13fa3-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="13fa3-114">Il valore massimo per *instanceCount* è 32.</span><span class="sxs-lookup"><span data-stu-id="13fa3-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="13fa3-115">Il numero massimo di vertici dichiarati per l'output, tramite [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), viene applicato singolarmente a ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="13fa3-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="13fa3-116">Il numero di istanze in questa dichiarazione, moltiplicato per il numero massimo di vertici per istanza tramite [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), deve essere <= 1024.</span><span class="sxs-lookup"><span data-stu-id="13fa3-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="13fa3-117">La quantità di dati che una data istanza geometry shader può emettere è 1024 scalari massimi, convalidata contando tutti i scalari dichiarati per l'input e moltiplicando il numero di vertici di output dichiarati.</span><span class="sxs-lookup"><span data-stu-id="13fa3-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="13fa3-118">L'uso delle istanze di Geometry shader aumenta in modo efficace la quantità totale di dati che possono essere emessi per primitive di input.</span><span class="sxs-lookup"><span data-stu-id="13fa3-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="13fa3-119">1024 scalars per una singola istanza restituisce fino a 1024 \* 32 scalari di dati di output in tutte le istanze di Geometry shader per una singola primitiva di input.</span><span class="sxs-lookup"><span data-stu-id="13fa3-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="13fa3-120">Tuttavia, più istanze, minore è il numero di vertici che ogni istanza può emettere.</span><span class="sxs-lookup"><span data-stu-id="13fa3-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="13fa3-121">Una singola istanza (nessuna istanza) può emettere 1024 vertici.</span><span class="sxs-lookup"><span data-stu-id="13fa3-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="13fa3-122">Se si dichiara \* 32 istanze significa che ogni istanza può restituire solo i vertici 1024/32 = 32.</span><span class="sxs-lookup"><span data-stu-id="13fa3-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="13fa3-123">La dichiarazione di creazione di istanze di Geometry shader rende disponibile al programma un registro di input di tipo Integer a 32 bit autonomo, *vGSInstanceID*.</span><span class="sxs-lookup"><span data-stu-id="13fa3-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="13fa3-124">Ogni istanza geometry shader è identificata dal valore contenuto in *vGSInstanceID* \[ 0, 1, 2... \] .</span><span class="sxs-lookup"><span data-stu-id="13fa3-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="13fa3-125">*vGSInstanceID* non fa parte della matrice di vertici di input geometry shader, ad esempio 3 vertici quando si inserisce un triangolo.</span><span class="sxs-lookup"><span data-stu-id="13fa3-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="13fa3-126">Il registro *vGSInstanceID* si trova autonomamente, ad esempio vPrimitiveID.</span><span class="sxs-lookup"><span data-stu-id="13fa3-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="13fa3-127">Quando ogni istanza geometry shader termina, esiste una riduzione implicita nella topologia di output, quindi le istanze consecutive non dipendono l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="13fa3-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="13fa3-128">Anche se l'hardware può eseguire ogni istanza geometry shader in parallelo, l'output di tutte le istanze alla fine viene serializzato come se tutte le chiamate geometry shader dell'istanza venissero eseguite in sequenza in un'iterazione del ciclo *vGSInstanceID* da 0 a *instanceCount*-1, con tagli della topologia di output impliciti alla fine di ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="13fa3-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="13fa3-129">Questa istruzione si applica alle fasi dello shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="13fa3-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="13fa3-130">Vertice</span><span class="sxs-lookup"><span data-stu-id="13fa3-130">Vertex</span></span> | <span data-ttu-id="13fa3-131">Hull</span><span class="sxs-lookup"><span data-stu-id="13fa3-131">Hull</span></span> | <span data-ttu-id="13fa3-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="13fa3-132">Domain</span></span> | <span data-ttu-id="13fa3-133">Geometria</span><span class="sxs-lookup"><span data-stu-id="13fa3-133">Geometry</span></span> | <span data-ttu-id="13fa3-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="13fa3-134">Pixel</span></span> | <span data-ttu-id="13fa3-135">Calcolo</span><span class="sxs-lookup"><span data-stu-id="13fa3-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="13fa3-136">X</span><span class="sxs-lookup"><span data-stu-id="13fa3-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="13fa3-137">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="13fa3-137">Minimum Shader Model</span></span>

<span data-ttu-id="13fa3-138">Questa istruzione è supportata nei modelli shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="13fa3-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="13fa3-139">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="13fa3-139">Shader Model</span></span>                                              | <span data-ttu-id="13fa3-140">Supportato</span><span class="sxs-lookup"><span data-stu-id="13fa3-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="13fa3-141">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="13fa3-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="13fa3-142">sì</span><span class="sxs-lookup"><span data-stu-id="13fa3-142">yes</span></span>       |
| [<span data-ttu-id="13fa3-143">Modello Shader 4,1</span><span class="sxs-lookup"><span data-stu-id="13fa3-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="13fa3-144">no</span><span class="sxs-lookup"><span data-stu-id="13fa3-144">no</span></span>        |
| [<span data-ttu-id="13fa3-145">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="13fa3-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="13fa3-146">no</span><span class="sxs-lookup"><span data-stu-id="13fa3-146">no</span></span>        |
| [<span data-ttu-id="13fa3-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13fa3-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="13fa3-148">no</span><span class="sxs-lookup"><span data-stu-id="13fa3-148">no</span></span>        |
| [<span data-ttu-id="13fa3-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13fa3-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="13fa3-150">no</span><span class="sxs-lookup"><span data-stu-id="13fa3-150">no</span></span>        |
| [<span data-ttu-id="13fa3-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13fa3-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="13fa3-152">no</span><span class="sxs-lookup"><span data-stu-id="13fa3-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="13fa3-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13fa3-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13fa3-154">Assembly Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13fa3-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





