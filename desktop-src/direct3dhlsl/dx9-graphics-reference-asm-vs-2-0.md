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
ms.openlocfilehash: 492eb282e4ca297b8913a4d08cde976e23fc34b0999983604931d77af8f6edbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908221"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento in e all'uscita dall'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

-   [Istruzioni: rispetto \_ alla \_ versione 2 0,](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene un elenco delle istruzioni disponibili.
-   [Registri: rispetto a \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) sono elencati i diversi tipi di registri usati dal vertex shader ALU.
-   [I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.
-   [I modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.
-   [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.

## <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader può contenere fino a 256 istruzioni archiviate. Il numero di istruzioni eseguite può essere molto superiore (a causa del supporto di ciclo/ripetizione) ed è limitato da D3DCAPS9. MaxVShaderInstructionsExecuted, che deve essere almeno 0xFFFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




