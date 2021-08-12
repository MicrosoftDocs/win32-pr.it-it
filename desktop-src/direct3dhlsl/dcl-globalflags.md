---
title: dcl_globalFlags (sm4 - asm)
description: dcl \_ globalFlags (sm4 - asm)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0901482dd2c282aab98dda72a5c449df69d4551a9a7bb68d80e47c9693c54609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286375"
---
# <a name="dcl_globalflags-sm4---asm"></a>dcl \_ globalFlags (sm4 - asm)

Dichiara i flag globali dello shader.



| dcl \_ globalFlags *flags* |
|--------------------------|



 

<dl> <dt>

<span id="flags"></span><span id="FLAGS"></span>*Bandiere*
</dt> <dd>

\[in \] Un flag shader globale. È attualmente definito un flag.

-   REFACTORING CONSENTITO: consente al driver di riordinare le operazioni aritmetiche per l'ottimizzazione, \_ come illustrato di seguito.

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> Il riordinamento delle operazioni aritmetiche può generare risultati diversi.

 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questa istruzione facoltativa si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Questa istruzione è inclusa per facilitare il debug di uno shader nell'assembly. non è possibile creare uno shader nel linguaggio di assembly usando Shader Model 4.

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 




