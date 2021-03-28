---
title: sample_d (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995637"
---
# <a name="sample_d-sm4---asm"></a>esempio \_ d (SM4-ASM)

Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| Ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcXDerivatives \[ . Swizzle \] , srcYDerivatives \[ . Swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                               | Descrizione                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                    | \[nell' \] indirizzo dei risultati dell'operazione.<br/>                                                                  |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                     | \[in \] un set di coordinate di trama. Per ulteriori informazioni, vedere l'istruzione di [esempio](sample--sm4---asm-.md) .<br/>      |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                 | \[in \] un registro di trama. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                      |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                     | \[in \] un registro del campionatore. Per ulteriori informazioni, vedere l'istruzione di **esempio** .<br/>                                      |
| <span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*<br/> | \[nei \] derivati per l'indirizzo di origine nella direzione x. Per ulteriori informazioni, vedere la sezione **osservazioni** .<br/> |
| <span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*<br/> | \[nei \] derivati per l'indirizzo di origine nella direzione y. Per ulteriori informazioni, vedere la sezione **osservazioni** .<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione si comporta come l'istruzione di [esempio](sample--sm4---asm-.md) , ad eccezione del fatto che i derivati per l'indirizzo di origine nella direzione x e la direzione y sono forniti rispettivamente da parametri aggiuntivi, *srcXDerivatives* e *srcYDerivatives*. Questi derivati si trovano nello spazio delle coordinate di trama normalizzato.

I componenti r, g e b di *srcXDerivatives* (POS-swizzle) forniscono du/DX, DV/DX e DW/DX. Il componente ' a' (POS-swizzle) viene ignorato.

I componenti r, g e b di *srcYDerivatives* (POS-swizzle) forniscono du/DY, DV/dy e DW/dy. Il componente ' a' (POS-swizzle) viene ignorato.

A differenza dell'istruzione di **esempio** , che consente di condividere un singolo calcolo di LOD in un timbro 2x2, il **campione \_ d** deve calcolare LOD in modo completamente indipendente, per ogni pixel quando viene usato nel pixel shader.

Se gli input derivati per **Sample \_ d** provengono da istruzioni di calcolo derivate nel pixel shader e i valori includono inf/Nan, il comportamento di **Sample \_ d** potrebbe non corrispondere all'istruzione di **esempio** , che calcola in modo implicito il derivato. I valori INF/NaN possono influire in modo diverso sul calcolo LOD.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

### <a name="restrictions"></a>Restrizioni

-   l' **esempio \_ d** eredita le stesse restrizioni dell'istruzione di **esempio** , oltre a una restrizione aggiuntiva riportata di seguito per i parametri aggiuntivi.
-   *srcXDerivatives* e *srcYDerivatives* devono essere Temp (r \# /x \# ), constantBuffer (CB \# ), i registri di input (v \# ) o i valori immediati.

Questa istruzione si applica alle fasi dello shader seguenti:



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

 

 





