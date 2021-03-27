---
title: Saturate (riferimento HLSL)
description: Consente di bloccare il risultato di un'operazione aritmetica a virgola mobile a precisione singola o doppia a \ 0,0 f... 1,0 f \ intervallo.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398336"
---
# <a name="saturate-hlsl-reference"></a>Saturate (riferimento HLSL)

Consente di bloccare il risultato di un'operazione aritmetica a virgola mobile a precisione singola o doppia a \[ 0,0 f... 1,0 f \] intervallo.



| \_Sat |
|-------|



 

Il modificatore di risultato dell'istruzione **saturate** esegue l'operazione seguente sui valori dei risultati da un'operazione aritmetica a virgola mobile a cui è stato \_ applicato il Sab:

`min(1.0f, max(0.0f, value))`

dove min () e Max () nell'espressione precedente si comportano nel modo in cui [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)o [DMax](dmax--sm5---asm-.md) operano.

`_sat(NaN)` restituisce 0, in base alle regole per min e max.

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

 

 




