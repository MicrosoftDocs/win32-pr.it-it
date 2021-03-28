---
title: GE (SM4-ASM)
description: Confronto a virgola mobile vettoriale a livello di componente maggiore di o uguale a.
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398224"
---
# <a name="ge-sm4---asm"></a>GE (SM4-ASM)

Confronto a virgola mobile vettoriale a livello di componente maggiore di o uguale a.



| GE dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] componente da confrontare con *src1*.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nel \] componente da confrontare con *src0*.<br/>         |



 

## <a name="remarks"></a>Commenti

Esegue il confronto float (*src0*  >=  *src1*) per ogni componente e scrive il risultato in *dest*.

Se il confronto è true, viene restituito 0xFFFFFFFF per quel componente. In caso contrario, viene restituito 0x0000000.

Le denormazioni vengono scaricate prima del confronto e i registri di origine originali non vengono modificati. + 0 è uguale a-0. Il confronto con NaN restituisce false.

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

 

 





