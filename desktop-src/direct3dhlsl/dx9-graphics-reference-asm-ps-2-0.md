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
# <a name="ps_2_0"></a>PS \_ 2 \_ 0

Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.

-   [le \_ istruzioni di PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contengono un elenco delle istruzioni disponibili.
-   [i \_ registri di PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) elencano i diversi tipi di registri usati da vertex shader Alu.
-   [Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Consentono di modificare la modalità di funzionamento di un'istruzione.
-   La [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.
-   I [modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   Il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.

## <a name="instruction-count"></a>Conteggio istruzioni

Gli shader presentano restrizioni per i conteggi massimi delle istruzioni. Totale slot di istruzioni: 96 (64 aritmetica e 32 trama).

## <a name="sampler-count"></a>Numero di campionatori

Il numero di campioni di trama disponibili è 16.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




