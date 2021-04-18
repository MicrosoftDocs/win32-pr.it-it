---
description: Funzionalità di origine della rete
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: Funzionalità di origine della rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e937a97cf743740d9cebf84ad477c52cdee5083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549952"
---
# <a name="network-source-features"></a>Funzionalità di origine della rete

L'origine di rete fornisce l'implementazione di base per lo streaming dei file multimediali ed espone l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . L'implementazione dell'origine di rete specifica dipende dal protocollo usato per aprire l'origine, ad esempio RTSP o HTTP. Le origini di rete specifiche del protocollo estendono le funzionalità di rete di base. Per informazioni sugli schemi e sui protocolli supportati, vedere [protocolli supportati](supported-protocols.md).

Origine rete:

-   Implementa funzionalità come la memorizzazione nella cache, il rilevamento del proxy e la riconnessione automatica.
-   Converte le chiamate indipendenti dal protocollo dal resolver di origine a chiamate specifiche del protocollo.
-   Interagisce con il livello socket e il sistema operativo. Analizza la descrizione SDP e la usa come dati di configurazione e legge i dati del flusso dal livello di socket sottostante. Quando viene ricevuta, l'origine di rete è responsabile del riordinamento e della richiesta di ritrasmissione dei pacchetti.

## <a name="network-source-creation"></a>Creazione dell'origine di rete

La creazione di un'origine multimediale per un'origine dalla rete non è diversa da un'origine multimediale per un file locale. L'applicazione passa l'URL per i metodi del [resolver](source-resolver.md) di origine a quello di origine, ad esempio [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) e specifica il flag di risoluzione di MF per la \_ risoluzione \_ . Per ulteriori informazioni sull'utilizzo di questo flag, vedere [using the source resolver](using-the-source-resolver.md).

A seconda dello schema fornito dall'applicazione, il resolver di origine carica l'oggetto gestore dello schema appropriato che espone l'interfaccia [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . L'applicazione può anche usare direttamente il gestore dello schema per creare l'origine di rete chiamando [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

