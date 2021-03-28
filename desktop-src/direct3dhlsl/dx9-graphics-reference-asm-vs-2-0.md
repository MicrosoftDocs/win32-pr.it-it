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
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.

-   [Istruzioni-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene un elenco delle istruzioni disponibili.
-   [Registers-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) elenca i diversi tipi di registri usati da vertex shader Alu.
-   I [modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare la modalità di funzionamento di un'istruzione.
-   I [modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   Il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.
-   Il [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.

## <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader può avere fino a 256 istruzioni archiviate. Il numero di istruzioni eseguite può essere molto più alto (a causa del supporto ciclo/Rep) ed è limitato da D3DCAPS9. MaxVShaderInstructionsExecuted, che deve essere almeno 0xFFFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




