---
title: GroupMemoryBarrierWithGroupSync (funzione)
description: Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi del gruppo non sono stati completati e tutti i thread del gruppo hanno raggiunto questa chiamata.
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
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976186"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>GroupMemoryBarrierWithGroupSync (funzione)

Blocca l'esecuzione di tutti i thread in un gruppo finché tutti gli accessi condivisi del gruppo non sono stati completati e tutti i thread del gruppo hanno raggiunto questa chiamata.

## <a name="syntax"></a>Sintassi

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
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
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




