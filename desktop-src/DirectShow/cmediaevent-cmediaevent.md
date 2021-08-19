---
description: 'Costruttore CMediaEvent.CMediaEvent : metodo costruttore.'
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Costruttore CMediaEvent.CMediaEvent (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1809bcca029838e7e1df6d71c5d005aec3d21bdbcde9ccbd1b7a23b77dd9ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402024"
---
# <a name="cmediaeventcmediaevent-constructor"></a>Costruttore CMediaEvent.CMediaEvent

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'oggetto a scopo di debug.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Allocare *il parametro pName* nella memoria statica. Questo nome viene visualizzato nel terminale di debug al momento della creazione e dell'eliminazione dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




