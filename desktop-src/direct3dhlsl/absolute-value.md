---
title: Valore assoluto
description: Accetta il valore assoluto di un operando di origine usato in un'operazione aritmetica.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 904ff3bb89e71a95a1c88851426ba283987ba6b96f336c91dd443794ee5e143d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795410"
---
# <a name="absolute-value"></a>Valore assoluto

Accetta il valore assoluto di un operando di origine usato in un'operazione aritmetica.



| \_Ass |
|-------|



 

Questo modificatore viene usato solo per le istruzioni e la virgola mobile a precisione singola e doppia. Il **\_ modificatore abs** forza il segno dei numeri sull'operando di origine positivo, inclusi i valori INF.

**\_ L'applicazione di abs** su NaN mantiene NaN, anche se il particolare modello di bit NaN che risulta non è definito.

Quando abs viene combinato con il modificatore negate, la combinazione forza il segno a essere negativo, come se il \_ **\_ modificatore abs** viene applicato per [](negate.md) primo, quindi nega **.**

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

 

 




