---
title: AllMemoryBarrierWithGroupSync (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria non sono stati completati e tutti i thread del gruppo non hanno raggiunto questa chiamata.
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
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045894"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>AllMemoryBarrierWithGroupSync (funzione)

Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria non sono stati completati e tutti i thread del gruppo non hanno raggiunto questa chiamata.

## <a name="syntax"></a>Sintassi

``` syntax
void AllMemoryBarrierWithGroupSync(void);
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

 

 




