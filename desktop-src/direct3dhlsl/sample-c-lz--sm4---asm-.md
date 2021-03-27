---
title: sample_c_lz (SM4-ASM)
description: Esegue un filtro di confronto. Questa istruzione si comporta come esempio \_ c, ad eccezione di LOD è 0 e i derivati vengono ignorati.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398234"
---
# <a name="sample_c_lz-sm4---asm"></a>esempio \_ c \_ LZ (SM4-ASM)

Esegue un filtro di confronto. Questa istruzione si comporta come [esempio \_ c](sample-c--sm4---asm-.md), ad eccezione di LOD è 0 e i derivati vengono ignorati.



| esempio \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//deve essere. r swizzle srcSampler, srcReferenceValue//componente singolo selezionato |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[nell' \] indirizzo dei risultati dell'operazione.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] un set di coordinate di trama. Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] un registro di trama. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] un registro del campionatore. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] un registro con un singolo componente selezionato, che viene utilizzato nel confronto.<br/>                            |



 

## <a name="remarks"></a>Commenti

"LZ" sta per il livello zero. Poiché i derivati vengono ignorati, questa istruzione è disponibile in shader diversi dal pixel shader.

Se questa istruzione viene usata con una trama mipmap, viene campionato il valore LOD 0, a meno che il campionatore non disponga di un morsetto LOD che inserisce il valore LOD in un altro punto o se è presente una polarizzazione LOD, che può semplicemente essere polarizzata a partire da 0. Poiché i derivati vengono ignorati, il filtro anisotropico si comporta come filtro di applicazione del filtro.

In pixel shader questa istruzione può essere usata all'interno di un controllo di flusso variabile quando le coordinate di trama sono derivate nello shader, a differenza dell' **esempio \_ c**.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

Questa istruzione è disponibile in tutti gli shader, non solo nel pixel shader, per coerenza.



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





