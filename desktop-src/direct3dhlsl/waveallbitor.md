---
title: Funzione WaveActiveBitOr
description: Restituisce l'operatore OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- Funzione WaveActiveBitOr HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7efe678093fca38940e0a98a31d4c39065bcf172d04aa5eb0932467fc716457b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504891"
---
# <a name="waveactivebitor-function"></a>Funzione WaveActiveBitOr

Restituisce l'operatore OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi

``` syntax
<int_type> WaveActiveBitOr(
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

Valore OR bit per bit.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




