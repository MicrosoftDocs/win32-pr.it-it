---
title: ISHR (SM5-ASM)
description: Spostamento aritmetico a destra (estensione di segno). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995729"
---
# <a name="ishr-sm5---asm"></a>ISHR (SM5-ASM)

Spostamento aritmetico a destra (estensione di segno).



| ISHL dest \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contiene i risultati dello spostamento.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]numero di bit da spostare.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] valori a 32 bit da spostare.<br/>        |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue uno spostamento aritmetico a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit unsigned integer fornito da LSB 5 bits (intervallo 0-31) in *src1*, replicando il valore di bit 31. Il risultato di 32 bit per componente viene inserito in *dest*.

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

 

 





