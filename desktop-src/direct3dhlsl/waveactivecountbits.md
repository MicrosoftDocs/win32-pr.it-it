---
title: Funzione WaveActiveCountBits
description: Conta il numero di variabili booleane che restituiscono true in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.
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
ms.openlocfilehash: a53a2953ba7d77f1969a7d5dabef3c17437e8bbb
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767605"
---
# <a name="waveactivecountbits-function"></a>Funzione WaveActiveCountBits

Conta il numero di variabili booleane che restituiscono true in tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.

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

Numero di corsie per cui la variabile booleana restituisce true, in tutte le corsie attive nell'onda corrente.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6.0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempio

Questa operazione può essere implementata in modo più efficiente rispetto a un WaveActiveSum completo, come descritto nell'esempio seguente:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




