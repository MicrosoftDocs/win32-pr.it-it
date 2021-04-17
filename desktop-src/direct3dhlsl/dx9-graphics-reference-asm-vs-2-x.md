---
title: vs_2_x
description: Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473755"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.

Vertex shader versione vs \_ 2 \_ x estende il set di funzionalità supportato da vs \_ 2 \_ 0. Ogni funzionalità aggiuntiva è rappresentata da un limite corrispondente nella struttura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) all'interno di [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps). Per usare una delle funzionalità avanzate rappresentate da questi limiti, è necessario specificare la versione di vertex shader come vs \_ 2 \_ x.

-   [Istruzioni: vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene un elenco delle istruzioni disponibili.
-   [Registers-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) elenca i diversi tipi di registri usati da vertex shader Alu.
-   I [modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare la modalità di funzionamento di un'istruzione.
-   I [modificatori del registro di origine vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   Il [Registro di origine swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.
-   Il [mascheramento del registro di destinazione](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina quali componenti del registro di destinazione vengono scritti.

## <a name="new-features"></a>Nuove funzioni e caratteristiche

Le nuove funzionalità sono le seguenti:

### <a name="dynamic-flow-control"></a>Controllo dinamico di flusso

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, sono supportate le istruzioni seguenti per il controllo dinamico del flusso:

-   [Se \_ comp-vs](if-comp---vs.md)
-   [Break-vs](break---vs.md)
-   [Interrompi \_ comp-vs](break-comp---vs.md)

Se si imposta anche [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , sono supportate le istruzioni aggiuntive per il controllo di flusso seguenti:

-   [setp \_ comp-vs](setp-comp---vs.md)
-   [Se prede-vs](if-pred---vs.md)
-   [callnz Predator-vs](callnz-pred---vs.md)
-   [Breakp-vs](breakp---vs.md)

L'intervallo di valori per la profondità del controllo di flusso dinamico è compreso tra 0 e 24 ed è uguale alla profondità di annidamento delle istruzioni di controllo del flusso dinamico. per informazioni dettagliate, vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) . Se questo limite è pari a zero, il dispositivo non supporta le istruzioni per il controllo dinamico dei flussi.

### <a name="number-of-temporary-registers"></a>Numero di registri temporanei

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta il numero di [registri temporanei](dx9-graphics-reference-asm-vs-registers-temporary.md)supportati dal dispositivo. L'intervallo di valori per questo limite è 12-32.

### <a name="static-flow-control-nesting-depth"></a>Profondità di annidamento del controllo di flusso statico

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: le istruzioni [loop-vs](loop---vs.md) / [Rep-vs](rep---vs.md) e [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [se bool-vs](if-bool---vs.md). loop-vs/Rep-vs possono essere nidificate fino a D3DVS20CAPS Deep. In modo indipendente, le istruzioni Call-vs/callnz bool-vs possono essere nidificate fino a D3DVS20CAPS Deep. Se viene impostato anche D3DVS20CAPS, [callnz prede-vs](callnz-pred---vs.md) viene conteggiato nella profondità di annidamento di Call-vs/callnz bool-vs/if bool-vs (vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md) per informazioni dettagliate).

### <a name="predication"></a>Predicazione

Se è impostato [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , il dispositivo supporta [setp \_ comp-vs](setp-comp---vs.md) e l'istruzione predicazione. Se anche D3DVS20CAPS è maggiore di 0, sono supportate le istruzioni aggiuntive per il controllo di flusso dinamico seguenti:

-   [Se prede-vs](if-pred---vs.md)
-   [callnz Predator-vs](callnz-pred---vs.md)
-   [Breakp-vs](breakp---vs.md)

### <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader può avere fino a 256 istruzioni archiviate. Il numero di istruzioni eseguite può essere molto più alto (a causa del supporto ciclo/Rep) ed è limitato da [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), che deve essere almeno 0xFFFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 