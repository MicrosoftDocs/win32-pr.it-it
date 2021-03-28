---
title: IAdd (SM4-ASM)
description: Aggiunta Integer.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398278"
---
# <a name="iadd-sm4---asm"></a>IAdd (SM4-ASM)

Aggiunta Integer.



| IAdd dest \[ . mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\] |
|------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] numero da aggiungere a *src1*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] numero da aggiungere a *src0*.<br/>           |



 

## <a name="remarks"></a>Commenti

Aggiunta a livello di componente di operandi a 32 bit *src0* e *src1*, inserendo il risultato corretto a 32 bit in *dest*. Non viene eseguita alcuna operazione Carry o borrow oltre i valori a 32 bit di ogni componente, quindi questa istruzione non è sensibile alla firma degli operandi.

Il modificatore negazioni facoltativo negli operandi di origine richiede il complemento di 2 prima di eseguire l'operazione.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





