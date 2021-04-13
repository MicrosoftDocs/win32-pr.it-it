---
title: WaveReadLaneAt (funzione)
description: Restituisce il valore dell'espressione per l'indice della corsia specificato all'interno dell'onda specificata.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Funzione WaveReadLaneAt HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2020
ms.locfileid: "104398811"
---
# <a name="wavereadlaneat-function"></a>WaveReadLaneAt (funzione)

Restituisce il valore dell'espressione per l'indice della corsia specificato all'interno dell'onda specificata.

## <a name="syntax"></a>Sintassi

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*expr* 
</dt> <dd>

Espressione da valutare.

</dd> <dt>

*laneIndex* 
</dt> <dd>

Indice della corsia per cui verrà restituito il risultato *expr* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore risultante è il risultato di *expr*. Sarà uniforme se *laneIndex* è uniforme.

## <a name="remarks"></a>Commenti

Questa funzione è effettivamente una trasmissione del valore nella corsia laneIndex'th.

Questa funzione è supportata dal modello shader 6,0, nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




