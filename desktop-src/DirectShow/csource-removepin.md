---
description: Il metodo RemovePin rimuove un segnaposto specificato dal filtro. Il metodo non elimina il segnaposto.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Metodo CSource.RemovePin (Source.h)
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
ms.openlocfilehash: 376c2b292b0bdba9a79593c8264ecce17b916a88cfd49407638d637d1fbda6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767841"
---
# <a name="csourceremovepin-method"></a>Metodo CSource.RemovePin

Il `RemovePin` metodo rimuove un segnaposto specificato dal filtro. Il metodo non elimina il segnaposto.

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

Puntatore [**all'oggetto CSourceStream**](csourcestream.md) che implementa il pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il filtro non contiene questo segnaposto.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo del distruttore chiama questo metodo per rimuovere il segnaposto di output dal filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




