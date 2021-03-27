---
title: Modelli shader rispetto ai profili shader
description: Modelli shader rispetto ai profili shader
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856677"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="63467-103">Modelli shader rispetto ai profili shader</span><span class="sxs-lookup"><span data-stu-id="63467-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="63467-104">Il linguaggio di ombreggiatura di alto livello per DirectX implementa una serie di modelli shader.</span><span class="sxs-lookup"><span data-stu-id="63467-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="63467-105">Con HLSL è possibile creare shader programmabili di tipo C per la pipeline Direct3D.</span><span class="sxs-lookup"><span data-stu-id="63467-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="63467-106">Ogni modello di shader si basa sul funzionalità del modello prima di esso, implementando una maggiore funzionalità con meno restrizioni.</span><span class="sxs-lookup"><span data-stu-id="63467-106">Each shader model builds on the capabilites of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="63467-107">Il modello di shader 1 è stato avviato con DirectX 8 ed è stato incluso il livello di assembly e le istruzioni di tipo C.</span><span class="sxs-lookup"><span data-stu-id="63467-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="63467-108">Questo modello presenta molte limitazioni dovute all'hardware Shader programmabile.</span><span class="sxs-lookup"><span data-stu-id="63467-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="63467-109">Il modello di shader 2 e 3 si espande notevolmente sul numero di istruzioni e le costanti shader possono usare.</span><span class="sxs-lookup"><span data-stu-id="63467-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="63467-110">Sono molto più potenti rispetto al modello di shader 1, ma presentano comunque alcune delle limitazioni esistenti del primo modello di shader.</span><span class="sxs-lookup"><span data-stu-id="63467-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="63467-111">A partire da Windows Vista, Shader Model 4 è una riprogettazione completa.</span><span class="sxs-lookup"><span data-stu-id="63467-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="63467-112">Consente istruzioni e costanti illimitate (all'interno dei vincoli hardware del computer), dispone di oggetti basati su modelli per rendere più semplice il campionamento della trama e più efficiente e presenta il minor numero di restrizioni di qualsiasi modello di shader.</span><span class="sxs-lookup"><span data-stu-id="63467-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="63467-113">Richiede tuttavia la Windows Driver Model che è disponibile solo nel sistema operativo Windows Vista (o versioni successive).</span><span class="sxs-lookup"><span data-stu-id="63467-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="63467-114">Profili shader</span><span class="sxs-lookup"><span data-stu-id="63467-114">Shader Profiles</span></span>

<span data-ttu-id="63467-115">Un profilo shader è la destinazione per la compilazione di uno shader; Questa tabella elenca i profili shader supportati da ogni modello shader.</span><span class="sxs-lookup"><span data-stu-id="63467-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63467-116">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="63467-116">Shader Model</span></span>                                       | <span data-ttu-id="63467-117">Profili shader</span><span class="sxs-lookup"><span data-stu-id="63467-117">Shader Profiles</span></span>                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="63467-118">Modello Shader 1</span><span class="sxs-lookup"><span data-stu-id="63467-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="63467-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="63467-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="63467-120">Modello Shader 2</span><span class="sxs-lookup"><span data-stu-id="63467-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="63467-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ level \_ 9 0 \_ , PS \_ 4 \_ 0 \_ level \_ 9 \_ 1, PS \_ 4 \_ 0 \_ level \_ 9 \_ 3, vs \_ 4 \_ 0 \_ level \_ 9 \_ 0, vs \_ 4 \_ 0 \_ level \_ 9 \_ 1, vs \_ 4 \_ 0 \_ level \_ 9 \_ 3, lib \_ 4 \_ 0 \_ level \_ 9 \_ 1, lib \_ 4 \_ 0 \_ \_ \_ Level 9 3</span><span class="sxs-lookup"><span data-stu-id="63467-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="63467-122">Modello Shader 3</span><span class="sxs-lookup"><span data-stu-id="63467-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="63467-123">PS \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63467-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="63467-124">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="63467-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="63467-125">cs \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="63467-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="63467-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="63467-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="63467-127">cs \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (sebbene GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 sono stati introdotti nel modello di Shader 4,0, Shader Model 5 aggiunge il supporto per i profili shader per i buffer strutturati e i buffer degli indirizzi byte).</span><span class="sxs-lookup"><span data-stu-id="63467-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="63467-128">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="63467-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="63467-129">cs \_ 6 \_ 0, DS \_ 6 0 \_ , GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63467-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63467-130">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="63467-130">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="63467-131">In Direct3D 9 sono stati introdotti i modelli shader 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="63467-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span><br/> <span data-ttu-id="63467-132">Direct3D 10 ha introdotto il modello di Shader 4.</span><span class="sxs-lookup"><span data-stu-id="63467-132">Direct3D 10 introduced shader model 4.</span></span><br/> <span data-ttu-id="63467-133">Direct3D 10,1 ha introdotto il modello di Shader 4,1.</span><span class="sxs-lookup"><span data-stu-id="63467-133">Direct3D 10.1 introduced shader model 4.1.</span></span><br/> |



 

## <a name="effect-profiles"></a><span data-ttu-id="63467-134">Profili effetti</span><span class="sxs-lookup"><span data-stu-id="63467-134">Effect Profiles</span></span>

<span data-ttu-id="63467-135">Un profilo di effetto è la destinazione per la compilazione di un effetto/shader; Questa tabella elenca i profili degli effetti supportati da ogni versione di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="63467-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63467-136">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="63467-136">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="63467-137">In Direct3D 9 è stato introdotto Effect-framework Profiles FX \_ 1 \_ 0 e FX \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="63467-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span><br/> <span data-ttu-id="63467-138">In Direct3D 10 è stato introdotto un effetto del profilo del Framework FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="63467-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span><br/> <span data-ttu-id="63467-139">Direct3D 10,1 ha introdotto Effect-framework profile FX \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="63467-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span><br/> <span data-ttu-id="63467-140">In Direct3D 11 è stato introdotto Effect-framework profile FX \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="63467-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="63467-141">Questi profili degli effetti legacy sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="63467-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="63467-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63467-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63467-143">Riferimento per HLSL</span><span class="sxs-lookup"><span data-stu-id="63467-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





