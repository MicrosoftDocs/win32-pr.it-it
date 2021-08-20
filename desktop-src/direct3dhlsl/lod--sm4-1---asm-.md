---
title: lod (sm4.1 - asm)
description: Restituisce il livello di dettaglio (LOD) che verrebbe usato per il filtro della trama.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0575ff4b7cd332375d6b4b172ec5f1df43c66ec0bed4158b993c244b8c5a0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906925"
---
# <a name="lod-sm41---asm"></a>lod (sm4.1 - asm)

Restituisce il livello di dettaglio (LOD) che verrebbe usato per il filtro della trama.



| lod dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource \[ .swizzle, \] srcSampler |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo dei risultati.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Un set di coordinate di trama.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Un registro di trama.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] Un registro del campionatore.<br/>           |



 

## <a name="remarks"></a>Commenti

Si comporta come [l'istruzione di](sample--sm4---asm-.md) esempio, ma non viene generato un esempio filtrato. L'istruzione calcola il vettore seguente (ClampedLOD, NonClampedLOD, 0, 0). NonClampedLOD è un valore LOD calcolato che ignora le eventuali maniglie del campionatore o della trama(ad esempio, può restituire valori negativi). ClampedLOD è un valore LOD calcolato che verrebbe usato dall'istruzione **di esempio** effettiva. Lo swizzle in *srcResource* consente di eseguire lo swizzle arbitrario dei valori restituiti prima che siano scritti nella destinazione.

Se non è presente alcuna risorsa associata a uno slot specificato, viene restituito 0.

Se il campionatore usa il filtro anisotropo, il loD deve corrispondere al livello di mip frazionario in base all'asse più piccolo del footprint ellittico.

Questa opzione è valida per i tipi di trama seguenti: Texture1D, Texture2D, Texture3D e TextureCube.

**L'istruzione lod** non viene definita se usata con un campionatore che specifica il filtro MIP del punto, in particolare qualsiasi enumerazione FILTER D3D10 che termina \_ con MIP \_ POINT. Un esempio è D3D10 \_ FILTER \_ MIN \_ MAG \_ MIP \_ POINT.)

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





