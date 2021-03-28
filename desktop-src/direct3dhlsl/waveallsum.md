---
title: WaveActiveSum (funzione)
description: Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie nell'onda corrente.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Funzione WaveActiveSum HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963562"
---
# <a name="waveactivesum-function"></a>WaveActiveSum (funzione)

Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie nell'onda corrente.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveActiveSum(
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

Valore sum.

## <a name="remarks"></a>Commenti

L'ordine delle operazioni non è definito.

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




