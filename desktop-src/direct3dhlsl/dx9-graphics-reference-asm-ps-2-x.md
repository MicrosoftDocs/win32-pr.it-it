---
title: ps_2_x
description: Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993504"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Un pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento all'interno e all'esterno dell'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o i dati che vengono scritti.

-   [le \_ istruzioni di PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contengono un elenco delle istruzioni disponibili.
-   [i \_ registri di PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) elencano i diversi tipi di registri usati da vertex shader Alu.
-   [Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Consentono di modificare la modalità di funzionamento di un'istruzione.
-   La [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.
-   I [modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   Il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) fornisce un controllo aggiuntivo sui componenti di registro letti, copiati o scritti.

## <a name="dynamic-flow-control"></a>Controllo dinamico di flusso

[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) rappresenta la profondità di annidamento delle istruzioni di controllo del flusso dinamico: [if](if-bool---ps.md), if [ \_ comp](if-comp---ps.md), [if \_ prede](if-pred---ps.md), [break-PS](break---ps.md)e [break \_ comp-PS](break-comp---ps.md). Il valore è uguale alla profondità di nidificazione del blocco if \_ comp. Se questo limite è pari a zero, il dispositivo non supporta le istruzioni per il controllo dinamico dei flussi.

## <a name="number-of-temporary-registers"></a>Numero di registri temporanei

Numero di registri temporanei supportati dal dispositivo. L'intervallo è compreso tra 12 e 32.

## <a name="static-flow-control-nesting-depth"></a>Profondità di annidamento del controllo di flusso statico

[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) rappresenta la profondità di annidamento di due tipi di istruzioni di controllo di flusso statiche: Rep del [ciclo](loop---ps.md)  / [](rep---ps.md) e [chiamata](call---ps.md)  / [callnz](callnz-bool---ps.md). le istruzioni Loop/Rep possono essere nidificate fino a **StaticFlowControlDepth** Deep. In modo indipendente, le istruzioni Call/callnz possono essere annidate fino a **StaticFlowControlDepth** Deep.

## <a name="number-of-instruction-slots"></a>Numero di slot di istruzioni

Il numero di slot di istruzioni può essere compreso tra 96 e un massimo di 512 e viene specificato da [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0). Il numero totale di istruzioni che è possibile eseguire è definito da **MaxPixelShaderInstructionsExecuted**. Può essere maggiore del numero di slot di istruzioni a causa delle chiamate di ciclo e subroutine.

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , il swizzle arbitrario è supportato. Vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Istruzioni gradiente

Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , sono supportate le istruzioni per la sfumatura. Vedere [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)e [texldd-PS](texldd---ps.md).

## <a name="predication"></a>Predicazione

Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ predicazione**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , l'istruzione predicazione è supportata. Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Limite di lettura dipendente

Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , non esistono limiti di lettura dipendenti.

## <a name="texture-instruction-limit"></a>Limite istruzioni trama

Se è impostato [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , non esiste alcun limite per le istruzioni di trama.

## <a name="sampler-count"></a>Numero di campionatori

Il numero di campioni di trama disponibili è 16.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 