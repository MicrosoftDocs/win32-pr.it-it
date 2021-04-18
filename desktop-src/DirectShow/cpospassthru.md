---
description: La classe CPosPassThru gestisce i comandi Seek per i filtri di trasformazione, passandoli upstream al filtro successivo.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Classe CPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328495"
---
# <a name="cpospassthru-class"></a>Classe CPosPassThru

![gerarchia della classe base cpospassthru](images/cutil14.png)

La `CPosPassThru` classe gestisce i comandi Seek per i filtri di trasformazione, passandogli upstream al filtro successivo.

Quando un'applicazione cerca il grafico dei filtri, il gestore del grafico dei filtri fornisce al comando seek i filtri del renderer. Il comando viene passato a Monte, tramite il pin di output di ogni filtro, fino a quando non raggiunge un filtro in grado di eseguire il comando (se presente). Per informazioni dettagliate, vedere la pagina relativa [alla ricerca](seeking.md). La `CPosPassThru` classe passa tutti i comandi Seek al pin di output sul filtro upstream, come illustrato nella figura seguente.

![la classe cpospassthru invia i comandi Seek upstream.](images/cpospassthru.png)

Sebbene questa classe venga fornita nella libreria di classi base, DirectShow fornisce anche la stessa classe in Quartz.dll. L'uso della versione Quartz.dll può ridurre in qualche modo le dimensioni del codice nel filtro, perché la classe viene caricata in fase di esecuzione dalla DLL. Per utilizzare tale versione, chiamare la funzione [**CreatePosPassThru**](createpospassthru.md) .

Nel metodo **NonDelegatingQueryInterface** del PIN di output, delegare all'oggetto **CPosPassThru** ogni volta che l'interfaccia richiesta è [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), come illustrato nel codice seguente:


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



Eccetto laddove specificato, tutti i metodi [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) in questa classe chiamano il metodo corrispondente sul pin connesso e restituiscono il risultato.



| Metodi pubblici                                                    | Descrizione                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CPosPassThru**](cpospassthru-cpospassthru.md)                 | Metodo del costruttore.                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | Obsoleta.                                                                                           |
| [**GetMediaTime**](cpospassthru-getmediatime.md)                 | Recupera i timestamp sull'esempio corrente. Virtuale.                                           |
| Metodi IMediaPosition                                            | Descrizione                                                                                         |
| [**ottenere la \_ durata**](cpospassthru-get-duration.md)                | Recupera la durata del flusso.                                                               |
| [**Inserisci \_ currentPosition**](cpospassthru-put-currentposition.md)  | Imposta la posizione corrente rispetto alla durata totale del flusso.                            |
| [**ottenere \_ StopTime**](cpospassthru-get-stoptime.md)                | Recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.         |
| [**Inserisci \_ StopTime**](cpospassthru-put-stoptime.md)                | Imposta l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.              |
| [**ottenere \_ PrerollTime**](cpospassthru-get-prerolltime.md)          | Recupera la quantità di dati che verranno accodati prima della posizione iniziale.                         |
| [**Inserisci \_ PrerollTime**](cpospassthru-put-prerolltime.md)          | Imposta la quantità di dati che verranno accodati prima della posizione iniziale.                              |
| [**velocità di ottenimento \_**](cpospassthru-get-rate.md)                        | Recupera la velocità di riproduzione.                                                                        |
| [**percentuale di inserimento \_**](cpospassthru-put-rate.md)                        | Imposta la velocità di riproduzione.                                                                             |
| [**ottenere \_ currentPosition**](cpospassthru-get-currentposition.md)  | Recupera la posizione corrente rispetto alla durata totale del flusso.                       |
| [**CanSeekForward**](cpospassthru-canseekforward.md)             | Determina se è possibile cercare il flusso all'indietro.                                               |
| [**CanSeekBackward**](cpospassthru-canseekbackward.md)           | Determina se il flusso può essere cercato in futuro.                                                |
| Metodi IMediaSeeking                                             | Descrizione                                                                                         |
| [**CheckCapabilities**](cpospassthru-checkcapabilities.md)       | Esegue una query per determinare se un flusso ha specificato funzionalità di ricerca.                                        |
| [**ConvertTimeFormat**](cpospassthru-converttimeformat.md)       | Esegue la conversione da un formato di ora a un altro.                                                           |
| [**GetAvailable**](cpospassthru-getavailable.md)                 | Recupera l'intervallo di tempo in cui la ricerca è efficiente.                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | Recupera tutte le funzionalità di ricerca del flusso.                                               |
| [**GetCurrentPosition**](cpospassthru-getcurrentposition.md)     | Recupera la posizione corrente rispetto alla durata totale del flusso.                       |
| [**GetDuration**](cpospassthru-getduration.md)                   | Recupera la durata del flusso.                                                               |
| [**GetPositions**](cpospassthru-getpositions.md)                 | Recupera la posizione corrente e la posizione di arresto rispetto alla durata totale del flusso. |
| [**GetPreroll**](cpospassthru-getpreroll.md)                     | Recupera la quantità di dati che verranno accodati prima della posizione iniziale.                         |
| [**Getrate**](cpospassthru-getrate.md)                           | Recupera la velocità di riproduzione.                                                                        |
| [**GetStopPosition**](cpospassthru-getstopposition.md)           | Recupera l'ora in cui la riproduzione viene arrestata rispetto alla durata del flusso.         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | Recupera il formato dell'ora corrente.                                                                  |
| [**IsFormatSupported**](cpospassthru-isformatsupported.md)       | Determina se è supportato un formato di ora specificato.                                            |
| [**IsUsingTimeFormat**](cpospassthru-isusingtimeformat.md)       | Determina se un formato di ora specificato è il formato attualmente in uso.                          |
| [**QueryPreferredFormat**](cpospassthru-querypreferredformat.md) | Recupera il formato di ora preferito per il flusso.                                                 |
| [**Posizioni**](cpospassthru-setpositions.md)                 | Imposta la posizione corrente e la posizione di arresto.                                                    |
| [**Frequenza**](cpospassthru-setrate.md)                           | Imposta la velocità di riproduzione.                                                                             |
| [**SetTimeFormat**](cpospassthru-settimeformat.md)               | Imposta il formato dell'ora.                                                                               |
| Funzioni di supporto                                                  | Descrizione                                                                                         |
| [**CreatePosPassThru**](createpospassthru.md)                    | Crea un `CPosPassThru` oggetto o [**CRendererPosPassThru**](crendererpospassthru.md) .            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




