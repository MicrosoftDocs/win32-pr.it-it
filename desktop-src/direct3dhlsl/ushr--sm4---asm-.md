---
title: ushr (sm4 - asm)
description: Maiusc a destra. | ushr (sm4 - asm)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55343f9c9b4db4fff4b0df7ab4e2a567f25f0eb43e93486fe9c41b89cf68454
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787821"
---
# <a name="ushr-sm4---asm"></a>ushr (sm4 - asm)

Maiusc a destra.



| ushr dest \[ .mask \] , src0 \[ .swizzle \] , src1.select \_ component |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da spostare.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Quantità di spostamento di *src0*.<br/>                 |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit intero senza segno fornito dall'intervallo LSB a 5 bit (intervallo 0-31) nel *componente src1.select \_*, inserendo 0. Il risultato a 32 bit per componente viene inserito in *dest*. Il conteggio è un valore scalare applicato a tutti i componenti.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





