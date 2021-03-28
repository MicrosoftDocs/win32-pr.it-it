---
title: uaddc (SM5-ASM)
description: Intero senza segno aggiungere con Carry.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516483"
---
# <a name="uaddc-sm5---asm"></a>uaddc (SM5-ASM)

Intero senza segno aggiungere con Carry.



| uaddc dest0 \[ . mask \] , DesT1 \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descrizione                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[\]indirizzo del risultato.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] 1 se viene prodotto Carry. In caso contrario, 0<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[nell' \] operando a 32 bit da aggiungere.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[nell' \] operando a 32 bit da aggiungere.<br/>          |



 

## <a name="remarks"></a>Commenti

*DesT1* può essere null se il trasporto non è necessario.

Usare questa istruzione per operazioni aritmetiche con precisione elevata.

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

 

 





