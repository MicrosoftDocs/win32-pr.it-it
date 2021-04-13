---
title: WaveActiveCountBits (funzione)
description: Conta il numero di variabili booleane che restituiscono true tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.
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
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2020
ms.locfileid: "104339779"
---
# <a name="waveactivecountbits-function"></a>WaveActiveCountBits (funzione)

Conta il numero di variabili booleane che restituiscono true tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.

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

Il numero di che restituisce true in tutte le corsie attive nell'onda corrente.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempio

Questa operazione può essere implementata in modo più efficiente rispetto a una WaveActiveSum completa, come descritto nell'esempio seguente:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




