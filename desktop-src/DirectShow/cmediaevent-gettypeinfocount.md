---
description: 'Metodo CMediaEvent.GetTypeInfoCount: recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.'
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Metodo CMediaEvent.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6476e7949c9cad8e9ba13a562bf93fe7e3ffff39fe34cbe1101193bf9bc18289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156999"
---
# <a name="cmediaeventgettypeinfocount-method"></a>Metodo CMediaEvent.GetTypeInfoCount

Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pctinfo* 
</dt> <dd>

Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto . Se l'oggetto fornisce informazioni sul tipo, questo numero è 1; in caso contrario, il numero è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ POINTER se *pctinfo non* è valido. In caso contrario, restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