Per altre informazioni, vedere [gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Media Foundation non supporta flussi di byte per le origini di rete. L'oggetto flusso di byte è supportato solo nello scenario di contenuto scaricato. Tutti i dati vengono trasmessi il più rapidamente possibile in modo che possano essere salvati come file nel computer locale. i server Web forniscono i dati scaricati. Non esiste alcuna comunicazione dal client al server dopo l'inizio del download. In questo caso viene usato il protocollo di download HTTP.

Se l'applicazione richiede al resolver di origine di creare un oggetto flusso di byte per gli schemi "http:", "MMS:" o "RTSP:", la chiamata ha esito negativo con l' \_ errore di schema MF E non \_ supportato \_ .

> [!Note]  
> In Windows 7, l'origine di rete supporta i file di Windows Media Station (. NSC). Questi file vengono usati nello streaming multicast del contenuto multimediale in una rete. Per creare l'origine di rete per un oggetto specificato. File NSC, l'applicazione deve usare il resolver di origine.

 

Se l'applicazione usa il gestore dello schema, la chiamata asincrona ignora il parametro *dwFlags* e restituisce un puntatore all'origine di rete al termine del completamento.

La figura seguente mostra il flusso di dati per lo streaming multimediale usando l'origine di rete.

![diagramma di flusso che mostra i percorsi dall'applicazione al server di streaming, con un ciclo tra l'origine di rete e la sessione multimediale](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>Configurazione dell'origine di rete

In questo argomento vengono descritte le funzionalità supportate dall'origine di rete e le opzioni di configurazione associate. Un'applicazione può configurare l'origine di rete durante la creazione dell'oggetto di origine di rete. Queste opzioni vengono archiviate in un oggetto **IPropertyStore** , che deve essere passato dall'applicazione nel parametro *pProps* dei metodi del resolver di origine o [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

### <a name="auto-reconnect"></a>Riconnessione automatica

La funzionalità di riconnessione automatica dell'origine di rete consente a un client di riconnettersi automaticamente al server multimediale quando la connessione TCP al server ha esito negativo o il client non riesce a ricevere i pacchetti. Quando la connessione non riesce, l'origine di rete tenta di riconnettersi al server multimediale utilizzando la stessa configurazione utilizzata nella connessione precedente. Il processo di riconnessione è asincrono. L'origine di rete genera l'evento [MEReconnectStart](mereconnectstart.md) quando inizia la riconnessione e l'evento [MEReconnectEnd](mereconnectend.md) quando la riconnessione ha esito positivo o negativo.

Se il numero di tentativi di riconnessione supera il valore massimo specificato dalla proprietà [**MFNETSOURCE \_ AUTORECONNECTLIMIT**](mfnetsource-autoreconnectlimit-property.md) , l'operazione di riconnessione viene annullata. Il numero di tentativi di riconnessione è archiviato nella [**proprietà \_ AUTORECONNECTPROGRESS di MFNETSOURCE**](mfnetsource-autoreconnectprogress-property.md) .

La riconnessione automatica consente la riproduzione uniforme del contenuto multimediale anche quando la connessione TCP al server multimediale ha esito negativo. Per un'esperienza di riproduzione uniforme, il client deve disporre di dati sufficienti, da almeno 1 a 2 minuti, nella cache per continuare la riproduzione fino alla riconnessione. La quantità massima di dati che l'origine di rete è in grado di memorizzare nel buffer può essere impostata nella proprietà [**\_ MAXBUFFERTIMEMS di MFNETSOURCE**](mfnetsource-maxbuffertimems-property.md) .

### <a name="fast-streaming"></a>Streaming veloce

Il client di origine della rete richiede al server di trasmettere alcuni dati all'inizio del contenuto a una velocità più elevata rispetto a quella specificata dalla velocità in bit del contenuto. Se nel server è abilitato l' *avvio rapido* , il server invia un flusso accelerato a velocità in bit, in modo che il client possa memorizzare nel buffer una quantità di dati sufficiente più velocemente che in tempo reale. Ciò consente di migliorare l'esperienza utente riducendo al minimo i ritardi di buffer iniziali, che possono essere causati da diversi fattori, ad esempio la velocità ridotta del computer client o della rete e la larghezza di banda disponibile.

Per specificare la quantità di dati di streaming veloce che il client può richiedere, impostare la proprietà [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) . Se l'origine di rete usa UDP come protocollo di trasporto, specificare la quantità massima di dati di streaming veloce impostando la [**proprietà \_ MAXUDPACCELERATEDSTREAMINGDURATION di MFNETSOURCE**](mfnetsource-maxudpacceleratedstreamingduration-property.md) .

È anche possibile eseguire lo streaming veloce sul client tramite la funzionalità *fast cache* , ovvero trasmettere il contenuto su richiesta più velocemente del tempo reale e memorizzare nella cache i dati nella cache locale del client. Per usare questo tipo di streaming veloce, è necessario abilitare la cache veloce nell'origine di rete e il server deve supportarla. Quando il client richiede il contenuto dal server, l'origine di rete verifica prima di tutto se il contenuto è già presente nella cache del client. Se il contenuto si trova nella cache locale del client e non è scaduto, ne viene eseguito il rendering. Se il contenuto non si trova nella cache locale o è già scaduto, il contenuto viene trasmesso e memorizzato nella cache e l'origine di rete la riproduce dalla cache locale. Nelle richieste successive, per le playlist, solo le voci mancanti vengono memorizzate nella cache e quindi riprodotte. Se una voce della playlist è già presente nella cache locale del client, viene riprodotta da questa posizione e non viene memorizzata di nuovo nella cache.

Per impostazione predefinita, la cache veloce è abilitata nel client di origine di rete. Tuttavia, i fattori seguenti determinano anche se la funzionalità viene utilizzata:

-   Il client deve avere una larghezza di banda aggiuntiva disponibile per scaricare e memorizzare nella cache il contenuto più velocemente della velocità normale.
-   Il client deve disporre di spazio su disco sufficiente. Se il client dispone di meno di 100 MB di spazio disponibile su disco dopo la memorizzazione nella cache del contenuto su richiesta richiesto, non viene memorizzato nella cache, ma viene trasmesso e sottoposto a rendering simultaneamente.

La funzionalità cache veloce è controllata dalla proprietà [**\_ CACHEENABLED di MFNETSOURCE**](mfnetsource-cacheenabled-property.md) .

### <a name="buffer-management"></a>Gestione del buffer

L'origine di rete offre una gestione efficiente del buffer che monitora lo stato del buffer nel client. Per impostazione predefinita, l'origine di rete memorizza nel buffer 5 secondi di dati all'avvio. Questo valore può essere configurato impostando la proprietà [**MFNETSOURCE \_ BUFFERINGTIME**](mfnetsource-bufferingtime-property.md) . In base a questo valore della proprietà, l'origine di rete calcola la dimensione del buffer sufficiente per garantire la riproduzione uniforme e senza interruzioni del contenuto multimediale. Se questa proprietà è impostata su 0, la gestione del buffer è disabilitata. Quando la quantità di contenuto nel buffer è bassa, l'origine di rete avvia il buffering e genera l'evento [MEBufferingStarted](mebufferingstarted.md) per indicare che è iniziata la memorizzazione nel buffer. Al momento della ricezione di questo evento, la pipeline interrompe il rendering. Quando il buffering è completo, l'origine di rete genera l'evento [MEBufferingStopped](mebufferingstopped.md) e il client può avviare di nuovo il rendering.

Il client avvia il rendering del contenuto dopo l'accumulo della quantità di dati indicata dalla dimensione del buffer del primo campione. Se questo valore è inferiore alla dimensione del buffer calcolata, la riproduzione viene avviata immediatamente. Questo comportamento è molto simile alla funzionalità di avvio rapido.

La [**proprietà \_ MAXBUFFERTIMEMS di MFNETSOURCE**](mfnetsource-maxbuffertimems-property.md) archivia la quantità massima di dati che possono essere memorizzati nel buffer.

### <a name="bandwidth-selection"></a>Selezione della larghezza di banda

Quando un client si connette al server multimediale, come parte della configurazione della connessione, l'origine di rete esegue una misurazione *statica di coppie di pacchetti* per stimare la larghezza di banda dei collegamenti iniziale tra client e server. In base al risultato di questa misurazione, il client può selezionare flussi audio e video che rientrano nella larghezza di banda stimata. In questo modo si garantisce la riproduzione uniforme del contenuto dei flussi multimediali.

Durante la fase di avvio rapido viene eseguita la misurazione *dinamica delle coppie di pacchetti* . In questo processo il client riceve grandi quantità di dati, che possono essere più pacchetti o esempi.

Il risultato della misurazione dinamica delle coppie di pacchetti è più accurato rispetto alla stima della larghezza di banda dei collegamenti restituita dalla misurazione statica delle coppie di pacchetti, perché il processo statico della coppia di pacchetti Invia un singolo pacchetto di dimensioni fisse, che potrebbe non restituire risultati accurati per le reti a larghezza di banda elevata.

L'applicazione può ottenere la larghezza di banda stimata usando la proprietà [**\_ PPBANDWIDTH di MFNETSOURCE**](mfnetsource-ppbandwidth-property.md) .

Le condizioni della rete possono variare in modo dinamico, causando problemi di riproduzione dell'origine di rete. L'origine di rete può modificare la selezione del flusso iniziale del client in base alla frequenza di ricezione e allo stato del buffer. Ad esempio, il client può passare a una velocità in bit inferiore durante la congestione della rete e tornare a una velocità in bit superiore quando il traffico di rete è migliorato e il client ha accumulato una quantità sufficiente di contenuto memorizzato nel buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



