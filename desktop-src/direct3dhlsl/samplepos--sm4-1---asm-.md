---
title: samplepos (SM 4.1-ASM)
description: Esegue una query sulla posizione di un campione in una visualizzazione risorse shader specificata o nell'rasterizzatore.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398287"
---
# <a name="samplepos-sm41---asm"></a>samplepos (SM 4.1-ASM)

Esegue una query sulla posizione di un campione in una visualizzazione risorse shader specificata o nell'rasterizzatore.



| samplepos dest \[ . mask \] , srcResource \[ . Swizzle \] , sampleIndex (operando scalare) |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[nella \] risorsa shader.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[nell' \] indice dell'esempio.<br/>                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione restituisce la posizione di esempio 2D di *sampleIndex* di esempio per la risorsa specificata. È valido solo per le risorse che possono essere caricate tramite [**ld2dms**](ld2dms--sm4-1---asm-.md) , a meno che il rasterizzatore non sia specificato come *srcResource*.

*srcResource* può essere un registro t \# (visualizzazione risorse shader) o un registro rasterizzatore.

L'istruzione calcola il vettore a virgola mobile (xposition, yposition, 0, 0).

Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione. La posizione di esempio è relativa al centro del pixel, in base al sistema di coordinate dei pixel.

Se *sampleIndex* è fuori limite, viene restituito zero vector. Se non è presente alcuna risorsa associata allo slot specificato, viene restituito 0.

**samplepos** può essere usato per elementi come i resolver personalizzati nel codice dello shader.

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

 

 





