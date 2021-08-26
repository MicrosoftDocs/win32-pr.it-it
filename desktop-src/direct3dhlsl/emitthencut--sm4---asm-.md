---
title: emitThenCut (sm4 - asm)
description: Equivale a un comando emit seguito da un comando cut. | emitThenCut (sm4 - asm)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab83fa3eca853a75dca74ef32116e3d13da2dbe76f34fa407f9b0d5f2459d66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023861"
---
# <a name="emitthencut-sm4---asm"></a>emitThenCut (sm4 - asm)

Equivale a un [comando emit](emit--sm4---asm-.md) seguito da un [comando cut.](cut--sm4---asm-.md)



| emitThenCut |
|-------------|



 

## <a name="remarks"></a>Commenti

Questo comando è utile quando si restituisce consapevolmente l'ultimo vertice in una topologia.

Se i flussi sono stati dichiarati, è necessario usare [emitthencut \_ stream](emitthencut-stream--sm5---asm-.md).

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




