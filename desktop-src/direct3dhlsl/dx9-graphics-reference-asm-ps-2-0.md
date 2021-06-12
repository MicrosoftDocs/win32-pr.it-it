---
title: ps_2_0
description: Informazioni su ps_2_0, un pixel shader programmabile, costituito da un set di istruzioni che operano sui dati pixel.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010984"
---
# <a name="ps_2_0"></a><span data-ttu-id="a0a3f-103">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0a3f-103">ps\_2\_0</span></span>

<span data-ttu-id="a0a3f-104">Un'pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="a0a3f-105">Registra i dati di trasferimento in e all'uscita dall'ALU.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="a0a3f-106">È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="a0a3f-107">[ps \_ 2 \_ 0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contiene un elenco delle istruzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-107">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="a0a3f-108">[ps \_ 2 \_ 0 Registers elenca](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) i diversi tipi di registri usati dal vertex shader ALU.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-108">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="a0a3f-109">[Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Vengono usati per modificare il funzionamento di un'istruzione.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="a0a3f-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="a0a3f-111">[I modificatori del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) pixel shader modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="a0a3f-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="a0a3f-113">Conteggio istruzioni</span><span class="sxs-lookup"><span data-stu-id="a0a3f-113">Instruction Count</span></span>

<span data-ttu-id="a0a3f-114">Gli shader hanno restrizioni per il numero massimo di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-114">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="a0a3f-115">Totale slot di istruzione: 96 (64 aritmetici e 32 trame).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-115">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="a0a3f-116">Conteggio campionatore</span><span class="sxs-lookup"><span data-stu-id="a0a3f-116">Sampler Count</span></span>

<span data-ttu-id="a0a3f-117">Il numero di campionatori di trama disponibili è 16.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-117">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0a3f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0a3f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a3f-119">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="a0a3f-119">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




