---
description: 'Il metodo Receive riceve il campione multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin:: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Metodo CBaseInputPin. Receive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324858"
---
# <a name="cbaseinputpinreceive-method"></a>Metodo CBaseInputPin. Receive

Il `Receive` metodo riceve il campione multimediale successivo nel flusso. Questo metodo implementa il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | Il PIN sta attualmente scaricando; esempio rifiutato.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Argomento puntatore **null** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                             |
| <dl> <dt>**errore di runtime di VFW \_ E \_ \_**</dt> </dl>   | Si è verificato un errore in fase di esecuzione.<br/>                      |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl>     | Il PIN è stato arrestato.<br/>                             |



 

## <a name="remarks"></a>Commenti

Il pin di output upstream chiama questo metodo per recapitare un campione al pin di input. Il pin di input deve eseguire una delle operazioni seguenti:

-   Elaborare l'esempio prima di restituire.
-   Restituisce ed elabora l'esempio in un thread di lavoro.
-   Rifiutare l'esempio.

Se il pin usa un thread di lavoro per elaborare l'esempio, aggiungere un conteggio dei riferimenti all'esempio all'interno di questo metodo. Quando il metodo restituisce il risultato, il pin upstream rilascia l'esempio. Quando il conteggio dei riferimenti dell'esempio raggiunge zero, l'esempio torna all'allocatore per riutilizzarlo.

Questo metodo è sincrono e può bloccare. Se il metodo potrebbe bloccarsi, il metodo [**CBaseInputPin:: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del PIN deve restituire s \_ OK.

Nella classe di base, questo metodo esegue i passaggi seguenti:

1.  Chiama il metodo [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) per verificare che il pin possa elaborare gli esempi. Se non è possibile, ad esempio, se il PIN viene arrestato, il metodo ha esito negativo.
2.  Recupera le proprietà di esempio e controlla se il formato è stato modificato (vedere di seguito).
3.  Se il formato è stato modificato, il metodo chiama il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il nuovo formato è accettabile.
4.  Se il nuovo formato non è accettabile, il metodo chiama il metodo [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) , pubblica un \_ evento EC ERRORABORT e restituisce un codice di errore.
5.  Supponendo che non si siano verificati errori, il metodo restituisce S \_ OK.

Verificare la presenza di un formato modificato come segue:

-   Se l'esempio supporta l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , verificare il membro **dwSampleFlags** della struttura delle [**\_ \_ Proprietà am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) . Se \_ \_ è presente il flag TYPECHANGED Sample, il formato è stato modificato.
-   In caso contrario, se l'esempio non supporta **IMediaSample2**, chiamare il metodo [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) . Se il metodo restituisce un valore non **null** , il formato è stato modificato.

Nella classe di base, questo metodo non elabora l'esempio. La classe derivata deve eseguire l'override di questo metodo per eseguire l'elaborazione. Ciò che si comporta dipende interamente dal filtro. La classe derivata deve chiamare il metodo della classe di base per verificare gli errori descritti in precedenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




