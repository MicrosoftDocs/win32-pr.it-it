---
title: 'Funzione WavePrefixSum '
description: Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questo.
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
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/31/2021
ms.locfileid: "104980983"
---
# <a name="waveprefixsum-function"></a>Funzione WavePrefixSum 

Restituisce la somma di tutti i valori nelle corsie attive con indici più piccoli rispetto a questo.

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

Non è possibile garantire l'ordine delle operazioni su questa routine. Quindi, il \[ \] flag esatto viene ignorato al suo interno.

Una somma suffissa può essere calcolata aggiungendo il prefisso Sum al valore della corsia corrente.

Si noti che la corsia attiva con l'indice più basso riceve sempre un valore 0 per la somma del prefisso.

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 

## <a name="examples"></a>Esempio

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

In un computer con una dimensione di onda pari a 8 e tutte le corsie attive eccetto le corsie 0 e 4, i valori seguenti verrebbero restituiti da WavePrefixSum.

| Indice della corsia | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inactive | n/d           |
| 1          | active   | = 0           |
| 2          | active   | = 0 + 2         |
| 3          | active   | = 0 + 2 + 2       |
| 4          | inactive | n/d           |
| 5          | active   | = 0 + 2 + 2 + 2     |
| 6          | active   | = 0 + 2 + 2 + 2 + 2   |
| 7          | active   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>Vedi anche

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modello shader 6](shader-model-6-0.md)
