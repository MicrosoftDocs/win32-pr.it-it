---
description: Imposta la parte FOURCC dell'oggetto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: Metodo FOURCCMap::SetFOURCC (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ac14c7174fde7184bfdbfbb5d82d3fc1288d46ff37158bbbab146c34db5ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536831"
---
# <a name="fourccmapsetfourcc-method"></a>Metodo FOURCCMap::SetFOURCC

Imposta la **parte FOURCC** dell'oggetto [**FOURCCMap.**](fourccmap.md)

## <a name="syntax"></a>Sintassi


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguid* 
</dt> <dd>

Puntatore alla parte dell'identificatore univoco globale **(GUID)** restituita **dell'oggetto FOURCCMap.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Fourcc.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




