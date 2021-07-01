---
description: Informazioni su Ricerca federata, che consente agli utenti di accedere e interagire con i dati remoti dall'interno Esplora risorse.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Attività iniziali con Ricerca federata in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de3fc42686e94f2edc1c5d45bbb0374afe79535
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119066"
---
# <a name="getting-started-with-federated-search-in-windows"></a>Attività iniziali con Ricerca federata in Windows

Il supporto di Windows 7 per la federazione della ricerca negli archivi dati remoti con tecnologie OpenSearch consente agli utenti di accedere ai dati remoti e interagire con loro dall'interno Esplora risorse. È possibile compilare un archivio dati basato sul Web in cui è possibile eseguire ricerche tramite la ricerca federata di Windows e abilitare l'integrazione avanzata delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice sul lato client Windows.

Questo argomento è organizzato come segue:

-   [Che cos'è Ricerca federata?](#what-is-federated-search)
-   [Passaggi per la compilazione della ricerca federata](#steps-for-building-federated-search)
-   [Funzionamento della ricerca federata](#how-federated-search-works)
-   [Invio di query e restituzione dei risultati della ricerca in RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Esempi di ricerca federata](#federated-search-examples)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-federated-search"></a>Che cos'è Ricerca federata?

Windows 7 supporta la connessione di origini esterne al client Windows tramite il [protocollo OpenSearch.](https://github.com/dewitt/opensearch) In questo modo gli utenti possono eseguire ricerche in un archivio dati remoto e visualizzare i risultati dall'interno Esplora risorse. Lo standard [OpenSearch](https://github.com/dewitt/opensearch) v1.1 definisce formati di file semplici che possono essere usati per descrivere in che modo un client deve eseguire query sul servizio Web per l'archivio dati e come il servizio deve restituire risultati per il rendering da parte del client. La ricerca federata Windows si connette ai servizi Web che ricevono query [OpenSearch](https://github.com/dewitt/opensearch) e restituisce i risultati in formato RSS o Atom XML.

La schermata seguente illustra i risultati della ricerca ottenuti dopo la ricerca in remoto in un sito di SharePoint.

![Screenshot che mostra i risultati della ricerca da un sito di SharePoint come visualizzato in Esplora risorse](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Passaggi per la compilazione della ricerca federata

Per compilare la ricerca federata, seguire questa procedura:

1.  Abilitare la ricerca nell'archivio dati da Esplora risorse fornendo un servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch)che può restituire risultati in formato RSS o Atom.
2.  Creare un file OpenSearch Description (con estensione osdx) che descrive come connettersi al servizio Web e come eseguire il mapping di qualsiasi elemento personalizzato in RSS o Atom XML.
3.  Distribuire i connettori di ricerca nei computer client Windows con un file OSDX.

Il diagramma seguente illustra i passaggi per la compilazione della ricerca federata.

![Diagramma del processo di compilazione della ricerca federata](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Funzionamento della ricerca federata

La comunicazione tra Esplora risorse e il [servizio Web OpenSearch](https://github.com/dewitt/opensearch) viene eseguita tramite il livello dati di Windows. Il livello dati di Windows può comunicare con diversi tipi di archivi dati tramite i provider di Windows Store. Ogni provider è specializzato nella comunicazione con archivi dati che supportano un protocollo specifico e hanno funzionalità specifiche. Ad esempio, la figura seguente illustra come il provider [OpenSearch](https://github.com/dewitt/opensearch) comunica con gli archivi dati che forniscono un servizio Web che supporta lo standard [OpenSearch.](https://github.com/dewitt/opensearch)

![diagramma che illustra la comunicazione da Esplora risorse nel client tramite l'archivio dati opensearch nel server remoto](images/windowssearchfederationfunctionality.png)

Per abilitare l'archivio dati per supportare la ricerca federata in Windows 7, è necessario eseguire una serie di attività. Nella tabella seguente sono elencate le attività per l'abilitazione dell'archivio dati, gli elementi necessari per eseguire ogni attività e la posizione in cui trovare la documentazione.



| Attività                                                                                                     | Requisito                                                                                                                                                                                            | Documentazione                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abilitare la ricerca nell'archivio dati in base Esplora risorse.<br/>                                    | Creare un servizio Web compatibile con OpenSearch.<br/> Creare un file OpenSearch Description (con estensione osdx).<br/>                                                                                       | [Connessione del servizio Web in Ricerca federata Windows](-search-federated-search-web-service.md)<br/> [Abilitazione dell'archivio dati nella ricerca federata di Windows](-search-federated-search-data-store.md)<br/> |
| Distribuire attivamente il servizio Web agli utenti all'interno di un'organizzazione.<br/>                               | Fornire un file OSDX agli utenti, copiarlo in locale e renderlo accessibile all'utente tramite un collegamento.<br/>                                                                                     | [Distribuzione di connettori di ricerca in Ricerca federata di Windows](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Enumerare i risultati della Esplora risorse in risposta a una query.<br/>                          | Implementare un servizio Web che accetta una stringa di query e restituisce i risultati in formato RSS o Atom.<br/>                                                                                              | [Connessione del servizio Web in Ricerca federata Windows](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Consentire agli utenti di aggiungere l'archivio dati alla Esplora risorse.<br/>                                | Creare un file con estensione osdx e fornirlo agli utenti.<br/>                                                                                                                                           | [Abilitazione dell'archivio dati nella ricerca federata di Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Visualizzare gli elementi come elementi simili a file in Esplora risorse.<br/>                                    | Restituire un URL al file o al flusso di contenuto usando elementi **enclosure** o **media:content**<br/> Specificare un'estensione di file o un tipo MIME riconosciuto dal computer client.<br/> | [Abilitazione dell'archivio dati nella ricerca federata di Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Visualizzare proprietà personalizzate in Esplora risorse, oltre a quelle definite negli standard RSS o Atom.<br/> | Fornire metadati aggiuntivi usando un altro spazio dei nomi XML nell'output RSS/Atom.<br/> Aggiungere una mappa delle proprietà al file con estensione osdx.<br/>                                                       | [Creazione di un file di descrizione OpenSearch in Ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Personalizzare le proprietà visualizzate per gli elementi in Esplora risorse.<br/>               | Aggiungere mapping proplist al file con estensione osdx.<br/>                                                                                                                                                   | [Creazione di un file di descrizione OpenSearch in Ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Visualizzare una visualizzazione pagina Web personalizzata degli elementi nel riquadro di anteprima.<br/>                              | Restituisce valori distinti per il collegamento e l'enclosure.<br/> Eseguire il mapping di un valore URL alla proprietà Della shell di Windows **System.WebPreviewUrl.**<br/>                                                               | [Creazione di un file di descrizione OpenSearch in Ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Visualizzare un pulsante della barra dei comandi Esplora risorse eseguire il roll-over della query nel sito Web.<br/>   | Specificare un `Url format="text/html"` modello nel file con estensione osdx.<br/>                                                                                                                              | [Creazione di un file di descrizione OpenSearch in Ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Invio di query e restituzione dei risultati della ricerca in RSS o Atom

Quando l'utente digitare un termine nella casella di ricerca nell'angolo superiore destro di Esplora risorse, la query viene inviata al provider [OpenSearch,](https://github.com/dewitt/opensearch) che quindi invia la query all'archivio dati remoto. Il servizio Web remoto risponde alla query fornendo risultati in un documento XML, in genere definito feed, in uno dei due formati supportati (RSS o Atom). Ogni elemento del risultato nel feed include elementi figlio XML per rappresentare o descrivere i metadati dell'elemento, ad esempio il titolo, l'URL, la descrizione, l'immagine di anteprima e così via. Il provider [OpenSearch](https://github.com/dewitt/opensearch) è responsabile del mapping dei valori degli elementi XML alle proprietà di sistema della shell di Windows che possono essere usate dalle applicazioni Windows.

## <a name="federated-search-examples"></a>Esempi di ricerca federata

Il file di descrizione opensearch di esempio seguente (con estensione osdx) è costituito da elementi e , che sono gli elementi figlio minimi necessari per connettere un archivio dati esterno al client Windows tramite il `ShortName` `Url` protocollo OpenSearch.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



L'esempio seguente illustra come rendere ricercabile un archivio dati abilitato per il Web in formato RSS e come specificare che deve essere restituito un elemento di ricerca:


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



L'esempio seguente illustra come eseguire il mapping delle proprietà alle proprietà di sistema predefinite in modo che gli elementi visualizzati siano ordinati e raggruppati:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



L'esempio seguente illustra come aggiungere una visualizzazione dell'immagine di anteprima a ogni elemento in Esplora risorse:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Risorse aggiuntive

Per altre informazioni sull'implementazione della federazione della ricerca in archivi dati remoti con tecnologie OpenSearch in Windows 7 e versioni successive, vedere "Risorse aggiuntive" in [Ricerca federata in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Connessione del servizio Web in Ricerca federata Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati nella ricerca federata di Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un file di descrizione OpenSearch in Ricerca federata di Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate nella ricerca federata di Windows](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca in Ricerca federata di Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 




