---
title: FRC (SM4-ASM)
description: Componente frazionario Extract.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976431"
---
# <a name="frc-sm4---asm"></a>FRC (SM4-ASM)

Componente frazionario Extract.



| FRC \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> *dest*  =  *src0*  -  [round \_ NI](round-ni--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] componente dell'operazione.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **src**  | **-INF** | **-F**     | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**     | **+ INF** | **NaN** |
| **dest** | NaN      | \[da + 0 a 1) | +0          | +0     | +0     | +0          | \[da + 0 a 1) | NaN      | NaN     |



 

F indica un numero reale finito.

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

 

 





