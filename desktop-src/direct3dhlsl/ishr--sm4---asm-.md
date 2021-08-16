---
title: ishr (sm4 - asm)
description: Spostamento aritmetico a destra (estensione del segno). | ishr (sm4 - asm)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2ec191320561b05ba736b7da5630fb50a610e739d0e74f9def3eaa10bb4e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511136"
---
# <a name="ishr-sm4---asm"></a>ishr (sm4 - asm)

Spostamento aritmetico a destra (estensione del segno).



| ishr dest \[ .mask \] , src0 \[ .swizzle \] , src1.select \_ component |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Contiene il risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Contiene il valore da spostare.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Contiene l'importo dello spostamento.<br/>            |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue uno spostamento aritmetico a livello di componente di ogni valore a 32 bit in *src0* a destra di un conteggio di bit intero senza segno fornito dall'intervallo 5 bit LSB (intervallo 0-31) nel *componente src1.select \_*, replicando il valore del bit 31. Il risultato a 32 bit per componente viene inserito in *dest*. Il conteggio è un valore scalare applicato a tutti i componenti.

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

 

 





