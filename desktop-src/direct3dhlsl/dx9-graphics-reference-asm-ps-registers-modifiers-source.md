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
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129678"
---
# <a name="pixel-shader-source-register-modifiers"></a>Modificatori del registro di origine pixel shader

Usare i modificatori del registro di origine per modificare il valore letto da un registro prima dell'esecuzione di un'istruzione. Il contenuto di un registro di origine rimane invariato. I modificatori sono utili per modificare l'intervallo di dati del registro in preparazione dell'istruzione . Un set di modificatori denominati selettori copia o replica i dati da un singolo canale (r,g,b,a) negli altri canali.

## <a name="ps_1_1---ps_1_4"></a>ps \_ 1 \_ 1 - ps \_ 1 \_ 4

Questa tabella identifica le versioni che supportano ogni modificatore:



| Modificatori del registro di origine                                                                                    | Sintassi         | Versione 1 \_ 1 | Versione 1 \_ 2     | Versione 1 \_ 3     | Versione 1 \_ 4     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [Pregiudizi](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | registrare \_ la distorsione | X       | X    | X    | X    |
| [Invertire](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1 - Registrazione   | X       | X    | X    | X    |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- Registro    | X       | X    | X    | X    |
| [ridimensionare per 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | registrare \_ x2   |         |      |      | X    |
| [ridimensionamento con segno](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | registrare \_ bx2  | X       | X    | X    | X    |
| [Modificatori texld e texcrd](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | register \_ d\*  | X       | X    | X    | X    |
| [swizzling del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | register.xyzw  | X       | X    | X    | X    |



 

I modificatori del registro di origine possono essere usati solo nelle istruzioni aritmetiche. Non possono essere usati nelle istruzioni relative all'indirizzo della trama. L'eccezione è il [modificatore scale by 2.](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) Per la versione 1 1, è possibile usare la scalabilità con segno \_ nell'argomento di origine di qualsiasi istruzione texm. \* Per la versione 1 \_ 2 o 1 3, è possibile usare la scalabilità con segno nell'argomento di origine \_ di qualsiasi istruzione di indirizzo di trama.

Alcune restrizioni specifiche del modificatore:

-   Negate può essere combinato con il modificatore bias, signed scaling o scalex2. Se combinato, negate viene eseguito per ultimo.
-   Invert non può essere combinato con altri modificatori.
-   Invert, negate, bias, signed scaling e scalex2 possono essere combinati con qualsiasi selettore.
-   I modificatori del registro di origine non devono essere usati nei registri costanti perché causeranno risultati non definiti. Per la versione \_ 1 4, i modificatori sulle costanti non sono consentiti e la convalida avrà esito negativo.

## <a name="ps_2_0-and-above"></a>ps \_ 2 \_ 0 e successive

Per la versione ps \_ 2 \_ 0 e successiva, il numero di modificatori è stato semplificato.

### <a name="negate"></a>Negate

Negare il contenuto del registro di origine.



| Modificatore di componente | Descrizione     |
|--------------------|-----------------|
| \- R               | Negazione dell'origine |



 

Il modificatore negate non può essere usato nel secondo registro di origine di queste istruzioni: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md)e [m4x4 - ps](m4x4---ps.md).



| Versioni dei pixel shader | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Valore assoluto

Prendere il valore assoluto del registro.



| Versioni dei pixel shader | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Se uno shader versione 3 legge da uno o più registri float costanti (c), uno dei \# seguenti deve essere true.

-   Tutti i registri a virgola mobile costanti devono usare il modificatore abs.
-   Nessuno dei registri a virgola mobile costanti può usare il modificatore abs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di registro pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




