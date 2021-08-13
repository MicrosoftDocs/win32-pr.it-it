---
description: Il metodo GetSyncSource recupera il clock di riferimento utilizzato dall'oggetto. Questo metodo implementa il metodo IMediaFilter::GetSyncSource.
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Metodo CBaseMediaFilter.GetSyncSource (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03bceee63109dedbf3b2fa9a855ddbfb410014d48de613f95c7bbfb98d6b0894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658874"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Metodo CBaseMediaFilter.GetSyncSource

Il `GetSyncSource` metodo recupera il clock di riferimento utilizzato dall'oggetto . Questo metodo implementa il [**metodo IMediaFilter::GetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClock* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) dell'orologio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o \_ PUNTATORE E.

## <a name="remarks"></a>Commenti

Se l'oggetto non usa un clock di riferimento, *\* pClock* viene impostato su **NULL.** Quando il metodo termina, se *\* pClock* è diverso da **NULL,** **l'interfaccia IReferenceClock** ha un conteggio dei riferimenti in sospeso. Al termine, assicurarsi di rilasciarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




