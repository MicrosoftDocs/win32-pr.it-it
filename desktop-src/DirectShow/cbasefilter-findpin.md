---
description: "Il metodo FindPin Recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter:: FindPin."
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Metodo CBaseFilter. FindPin (Amfilter. h)
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
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330413"
---
# <a name="cbasefilterfindpin-method"></a>CBaseFilter. FindPin, metodo

Il `FindPin` metodo recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

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

Puntatore a una stringa Unicode costante a terminazione null che identifica il PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                       | Descrizione                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                       |
| <dl> <dt>**\_puntatore E**</dt> </dl>         | Argomento puntatore **null** .<br/>     |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Impossibile trovare un pin corrispondente.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBasePin:: Name**](cbasepin-name.md) per confrontare il nome di ogni pin con la stringa specificata dal parametro *ID* .

Se il metodo ha esito positivo, l'interfaccia **Ipin** ha un conteggio dei riferimenti in attesa. Assicurarsi di rilasciarlo al termine dell'operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




