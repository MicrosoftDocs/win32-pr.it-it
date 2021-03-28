---
title: dcl_output oMask (SM5-ASM)
description: Dichiarare un registro di output che deve essere scritto dallo shader.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398301"
---
# <a name="dcl_output-omask-sm5---asm"></a>\_oMask di output di DCL (SM5-ASM)

Dichiarare un registro di output che deve essere scritto dallo shader.



| \_o \# \[ . mask output DCL\] |
|--------------------------|



 



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*o*<br/> | \[nel \] Registro di output.<br/> |



 

## <a name="remarks"></a>Commenti


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Restrizioni

-   Il componente mask può essere qualsiasi subset di \[ xyzw \] . Tuttavia, lasciando vuoti tra i componenti, lo spazio viene sprecato.
-   È lecito dichiarare un superset della maschera dei componenti dichiarata per l'input dalla fase successiva. Non sono tuttavia consentite maschere che si escludono a vicenda. Il vertex shader che ha output O3. XY significa che il pixel shader inserire V3. z non è valido, ma l'inserimento di V3. x o V3. y o V3. XY è valido.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

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

 

 





