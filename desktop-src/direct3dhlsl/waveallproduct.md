---
title: WaveActiveProduct (funzione)
description: Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- Funzione WaveActiveProduct HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873113"
---
# <a name="waveactiveproduct-function"></a>WaveActiveProduct (funzione)

Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*expr* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore del prodotto.

## <a name="remarks"></a>Commenti

L'ordine delle operazioni non è definito.

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




