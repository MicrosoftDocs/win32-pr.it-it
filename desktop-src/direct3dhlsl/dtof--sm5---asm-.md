---
title: dtof (sm5 - asm)
description: Conversione a livello di componente da dati a virgola mobile e precisione doppia a dati a virgola mobile a precisione singola.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d16ddf79b1a201bf78e0b45d1206169576bee4193b8c8158469055131768efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792328"
---
# <a name="dtof-sm5---asm"></a>dtof (sm5 - asm)

Conversione a livello di componente da dati a virgola mobile e precisione doppia a dati a virgola mobile a precisione singola.



| dtof dest \[ \] .mask, \[ - \] src \[ .swizzle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei dati convertiti.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] I dati da convertire.<br/>          |



 

## <a name="remarks"></a>Commenti

Ogni componente dell'origine viene convertito dalla rappresentazione a precisione doppia alla rappresentazione a precisione singola usando l'arrotondamento arrotondato al più vicino.

Gli swizzle validi per il parametro source sono .xyzw, .xyxy, .zwxy, .zwzw.

Le maschere *dest* valide sono uno o due componenti. Ad esempio: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw Il risultato della prima conversione passa al primo componente nella maschera e il risultato del secondo componente va nel secondo componente della maschera, se presente.

*I componenti dest* sono float32.

*src* è un doppio vec2 attraverso (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB) post swizzle.

Per le conversioni double float32<->, le implementazioni possono rispettare le denorme float32 o scaricarle.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





