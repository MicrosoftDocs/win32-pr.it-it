---
title: Negate
description: Capovolge il segno del valore di un operando di origine utilizzato in un'operazione aritmetica.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046072"
---
# <a name="negate"></a>Negate

Capovolge il segno del valore di un operando di origine utilizzato in un'operazione aritmetica.



| \-  |
|-----|



 

Per le istruzioni e i punti a virgola mobile a precisione singola e doppia, il modificatore negazioni capovolge il segno dei numeri nell'operando di origine, inclusi i valori INF. L'applicazione di **negazione** in NaN conserva Nan, anche se il particolare modello di bit Nan che risulta non è definito.

Per le istruzioni Integer, il modificatore **negazioni** accetta il complemento 2 del numero o dei numeri nell'operando di origine.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo modificatore è supportato nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di istruzione](instruction-modifiers.md)
</dt> </dl>

 

 




