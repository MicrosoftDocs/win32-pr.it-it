---
title: WaveIsFirstLane (funzione)
description: Restituisce true solo per la corsia attiva nell'onda corrente con l'indice più piccolo.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Funzione WaveIsFirstLane HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339659"
---
# <a name="waveisfirstlane-function"></a>WaveIsFirstLane (funzione)

Restituisce true solo per la corsia attiva nell'onda corrente con l'indice più piccolo.

## <a name="syntax"></a>Sintassi


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

True solo per la corsia attiva nell'onda corrente con l'indice più piccolo.

## <a name="remarks"></a>Commenti

Questa funzione può essere usata per identificare le operazioni che devono essere eseguite una sola volta per ogni Wave.

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




