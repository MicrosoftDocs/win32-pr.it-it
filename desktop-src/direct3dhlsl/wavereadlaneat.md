---
title: Funzione WaveReadLaneAt
description: Restituisce il valore dell'espressione per l'indice di corsia specificato all'interno dell'onda specificata.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Funzione WaveReadLaneAt HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08fa669f8c4284c26052dd68bdbe9ab4f5b99b80b8bdf9445aa3375f0a87a9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504621"
---
# <a name="wavereadlaneat-function"></a>Funzione WaveReadLaneAt

Restituisce il valore dell'espressione per l'indice di corsia specificato all'interno dell'onda specificata.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Expr* 
</dt> <dd>

Espressione da valutare.

</dd> <dt>

*laneIndex* 
</dt> <dd>

Indice della corsia per cui verrà restituito il risultato *expr.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore risultante è il risultato di *expr*. Sarà uniforme se *laneIndex* è uniforme.

## <a name="remarks"></a>Commenti

Questa funzione è in effetti una trasmissione del valore nella *laneIndex*'th lane.

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader.

## <a name="see-also"></a>Vedi anche

* [Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [Modello shader 6](shader-model-6-0.md)
