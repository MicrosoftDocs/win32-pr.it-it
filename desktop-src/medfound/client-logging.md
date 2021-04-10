---
description: Registrazione client
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registrazione client (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225832"
---
# <a name="client-logging-microsoft-media-foundation"></a>Registrazione client (Microsoft Media Foundation)

L'origine di rete supporta la registrazione client, che consente al server multimediale di tenere traccia dell'attività dei client che si connettono. I registri client consentono a un server di registrare le statistiche di connessione, rendering e flusso. Questi log possono essere usati dai provider di contenuti in diversi scenari, ad esempio, per tracciare l'utilizzo del server multimediale e generare la fatturazione o per fornire contenuti di qualità adeguata a seconda della velocità della rete del client.

Un file di log contiene diverse voci dell'evento client. Ogni voce di log contiene un numero di campi delimitati da spazi. Esistono due tipi di log client: *rendering* (riproduzione) e *streaming* (ricezione). Poiché il contenuto può essere riprodotto e trasmesso simultaneamente, il client può inviare una combinazione di entrambi i tipi di dati di log. In alcuni casi, per la stessa sessione possono esistere due voci di log. Ad esempio, quando la cache veloce è abilitata, il client può completare la ricezione del contenuto trasmesso prima di completarne il rendering. In tal caso, i dati del log di streaming verrebbero inviati prima dei dati del log di rendering.

Il client invia i dati di log di rendering al server quando il client passa da qualsiasi stato di riproduzione (riproduzione, avanzamento rapido o riavvolgimento) a uno stato non di riproduzione (arresto, pausa, fine del flusso e inizio del flusso). Quando vengono inviati i dati di un log di rendering, viene effettuata una connessione direttamente al server multimediale o a un server proxy configurato.

Se il contenuto viene archiviato in un file di cache locale temporaneo nel computer in cui è in esecuzione il client di, il client può leggere un file dalla cache locale e inviare i dati del log di rendering per indicare che ha eseguito il contenuto. In questo caso, il client legge un file dalla cache locale, la voce del log di rendering non contiene statistiche di rete e il protocollo è impostato su cache.

Il client invia i dati di log di streaming al server per indicare il modo in cui il client ha ricevuto il contenuto, ma non come è stato eseguito il rendering. Il client può inviare il log di streaming Long prima che il client completi il rendering del contenuto.

In questo argomento non vengono fornite informazioni su tutti i campi del log. Per un riferimento completo, vedere [struttura dei dati del log di Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Configurazione di campi di log

Media Foundation consente al client di configurare l'origine di rete usando le proprietà. L'applicazione deve impostare le proprietà appropriate in un archivio di proprietà e passarla a uno dei metodi del resolver di origine. Il resolver di origine crea l'origine di rete come richiesto e apre una connessione con il server. Se la connessione ha esito positivo, il client invia informazioni su se stesso.

Nella tabella seguente vengono descritti i campi di log e le proprietà corrispondenti che un'applicazione può impostare tramite il resolver di origine. Queste informazioni non cambiano durante la sessione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo di registrazione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>Identificazione univoca del lettore. Queste informazioni vengono inviate all'inizio della connessione. Si tratta in genere di un GUID del client. Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .<br/> Il client invia queste informazioni al server all'inizio della connessione.<br/> Valore di esempio: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-playerversion</td>
<td>Numero di versione del lettore inviato all'inizio della connessione. Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .<br/> Il client invia queste informazioni al server all'inizio della connessione.<br/></td>
</tr>
<tr class="odd">
<td>CS (User-Agent)</td>
<td>Tipo di browser utilizzato se il lettore è incorporato in un browser. Questo valore può essere impostato dal client nella proprietà <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .<br/> Se il lettore non è incorporato, questo campo fa riferimento all'agente utente del client che ha generato il log. In questo caso, il client deve impostare la proprietà <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .<br/> Il client invia queste informazioni al server all'inizio della connessione.<br/> Valore di esempio: &quot; Mozilla/4.0 _ (compatibile; _MSIE_4.01; _Windows_98)&quot;<br/></td>
</tr>
<tr class="even">
<td>CS (Referer)</td>
<td>URL della pagina Web in cui il lettore è stato incorporato (se era incorporato). Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .<br/> Il client invia queste informazioni al server alla fine della connessione.<br/> Valore di esempio: &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>Per le voci di log del lettore, il programma host (exe) eseguito. Ad esempio, una pagina Web in un browser, un'applet Microsoft Visual Basic o un lettore autonomo. Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .<br/> Il client invia queste informazioni al server alla fine della connessione.<br/> Valori di esempio:<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>Numero di versione del programma host (exe). Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .<br/> Il client invia queste informazioni al server alla fine della connessione.<br/></td>
</tr>
</tbody>
</table>



 

Nell'esempio di codice seguente viene illustrata la configurazione dell'origine di rete da parte di un'applicazione client. Questo esempio Mostra come impostare il campo del log "c-hostexe".


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

Quando l'applicazione chiama uno dei metodi del resolver di origine, crea l'origine di rete, imposta le proprietà specificate nell'archivio delle proprietà e apre una sessione con il server multimediale. Oltre alle informazioni configurabili descritte nella sezione precedente, i dati aggiuntivi vengono trasferiti tra il server e il client all'inizio della sessione, durante il flusso e quando la sessione viene chiusa.

L'applicazione può recuperare le statistiche di rete usando l'identificatore del servizio **MFNETSOURCE \_ Statistics \_** . Per usare questo servizio, l'applicazione può chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà contenente le statistiche di rete nella proprietà [**MFNETSOURCE \_ Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . È possibile recuperare valori specifici fornendo l'identificatore corrispondente definito nell'enumerazione **MFNETSOURCE \_ Statistics \_ IDS** .

Nell'esempio di codice seguente viene illustrato come utilizzare il servizio per ottenere il numero di pacchetti ricevuti dal client.


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



Nell'elenco seguente vengono descritti alcuni degli identificatori delle statistiche di rete definiti in [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).



| Identificatore statistiche di rete              | Descrizione                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ID AVGBANDWIDTHBPS \_ MFNETSOURCE**       | Larghezza di banda media (in bit al secondo) a cui il client è connesso al server. Il valore viene calcolato nell'intera durata della connessione.                                                              |
| **\_ID BUFFERINGCOUNT \_ MFNETSOURCE**        | Numero di volte in cui il client è memorizzato nel buffer durante la riproduzione del flusso.                                                                                                                                                              |
| **\_ID BYTESRECEIVED \_ MFNETSOURCE**         | Numero di byte ricevuti dal client dal server. Il valore non include alcun overhead aggiunto dallo stack di rete. Lo stesso contenuto trasmesso tramite protocolli diversi può produrre valori diversi. |
| **\_ID LINKBANDWIDTH \_ MFNETSOURCE**         | Larghezza di banda massima disponibile del client in bit al secondo.                                                                                                                                                              |
| **\_ID LOSTPACKETS \_ MFNETSOURCE**           | Numero di pacchetti inviati dal server ma persi durante la trasmissione e mai riprodotti dal client. Il valore non include i pacchetti TCP o UDP.                                                                          |
| **\_ID RECVPACKETS \_ MFNETSOURCE**           | Numero di pacchetti ricevuti dal server. il valore non include i pacchetti TCP o UDP.                                                                                                                                  |
| **\_ID RECOVEREDBYECCPACKETS \_ MFNETSOURCE** | Pacchetti persi nella rete ripristinati e ripristinati a livello di client. Questo valore non include i pacchetti TCP o UDP.                                                                                          |
| **\_ID RESENDSREQUESTED \_ MFNETSOURCE**      | Numero di richieste effettuate dal client per la ricezione di nuovi pacchetti. Questo valore non include i pacchetti TCP o UDP.                                                                                                          |
| **\_ID RECOVEREDPACKETS \_ MFNETSOURCE**      | Numero di pacchetti ripristinati perché sono stati inviati tramite UDP. Questo valore non include i pacchetti TCP o UDP. Questo campo contiene uno zero, a meno che il client non usi il riinvio UDP.                                        |
| **\_ID BUFFERPROGRESS \_ MFNETSOURCE**        | Percentuale del buffer di riproduzione riempita durante il buffering.                                                                                                                                                              |
| **\_ID del protocollo MFNETSOURCE \_**              | Protocollo utilizzato per accedere al flusso. Questo può essere diverso dal protocollo richiesto dal client.                                                                                                                             |
| **\_ID trasporto \_ MFNETSOURCE**             | Protocollo di trasporto usato per fornire il flusso. Deve essere UDP o TCP.                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità di origine della rete](network-source-features.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

