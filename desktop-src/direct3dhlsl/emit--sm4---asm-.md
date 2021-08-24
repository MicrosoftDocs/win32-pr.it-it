---
title: emit (sm4 - asm)
description: Creare un vertice.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce90ed4ea87c74c09c6f45d590e8bc7a70bbb8178988b059c2b3a79726aabcb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673081"
---
# <a name="emit-sm4---asm"></a>emit (sm4 - asm)

Creare un vertice.



| Emettere |
|------|



 

## <a name="remarks"></a>Commenti

**emit** fa in modo che tutti i registri o dichiarati \# siano letti da Geometry Shader per generare un vertice.

Quando vengono **emesse** più chiamate di emissione, vengono generate primitive.

**emit** può essere visualizzato un numero qualsiasi di volte in un Geometry Shader, incluso il controllo di flusso.

Se i flussi sono stati dichiarati, è necessario usare [il flusso emit \_ ](emit-stream--sm5---asm-.md).

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               | x               |              |



 

### <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 




