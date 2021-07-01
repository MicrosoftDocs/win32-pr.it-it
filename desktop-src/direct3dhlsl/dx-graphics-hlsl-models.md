---
title: Modelli di shader e profili shader
description: Modelli di shader e profili shader
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119616"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="9c07b-103">Modelli di shader e profili shader</span><span class="sxs-lookup"><span data-stu-id="9c07b-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="9c07b-104">Il linguaggio di ombreggiatura di alto livello per DirectX implementa una serie di modelli di shader.</span><span class="sxs-lookup"><span data-stu-id="9c07b-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="9c07b-105">Con HLSL è possibile creare shader programmabili simili a C per la pipeline Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9c07b-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="9c07b-106">Ogni modello shader si basa sulle funzionalità del modello precedente, implementando più funzionalità con meno restrizioni.</span><span class="sxs-lookup"><span data-stu-id="9c07b-106">Each shader model builds on the capabilities of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="9c07b-107">Il modello shader 1 è stato avviato con DirectX 8 e include istruzioni a livello di assembly e di tipo C.</span><span class="sxs-lookup"><span data-stu-id="9c07b-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="9c07b-108">Questo modello presenta molte limitazioni causate dall'hardware dello shader programmabile in anticipo.</span><span class="sxs-lookup"><span data-stu-id="9c07b-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="9c07b-109">Il modello di shader 2 e 3 è notevolmente espanso in base al numero di istruzioni e gli shader costanti possono usare.</span><span class="sxs-lookup"><span data-stu-id="9c07b-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="9c07b-110">Sono molto più potenti del modello shader 1, ma presentano comunque alcune delle limitazioni esistenti del primo modello shader.</span><span class="sxs-lookup"><span data-stu-id="9c07b-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="9c07b-111">A partire da Windows Vista, il modello shader 4 è una riprogettazione completa.</span><span class="sxs-lookup"><span data-stu-id="9c07b-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="9c07b-112">Consente istruzioni e costanti illimitate (all'interno dei vincoli hardware del computer), dispone di oggetti modellati per rendere il campionamento delle trame più pulito e più efficiente e presenta il numero minimo di restrizioni di qualsiasi modello shader.</span><span class="sxs-lookup"><span data-stu-id="9c07b-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="9c07b-113">Richiede tuttavia il Windows Driver Model disponibile solo nel sistema operativo Windows Vista (o versioni successive).</span><span class="sxs-lookup"><span data-stu-id="9c07b-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="9c07b-114">Profili shader</span><span class="sxs-lookup"><span data-stu-id="9c07b-114">Shader Profiles</span></span>

<span data-ttu-id="9c07b-115">Un profilo shader è la destinazione per la compilazione di uno shader. Questa tabella elenca i profili di shader supportati da ogni modello di shader.</span><span class="sxs-lookup"><span data-stu-id="9c07b-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



| <span data-ttu-id="9c07b-116">Modello shader</span><span class="sxs-lookup"><span data-stu-id="9c07b-116">Shader model</span></span>                                                   | <span data-ttu-id="9c07b-117">Profili shader</span><span class="sxs-lookup"><span data-stu-id="9c07b-117">Shader profiles</span></span>                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c07b-118">Modello shader 1</span><span class="sxs-lookup"><span data-stu-id="9c07b-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="9c07b-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9c07b-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9c07b-120">Modello shader 2</span><span class="sxs-lookup"><span data-stu-id="9c07b-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="9c07b-121">ps \_ 2 \_ 0, ps \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 \_ level \_ 9 \_ 0, ps \_ 4 \_ 0 level \_ \_ 9 \_ 1, ps \_ 4 \_ 0 level \_ \_ 9 \_ 3, vs \_ 4 \_ 0 level \_ \_ \_ 9 0, vs \_ \_ 4 0 \_ level \_ \_ 9 1, vs \_ 4 \_ 0 level \_ \_ 9 \_ 3, lib \_ 4 \_ 0 level \_ \_ 9 \_ 1, lib \_ 4 \_ 0 level \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9c07b-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="9c07b-122">Modello shader 3</span><span class="sxs-lookup"><span data-stu-id="9c07b-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="9c07b-123">ps \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c07b-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="9c07b-124">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="9c07b-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="9c07b-125">cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9c07b-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="9c07b-126">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="9c07b-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="9c07b-127">cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (anche se gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps 4 1, vs 4 0 e vs 4 1 \_ \_ \_ \_ \_ \_ sono stati introdotti nel modello shader 4.0, il modello shader 5 aggiunge il supporto a questi profili shader per buffer strutturati e buffer di indirizzi byte).</span><span class="sxs-lookup"><span data-stu-id="9c07b-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="9c07b-128">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="9c07b-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="9c07b-129">cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c07b-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |

<span data-ttu-id="9c07b-130">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9c07b-130">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="9c07b-131">Direct3D 9 ha introdotto i modelli di shader 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="9c07b-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span>
- <span data-ttu-id="9c07b-132">Direct3D 10 ha introdotto il modello shader 4.</span><span class="sxs-lookup"><span data-stu-id="9c07b-132">Direct3D 10 introduced shader model 4.</span></span>
- <span data-ttu-id="9c07b-133">Direct3D 10.1 ha introdotto il modello shader 4.1.</span><span class="sxs-lookup"><span data-stu-id="9c07b-133">Direct3D 10.1 introduced shader model 4.1.</span></span>



 

## <a name="effect-profiles"></a><span data-ttu-id="9c07b-134">Profili di effetto</span><span class="sxs-lookup"><span data-stu-id="9c07b-134">Effect Profiles</span></span>

<span data-ttu-id="9c07b-135">Un profilo di effetto è la destinazione per la compilazione di un effetto/shader. Questa tabella elenca i profili di effetto supportati da ogni versione di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9c07b-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>

<span data-ttu-id="9c07b-136">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9c07b-136">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="9c07b-137">Direct3D 9 ha introdotto i profili del framework degli effetti fx \_ 1 \_ 0 e fx \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9c07b-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span>
- <span data-ttu-id="9c07b-138">Direct3D 10 ha introdotto effect-framework profile fx \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9c07b-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span>
- <span data-ttu-id="9c07b-139">Direct3D 10.1 ha introdotto effect-framework profile fx \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="9c07b-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span>
- <span data-ttu-id="9c07b-140">Direct3D 11 ha introdotto effect-framework profile fx \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9c07b-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="9c07b-141">Questi profili di effetti legacy sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="9c07b-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9c07b-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c07b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c07b-143">Informazioni di riferimento per HLSL</span><span class="sxs-lookup"><span data-stu-id="9c07b-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





