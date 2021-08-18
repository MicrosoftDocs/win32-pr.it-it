---
description: Il metodo ChangeOutputFormat modifica dinamicamente il tipo di supporto per la connessione e recapita nuove informazioni sul segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Metodo CDynamicOutputPin.ChangeOutputFormat (Amfilter.h)
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
ms.openlocfilehash: 534d588bc1633770c35b0e0edbc2079ed8f7ab5035d3a8d2ff181042d26fdb3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074275"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>Metodo CDynamicOutputPin.ChangeOutputFormat

Il `ChangeOutputFormat` metodo modifica dinamicamente il tipo di supporto per la connessione e fornisce informazioni sul nuovo segmento. La modifica può verificarsi durante l'esecuzione del grafico dei filtri. Una volta chiamato questo metodo, gli esempi con il tipo di supporto precedente non possono essere recapitati. Il chiamante deve assicurarsi che non siano in sospeso esempi vecchi.

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

*Pmt* 
</dt> <dd>

Puntatore a [**una struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che specifica il tipo di supporto.

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

Frequenza dei segmenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                                                                                                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Esito negativo. È possibile che il filtro proprietario non abbia chiamato [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin non è connesso.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questo metodo modifica il tipo di formato durante l'esecuzione del filtro. Se il pin downstream accetta il nuovo formato, non è necessaria alcuna riconnessione. In caso contrario, il metodo tenta di riconnettere il pin. Se il metodo modifica correttamente il formato, recapita le informazioni sul nuovo segmento. Questo metodo chiama il [**metodo CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) per eseguire la modifica del formato.

È necessario chiamare il [**metodo CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) prima di chiamare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




