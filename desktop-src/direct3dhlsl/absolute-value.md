---
title: Valore assoluto
description: Assumere il valore assoluto di un operando di origine utilizzato in un'operazione aritmetica.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335615"
---
# <a name="absolute-value"></a>Valore assoluto

Assumere il valore assoluto di un operando di origine utilizzato in un'operazione aritmetica.



| \_ABS |
|-------|



 

Questo modificatore viene utilizzato per solo istruzioni e virgola mobile a precisione singola e doppia. Il modificatore **\_ ABS** forza il segno dei numeri sull'operando di origine positivo, inclusi i valori inf.

L'applicazione di **\_ ABS** su Nan conserva Nan, anche se il particolare modello di bit Nan che risulta non è definito.

Quando \_ ABS viene combinato con il modificatore [negazioni](negate.md) , la combinazione forza il segno a essere negativo, come se il modificatore **\_ ABS** venisse applicato per primo, quindi la **negazione**.

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

 

 




