---
title: ISHR (SM4-ASM)
description: Spostamento aritmetico a destra (estensione di segno). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995732"
---
# <a name="ishr-sm4---asm"></a>ISHR (SM4-ASM)

Spostamento aritmetico a destra (estensione di segno).



| ISHR dest \[ . mask \] , src0 \[ . Swizzle \] , src1. Select \_ Component |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contiene il risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] contiene il valore da spostare.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] contiene l'importo dello spostamento.<br/>            |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue uno spostamento aritmetico a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) nel *\_ componente src1. Select*, replicando il valore di bit 31. Il risultato di 32 bit per componente viene inserito in *dest*. Il conteggio è un valore scalare applicato a tutti i componenti.

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

 

 





