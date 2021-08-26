---
title: dcl_output oMask (sm5 - asm)
description: Dichiarare un registro di output che deve essere scritto dallo shader.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a6860904b557bc21a5202bbfd60105852adc260580457afb02b4fe6d92352b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068511"
---
# <a name="dcl_output-omask-sm5---asm"></a>dcl \_ output oMask (sm5 - asm)

Dichiarare un registro di output che deve essere scritto dallo shader.



| dcl \_ output o \# \[ .mask\] |
|--------------------------|



 



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*o*<br/> | \[nel \] registro di output.<br/> |



 

## <a name="remarks"></a>Commenti


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Restrizioni

-   La maschera del componente può essere qualsiasi subset \[ di xyzw \] . Tuttavia, lasciando spazi tra i componenti si spreca spazio.
-   È legale dichiarare un superset della maschera del componente dichiarata per l'input dalla fase successiva. Non sono tuttavia consentite maschere che si escludono a vicenda. Il vertex shader che restituisce o3.xy indica che l'input pixel shader v3.z non è valido, ma l'input v3.x o v3.y o v3.xy è valido.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

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

 

 





