---
title: dcl_tgsm_structured (sm5 - asm)
description: Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread del compute shader. La memoria viene visualizzata come matrice di strutture .
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5bf6a6782c455a9bb51ad941a8b6cb42bd70806512a2eef2ed5bd301e57c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673901"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>dcl \_ tgsm \_ structured (sm5 - asm)

Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread del compute shader. La memoria viene visualizzata come matrice di strutture .



| dcl \_ tgsm \_ structured g , \# structByteStride, structCount |
|----------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descrizione                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                                             | \[in \] Riferimento a un blocco di memoria condivisa di dimensioni *structByteStride* \* *byte conteggi.* <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] Stride della struttura. Questo valore è un uint in byte e deve essere un multiplo di 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[in \] Numero di strutture.<br/>                                                                   |



 

## <a name="remarks"></a>Commenti

Lo spazio di archiviazione totale per tutti i valori g deve essere <= la quantità di memoria condivisa disponibile per ogni gruppo di thread, ovvero \# 32 KB o 8192 scalari a 32 bit.

In casi estremi, è possibile dichiarare 8192 g totali, se ognuno ha \# *structByteStride* di 4 e *structCount* di 1.

All'estremità opposta, è possibile dichiarare un singolo g con uno stride della struttura di 32 KB e un numero \# di strutture di 1.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





