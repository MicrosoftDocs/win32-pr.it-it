---
description: Il metodo EndOfStream notifica al filtro che non sono previsti dati aggiuntivi dal pin di input.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Metodo CTransformFilter. EndOfStream (Transfrm. h)
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
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326933"
---
# <a name="ctransformfilterendofstream-method"></a>CTransformFilter. EndOfStream, metodo

Il `EndOfStream` metodo notifica al filtro che non sono previsti dati aggiuntivi dal pin di input.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo [**CTransformInputPin:: EndOfStream**](ctransforminputpin-endofstream.md) del PIN di input chiama questo metodo. Questo metodo recapita la notifica di fine flusso a valle. Se la classe derivata utilizza un thread di lavoro per recapitare gli esempi di contenuti multimediali, deve eseguire l'override di questo metodo e accodare la notifica di fine del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




