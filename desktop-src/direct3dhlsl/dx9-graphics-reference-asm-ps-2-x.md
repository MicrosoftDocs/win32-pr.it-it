---
title: ps_2_x
description: Informazioni su ps_2_x, un'pixel shader programmabile, che è costituito da un set di istruzioni che operano sui dati pixel.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37bc9709effeb865651ca920a155094946b88753586174ecf6e1ab06eabd2fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489411"
---
# <a name="ps_2_x"></a>ps \_ 2 \_ x

Un'pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento in e da ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

-   [ps \_ 2 \_ x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contiene un elenco delle istruzioni disponibili.
-   [ps \_ 2 \_ x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) elenca i diversi tipi di registri usati dal vertex shader ALU.
-   [Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Vengono usati per modificare il funzionamento di un'istruzione.
-   [Destination Register Write Mask determina](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) quali componenti del registro di destinazione vengono scritti.
-   [I modificatori del registro di origine pixel shader modificano](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.

## <a name="dynamic-flow-control"></a>Controllo Flow dinamico

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) rappresenta la profondità di annidamento delle istruzioni di controllo dinamico del [flusso:](if-bool---ps.md)se , se [ \_ comp](if-comp---ps.md), se [ \_ pred](if-pred---ps.md), [break - ps](break---ps.md)e break comp - [ \_ ps](break-comp---ps.md). Il valore è uguale alla profondità di annidamento del blocco if \_ comp. Se questo limite è zero, il dispositivo non supporta le istruzioni di controllo dinamico del flusso.

## <a name="number-of-temporary-registers"></a>Numero di registri temporanei

Numero di registri temporanei supportati dal dispositivo. L'intervallo è compreso tra 12 e 32.

## <a name="static-flow-control-nesting-depth"></a>Profondità annidamento controllo Flow statici

[**StaticFlowControlDepth rappresenta la**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: [loop](loop---ps.md)  / [rep](rep---ps.md) e [](call---ps.md)  / [callnz](callnz-bool---ps.md). Le istruzioni loop /rep possono essere annidate fino **a StaticFlowControlDepth** deep. Indipendentemente, le istruzioni /callnz possono essere annidate fino a **StaticFlowControlDepth** deep.

## <a name="number-of-instruction-slots"></a>Numero di slot di istruzioni

Il numero di slot di istruzioni può variare da 96 a un massimo di 512 ed è specificato da [**MaxPixelShaderInstructionSlots.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) Il numero totale di istruzioni che è possibile eseguire è definito da **MaxPixelShaderInstructionsExecuted.** Può essere maggiore del numero di slot di istruzione a causa di chiamate di ciclo e subroutine.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Se [**è impostato D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) lo swizzle arbitrario è supportato. Vedere [Source Register Swizzling ( Swizzling del registro di origine).](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)

## <a name="gradient-instructions"></a>Istruzioni per la sfumatura

Se [**è impostato D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) sono supportate le istruzioni per la sfumatura. Vedere [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)e [texldd - ps](texldd---ps.md).

## <a name="predication"></a>Predicazione

Se [**la predicazione \_ 0 \_ D3DD3DPSHADERCAPS2**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) è impostata, il predicato dell'istruzione è supportato. Vedere [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite di lettura dipendente

Se [**è impostato \_ \_ NODEPENDENTREADLIMIT D3DD3DPSHADERCAPS2 0,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) non sono previsti limiti di lettura dipendenti.

## <a name="texture-instruction-limit"></a>Limite istruzioni trama

Se [**è impostato D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) non esiste alcun limite per le istruzioni di trama.

## <a name="sampler-count"></a>Conteggio campionatore

Il numero di campionatori di trama disponibili è 16.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 