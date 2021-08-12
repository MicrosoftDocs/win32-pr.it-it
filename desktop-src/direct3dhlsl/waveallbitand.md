---
title: Funzione WaveActiveBitAnd
description: Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- Funzione WaveActiveBitAnd HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96d09d91df4ff9226a8fb86203be0bd79bc3c11d1882553607358c3c84d3814c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282999"
---
# <a name="waveactivebitand-function"></a>Funzione WaveActiveBitAnd

Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi


``` syntax
<int_type> WaveActiveBitAnd(
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

Valore AND bit per bit.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




