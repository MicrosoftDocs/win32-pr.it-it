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
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099119"
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

Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto. Se l'oggetto fornisce informazioni sul tipo, questo numero è 1. In caso contrario, il numero è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ POINTER se *pctinfo non è* valido; in caso contrario, restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




