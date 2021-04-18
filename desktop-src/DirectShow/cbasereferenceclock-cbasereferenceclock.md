---
description: Metodo del costruttore.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Costruttore CBaseReferenceClock. CBaseReferenceClock (Refclock. h)
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
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330304"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>Costruttore CBaseReferenceClock. CBaseReferenceClock

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

*pName* 
</dt> <dd>

Puntatore a una stringa che contiene il nome dell'oggetto. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Se si verifica un errore, il metodo restituisce un codice di errore in questo parametro. Non impostare questo parametro su **null**.

</dd> <dt>

*pSched* 
</dt> <dd>

Puntatore a un oggetto [**CAMSchedule**](camschedule.md) . Se **null**, questo metodo crea un nuovo oggetto **CAMSchedule** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Refclock. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




