---
title: 'Funzione WavePrefixProduct '
description: Restituisce il prodotto di tutti i valori nelle corsie attive in questa Wave con indici inferiori a questa corsia.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Funzione WavePrefixProduct HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399934"
---
# <a name="waveprefixproduct-function"></a>Funzione WavePrefixProduct 

Restituisce il prodotto di tutti i valori nelle corsie attive in questa Wave con indici inferiori a questa corsia.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Parametri

*value* 

Valore da moltiplicare.

## <a name="return-value"></a>Valore restituito

Prodotto di tutti i valori.

## <a name="remarks"></a>Commenti

Non è possibile garantire l'ordine delle operazioni su questa routine. Quindi, il \[ \] flag esatto viene ignorato al suo interno.

Un prodotto suffisso può essere calcolato moltiplicando il prodotto di prefisso per il valore della corsia corrente.

Si noti che la corsia attiva con l'indice più basso riceve sempre 1 per il prodotto prefisso.

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 

## <a name="examples"></a>Esempio

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

In un computer con una dimensione di onda pari a 8 e tutte le corsie attive eccetto le corsie 0 e 4, i valori seguenti verrebbero restituiti da WavePrefixProduct.

| Indice della corsia | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inactive | n/d           |
| 1          | active   | = 1           |
| 2          | active   | = 1 \* 2        |
| 3          | active   | = 1 \* 2 \* 2     |
| 4          | inactive | n/d           |
| 5          | active   | = 1 \* 2 \* 2 2 \*       |
| 6          | active   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | active   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Vedi anche

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modello shader 6](shader-model-6-0.md)
