---
title: sample_c_lz (sm4 - asm)
description: Esegue un filtro di confronto. Questa istruzione si comporta come l'esempio \_ c, ad eccezione del fatto che LOD è 0 e i derivati vengono ignorati.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2866bdfddf91f9bd6ab1bbccbc9d76de071065b3cf28c1093cb1fdb041f3db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981501"
---
# <a name="sample_c_lz-sm4---asm"></a>sample \_ c \_ lz (sm4 - asm)

Esegue un filtro di confronto. Questa istruzione si comporta come [l'esempio \_ c](sample-c--sm4---asm-.md), ad eccezione del fatto che LOD è 0 e i derivati vengono ignorati.



| sample \_ c \_ lz \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Indirizzo dei risultati dell'operazione.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Un set di coordinate di trama. Per altre informazioni, vedere [l'istruzione di](sample--sm4---asm-.md) esempio.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] Un registro di trama. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] Un registro del campionatore. Per altre informazioni, vedere **l'istruzione di** esempio.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Un registro con un singolo componente selezionato, usato nel confronto.<br/>                            |



 

## <a name="remarks"></a>Commenti

"lz" è l'acronimo di level-zero. Poiché i derivati vengono ignorati, questa istruzione è disponibile in shader diversi dal pixel shader.

Se questa istruzione viene usata con una trama con mipmapped, loD 0 viene campionato, a meno che il campionatore non abbia un blocco LOD che posiziona il LOD in un'altra posizione o se è presente una distorsione LOD, che si limita a distorsione a partire da 0. Poiché i derivati vengono ignorati, il filtro anisotropo si comporta come filtro isotropo.

Nei pixel shader questa istruzione può essere usata all'interno di un controllo di flusso variabile quando le coordinate della trama sono derivate nello shader, a differenza **dell'esempio \_ c**.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

Questa istruzione è disponibile in tutti gli shader, non solo nel pixel shader, per coerenza.



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





