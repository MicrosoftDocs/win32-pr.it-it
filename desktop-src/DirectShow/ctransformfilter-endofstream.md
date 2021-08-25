---
description: Il metodo EndOfStream notifica al filtro che non sono previsti dati aggiuntivi dal pin di input.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Metodo CTransformFilter.EndOfStream (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade419666b1df36e851d5d945e14d9035c1377145cecd472244c9178758f45f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907631"
---
# <a name="ctransformfilterendofstream-method"></a>Metodo CTransformFilter.EndOfStream

Il `EndOfStream` metodo notifica al filtro che non sono previsti dati aggiuntivi dal pin di input.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Il metodo [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) del pin di input chiama questo metodo. Questo metodo recapita la notifica di fine flusso a valle. Se la classe derivata usa un thread di lavoro per distribuire campioni multimediali, deve eseguire l'override di questo metodo e accodare la notifica di fine flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




