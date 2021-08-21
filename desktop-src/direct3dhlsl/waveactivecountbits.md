---
title: Funzione WaveActiveCountBits
description: Conta il numero di variabili booleane che restituiscono true in tutte le corsie attive nell'ondata corrente e replica il risultato in tutte le corsie dell'onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Funzione WaveActiveCountBits HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e1642cbd5cbdef162511185e9d2c05e849d78486b82e8219623286f33e39223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504936"
---
# <a name="waveactivecountbits-function"></a>Funzione WaveActiveCountBits

Conta il numero di variabili booleane che restituiscono true in tutte le corsie attive nell'ondata corrente e replica il risultato in tutte le corsie dell'onda.

## <a name="syntax"></a>Sintassi


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bBit* 
</dt> <dd>

Variabili booleane da valutare. Se si specifica un valore booleano true esplicito, viene restituito il numero di corsie attive.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Numero di che restituiscono true in tutte le corsie attive nell'ondata corrente.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempio

Questo può essere implementato in modo più efficiente rispetto a un WaveActiveSum completo, come descritto nell'esempio seguente:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




