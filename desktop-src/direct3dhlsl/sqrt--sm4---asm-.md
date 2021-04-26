---
title: sqrt (sm4 - asm)
description: Radice quadrata per componente.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996608"
---
# <a name="sqrt-sm4---asm"></a>sqrt (sm4 - asm)

Radice quadrata per componente.



| sqrt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Risultato dell'operazione.<br/> *dest* = sqrt(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti per i quali prendere la radice quadrata.<br/>             |



 

## <a name="remarks"></a>Commenti

La precisione è 1 ulp.

La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow.

F indica un numero finito reale.



|          | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | NaN      | NaN    | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 





