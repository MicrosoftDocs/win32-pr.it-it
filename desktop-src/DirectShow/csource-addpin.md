---
description: Il metodo AddPin aggiunge un nuovo PIN di output al filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Metodo CSource. AddPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324658"
---
# <a name="csourceaddpin-method"></a>CSource. AddPin, metodo

Il `AddPin` metodo aggiunge un nuovo PIN di output al filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddPin(
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



| Codice restituito                                                                                   | Descrizione                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>             |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente<br/> |



 

## <a name="remarks"></a>Commenti

Quando si crea un nuovo PIN derivato da **CSourceStream**, il costruttore **CSourceStream** chiama automaticamente questo metodo per aggiungere il pin di output al filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




