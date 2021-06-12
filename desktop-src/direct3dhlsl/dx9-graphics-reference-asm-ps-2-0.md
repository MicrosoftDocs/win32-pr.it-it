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
# <a name="ps_2_0"></a>ps \_ 2 \_ 0

Un'pixel shader programmabile è costituito da un set di istruzioni che operano sui dati pixel. Registra i dati di trasferimento in e all'uscita dall'ALU. È possibile applicare un controllo aggiuntivo per modificare l'istruzione, i risultati o quali dati vengono scritti.

-   [ps \_ 2 \_ 0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contiene un elenco delle istruzioni disponibili.
-   [ps \_ 2 \_ 0 Registers elenca](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) i diversi tipi di registri usati dal vertex shader ALU.
-   [Modificatori](dx9-graphics-reference-asm-ps-registers-modifiers.md) Vengono usati per modificare il funzionamento di un'istruzione.
-   [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina quali componenti del registro di destinazione vengono scritti.
-   [I modificatori del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) pixel shader modificano i dati del registro di origine prima dell'esecuzione dell'istruzione.
-   [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un controllo aggiuntivo sui componenti del registro da leggere, copiare o scrivere.

## <a name="instruction-count"></a>Conteggio istruzioni

Gli shader hanno restrizioni per il numero massimo di istruzioni. Totale slot di istruzione: 96 (64 aritmetici e 32 trame).

## <a name="sampler-count"></a>Conteggio campionatore

Il numero di campionatori di trama disponibili è 16.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




