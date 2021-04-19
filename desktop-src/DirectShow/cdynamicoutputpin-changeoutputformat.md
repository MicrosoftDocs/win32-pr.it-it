---
description: Il metodo ChangeOutputFormat modifica dinamicamente il tipo di supporto per la connessione e recapita nuove informazioni sul segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Metodo CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333452"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>CDynamicOutputPin. ChangeOutputFormat, metodo

Il `ChangeOutputFormat` metodo modifica dinamicamente il tipo di supporto per la connessione e recapita nuove informazioni sul segmento. La modifica può verificarsi durante l'esecuzione del grafico dei filtri. Una volta chiamato questo metodo, non è possibile recapitare gli esempi con il vecchio tipo di supporto. Il chiamante deve assicurarsi che non siano presenti esempi obsoleti in sospeso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

Ora di inizio del segmento.

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

Ora di arresto del segmento.

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

Frequenza segmento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                                                                                                                      |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                | Esito negativo. Probabilmente il filtro proprietario non ha chiamato [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il PIN non è connesso.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questo metodo modifica il tipo di formato durante l'esecuzione del filtro. Se il pin downstream accetta il nuovo formato, non è necessaria alcuna riconnessione. In caso contrario, il metodo tenterà di riconnettere il PIN. Se il metodo modifica correttamente il formato, recapita le informazioni sul nuovo segmento. Questo metodo chiama il metodo [**CDynamicOutputPin:: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) per eseguire la modifica del formato.

Prima di chiamare questo metodo, è necessario chiamare il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




