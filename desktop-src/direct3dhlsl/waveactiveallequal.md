---
title: Funzione WaveActiveAllEqual
description: Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e quindi uniforme su di essa).
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
ms.openlocfilehash: f62493a1bf08b85e95acad319bac2d022c30a53d43c28a87d0f5f603e78d300f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786111"
---
# <a name="waveactiveallequal-function"></a>Funzione WaveActiveAllEqual

Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e quindi uniforme su di essa).

## <a name="syntax"></a>Sintassi


``` syntax
bool WaveActiveAllEqual(
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

True se l'espressione è la stessa per ogni corsia attiva nell'onda corrente.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




