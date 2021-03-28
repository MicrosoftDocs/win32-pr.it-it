---
title: WaveActiveBitAnd (funzione)
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
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047601"
---
# <a name="waveactivebitand-function"></a>WaveActiveBitAnd (funzione)

Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi


``` syntax
<int_type> WaveActiveBitAnd(
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

Il valore AND bit per bit.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




