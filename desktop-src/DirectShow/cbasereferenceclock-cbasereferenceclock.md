---
description: Costruttore CBaseReferenceClock.CBaseReferenceClock - Metodo costruttore.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Costruttore CBaseReferenceClock.CBaseReferenceClock (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ea08e5555aa6286dac80642f19969e6e669a4ec6ccddb4e530d13e0253b4bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954990"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>Costruttore CBaseReferenceClock.CBaseReferenceClock

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa contenente il nome dell'oggetto. Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Se si verifica un errore, il metodo restituisce un codice di errore in questo parametro. Non impostare questo parametro su **NULL.**

</dd> <dt>

*pSched* 
</dt> <dd>

Puntatore a un [**oggetto CAMSchedule.**](camschedule.md) Se **NULL,** questo metodo crea un nuovo **oggetto CAMSchedule.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




