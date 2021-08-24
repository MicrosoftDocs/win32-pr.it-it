---
title: eq (sm4 - asm)
description: Confronto di uguaglianza a virgola mobile vettoriale per componente.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a90af3fd6f65a6a81c32592650c4be33996c96a1d99415ec1dfecb0b0f83ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789041"
---
# <a name="eq-sm4---asm"></a>eq (sm4 - asm)

Confronto di uguaglianza a virgola mobile vettoriale per componente.



| eq dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|----------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Il componente da convertire in *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Il componente da convertire in *src0*.<br/>         |



 

## <a name="remarks"></a>Commenti

Esegue il confronto float (*src0*  ==  *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, 0xFFFFFFFF restituito per tale componente. In caso 0x0000000 viene restituito .

I denorm vengono scaricati prima del confronto (i registri dell'origine originale non vengono toccati). +0 è uguale a -0. Il confronto con NaN restituisce false.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





