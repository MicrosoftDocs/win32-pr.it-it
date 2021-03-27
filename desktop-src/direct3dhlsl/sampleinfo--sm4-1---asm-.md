---
title: sampleinfo (SM 4.1-ASM)
description: Esegue una query sul numero di campioni in una determinata visualizzazione risorse shader o nell'rasterizzatore.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857813"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (SM 4.1-ASM)

Esegue una query sul numero di campioni in una determinata visualizzazione risorse shader o nell'rasterizzatore.



| \[\_uint \] dest \[ . mask \] , srcResource \[ . Swizzle\] |
|---------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[nella \] risorsa shader.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questa istruzione restituisce il numero di campioni per la risorsa o il rasterizzatore specificato. È valido solo per le risorse che possono essere caricate tramite [**ld2dms**](ld2dms--sm4-1---asm-.md) , a meno che il rasterizzatore non sia specificato come *srcResource*. *srcResource* potrebbe essere un registro t \# (visualizzazione risorse shader) o un registro rasterizzatore.

L'istruzione calcola il vettore (SampleCount, 0, 0, 0).

Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione. Il valore restituito è a virgola mobile, a meno che non \_ venga usato il modificatore uint, nel qual caso il valore restituito è Integer. Se non è presente alcuna risorsa associata allo slot specificato, viene restituito 0.

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
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





