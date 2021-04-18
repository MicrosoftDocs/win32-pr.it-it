---
description: Il metodo RemovePin rimuove dal filtro un PIN specificato. Il metodo non elimina il PIN.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Metodo CSource. RemovePin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332208"
---
# <a name="csourceremovepin-method"></a>CSource. RemovePin, metodo

Il `RemovePin` metodo rimuove un PIN specificato dal filtro. Il metodo non elimina il PIN.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStream* 
</dt> <dd>

Puntatore all'oggetto [**CSourceStream**](csourcestream.md) che implementa il PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Il filtro non contiene questo pin.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo del distruttore chiama questo metodo per rimuovere il pin di output dal filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




