---
title: ps_2_0
description: Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104975906"
---
# <a name="ps_2_0"></a><span data-ttu-id="03440-105">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="03440-105">ps\_2\_0</span></span>

<span data-ttu-id="03440-106">Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel.</span><span class="sxs-lookup"><span data-stu-id="03440-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="03440-107">Registra i dati di trasferimento all'interno e all'esterno dell'ALU.</span><span class="sxs-lookup"><span data-stu-id="03440-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="03440-108">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="03440-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="03440-109">[le \_ istruzioni di PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contengono un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="03440-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="03440-110">[i \_ registri di PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) elencano i diversi tipi di registri usati da vertex shader Alu.</span><span class="sxs-lookup"><span data-stu-id="03440-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="03440-111">[Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Consentono di modificare la modalità di funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="03440-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="03440-112">La [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="03440-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="03440-113">I [modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="03440-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="03440-114">Il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.</span><span class="sxs-lookup"><span data-stu-id="03440-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="03440-115">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="03440-115">Instruction Count</span></span>

<span data-ttu-id="03440-116">Gli shader presentano restrizioni per i conteggi massimi delle istruzioni.</span><span class="sxs-lookup"><span data-stu-id="03440-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="03440-117">Totale slot di istruzioni: 96 (64 aritmetica e 32 trama).</span><span class="sxs-lookup"><span data-stu-id="03440-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="03440-118">Numero di campionatori</span><span class="sxs-lookup"><span data-stu-id="03440-118">Sampler Count</span></span>

<span data-ttu-id="03440-119">Il numero di campioni di trama disponibili è 16.</span><span class="sxs-lookup"><span data-stu-id="03440-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03440-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03440-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03440-121">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="03440-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




