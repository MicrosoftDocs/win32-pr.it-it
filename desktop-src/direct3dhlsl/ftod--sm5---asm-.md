---
title: ftod (sm5 - asm)
description: Conversione a livello di componente da dati a virgola mobile e precisione singola a dati a virgola mobile a precisione doppia.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31396aa0f2b82dc4ea366bbdde704d55fa850d0d0a9f2f1f3de539a763facb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982431"
---
# <a name="ftod-sm5---asm"></a>ftod (sm5 - asm)

Conversione a livello di componente da dati a virgola mobile e precisione singola a dati a virgola mobile a precisione doppia.



| ftod dest \[ \] .mask, \[ - \] src \[ .swizzle \] , |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei dati convertiti.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] I dati da convertire.<br/>          |



 

## <a name="remarks"></a>Commenti

Ogni componente dell'origine viene convertito dalla rappresentazione a precisione singola alla rappresentazione a precisione doppia.

Le maschere *dest* valide sono xy, zw e xyzw. .xy riceve il risultato della prima conversione e .zw riceve il risultato della seconda conversione.

*dest* è un doppio vec2 attraverso (x 32LSB, y 32MSB) e (z 32LSB, w 32MSB).

*src* è un vec2 float tra x e y (zw ignorato) (post swizzle).

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

 

 





