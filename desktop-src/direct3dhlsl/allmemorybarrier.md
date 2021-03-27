---
title: AllMemoryBarrier (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo fino a quando tutti gli accessi alla memoria non sono stati completati.
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
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398011"
---
# <a name="allmemorybarrier-function"></a>AllMemoryBarrier (funzione)

Blocca l'esecuzione di tutti i thread in un gruppo fino a quando tutti gli accessi alla memoria non sono stati completati.

## <a name="syntax"></a>Sintassi

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Una barriera di memoria garantisce il completamento delle operazioni di memoria in attesa. I thread sono sincronizzati alle barriere GroupSync. Questo potrebbe bloccare un thread o thread se sono in corso operazioni di memoria.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




