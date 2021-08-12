---
title: countbits (sm5 - asm)
description: Conta il numero di bit impostati in un numero.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b13be61d470f5a8504c893f85bea4b7f500591d35118aec2bf6576b897a4b5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286953"
---
# <a name="countbits-sm5---asm"></a>countbits (sm5 - asm)

Conta il numero di bit impostati in un numero.



| countbits dest \[ .mask \] , src0 \[ .swizzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Numero a 32 bit di input.<br/>    |



 

## <a name="remarks"></a>Commenti

Questa istruzione può essere usata per calcolare la percentuale di code coverage di input dello shader.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





