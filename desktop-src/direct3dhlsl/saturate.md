---
title: Saturazione (informazioni di riferimento su HLSL)
description: Imposta il risultato di un'operazione aritmetica a virgola mobile a precisione singola o doppia su \ 0,0f... Intervallo 1,0f\.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790744"
---
# <a name="saturate-hlsl-reference"></a>Saturazione (informazioni di riferimento su HLSL)

Imposta il risultato di un'operazione aritmetica a virgola mobile a precisione singola o doppia su \[ 0,0f... Intervallo di 1,0f. \]



| \_Sab |
|-------|



 

Il modificatore del risultato dell'istruzione **saturate** esegue l'operazione seguente sui valori dei risultati da un'operazione aritmetica a virgola \_ mobile applicata:

`min(1.0f, max(0.0f, value))`

dove min() e max() nell'espressione precedente si comportano nel modo in cui [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md)o [dmax](dmax--sm5---asm-.md) operano.

`_sat(NaN)` restituisce 0, in base alle regole per min e max.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo modificatore è supportato nei modelli shader seguenti.



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

[Modificatori di istruzioni](instruction-modifiers.md)
</dt> </dl>

 

 




