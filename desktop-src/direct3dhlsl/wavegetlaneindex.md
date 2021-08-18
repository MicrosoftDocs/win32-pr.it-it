---
title: Funzione WaveGetLaneIndex
description: Restituisce l'indice della corsia corrente all'interno dell'onda corrente.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Funzione WaveGetLaneIndex HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb6b0290b46727cdf0d9ce705d2910df003cbc114638a0135be2023bb836202a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721721"
---
# <a name="wavegetlaneindex-function"></a>Funzione WaveGetLaneIndex

Restituisce l'indice della corsia corrente all'interno dell'onda corrente.

## <a name="syntax"></a>Sintassi

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Indice della corsia corrente. Il risultato sarà compreso tra 0 e il risultato restituito da [**WaveGetLaneCount.**](wavegetlanecount.md)

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




