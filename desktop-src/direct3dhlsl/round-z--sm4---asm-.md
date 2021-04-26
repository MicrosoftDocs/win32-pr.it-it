---
title: round_z (sm4 - asm)
description: Arrotondamento a virgola mobile a float integrale. | round_z (sm4 - asm)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997128"
---
# <a name="round_z-sm4---asm"></a>round \_ z (sm4 - asm)

Arrotondamento a virgola mobile a float integrale.



| round \_ z \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-----------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un round a virgola mobile a livello di componente dei valori in *src0*, scrivendo valori a virgola mobile integrali *in dest*.

**round \_ z** arrotonda verso zero.

La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

F indica un numero finito-reale.

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

 

 





