---
title: vs_2_x
description: Informazioni su vs_2_x, un vertex shader programmabile, costituito da un set di istruzioni che operano sui dati dei vertici.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a412c7980ef12bfd8814933cd9d3de07db27fac353a636406e96e1377cd57829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023971"
---
# <a name="vs_2_x"></a>vs \_ 2 \_ x

Un vertex shader programmabile è costituito da un set di istruzioni che operano sui dati dei vertici. Registra i dati di trasferimento in e da ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

La versione vertex shader rispetto \_ alla versione 2 \_ x estende il set di funzionalità supportato da vs \_ 2 \_ 0. Ogni funzionalità aggiuntiva è rappresentata da un limite corrispondente nella [**struttura D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) all'interno [di D3DVS20CAPS.](/windows/desktop/direct3d9/d3dvs20caps) Per usare una qualsiasi delle funzionalità avanzate rappresentate da queste estremità, la versione del vertex shader deve essere specificata come \_ vs 2 \_ x.

-   [Instructions - vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene un elenco delle istruzioni disponibili.
-   [Registri: rispetto \_ a 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) elenca i diversi tipi di registri usati dal vertex shader ALU.
-   [I modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md) vengono usati per modificare il funzionamento di un'istruzione.
-   [I modificatori del registro di origine vertex shader modificano](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.
-   [Destination Register Masking determina](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) quali componenti del registro di destinazione vengono scritti.

## <a name="new-features"></a>Nuove funzioni e caratteristiche

Le nuove funzionalità sono le seguenti:

### <a name="dynamic-flow-control"></a>Controllo Flow dinamico

Se [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, sono supportate le istruzioni di controllo dinamico del flusso seguenti:

-   [if \_ comp - vs](if-comp---vs.md)
-   [break - vs](break---vs.md)
-   [break \_ comp - vs](break-comp---vs.md)

Se [è impostato anche D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) sono supportate le istruzioni aggiuntive seguenti per il controllo di flusso:

-   [setp \_ comp - vs](setp-comp---vs.md)
-   [if pred - vs](if-pred---vs.md)
-   [callnz pred - vs](callnz-pred---vs.md)
-   [breakp - vs](breakp---vs.md)

L'intervallo di valori per la profondità del controllo dinamico del flusso è compreso tra 0 e 24 ed è uguale alla profondità di annidamento delle istruzioni di controllo dinamico del flusso.Per informazioni dettagliate, vedere limiti di annidamento del controllo di [Flow.](dx9-graphics-reference-asm-vs-instructions-flow-control.md) Se questo limite è zero, il dispositivo non supporta le istruzioni di controllo dinamico del flusso.

### <a name="number-of-temporary-registers"></a>Numero di registri temporanei

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta il [numero](dx9-graphics-reference-asm-vs-registers-temporary.md)di registri temporanei supportati dal dispositivo. L'intervallo di valori per questo limite è compreso tra 12 e 32.

### <a name="static-flow-control-nesting-depth"></a>Profondità annidamento controllo Flow statici

[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) rappresenta la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: [loop -](loop---vs.md)vs rep - vs and call - / [](rep---vs.md) [vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md)if / [bool -](if-bool---vs.md)vs . loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep (Ciclo - vs/rep) e istruzioni possono essere annidate fino a D3DVS20CAPS deep. In modo indipendente, chiamare - vs/callnz bool - e le istruzioni possono essere annidate fino a D3DVS20CAPS deep. Se è impostato anche D3DVS20CAPS, chiamare [pred](callnz-pred---vs.md) - vs viene conteggiato per la profondità di annidamento della chiamata - vs/callnz bool - vs/if bool - vs (vedere limiti di annidamento del controllo [di Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) per informazioni dettagliate).

### <a name="predication"></a>Predicazione

Se [è impostato D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) il dispositivo supporta [setp comp - \_ e](setp-comp---vs.md) il predicato dell'istruzione. Se anche D3DVS20CAPS è maggiore di 0, sono supportate le istruzioni di controllo dinamico del flusso aggiuntive seguenti:

-   [if pred - vs](if-pred---vs.md)
-   [callnz pred - vs](callnz-pred---vs.md)
-   [breakp - vs](breakp---vs.md)

### <a name="instruction-count"></a>Conteggio istruzioni

Ogni vertex shader può contenere fino a 256 istruzioni archiviate. Il numero di istruzioni eseguite può essere molto più elevato (a causa del supporto del ciclo/rep) ed è limitato da [**D3DCAPS9,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)che deve essere almeno 0xFFFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex shader](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 