---
title: Funzione AllMemoryBarrier
description: Blocca l'esecuzione di tutti i thread in un gruppo fino al completamento di tutti gli accessi alla memoria.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- Funzione AllMemoryBarrier HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fc5d22c36d67aa0e8df8352ba8fa6f2d579ddabd4825e6508499420a56bd0ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626751"
---
# <a name="allmemorybarrier-function"></a>Funzione AllMemoryBarrier

Blocca l'esecuzione di tutti i thread in un gruppo fino al completamento di tutti gli accessi alla memoria.

## <a name="syntax"></a>Sintassi

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Una barriera di memoria garantisce il completamento delle operazioni di memoria in sospeso. I thread vengono sincronizzati in base alle barriere di GroupSync. Ciò può bloccare uno o più thread se sono in corso operazioni di memoria.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




