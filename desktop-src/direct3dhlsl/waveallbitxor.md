---
title: WaveActiveBitXor (funzione)
description: Restituisce l'oggetto XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.
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
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047593"
---
# <a name="waveactivebitxor-function"></a>WaveActiveBitXor (funzione)

Restituisce l'oggetto XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*expr* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore XOR bit per bit.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




