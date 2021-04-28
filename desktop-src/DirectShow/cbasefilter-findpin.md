---
description: "Metodo CBaseFilter.FindPin: il metodo FindPin recupera il segnaposto con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter::FindPin."
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
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099819"
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

Puntatore a una stringa Unicode con terminazione Null costante che identifica il segnaposto.

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
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>         | Argomento del puntatore **NULL.**<br/>     |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Impossibile trovare un segnaposto corrispondente.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo CBasePin::Name**](cbasepin-name.md) per confrontare il nome di ogni segnaposto con la stringa specificata dal *parametro Id.*

Se il metodo ha esito positivo, **l'interfaccia IPin** ha un conteggio dei riferimenti in sospeso. Al termine, assicurarsi di rilasciarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




