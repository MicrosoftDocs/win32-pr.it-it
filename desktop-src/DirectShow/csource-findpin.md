---
description: "Il metodo FindPin Recupera il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter:: FindPin."
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Metodo CSource. FindPin (source. h)
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
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324651"
---
# <a name="csourcefindpin-method"></a>CSource. FindPin, metodo

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

Puntatore a una stringa con terminazione null che identifica il PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN. Se il metodo ha esito negativo, \* *ppPin* è impostato su **null**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>         | Argomento puntatore **null** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Non è stato possibile trovare un pin con questo identificatore.<br/> |



 

## <a name="remarks"></a>Commenti

Il primo pin è sempre denominato "1"; il secondo pin è denominato "2"; e così via. Per ulteriori informazioni, vedere [**CSourceStream:: QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




