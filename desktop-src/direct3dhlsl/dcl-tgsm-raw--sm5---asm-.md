---
title: dcl_tgsm_raw (SM5-ASM)
description: Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719465"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>\_RAW DCL TGSM \_ (SM5-ASM)

Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader.



| DCL \_ TGSM \_ RAW g \# , GetByteCount |
|-------------------------------|



 



| Elemento                                                                                                       | Descrizione                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*g\#*<br/>                                                 | \[in \] un riferimento a un blocco di dimensioni  non tipizzate della memoria condivisa. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[in \] deve essere un multiplo di 4. <br/>                                             |



 

## <a name="remarks"></a>Commenti

Lo spazio di archiviazione totale per tutti i g \# deve essere <= la quantità di memoria condivisa disponibile per ogni gruppo di thread, ovvero 32 KB.

In un caso estremo, è possibile dichiarare il totale di 8192 g \# s, ognuno  con un valore di i/o di 4.

Nell'estremo opposto è possibile dichiarare un singolo g \# con un valore di  32768.

> [!Note]  
> cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano [DCL \_ TGSM \_ strutturate](dcl-tgsm-structured--sm5---asm-.md), ma **non \_ TGSM DCL \_ RAW**.

 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





