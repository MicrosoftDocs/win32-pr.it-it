---
title: iadd (sm4 - asm)
description: Addizione di numeri interi.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9226223b5a065714ca17bd63775b8d4e8a3bc9b96de111cec87b879114728bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285790"
---
# <a name="iadd-sm4---asm"></a>iadd (sm4 - asm)

Addizione di numeri interi.



| iadd dest \[ \] .mask, \[ - \] src0 \[ .swizzle, \] \[ - \] src1 \[ .swizzle\] |
|------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Numero da aggiungere a *src1.*<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Numero da aggiungere a *src0*.<br/>           |



 

## <a name="remarks"></a>Commenti

Aggiunta a livello di componente degli operandi a 32 bit *src0* e *src1,* inserendo il risultato corretto a 32 bit in *dest*. Non viene eseguito alcun carry o borrow oltre i valori a 32 bit di ogni componente, pertanto questa istruzione non è sensibile al valore signed-ness dei relativi operandi.

Il modificatore di negazione facoltativo sugli operandi di origine accetta il complemento 2 prima di eseguire l'operazione.

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

 

 





