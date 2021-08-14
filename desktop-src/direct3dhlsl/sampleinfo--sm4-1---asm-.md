---
title: sampleinfo (sm4.1 - asm)
description: Esegue una query sul numero di esempi in una determinata visualizzazione di risorse shader o nel rasterizzatore.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2227afbf7a08a0010efc2efb8fcf87bae85c8f5775e596d92b761b556f8bfb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510469"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (sm4.1 - asm)

Esegue una query sul numero di esempi in una determinata visualizzazione di risorse shader o nel rasterizzatore.



| \[\_uint \] dest \[ .mask \] , srcResource \[ .swizzle\] |
|---------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[nella \] risorsa shader.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questa istruzione restituisce il numero di esempi per la risorsa specificata o il rasterizzatore. È valido solo per le risorse che possono essere caricate usando [**ld2dms**](ld2dms--sm4-1---asm-.md) a meno che il rasterizzatore non sia *specificato come srcResource*. *srcResource* può essere un registro t \# (una visualizzazione di risorse shader) o un registro rasterizzatore.

L'istruzione calcola il vettore (SampleCount,0,0,0).

Lo swizzle in *srcResource* consente di scorrere arbitrariamente i valori restituiti prima che siano scritti nella destinazione. Il valore restituito è a virgola mobile, a meno che non venga usato il modificatore \_ uint, nel qual caso il valore restituito è integer. Se non è presente alcuna risorsa associata a uno slot specificato, viene restituito 0.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

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

 

 





