---
title: Funzione WaveActiveBitXor
description: Restituisce l'XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- Funzione WaveActiveBitXor HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 733ab8c40a59b784af8a7d50c4f8e1e543f344ee2d75ed9b6896992e6176ff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504881"
---
# <a name="waveactivebitxor-function"></a>Funzione WaveActiveBitXor

Restituisce l'XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Expr* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore XOR bit per bit.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




