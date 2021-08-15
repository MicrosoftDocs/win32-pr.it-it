---
title: gather4 (sm4.1 - asm)
description: Raccoglie i quattro texel usati in un'operazione di filtro bi-lineare e li racchiude in un unico registro. | gather4 (sm4.1 - asm)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb39918bdb421123cb3e2bfe41931740e271f85a27cf36b8994d493656d91c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457581"
---
# <a name="gather4-sm41---asm"></a>gather4 (sm4.1 - asm)

Raccoglie i quattro texel usati in un'operazione di filtro bi-lineare e li racchiude in un unico registro.



| gather4 \[ \_ aoffimmi(u,v) \] dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource \[ .swizzle \] srcSampler.r |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo del risultato dell'operazione.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Contiene le coordinate della trama. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Un registro risorse. <br/> Lo swizzle consente di scorrere arbitrariamente i valori restituiti prima che siano scritti in *dest*. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] Un registro sampler.<br/> Questo parametro deve avere uno swizzle .r (rosso), che indica che il valore del canale R viene copiato in *dest*. <br/> |



 

## <a name="remarks"></a>Commenti

Questa operazione funziona solo con trame 2D o CubeMap a canale singolo. Per le trame 2D vengono usate solo le modalità di indirizzamento del campionatore e il livello superiore di qualsiasi piramide mip.

Questa istruzione si comporta come [l'istruzione di](sample--sm4---asm-.md) esempio, ma non viene generato un esempio filtrato. I quattro esempi che contribuiscono al filtro vengono inseriti in xyzw in senso antiorario a partire dal campione in basso a sinistra della posizione su cui è stata eseguita la query. Questo è lo stesso del campionamento in punti con delta delle coordinate della trama (u,v) nelle posizioni seguenti: (-,+),(+,+),(+,-),(-,-), dove la grandezza dei delta è sempre metà texel.

Per le trame CubeMap quando viene usato un footprint bi-lineare che si estende su un bordo texel dal viso adiacente. Gli angoli usano le stesse regole **dell'istruzione di** esempio. che è l'angolo non arrotondato è considerato la media dei tre angoli del viso che causano l'errore.

Le restrizioni relative al formato della trama che si applicano alle **istruzioni di** esempio si applicano anche all'istruzione **gather4.**

Per le implementazioni hardware, le ottimizzazioni nel filtro bilineare tradizionale che rilevano gli esempi direttamente sui texel e ignorano la lettura dei texel con peso 0 non possono essere sfruttate con **gather4**. **gather4** restituisce sempre tutti i texel richiesti.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





