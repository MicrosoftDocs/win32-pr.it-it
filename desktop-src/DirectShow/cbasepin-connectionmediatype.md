---
description: 'Il metodo ConnectionMediaType Recupera il tipo di supporto per la connessione pin corrente, se presente. Questo metodo implementa il metodo IPin:: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Metodo CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324690"
---
# <a name="cbasepinconnectionmediatype-method"></a>CBasePin. ConnectionMediaType, metodo

Il metodo **ConnectionMediaType** Recupera il tipo di supporto per la connessione pin corrente, se presente. Questo metodo implementa il metodo [**Ipin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che riceve il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>             | Argomento puntatore **null** .<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il PIN non è connesso.<br/>      |



 

## <a name="remarks"></a>Commenti

Se il PIN è connesso, questo metodo copia il tipo di supporto nella struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) specificata da *PMT*. Il chiamante deve liberare il blocco di formato del tipo di supporto. È possibile usare la funzione [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) o la funzione di supporto [**FreeMediaType**](freemediatype.md) .

Se il PIN non è connesso, questo metodo Azzera il blocco di memoria specificato da *PMT* e restituisce un codice di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

