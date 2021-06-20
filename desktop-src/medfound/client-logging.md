---
description: Informazioni sulla registrazione client per Microsoft Media Foundation. La registrazione consente al server multimediale di tenere traccia dell'attività dei client che si connettono a esso.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registrazione client (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409934"
---
# <a name="client-logging-microsoft-media-foundation"></a>Registrazione client (Microsoft Media Foundation)

L'origine di rete supporta la registrazione client, che consente al server multimediale di tenere traccia dell'attività dei client che si connettono a esso. I log client consentono a un server di registrare le statistiche di connessione, rendering e streaming. Questi log possono essere usati dai provider di contenuti in diversi scenari, ad esempio per tracciare l'utilizzo del server multimediale e generare la fatturazione o per distribuire contenuti di qualità appropriata a seconda della velocità della rete del client.

Un file di log contiene diverse voci di eventi client. Ogni voce di log contiene un numero di campi delimitati da spazi. Esistono due tipi di log client: *rendering* (riproduzione) *e streaming* (ricezione). Poiché il contenuto può essere riprodotto e trasmesso contemporaneamente, il client può inviare una combinazione di entrambi i tipi di dati di log. In alcuni casi, possono esistere due voci di log per la stessa sessione. Ad esempio, quando La cache veloce è abilitata, il client può terminare la ricezione del contenuto trasmesso prima di completare il rendering. In tal caso, i dati del log di streaming vengono inviati prima dei dati del log di rendering.

Il client invia i dati del log di rendering al server quando il client cambia da qualsiasi stato di riproduzione (riproduzione, avanzamento rapido o riavvolgimento) a uno stato di non riproduzione (arresto, sospensione, fine del flusso e inizio del flusso). Quando vengono inviati dati per un log di rendering, viene stabilita una connessione direttamente al server multimediale o a un server proxy configurato.

Se il contenuto viene archiviato in un file di cache locale temporaneo nel computer che esegue il client, il client può leggere un file dalla cache locale e inviare i dati del log di rendering per indicare che ha riprodotto il contenuto. In questo caso, il client legge un file dalla cache locale, la voce del log di rendering non contiene statistiche di rete e il protocollo è impostato su Cache.

Il client invia i dati del log di streaming al server per indicare come il client ha ricevuto il contenuto, ma non come è stato eseguito il rendering. Il client può inviare il log di streaming molto prima che il client finisca di eseguire il rendering del contenuto.

In questo argomento non vengono fornite informazioni su tutti i campi del log. Per informazioni di riferimento complete, vedere [Struttura dei dati dei log di Windows Media.](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84)

## <a name="configuring-log-fields"></a>Configurazione dei campi di log

Media Foundation consente al client di configurare l'origine di rete usando le proprietà . L'applicazione deve impostare le proprietà appropriate in un archivio delle proprietà e passarlo a uno dei metodi del sistema di risoluzione di origine. Il sistema di risoluzione di origine crea l'origine di rete come richiesto e apre una connessione con il server. Se la connessione ha esito positivo, il client invia informazioni su se stesso.

Nella tabella seguente vengono descritti i campi del log e le proprietà corrispondenti che un'applicazione può impostare tramite il sistema di risoluzione dell'origine. Queste informazioni non cambiano durante la sessione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo Registrazione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>Identificazione univoca del giocatore. Queste informazioni vengono inviate all'inizio della connessione. In genere, si tratta di un GUID del client. Il client può inviare queste informazioni al server nella <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> proprietà .<br/> Il client invia queste informazioni al server all'inizio della connessione.<br/> Valore di esempio: &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-playerversion</td>
<td>Numero di versione del lettore inviato all'inizio della connessione. Il client può inviare queste informazioni al server nella <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> proprietà .<br/> Il client invia queste informazioni al server all'inizio della connessione.<br/></td>
</tr>
<tr class="odd">
<td>cs(User-Agent)</td>
<td>Tipo di browser usato se il lettore è stato incorporato in un browser. Questo valore può essere impostato dal client nella <a href="mfnetsource-browseruseragent-property.md"><strong>proprietà</strong></a> MFNETSOURCE_BROWSERUSERAGENT.<br/> Se il lettore non è stato incorporato, questo campo fa riferimento all'agente utente del client che ha generato il log. In questo caso, il client deve impostare la <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> proprietà .<br/> Il client invia queste informazioni al server all'inizio della connessione.<br/> Valore di esempio: &quot; Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;<br/></td>
</tr>
<tr class="even">
<td>cs(Referer)</td>
<td>URL della pagina Web in cui è stato incorporato il lettore (se è stato incorporato). Il client può inviare queste informazioni al server nella <a href="mfnetsource-browserwebpage-property.md"><strong>proprietà MFNETSOURCE_BROWSERWEBPAGE.</strong></a><br/> Il client invia queste informazioni al server al termine della connessione.<br/> Valore di esempio: &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>Per le voci di log del lettore, il programma host (.exe) che è stato eseguito. Ad esempio, una pagina Web in un browser, un'applet di Microsoft Visual Basic o un lettore autonomo. Il client può inviare queste informazioni al server nella <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> proprietà .<br/> Il client invia queste informazioni al server al termine della connessione.<br/> Valori di esempio:<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>Numero di versione del programma host (.exe). Il client può inviare queste informazioni al server nella <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> proprietà .<br/> Il client invia queste informazioni al server al termine della connessione.<br/></td>
</tr>
</tbody>
</table>



 

