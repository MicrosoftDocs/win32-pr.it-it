---
title: Funzione DeviceMemoryBarrierWithGroupSync
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati e tutti i thread nel gruppo non hanno raggiunto questa chiamata.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- Funzione DeviceMemoryBarrierWithGroupSync HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2567a209b86481cd0f25922e8e3b1cf947196a2c799344089591cf70fa3624fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625821"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>Funzione DeviceMemoryBarrierWithGroupSync

Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi alla memoria del dispositivo non sono stati completati e tutti i thread nel gruppo non hanno raggiunto questa chiamata.

## <a name="syntax"></a>Sintassi

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
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
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì       |



 

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

 

 




