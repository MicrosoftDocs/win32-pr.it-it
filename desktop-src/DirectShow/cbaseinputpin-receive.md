---
description: "Metodo CBaseInputPin.Receive: il metodo Receive riceve l'esempio multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin::Receive."
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Metodo CBaseInputPin.Receive (Amfilter.h)
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
ms.openlocfilehash: 4fe88913ad374923c11cf058a3dc0aa70580411e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099689"
---
# <a name="cbaseinputpinreceive-method"></a>Metodo CBaseInputPin.Receive

Il `Receive` metodo riceve l'esempio multimediale successivo nel flusso. Questo metodo implementa il [**metodo IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Lo scaricamento del pin è in corso. l'esempio è stato rifiutato.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>               | Argomento del puntatore **NULL.**<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                             |
| <dl> <dt>**ERRORE DI RUNTIME DI VFW \_ E \_ \_**</dt> </dl>   | Si è verificato un errore di run-time.<br/>                      |
| <dl> <dt>**VFW \_ E \_ STATO \_ ERRATO**</dt> </dl>     | Il pin è stato arrestato.<br/>                             |



 

## <a name="remarks"></a>Commenti

Il pin di output upstream chiama questo metodo per recapitare un campione al pin di input. Il pin di input deve eseguire una delle operazioni seguenti:

-   Elaborare l'esempio prima della restituzione.
-   Restituire ed elaborare l'esempio in un thread di lavoro.
-   Rifiutare l'esempio.

Se il pin usa un thread di lavoro per elaborare l'esempio, aggiungere un conteggio dei riferimenti all'esempio all'interno di questo metodo. Dopo la fine del metodo, il pin upstream rilascia l'esempio. Quando il conteggio dei riferimenti del campione raggiunge lo zero, il campione torna all'allocatore per il nuovo utilizzo.

Questo metodo è sincrono e può bloccarsi. Se il metodo potrebbe bloccarsi, il metodo [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del pin deve restituire S \_ OK.

Nella classe di base questo metodo esegue i passaggi seguenti:

1.  Chiama il [**metodo CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) per verificare che il pin sia in grado di elaborare gli esempi ora. Se non è possibile, ad esempio, se il pin viene arrestato, il metodo ha esito negativo.
2.  Recupera le proprietà di esempio e controlla se il formato è stato modificato (vedere di seguito).
3.  Se il formato è stato modificato, il metodo chiama il metodo [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il nuovo formato è accettabile.
4.  Se il nuovo formato non è accettabile, il metodo chiama il metodo [**CBasePin::EndOfStream,**](cbasepin-endofstream.md) pubblica un evento \_ EC ERRORABORT e restituisce un codice di errore.
5.  Supponendo che non siano presenti errori, il metodo restituisce S \_ OK.

Verificare la modifica del formato nel modo seguente:

-   Se l'esempio supporta [**l'interfaccia IMediaSample2,**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) controllare il **membro dwSampleFlags** della [**struttura AM \_ SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) Se è presente il flag AM \_ SAMPLE \_ TYPECHANGED, il formato è stato modificato.
-   In caso contrario, se l'esempio non supporta **IMediaSample2,** chiamare il [**metodo IMediaSample::GetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) Se il metodo restituisce un valore non **NULL,** il formato è stato modificato.

Nella classe di base questo metodo non elabora l'esempio. La classe derivata deve eseguire l'override di questo metodo per eseguire l'elaborazione. Ciò che ciò comporta dipende interamente dal filtro. La classe derivata deve chiamare il metodo della classe base per verificare la presenza degli errori descritti in precedenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




