---
title: DeviceMemoryBarrier (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati.
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
ms.openlocfilehash: 1875b780f528000d46ba31bb979072d6d462fa91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397083"
---
# <a name="devicememorybarrier-function"></a>DeviceMemoryBarrier (funzione)

Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati.

## <a name="syntax"></a>Sintassi

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




