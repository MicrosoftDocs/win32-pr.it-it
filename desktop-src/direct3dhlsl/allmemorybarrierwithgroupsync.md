---
title: Funzione AllMemoryBarrierWithGroupSync
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria non sono stati completati e tutti i thread nel gruppo non hanno raggiunto questa chiamata.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- Funzione AllMemoryBarrierWithGroupSync HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d3c146ff04597b7eca13dd5cbef93dc1c79f81709353bf5b4fa1a993a8da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626691"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>Funzione AllMemoryBarrierWithGroupSync

Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria non sono stati completati e tutti i thread nel gruppo non hanno raggiunto questa chiamata.

## <a name="syntax"></a>Sintassi

``` syntax
void AllMemoryBarrierWithGroupSync(void);
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

 

 




