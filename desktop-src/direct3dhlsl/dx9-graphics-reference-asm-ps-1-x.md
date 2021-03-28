---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Il pixel shader Assembler è costituito da un set di istruzioni che operano sui dati pixel contenuti nei registri.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220897"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4

Il pixel shader Assembler è costituito da un set di istruzioni che operano sui dati pixel contenuti nei registri. Le operazioni sono espresse come istruzioni costituite da un operatore e da uno o più operandi. Le istruzioni usano i registri per trasferire i dati all'interno e all'esterno del pixel shader ALU. I registri possono essere usati anche da alcune istruzioni per contenere risultati temporanei.

> [!Note]  
> Il supporto di HLSL per pixel shader 1. x è deprecato.

 

## <a name="instructions"></a>Istruzioni

Esistono due categorie principali di istruzioni pixel shader: istruzioni aritmetiche e istruzioni per l'indirizzamento delle trame. Le istruzioni aritmetiche modificano i dati dei colori. Le operazioni di indirizzamento delle trame elaborano i dati delle coordinate di trama e, nella maggior parte dei casi, Le istruzioni pixel shader vengono eseguite in base ai singoli pixel; ovvero non conoscono altri pixel nella pipeline.

Le istruzioni per l'indirizzamento della trama utilizzano ognuna uno slot, ma è possibile associare le istruzioni aritmetiche per abilitare sia i componenti colore (RGB) che l'istruzione di un componente alfa in un unico slot.

[PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 istruzioni](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiene un elenco delle istruzioni disponibili.

Quando è abilitato il campionamento multiplo, i pixel shader vengono eseguiti una sola volta per pixel, non una volta per ogni subpixel. Il campionamento multiplo aumenta solo la risoluzione dei bordi del poligono, nonché i test di profondità e stencil. Se, ad esempio, è abilitato il multicampionamento 3x3 e viene trovato un triangolo rasterizzato per coprire cinque dei nove sottopixel per un determinato pixel, il pixel shader viene eseguito una volta e lo stesso risultato viene applicato a tutti i cinque subpixel.

## <a name="registers"></a>Registri

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 i registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS 1 \_ \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) elenca i diversi registri usati da shader Alu.

## <a name="modifiers"></a>Modificatori

È possibile utilizzare i [modificatori per PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) per modificare la funzionalità di un'istruzione o i dati letti o scritti in un registro.

Direct3D 9 richiede calcoli intermedi per mantenere una precisione di almeno 8 bit per tutti i formati di superficie. È consigliabile usare sia una precisione maggiore (a 12 bit) per la matematica in fase che la saturazione a 8 bit tra le fasi della trama. Non sono supportate le eccezioni o le modalità di arrotondamento modificabili. La moltiplicazione deve essere supportata con una precisione round-to-più vicina per evitare una perdita di precisione minima.

## <a name="sampler-count"></a>Numero di campionatori

Il numero di campioni di trama disponibili è:

-   Per PS \_ 1 \_ 0-PS \_ 1 \_ 3, il valore massimo è 4.
-   Per PS \_ 1 \_ 4, il valore massimo è 6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




