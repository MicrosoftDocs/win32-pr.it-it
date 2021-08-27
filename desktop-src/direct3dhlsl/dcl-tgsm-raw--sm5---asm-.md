---
title: dcl_tgsm_raw (sm5 - asm)
description: Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread del compute shader.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0945cde7719129ca43368e50258c02727103209b8d467932e79acd1e1150c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024691"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>dcl \_ tgsm \_ raw (sm5 - asm)

Dichiarare un riferimento a un'area di spazio di memoria condivisa disponibile per il gruppo di thread del compute shader.



| dcl \_ tgsm \_ raw g , \# byteCount |
|-------------------------------|



 



| Elemento                                                                                                       | Descrizione                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                 | \[in \] Riferimento a un blocco di dimensioni *byteCount* della memoria condivisa non tipiata. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*Bytecount*<br/> | \[in \] Deve essere un multiplo di 4. <br/>                                             |



 

## <a name="remarks"></a>Commenti

Lo spazio di archiviazione totale per tutti i g deve essere <= la quantità di memoria condivisa disponibile per ogni gruppo di \# thread, ovvero 32 KB.

In casi estremi, è possibile dichiarare 8192 g totali, ognuno \# con *un byteCount* di 4.

All'estremità opposta, è possibile dichiarare un singolo g \# con *un byteCount* di 32768.

> [!Note]  
> cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supporta [dcl \_ tgsm \_ strutturato,](dcl-tgsm-structured--sm5---asm-.md)ma non **dcl \_ tgsm \_ raw.**

 

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

 

 





