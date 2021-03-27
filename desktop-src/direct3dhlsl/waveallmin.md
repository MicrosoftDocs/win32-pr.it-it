---
title: WaveActiveMin (funzione)
description: Restituisce il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente che viene replicato nuovamente in tutte le corsie attive.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Funzione WaveActiveMin HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047594"
---
# <a name="waveactivemin-function"></a>WaveActiveMin (funzione)

Restituisce il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente che viene replicato nuovamente in tutte le corsie attive.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveActiveMin(
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

Valore minimo.

## <a name="remarks"></a>Commenti

L'ordine delle operazioni non è definito.

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




