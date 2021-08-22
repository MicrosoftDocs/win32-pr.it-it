---
description: "Metodo CBaseFilter.FindPin: il metodo FindPin recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter::FindPin."
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Metodo CBaseFilter.FindPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3818ef4356f11a2d003abe4e9442c4de06108aa32e50f480a3d097ea5db0c343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017189"
---
# <a name="cbasefilterfindpin-method"></a>Metodo CBaseFilter.FindPin

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

Puntatore a una stringa Unicode costante con terminazione Null che identifica il pin.

</dd> <dt>

*ppPin* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                       | Descrizione                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>         | Argomento del puntatore **NULL.**<br/>     |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Impossibile trovare un pin corrispondente.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo CBasePin::Name**](cbasepin-name.md) per confrontare il nome di ogni pin con la stringa specificata dal *parametro Id.*

Se il metodo ha esito positivo, **l'interfaccia IPin** ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciarlo al termine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




