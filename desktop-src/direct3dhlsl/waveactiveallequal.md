---
title: WaveActiveAllEqual (funzione)
description: Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e di conseguenza uniforme).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Funzione WaveActiveAllEqual HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734799"
---
# <a name="waveactiveallequal-function"></a>WaveActiveAllEqual (funzione)

Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e di conseguenza uniforme).

## <a name="syntax"></a>Sintassi


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*expr* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

True se l'espressione è la stessa per ogni corsia attiva nell'onda corrente.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




