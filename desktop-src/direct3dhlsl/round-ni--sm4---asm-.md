---
title: round_ni (SM4-ASM)
description: Arrotondamento a virgola mobile al valore float integrale. | round_ni (SM4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3daafd64e76bd8c04acf7812b096f7374befef6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058540"
---
# <a name="round_ni-sm4---asm"></a>Round \_ NI (SM4-ASM)

Arrotondamento a virgola mobile al valore float integrale.



| Round \_ NI \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un arrotondamento a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali in *dest*. **round \_ NI** viene arrotondato verso l'infinito, comunemente noto come Floor ().

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.

F indica un numero reale finito.



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **src**  | **-INF** | **-F** | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F** | **+ INF** | **NaN** |
| **dest** | -inf     | -F     | -0          | -0     | +0     | +0          | + F     | +inf     | NaN     |



 

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

 

 





