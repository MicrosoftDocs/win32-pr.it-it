---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Il pixel shader Assembler è costituito da un set di istruzioni che operano sui dati pixel contenuti nei registri.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220897"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="8f340-103">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="8f340-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="8f340-104">Il pixel shader Assembler è costituito da un set di istruzioni che operano sui dati pixel contenuti nei registri.</span><span class="sxs-lookup"><span data-stu-id="8f340-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="8f340-105">Le operazioni sono espresse come istruzioni costituite da un operatore e da uno o più operandi.</span><span class="sxs-lookup"><span data-stu-id="8f340-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="8f340-106">Le istruzioni usano i registri per trasferire i dati all'interno e all'esterno del pixel shader ALU.</span><span class="sxs-lookup"><span data-stu-id="8f340-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="8f340-107">I registri possono essere usati anche da alcune istruzioni per contenere risultati temporanei.</span><span class="sxs-lookup"><span data-stu-id="8f340-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="8f340-108">Il supporto di HLSL per pixel shader 1. x è deprecato.</span><span class="sxs-lookup"><span data-stu-id="8f340-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="8f340-109">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="8f340-109">Instructions</span></span>

<span data-ttu-id="8f340-110">Esistono due categorie principali di istruzioni pixel shader: istruzioni aritmetiche e istruzioni per l'indirizzamento delle trame.</span><span class="sxs-lookup"><span data-stu-id="8f340-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="8f340-111">Le istruzioni aritmetiche modificano i dati dei colori.</span><span class="sxs-lookup"><span data-stu-id="8f340-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="8f340-112">Le operazioni di indirizzamento delle trame elaborano i dati delle coordinate di trama e, nella maggior parte dei casi,</span><span class="sxs-lookup"><span data-stu-id="8f340-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="8f340-113">Le istruzioni pixel shader vengono eseguite in base ai singoli pixel; ovvero non conoscono altri pixel nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f340-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="8f340-114">Le istruzioni per l'indirizzamento della trama utilizzano ognuna uno slot, ma è possibile associare le istruzioni aritmetiche per abilitare sia i componenti colore (RGB) che l'istruzione di un componente alfa in un unico slot.</span><span class="sxs-lookup"><span data-stu-id="8f340-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="8f340-115">[PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 istruzioni](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="8f340-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="8f340-116">Quando è abilitato il campionamento multiplo, i pixel shader vengono eseguiti una sola volta per pixel, non una volta per ogni subpixel.</span><span class="sxs-lookup"><span data-stu-id="8f340-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="8f340-117">Il campionamento multiplo aumenta solo la risoluzione dei bordi del poligono, nonché i test di profondità e stencil.</span><span class="sxs-lookup"><span data-stu-id="8f340-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="8f340-118">Se, ad esempio, è abilitato il multicampionamento 3x3 e viene trovato un triangolo rasterizzato per coprire cinque dei nove sottopixel per un determinato pixel, il pixel shader viene eseguito una volta e lo stesso risultato viene applicato a tutti i cinque subpixel.</span><span class="sxs-lookup"><span data-stu-id="8f340-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="8f340-119">Registri</span><span class="sxs-lookup"><span data-stu-id="8f340-119">Registers</span></span>

<span data-ttu-id="8f340-120">[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 i registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS 1 \_ \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) elenca i diversi registri usati da shader Alu.</span><span class="sxs-lookup"><span data-stu-id="8f340-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="8f340-121">Modificatori</span><span class="sxs-lookup"><span data-stu-id="8f340-121">Modifiers</span></span>

<span data-ttu-id="8f340-122">È possibile utilizzare i [modificatori per PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) per modificare la funzionalità di un'istruzione o i dati letti o scritti in un registro.</span><span class="sxs-lookup"><span data-stu-id="8f340-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="8f340-123">Direct3D 9 richiede calcoli intermedi per mantenere una precisione di almeno 8 bit per tutti i formati di superficie.</span><span class="sxs-lookup"><span data-stu-id="8f340-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="8f340-124">È consigliabile usare sia una precisione maggiore (a 12 bit) per la matematica in fase che la saturazione a 8 bit tra le fasi della trama.</span><span class="sxs-lookup"><span data-stu-id="8f340-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="8f340-125">Non sono supportate le eccezioni o le modalità di arrotondamento modificabili.</span><span class="sxs-lookup"><span data-stu-id="8f340-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="8f340-126">La moltiplicazione deve essere supportata con una precisione round-to-più vicina per evitare una perdita di precisione minima.</span><span class="sxs-lookup"><span data-stu-id="8f340-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="8f340-127">Numero di campionatori</span><span class="sxs-lookup"><span data-stu-id="8f340-127">Sampler Count</span></span>

<span data-ttu-id="8f340-128">Il numero di campioni di trama disponibili è:</span><span class="sxs-lookup"><span data-stu-id="8f340-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="8f340-129">Per PS \_ 1 \_ 0-PS \_ 1 \_ 3, il valore massimo è 4.</span><span class="sxs-lookup"><span data-stu-id="8f340-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="8f340-130">Per PS \_ 1 \_ 4, il valore massimo è 6.</span><span class="sxs-lookup"><span data-stu-id="8f340-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f340-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f340-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f340-132">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="8f340-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




