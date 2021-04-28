---
description: "Metodo CSource.FindPin: il metodo FindPin recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter::FindPin."
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Metodo CSource.FindPin (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098859"
---
# <a name="csourcefindpin-method"></a>Metodo CSource.FindPin

Il `FindPin` metodo recupera il pin con l'identificatore specificato. Questo metodo implementa il [**metodo IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica il pin.

</dd> <dt>

*ppPin* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin. Se il metodo ha esito negativo, \* *ppPin* è impostato su **NULL**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                                   |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>         | Argomento del puntatore **NULL.**<br/>                 |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Impossibile trovare un pin con questo identificatore.<br/> |



 

## <a name="remarks"></a>Commenti

Il primo segnaposto è sempre denominato "1". il secondo pin è denominato "2"; e così via. Per altre informazioni, vedere [**CSourceStream::QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




