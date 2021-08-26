---
title: 'Funzione WavePrefixProduct '
description: Restituisce il prodotto di tutti i valori nelle corsie attive in questa ondata con indici inferiori a questa corsia.
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
ms.openlocfilehash: d8cb780f951433afc480c38d52c8120e086a91d32117fe9bb566657e0fcf9f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948961"
---
# <a name="waveprefixproduct-function"></a>Funzione WavePrefixProduct 

Restituisce il prodotto di tutti i valori nelle corsie attive in questa ondata con indici inferiori a questa corsia.

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

L'ordine delle operazioni su questa routine non può essere garantito. Pertanto, in effetti, il \[ \] flag preciso viene ignorato al suo interno.

Un prodotto suffisso può essere calcolato moltiplicando il prodotto prefisso per il valore della corsia corrente.

Si noti che la corsia attiva con l'indice più basso riceverà sempre un valore 1 per il prodotto prefisso.

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 

## <a name="examples"></a>Esempio

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

In un computer con una dimensione dell'onda di 8 e tutte le corsie attive tranne le corsie 0 e 4, i valori seguenti verrebbero restituiti da WavePrefixProduct.

| lane index | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inactive | n/d           |
| 1          | active   | = 1           |
| 2          | active   | = 1 \* 2        |
| 3          | active   | = 1 \* 2 \* 2     |
| 4          | inactive | n/d           |
| 5          | active   | = 1 \* 2 \* 2 \* 2       |
| 6          | active   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | active   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 2 |

## <a name="see-also"></a>Vedi anche

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modello shader 6](shader-model-6-0.md)
