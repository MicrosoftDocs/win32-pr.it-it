---
title: Funzione WaveActiveMax
description: Restituisce il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Funzione WaveActiveMax HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c85936ca28aabe0365fd912b4d764739b0ab15765241a243ad67143dacd0d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484201"
---
# <a name="waveactivemax-function"></a>Funzione WaveActiveMax

Restituisce il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Expr* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore massimo.

## <a name="remarks"></a>Commenti

L'ordine delle operazioni non è definito.

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




