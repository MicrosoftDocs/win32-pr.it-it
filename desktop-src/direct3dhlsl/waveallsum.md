---
title: Funzione WaveActiveSum
description: Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie nell'onda corrente.
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
ms.openlocfilehash: 403768b875ed9462b79fb5d0abeee9539189597591f3a3b20f5a3b9662995542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742261"
---
# <a name="waveactivesum-function"></a>Funzione WaveActiveSum

Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie nell'onda corrente.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveActiveSum(
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

Valore della somma.

## <a name="remarks"></a>Commenti

L'ordine delle operazioni non è definito.

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




