---
description: Ottiene il periodo del set di animazioni.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: Metodo ID3DXAnimationSet::GetPeriod (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522330"
---
# <a name="id3dxanimationsetgetperiod-method"></a>Metodo ID3DXAnimationSet::GetPeriod

Ottiene il periodo del set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Periodo del set di animazioni.

## <a name="remarks"></a>Commenti

Il periodo è l'intervallo di tempo in cui i fotogrammi chiave dell'animazione sono validi. Per le animazioni a ciclo continuo, questo è il periodo del ciclo. Le unità di tempo in cui sono specificati i fotogrammi chiave (ad esempio, i secondi) sono determinate dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
