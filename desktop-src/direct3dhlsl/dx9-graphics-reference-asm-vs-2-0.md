---
title: vs_2_0
description: Informazioni su vs_2_0, un vertex shader programmabile, costituito da un set di istruzioni che operano sui dati dei vertici.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010854"
---
# <a name="vs_2_0"></a><span data-ttu-id="bd776-103">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bd776-103">vs\_2\_0</span></span>

<span data-ttu-id="bd776-104">Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="bd776-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="bd776-105">Registra i dati di trasferimento in e da ALU.</span><span class="sxs-lookup"><span data-stu-id="bd776-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="bd776-106">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="bd776-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="bd776-107">[Instructions - vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="bd776-107">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="bd776-108">[Registri- rispetto \_ a 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) elenca i diversi tipi di registri usati dal vertex shader ALU.</span><span class="sxs-lookup"><span data-stu-id="bd776-108">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="bd776-109">[I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="bd776-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="bd776-110">[I modificatori del registro di origine vertex shader modificano](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="bd776-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="bd776-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.</span><span class="sxs-lookup"><span data-stu-id="bd776-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="bd776-112">[Destination Register Masking determina](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="bd776-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="bd776-113">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="bd776-113">Instruction Count</span></span>

<span data-ttu-id="bd776-114">Ogni vertex shader può contenere fino a 256 istruzioni archiviate.</span><span class="sxs-lookup"><span data-stu-id="bd776-114">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="bd776-115">Il numero di istruzioni eseguite può essere molto più elevato (a causa del supporto per cicli/rep) ed è limitato da D3DCAPS9. MaxVShaderInstructionsExecuted, che deve essere almeno 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="bd776-115">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd776-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd776-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd776-117">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="bd776-117">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




