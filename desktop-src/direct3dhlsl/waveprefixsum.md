---
title: 'Funzione WavePrefixSum '
description: Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questa.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Funzione WavePrefixSum HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbb9ced3fbf7e150cbe3b9bca7eb176e61cf6c8881def22a977ae37a2dbf4b1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671091"
---
# <a name="waveprefixsum-function"></a>Funzione WavePrefixSum 

Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questa.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parametri

*value* 

Valore da sommare.

## <a name="return-value"></a>Valore restituito

Somma dei valori.

## <a name="remarks"></a>Commenti

L'ordine delle operazioni su questa routine non può essere garantito. Pertanto, in effetti, il \[ \] flag preciso viene ignorato al suo interno.

È possibile calcolare una somma suffissa aggiungendo la somma del prefisso al valore della corsia corrente.

Si noti che la corsia attiva con l'indice più basso riceverà sempre 0 per la somma del prefisso.

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 

## <a name="examples"></a>Esempio

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

In un computer con una dimensione dell'onda di 8 e tutte le corsie attive tranne le corsie 0 e 4, i valori seguenti verrebbero restituiti da WavePrefixSum.

| lane index | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inactive | n/d           |
| 1          | active   | = 0           |
| 2          | active   | = 0+2         |
| 3          | active   | = 0+2+2       |
| 4          | inactive | n/d           |
| 5          | active   | = 0+2+2+2+2     |
| 6          | active   | = 0+2+2+2+2+2   |
| 7          | active   | = 0+2+2+2+2+2+2 |

## <a name="see-also"></a>Vedi anche

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modello shader 6](shader-model-6-0.md)
