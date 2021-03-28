---
title: gather4 (SM5-ASM)
description: Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234710"
---
# <a name="gather4-sm5---asm"></a>gather4 (SM5-ASM)

Raccoglie i quattro Texel che verrebbero usati in un'operazione di filtraggio bilineare e li imballa in un unico registro. Questa istruzione funziona solo con trame 2D o mappa cubi, incluse le matrici. Vengono utilizzate solo le modalità di indirizzamento del campionatore e viene utilizzato il livello principale di qualsiasi piramide MIP.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ Component\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] un set di coordinate di trama.<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama.<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore.<br/>                          |



 

## <a name="remarks"></a>Commenti

Questa istruzione si comporta come l'istruzione di [**esempio**](sample--sm4---asm-.md) , ma non viene generato un campione filtrato. I quattro esempi che contribuiscono al filtraggio vengono inseriti in xyzw in senso antiorario a partire dall'esempio in basso a sinistra della posizione sottoposta a query. Equivale al campionamento dei punti con (u, v) le coordinate di trama Delta nei percorsi seguenti: (-, +), (+, +), (+,-), (-,-), dove la grandezza dei Delta è sempre metà di un Texel.

Per le trame mappa cubi, quando un'impronta bi lineare si estende su un bordo, vengono usati i Texel del volto adiacente. Gli angoli utilizzano le stesse regole dell'istruzione di [**esempio**](sample--sm4---asm-.md) ; ovvero, l'angolo sconosciuto viene considerato la media dei tre angoli della faccia di cui si sta effettuando il ping.

Sono presenti restrizioni relative al formato di trama che si applicano a **gather4** , espresse nell'elenco dei formati.

Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.

Il componente. Select \_ in *srcSampler* sceglie il componente della trama di origine (r/g/b/a) da cui leggere 4 Texel.

Per i formati con componenti float32, se il valore recuperato è normalizzato, denormalizzato, +-0 o +-INF, viene restituito allo shader inalterato. NaN viene restituito come NaN, ma la rappresentazione di bit esatta di NaN può essere modificata. Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi in corrispondenza degli angoli, quindi la restituzione di bit invariati per il Texel sintetizzato non si applica e le denormazioni potrebbero essere scaricate.

Per le implementazioni dell'hardware, le ottimizzazioni nei filtri bilineari tradizionali che rilevano esempi direttamente nei Texel e ignorano la lettura di Texel che non possono essere utilizzate con questa istruzione. *gather4* restituisce sempre tutti i Texel richiesti.

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

 

 





