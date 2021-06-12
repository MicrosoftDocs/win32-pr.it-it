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
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento in e da ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

-   [Instructions - vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene un elenco delle istruzioni disponibili.
-   [Registri- rispetto \_ a 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) elenca i diversi tipi di registri usati dal vertex shader ALU.
-   [I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.
-   [I modificatori del registro di origine vertex shader modificano](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.
-   [Destination Register Masking determina](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) quali componenti del registro di destinazione vengono scritti.

## <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader può contenere fino a 256 istruzioni archiviate. Il numero di istruzioni eseguite può essere molto più elevato (a causa del supporto per cicli/rep) ed è limitato da D3DCAPS9. MaxVShaderInstructionsExecuted, che deve essere almeno 0xFFFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




