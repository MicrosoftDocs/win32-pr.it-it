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
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095559"
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

Puntatore al proprietario dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Allocare *il parametro pName* nella memoria statica. Questo nome viene visualizzato nel terminale di debug al momento della creazione e dell'eliminazione dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




