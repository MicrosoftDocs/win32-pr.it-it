---
description: Il metodo CancelNotification Annulla l'evento timer che pianifica il rendering.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Metodo CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329403"
---
# <a name="cbaserenderercancelnotification-method"></a>CBaseRenderer. CancelNotification, metodo

Il `CancelNotification` metodo annulla l'evento timer che pianifica il rendering.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Nessun evento timer in sospeso.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                          |



 

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo quando il flusso viene arrestato. Il metodo annulla qualsiasi rendering pianificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




