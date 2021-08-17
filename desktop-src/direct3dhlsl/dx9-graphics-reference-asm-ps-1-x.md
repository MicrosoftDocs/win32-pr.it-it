---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: L pixel shader assembler è costituito da un set di istruzioni che operano sui dati pixel contenuti nei registri.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e10e4eee48490e7ae998e39d71265aef74339c1979112e2fcf0e47e5b07cda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512942"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4

L pixel shader assembler è costituito da un set di istruzioni che operano sui dati pixel contenuti nei registri. Le operazioni sono espresse come istruzioni costituite da un operatore e da uno o più operandi. Le istruzioni usano i registri per trasferire i dati all'pixel shader ALU. I registri possono essere usati anche da alcune istruzioni per contenere risultati temporanei.

> [!Note]  
> Il supporto HLSL per pixel shader 1.x è deprecato.

 

## <a name="instructions"></a>Istruzioni

Esistono due categorie principali di istruzioni pixel shader: istruzioni aritmetiche e istruzioni di indirizzamento della trama. Le istruzioni aritmetiche modificano i dati relativi ai colori. Le operazioni di indirizzamento delle trame elaborano i dati delle coordinate della trama e, nella maggior parte dei casi, campionare una trama. Le istruzioni del pixel shader vengono eseguite in base al pixel. in altre parole, non hanno alcuna conoscenza di altri pixel nella pipeline.

Le istruzioni di indirizzamento delle trame utilizzano ognuna uno slot, ma le istruzioni aritmetiche possono essere abbinate per abilitare sia i componenti colore (RGB) che un'istruzione del componente alfa in un singolo slot.

[ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Istruzioni](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiene un elenco delle istruzioni disponibili.

Quando è abilitato il multicampionamento, i pixel shader vengono eseguiti una sola volta per pixel, non una volta per ogni sottopixel. Il multicampionamento aumenta solo la risoluzione dei bordi dei poligoni, nonché i test di profondità e stencil. Ad esempio, se è abilitato il multicampionamento 3x3 e viene rilevato che un triangolo rasterizzato copre cinque dei nove sottopixel per un determinato pixel, il pixel shader viene eseguito una sola volta e lo stesso risultato di colore viene applicato a tutti e cinque i sottopixel.

## <a name="registers"></a>Registri

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registri](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) elenca i diversi registri usati dall'ALU dello shader.

## <a name="modifiers"></a>Modificatori

[I modificatori per ps \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) possono essere usati per modificare la funzionalità di un'istruzione o i dati letti o scritti in un registro.

Direct3D 9 richiede calcoli intermedi per mantenere almeno la precisione a 8 bit per tutti i formati di superficie. È consigliabile sia una maggiore precisione (12 bit) per la matematica in fase sia la saturazione a 8 bit tra le fasi della trama. Non sono supportate modalità di arrotondamento modificabili o eccezioni. La moltiplicazione deve essere supportata con una precisione arrotondata alla più vicina per mantenere al minimo la perdita di precisione.

## <a name="sampler-count"></a>Conteggio campionatore

Il numero di campionatori di trama disponibili è:

-   Per ps \_ 1 \_ 0 - ps \_ 1 \_ 3, il valore massimo è 4.
-   Per ps \_ 1 \_ 4, il valore massimo è 6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel shader](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




