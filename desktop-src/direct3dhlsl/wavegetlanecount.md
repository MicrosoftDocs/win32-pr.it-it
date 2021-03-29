---
title: WaveGetLaneCount (funzione)
description: Restituisce il numero di corsie in un'onda in questa architettura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Funzione WaveGetLaneCount HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399935"
---
# <a name="wavegetlanecount-function"></a>WaveGetLaneCount (funzione)

Restituisce il numero di corsie in un'onda in questa architettura.

## <a name="syntax"></a>Sintassi

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Il risultato sarà compreso tra 4 e 128 e includerà tutte le onde, ovvero attive, inattive e/o corsie helper. Il risultato restituito da questa funzione può variare in modo significativo a seconda dell'implementazione del driver.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




