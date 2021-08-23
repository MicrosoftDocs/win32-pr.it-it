---
title: Funzione DeviceMemoryBarrier
description: Blocca l'esecuzione di tutti i thread in un gruppo fino al completamento di tutti gli accessi alla memoria del dispositivo.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- Funzione DeviceMemoryBarrier HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f3629f7eaf8b3e271ca988b73e1dedab1e428136cc86663b64b838597d1b98c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855261"
---
# <a name="devicememorybarrier-function"></a>Funzione DeviceMemoryBarrier

Blocca l'esecuzione di tutti i thread in un gruppo fino al completamento di tutti gli accessi alla memoria del dispositivo.

## <a name="syntax"></a>Sintassi

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




