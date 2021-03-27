---
title: LOD (SM 4.1-ASM)
description: Restituisce il livello di dettaglio (LOD) che verrebbe usato per il filtro della trama.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719411"
---
# <a name="lod-sm41---asm"></a>LOD (SM 4.1-ASM)

Restituisce il livello di dettaglio (LOD) che verrebbe usato per il filtro della trama.



| LOD dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo dei risultati.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] un set di coordinate di trama.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore.<br/>           |



 

## <a name="remarks"></a>Commenti

Questo comportamento è analogo all'istruzione di [esempio](sample--sm4---asm-.md) , ma non viene generato un campione filtrato. L'istruzione calcola il vettore seguente (ClampedLOD, NonClampedLOD, 0, 0). NonClampedLOD è un valore LOD calcolato che ignora tutti i bloccaggi dal campionatore o dalla trama (ad esempio, può restituire valori negativi). ClampedLOD è un valore LOD calcolato che verrebbe usato dall'istruzione di **esempio** effettiva. Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.

Se non è presente alcuna risorsa associata allo slot specificato, viene restituito 0.

Se il campionatore utilizza un filtro anisotropico, il LOD deve corrispondere al livello MIP frazionario basato sull'asse più piccolo dell'impronta ellittica.

Questa operazione è valida per i tipi di trama seguenti: Texture1D, Texture2D, Texture3D e TextureCube.

L'istruzione **LOD** non è definita se usata con un campionatore che specifica il filtro MIP del punto, in particolare, qualsiasi \_ enumerazione del filtro D3D10 che termina in un \_ punto MIP. Un esempio è D3D10 \_ FILTRARE \_ il \_ \_ punto MIP min mag \_ .)

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





