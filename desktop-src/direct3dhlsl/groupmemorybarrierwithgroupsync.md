---
title: Funzione GroupMemoryBarrierWithGroupSync
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi al gruppo non sono stati completati e tutti i thread del gruppo non hanno raggiunto questa chiamata.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- Funzione GroupMemoryBarrierWithGroupSync HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbcfdea451c0cb7ad2b84297c422fa6865b1f45d757612a7b5d220a8829a99b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854451"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>Funzione GroupMemoryBarrierWithGroupSync

Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi al gruppo non sono stati completati e tutti i thread del gruppo non hanno raggiunto questa chiamata.

## <a name="syntax"></a>Sintassi

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli di shader superiori | sì       |



 

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

 

 




