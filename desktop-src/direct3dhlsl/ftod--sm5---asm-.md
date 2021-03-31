---
title: ftod (SM5-ASM)
description: Conversione per componente da dati a virgola mobile a precisione singola a dati a virgola mobile a precisione doppia.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335567"
---
# <a name="ftod-sm5---asm"></a>ftod (SM5-ASM)

Conversione per componente da dati a virgola mobile a precisione singola a dati a virgola mobile a precisione doppia.



| ftod dest \[ . mask \] , \[ - \] src \[ . Swizzle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei dati convertiti.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] dati da convertire.<br/>          |



 

## <a name="remarks"></a>Commenti

Ogni componente dell'origine viene convertito dalla rappresentazione con precisione singola alla rappresentazione a precisione doppia.

Le maschere *dest* valide sono. XY,. ZW e. xyzw. . XY riceve il risultato della prima conversione e. ZW riceve il risultato della seconda conversione.

*dest* è un doppio vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

*src* è un vec2 float tra x e y (ZW ignorato) (post swizzle).

Per le conversioni float32<->doppie, le implementazioni possono rispettare le denormazioni di float32 o scaricarle.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





