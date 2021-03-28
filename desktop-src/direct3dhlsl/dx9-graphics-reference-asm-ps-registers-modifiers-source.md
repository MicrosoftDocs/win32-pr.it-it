---
title: Modificatori del registro di origine pixel shader
description: Usare i modificatori del registro di origine per modificare il valore letto da un registro prima dell'esecuzione di un'istruzione.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332615"
---
# <a name="pixel-shader-source-register-modifiers"></a>Modificatori del registro di origine pixel shader

Usare i modificatori del registro di origine per modificare il valore letto da un registro prima dell'esecuzione di un'istruzione. Il contenuto di un registro di origine viene lasciato invariato. I modificatori sono utili per modificare l'intervallo dei dati del registro in preparazione all'istruzione. Un set di modificatori chiamati selettori copia o replica i dati da un singolo canale (r, g, b, a) negli altri canali.

## <a name="ps_1_1---ps_1_4"></a>PS \_ 1 \_ 1-PS \_ 1 \_ 4

Questa tabella identifica le versioni che supportano ogni modificatore:



| Modificatori del registro di origine                                                                                    | Sintassi         | Versione |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |     |     |
| [distorsione](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | \_distorsione registro | X       | X    | X    | X    |     |     |
| [inversione](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1-registrazione   | X       | X    | X    | X    |     |     |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- Registro    | X       | X    | X    | X    |     |     |
| [Ridimensiona per 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | Registra \_ X2   |         |      |      | X    |     |     |
| [scalabilità con segno](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | Registra \_ BX2  | X       | X    | X    | X    |     |     |
| [modificatori texld e texcrd](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | Registra \_ d\*  | X       | X    | X    | X    |     |     |
| [swizzling del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | Register. xyzw  | X       | X    | X    | X    |     |     |



 

I modificatori del registro di origine possono essere utilizzati solo nelle istruzioni aritmetiche. Non possono essere usati nelle istruzioni relative all'indirizzo di trama. L'eccezione è rappresentata dal modificatore [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) . Per la versione 1 \_ , è possibile usare la scala con segno nell'argomento di origine di qualsiasi \* istruzione texm. Per la versione 1 \_ 2 o 1 \_ 3, la scala con segno può essere usata nell'argomento di origine di qualsiasi istruzione di indirizzo di trama.

Alcune restrizioni specifiche del modificatore:

-   È possibile combinare negate con il modificatore di distorsione, di ridimensionamento con firma o di scalex2. In combinazione, viene eseguita l'ultima negazione.
-   Non è possibile combinare l'inversione con altri modificatori.
-   Invertire, negare, bias, la scalabilità con segno e scalex2 possono essere combinati con uno qualsiasi dei selettori.
-   I modificatori del registro di origine non devono essere usati nei registri costanti perché determineranno risultati non definiti. Per la versione 1 \_ 4, i modificatori sulle costanti non sono consentiti e la convalida avrà esito negativo.

## <a name="ps_2_0-and-above"></a>PS \_ 2 \_ 0 e versioni successive

Per la versione PS \_ 2 \_ 0 e su, il numero di modificatori è stato semplificato.

### <a name="negate"></a>Negate

Negare il contenuto del registro di origine.



| Modificatore Component | Descrizione     |
|--------------------|-----------------|
| \- r               | Negazione origine |



 

Non è possibile usare il modificatore negazioni nel secondo registro di origine di queste istruzioni: [M3X2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)e [M4x4-PS](m4x4---ps.md).



| Versioni pixel shader | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Valore assoluto

Assumere il valore assoluto del registro.



| Versioni pixel shader | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Se una versione 3 dello shader legge da uno o più registri float costanti (c \# ), uno dei seguenti deve essere true.

-   Tutti i registri a virgola mobile costanti devono usare il modificatore ABS.
-   Nessun registro a virgola mobile costante può utilizzare il modificatore ABS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