Nell'esempio di codice seguente viene illustrato come un'applicazione client configura l'origine di rete. In questo esempio viene impostato il campo di log "c-hostexe".


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a>Recupero delle statistiche di rete

Quando l'applicazione chiama uno dei metodi del resolver di origine, crea l'origine di rete, imposta le proprietà specificate nell'archivio delle proprietà e apre una sessione con il server multimediale. Oltre alle informazioni configurabili descritte nella sezione precedente, i dati aggiuntivi vengono trasferiti tra il server e il client all'inizio della sessione, durante lo streaming e quando la sessione viene chiusa.

L'applicazione può recuperare le statistiche di rete usando l'identificatore del servizio **MFNETSOURCE \_ STATISTICS \_ SERVICE.** Per usare questo servizio, l'applicazione può chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà che contiene statistiche di rete nella [**proprietà MFNETSOURCE \_ STATISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) È possibile recuperare valori specifici fornendo l'identificatore corrispondente definito **nell'enumerazione MFNETSOURCE \_ STATISTICS \_ IDS.**

Nell'esempio di codice seguente viene illustrato come usare il servizio per ottenere il numero di pacchetti ricevuti dal client.


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



L'elenco seguente descrive alcuni degli identificatori delle statistiche di rete definiti in [**MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).



| Identificatore delle statistiche di rete              | Descrizione                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFNETSOURCE \_ AVGBANDWIDTHBPS \_ ID**       | Larghezza di banda media (in bit al secondo) alla quale il client era connesso al server. Il valore viene calcolato per l'intera durata della connessione.                                                              |
| **MFNETSOURCE \_ BUFFERINGCOUNT \_ ID**        | Numero di volte in cui il client ha memorizzato nel buffer durante la riproduzione del flusso.                                                                                                                                                              |
| **MFNETSOURCE \_ BYTESRECEIVED \_ ID**         | Numero di byte ricevuti dal client dal server. Il valore non include alcun sovraccarico aggiunto dallo stack di rete. Lo stesso contenuto trasmesso tramite protocolli diversi può comportare valori diversi. |
| **MFNETSOURCE \_ LINKBANDWIDTH \_ ID**         | Larghezza di banda massima disponibile del client in bit al secondo.                                                                                                                                                              |
| **MFNETSOURCE \_ LOSTPACKETS \_ ID**           | Numero di pacchetti inviati dal server ma persi durante la trasmissione e mai riprodotti dal client. Il valore non include pacchetti TCP o UDP.                                                                          |
| **MFNETSOURCE \_ RECVPACKETS \_ ID**           | Numero di pacchetti ricevuti dal server Il valore non include pacchetti TCP o UDP.                                                                                                                                  |
| **MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ ID** | Pacchetti persi nella rete che sono stati ripristinati e ripristinati a livello client. Questo valore non include pacchetti TCP o UDP.                                                                                          |
| **MFNETSOURCE \_ RESENDSREQUESTED \_ ID**      | Numero di richieste effettuate dal client per ricevere nuovi pacchetti. Questo valore non include pacchetti TCP o UDP.                                                                                                          |
| **MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**      | Numero di pacchetti ripristinati perché sono stati reinviati tramite UDP. Questo valore non include pacchetti TCP o UDP. Questo campo contiene uno zero a meno che il client non utilizzi il reinvio UDP.                                        |
| **MFNETSOURCE \_ BUFFERPROGRESS \_ ID**        | Percentuale del buffer di playout riempito durante la memorizzazione nel buffer.                                                                                                                                                              |
| **ID PROTOCOLLO MFNETSOURCE \_ \_**              | Protocollo utilizzato per accedere al flusso. Questo comportamento può differire dal protocollo richiesto dal client.                                                                                                                             |
| **ID TRASPORTO MFNETSOURCE \_ \_**             | Protocollo di trasporto usato per recapitare il flusso. Deve essere UDP o TCP.                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità dell'origine di rete](network-source-features.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

