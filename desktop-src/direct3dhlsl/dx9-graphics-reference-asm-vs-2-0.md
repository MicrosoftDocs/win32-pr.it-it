---
title: vs_2_0
description: Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976146"
---
# <a name="vs_2_0"></a><span data-ttu-id="0c816-105">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c816-105">vs\_2\_0</span></span>

<span data-ttu-id="0c816-106">Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="0c816-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="0c816-107">Registra i dati di trasferimento all'interno e all'esterno dell'ALU.</span><span class="sxs-lookup"><span data-stu-id="0c816-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="0c816-108">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="0c816-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="0c816-109">[Istruzioni-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="0c816-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="0c816-110">[Registers-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) elenca i diversi tipi di registri usati da vertex shader Alu.</span><span class="sxs-lookup"><span data-stu-id="0c816-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="0c816-111">I [modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare la modalità di funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="0c816-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="0c816-112">I [modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="0c816-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="0c816-113">Il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.</span><span class="sxs-lookup"><span data-stu-id="0c816-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="0c816-114">Il [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="0c816-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="0c816-115">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="0c816-115">Instruction Count</span></span>

<span data-ttu-id="0c816-116">Ogni vertex shader può avere fino a 256 istruzioni archiviate.</span><span class="sxs-lookup"><span data-stu-id="0c816-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="0c816-117">Il numero di istruzioni eseguite può essere molto più alto (a causa del supporto ciclo/Rep) ed è limitato da D3DCAPS9. MaxVShaderInstructionsExecuted, che deve essere almeno 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="0c816-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c816-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c816-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c816-119">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="0c816-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




