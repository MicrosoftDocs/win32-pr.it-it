---
title: dcl_tgsm_structured (SM5-ASM)
description: Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader. La memoria viene visualizzata come una matrice di strutture.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993040"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>\_ \_ strutturato DCL TGSM (SM5-ASM)

Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread compute shader. La memoria viene visualizzata come una matrice di strutture.



| DCL \_ TGSM \_ strutturato g \# , structByteStride, structCount |
|----------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descrizione                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*g\#*<br/>                                                                             | \[in \] un riferimento a un blocco di memoria condivisa di dimensioni *structByteStride* \* *structCount* byte. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[nello \] stride della struttura. Questo valore è un uint in byte e deve essere un multiplo di 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[nel \] numero di strutture.<br/>                                                                   |



 

## <a name="remarks"></a>Commenti

Lo spazio di archiviazione totale per tutte le g \# deve essere <= la quantità di memoria condivisa disponibile per gruppo di thread, ovvero 32 KB, o scalari a 8192 32 bit.

In un caso estremo, è possibile dichiarare il totale di 8192 g \# s, se ogni *structByteStride* ha un valore pari a 4 e un *structCount* di 1.

Nell'estremo opposto è possibile dichiarare un singolo g \# con uno stride della struttura di 32 KB e un conteggio di struttura pari a 1.

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

 

 





