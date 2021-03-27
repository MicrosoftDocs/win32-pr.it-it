---
title: f32tof16 (SM5-ASM)
description: Conversione da float16 a float32 a livello di componente. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982031"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Conversione da float16 a float32 a livello di componente.



| f32tof16 dest \[ . mask \] , \[ - \] src \[ . Swizzle\] |
|----------------------------------------------|



 



| Elemento                                                            | Descrizione                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato di float16.<br/> |
| <span id="src"></span><span id="SRC"></span>*src*<br/>    | \[nel \] valore float32 da convertire.<br/>  |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una conversione a livello di componente di un valore float32 in un risultato di valore float16 inserito in LSB 16 bit.

Questa istruzione segue le regole D3D per la conversione a virgola mobile.

Usare questa istruzione per la compressione dei dati basata su shader.

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

 

 





