---
title: gather4 (SM 4.1-ASM)
description: Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981559"
---
# <a name="gather4-sm41---asm"></a>gather4 (SM 4.1-ASM)

Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] srcSampler. r |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] contiene le coordinate di trama. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro delle risorse. <br/> Swizzle consente il swizzled arbitrario dei valori restituiti prima che vengano scritti in *dest*. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore.<br/> Questo parametro deve avere un Swizzle. r (rosso), che indica che il valore del canale R viene copiato in *dest*. <br/> |



 

## <a name="remarks"></a>Commenti

Questa operazione funziona solo con trame 2D o mappa cubi a canale singolo. Per le trame 2D vengono usate solo le modalità di indirizzamento del campionatore e viene usato il livello superiore di qualsiasi piramide MIP.

Questa istruzione si comporta come l'istruzione di [esempio](sample--sm4---asm-.md) , ma non viene generato un campione filtrato. I quattro esempi che contribuiscono al filtraggio vengono inseriti in xyzw in senso antiorario a partire dall'esempio in basso a sinistra della posizione sottoposta a query. Equivale al campionamento dei punti con (u, v) le coordinate di trama Delta nei percorsi seguenti: (-, +), (+, +), (+,-), (-,-), dove la grandezza dei Delta è sempre metà di un Texel.

Per le trame mappa cubi quando un footprint bidirezionale si estende su un Texel perimetrale dal volto adiacente vengono usati. Gli angoli utilizzano le stesse regole dell'istruzione di **esempio** ; ovvero l'angolo sconosciuto è considerato la media dei tre angoli della faccia con inping.

Le restrizioni relative al formato di trama applicabili alle istruzioni di **esempio** sono valide anche per l'istruzione **gather4** .

Per le implementazioni dell'hardware, le ottimizzazioni nei filtri bilineari tradizionali che rilevano esempi direttamente nei Texel e ignorano la lettura di Texel che non possono essere utilizzate con **gather4**. **gather4** restituisce sempre tutti i Texel richiesti.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





