---
description: 'Costruttore CAMMsgEvent.CAMMsgEvent : metodo del costruttore.'
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Costruttore CAMMsgEvent.CAMMsgEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096536"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Costruttore CAMMsgEvent.CAMMsgEvent

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Phr* 
</dt> <dd>

Puntatore a **un valore HRESULT.** Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In questo caso, l'oggetto non è in uno stato valido.

Per compatibilità con le versioni precedenti di strmbase.lib, il valore predefinito di questo parametro è **NULL.** È tuttavia preferibile passare un valore non **NULL,** in modo che il chiamante possa controllare lo stato dell'oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




