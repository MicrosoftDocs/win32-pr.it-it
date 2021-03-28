---
title: dtof (SM5-ASM)
description: Conversione per componenti da dati a virgola mobile a precisione doppia a dati a virgola mobile a precisione singola.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335463"
---
# <a name="dtof-sm5---asm"></a>dtof (SM5-ASM)

Conversione per componenti da dati a virgola mobile a precisione doppia a dati a virgola mobile a precisione singola.



| dtof dest \[ . mask \] , \[ - \] src \[ . Swizzle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei dati convertiti.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] dati da convertire.<br/>          |



 

## <a name="remarks"></a>Commenti

Ogni componente dell'origine viene convertito dalla rappresentazione a precisione doppia alla rappresentazione a precisione singola usando l'arrotondamento arrotondato per eccesso.

Il valore di swizzles valido per il parametro di origine è xyzw, Xyxy, zwxy, zwzw.

Le maschere *dest* valide sono uno o due componenti. Ovvero:. x,. y,. z,. w,. XY,. xz,. XW,. YZ,. YW,. ZW il risultato della prima conversione passa al primo componente nella maschera e il risultato del secondo componente viene inserito nel secondo componente della maschera, se presente.

i componenti *dest* sono float32.

*src* è una doppia vec2 tra (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB) Post Swizzle.

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

 

 





