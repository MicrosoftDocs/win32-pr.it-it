---
title: f16tof32 (sm5 - asm)
description: Conversione da float16 a float32 per componente. | f16tof32 (sm5 - asm)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc4456737d5ddaaed351ae2a1cc76418c33af9c498e725099e1912d8fabe7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562652"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (sm5 - asm)

Conversione da float16 a float32 per componente.



| f16tof32 dest \[ .mask \] , \[ - \] src \[ .swizzle\] |
|----------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato float32.<br/> |
| <span id="src"></span><span id="SRC"></span>*Src*<br/>    | \[in \] Valore float16 da convertire.<br/>      |



 

## <a name="remarks"></a>Commenti

Questa operazione esegue una conversione per componente di un valore float16 da bit LSB a un risultato float32.

Questa operazione segue le regole D3D per la conversione a virgola mobile.

Usare questa istruzione per la decompressione dei dati basata su shader.

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

 

 





