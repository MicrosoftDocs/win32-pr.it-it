---
title: gather4_po (SM5-ASM)
description: Variante di gather4, ma anziché supportare un offset immediato \-8.. 7 \, l'offset viene visualizzato come parametro per l'istruzione e dispone anche di un intervallo più ampio di \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976426"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ po (SM5-ASM)

Variante di [gather4](gather4--sm5---asm-.md), ma anziché supportare un offset immediato \[ -8.. 7 \] , l'offset viene visualizzato come parametro per l'istruzione e dispone anche di un intervallo più ampio di \[ -32.. 31 \] .



| gather4 \_ po dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ Component\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] un set di coordinate di trama.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[nell' \] offset.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore.<br/>                         |



 

## <a name="remarks"></a>Commenti

I primi due componenti del parametro offset a 4 vettori forniscono offset integer a 32 bit. Gli altri componenti di questo parametro vengono ignorati.

I 6 bit meno significativi di ogni valore di offset vengono rispettati come valore con segno, producendo un \[ intervallo di-32.. 31. \]

Questa istruzione funziona solo con le trame 2D, a differenza di **gather4**, che funziona anche con TextureCubes.

Le uniche modalità rispettate nel campionatore sono le modalità di indirizzamento. Viene utilizzata solo la MIP più dettagliata nella visualizzazione risorse.

Se l'indirizzo cade in un centro Texel, questo non significa che gli altri Texel possono essere azzerati.

Il parametro *srcSampler* include \[ . Select ( \_ componente), che consente il recupero di \] qualsiasi singolo componente di una trama, inclusa la restituzione di valori predefiniti per i componenti mancanti.

Per i formati con componenti float32, se il valore recuperato è normalizzato, denormalizzato, +-0 o +-INF, viene restituito allo shader inalterato. NaN viene restituito come NaN, ma la rappresentazione di bit esatta di NaN può essere modificata. Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi negli angoli, quindi la nozione di restituzione di bit invariati per il Texel sintetizzato non si applica e le denormazioni potrebbero essere scaricate.

Usare questa istruzione per estendere l'intervallo di offset di **gather4** in modo che sia più grande e programmabile. Il suffisso "po" sul nome indica "offset programmabile".

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





