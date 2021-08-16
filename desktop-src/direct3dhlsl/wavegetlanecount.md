---
title: Funzione WaveGetLaneCount
description: Restituisce il numero di corsie in un'onda su questa architettura.
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
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504739"
---
# <a name="wavegetlanecount-function"></a>Funzione WaveGetLaneCount

Restituisce il numero di corsie in un'onda su questa architettura.

## <a name="syntax"></a>Sintassi

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Il risultato sarà compreso tra 4 e 128 e include tutte le onde: corsie attive, inattive e/o helper. Il risultato restituito da questa funzione può variare in modo significativo a seconda dell'implementazione del driver.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




