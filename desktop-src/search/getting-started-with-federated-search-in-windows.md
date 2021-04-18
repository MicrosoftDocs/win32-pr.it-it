---
description: Il supporto di Windows 7 per la Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch consente agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Introduzione con ricerca federata in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525470"
---
# <a name="getting-started-with-federated-search-in-windows"></a>Introduzione con ricerca federata in Windows

Il supporto di Windows 7 per la Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch consente agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse. È possibile creare un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante ricerca federata di Windows e abilitare l'integrazione avanzata delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice lato client Windows.

Questo argomento è organizzato nel modo seguente:

-   [Che cos'è la ricerca federata?](#what-is-federated-search)
-   [Passaggi per la compilazione della ricerca federata](#steps-for-building-federated-search)
-   [Funzionamento della ricerca federata](#how-federated-search-works)
-   [Invio di query e restituzione di risultati della ricerca in formato RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [Esempi di ricerca federati](#federated-search-examples)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-federated-search"></a>Che cos'è la ricerca federata?

Windows 7 supporta la connessione di origini esterne al client Windows tramite il protocollo [OpenSearch](https://github.com/dewitt/opensearch) . Ciò consente agli utenti di eseguire ricerche in un archivio dati remoto e visualizzare i risultati da Esplora risorse. Lo standard [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 definisce formati di file semplici che possono essere utilizzati per descrivere il modo in cui un client deve eseguire una query sul servizio Web per l'archivio dati e il modo in cui il servizio deve restituire i risultati per il rendering da parte del client. La ricerca federata Windows si connette ai servizi Web che ricevono query [OpenSearch](https://github.com/dewitt/opensearch) e restituisce i risultati in formato XML Atom o RSS.

Lo screenshot seguente illustra i risultati della ricerca ottenuti dopo la ricerca remota in un sito di SharePoint.

![screenshot che mostra i risultati della ricerca da un sito di SharePoint come visualizzato in Esplora risorse](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a>Passaggi per la compilazione della ricerca federata

Per compilare la ricerca federata, seguire questa procedura:

1.  Consente di eseguire la ricerca nell'archivio dati da Esplora risorse fornendo un servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch)che può restituire risultati in formato RSS o Atom.
2.  Creare un file di descrizione OpenSearch (con estensione osdx) che descriva come connettersi al servizio Web e come eseguire il mapping di eventuali elementi personalizzati nel codice XML Atom o RSS.
3.  Distribuire i connettori di ricerca nei computer client Windows con un file con estensione osdx.

Il diagramma seguente illustra i passaggi per la compilazione della ricerca federata.

![diagramma del processo per la compilazione della ricerca federata](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a>Funzionamento della ricerca federata

La comunicazione tra Esplora risorse e il servizio Web [OpenSearch](https://github.com/dewitt/opensearch) viene eseguita tramite il livello dati di Windows. Il livello dati di Windows è in grado di comunicare con diversi tipi di archivi dati tramite i provider di Windows Store. Ogni provider è specializzato nella comunicazione con archivi dati che supportano un determinato protocollo e hanno funzionalità specifiche. Nella figura seguente, ad esempio, viene illustrato il modo in cui il provider [OpenSearch](https://github.com/dewitt/opensearch) comunica con gli archivi dati che forniscono un servizio Web che supporta lo standard [OpenSearch](https://github.com/dewitt/opensearch) .

![diagramma che illustra la comunicazione da Esplora risorse sul client tramite l'archivio dati OpenSearch nel server remoto](images/windowssearchfederationfunctionality.png)

Per consentire all'archivio dati di supportare la ricerca federata in Windows 7, è necessario eseguire una serie di attività. La tabella seguente elenca le attività per l'abilitazione dell'archivio dati, gli elementi necessari per eseguire ogni attività e la posizione in cui trovare la documentazione.



| Attività                                                                                                     | Requisito                                                                                                                                                                                            | Documentazione                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consente di eseguire la ricerca in Esplora risorse dell'archivio dati.<br/>                                    | Compilare un servizio Web compatibile con OpenSearch.<br/> Creare un file di descrizione OpenSearch (con estensione osdx).<br/>                                                                                       | [Connessione del servizio Web in ricerca federata di Windows](-search-federated-search-web-service.md)<br/> [Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)<br/> |
| Distribuisci attivamente il servizio Web agli utenti all'interno di un'azienda.<br/>                               | Fornire un file con estensione osdx agli utenti, copiarlo localmente e renderlo accessibile all'utente tramite un collegamento.<br/>                                                                                     | [Distribuzione di connettori di ricerca nella ricerca federata di Windows](-search-federated-search-deploying.md)<br/>                                                                                                              |
| Enumerare i risultati della ricerca in Esplora risorse in risposta a una query.<br/>                          | Implementare un servizio Web che accetta una stringa di query e restituisce i risultati in formato RSS o Atom.<br/>                                                                                              | [Connessione del servizio Web in ricerca federata di Windows](-search-federated-search-web-service.md)<br/>                                                                                                            |
| Consentire agli utenti di aggiungere l'archivio dati alla finestra Esplora risorse.<br/>                                | Creare un file con estensione osdx e fornirlo agli utenti.<br/>                                                                                                                                           | [Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Visualizza gli elementi come elementi di tipo file in Esplora risorse.<br/>                                    | Restituire un URL al file o al flusso di contenuto usando l' **enclosure** o i **supporti:** elementi di contenuto<br/> Specificare un'estensione di file o un tipo MIME riconosciuto dal computer client.<br/> | [Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)<br/>                                                                                                                |
| Visualizzare le proprietà personalizzate in Esplora risorse, oltre a quelle definite negli standard RSS o Atom.<br/> | Fornire metadati aggiuntivi usando un altro spazio dei nomi XML nell'output RSS/Atom.<br/> Aggiungere una mappa di proprietà al file con estensione osdx.<br/>                                                       | [Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Personalizzare le proprietà visualizzate per gli elementi in Esplora risorse.<br/>               | Aggiungere i mapping di proprietà di un file con estensione osdx.<br/>                                                                                                                                                   | [Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Visualizza una visualizzazione pagina Web personalizzata degli elementi nel riquadro di anteprima.<br/>                              | Restituisce valori di collegamento e enclosure distinti.<br/> Eseguire il mapping di un valore URL alla proprietà della shell di Windows **System. WebPreviewUrl** .<br/>                                                               | [Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| Consente di visualizzare un pulsante della barra dei comandi in Esplora risorse che esegue il rollforward della query nel sito Web.<br/>   | Fornire un `Url format="text/html"` modello nel file con estensione osdx.<br/>                                                                                                                              | [Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Invio di query e restituzione di risultati della ricerca in formato RSS o Atom

Quando l'utente digita un termine nella casella di ricerca nell'angolo superiore destro di Esplora risorse, la query viene inviata al provider [OpenSearch](https://github.com/dewitt/opensearch) , che quindi Invia la query all'archivio dati remoto. Il servizio Web remoto risponde alla query fornendo i risultati in un documento XML, in genere definito feed, in uno dei due formati supportati (RSS o Atom). Ogni elemento di risultato nel feed include elementi figlio XML per rappresentare o descrivere i metadati degli elementi, ad esempio titolo, URL, descrizione, immagine di anteprima e così via. Il provider [OpenSearch](https://github.com/dewitt/opensearch) è responsabile del mapping dei valori degli elementi XML alle proprietà di sistema della shell di Windows che possono essere utilizzate dalle applicazioni Windows.

## <a name="federated-search-examples"></a>Esempi di ricerca federati

Il file di descrizione OpenSearch (con estensione osdx) di esempio seguente è costituito da `ShortName` `Url` elementi e, che sono gli elementi figlio minimi necessari per connettere un archivio dati esterno al client Windows tramite il protocollo OpenSearch.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



Nell'esempio seguente viene illustrato come creare un archivio dati abilitato per il Web in formato RSS e come specificare che venga restituito un elemento di ricerca:


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



Nell'esempio seguente viene illustrato come eseguire il mapping delle proprietà alle proprietà di sistema predefinite in modo che gli elementi visualizzati siano ordinati e raggruppati:


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



Nell'esempio seguente viene illustrato come aggiungere una visualizzazione dell'immagine di anteprima a ogni elemento in Esplora risorse:


```
<media:thumbnail>    
```



## <a name="additional-resources"></a>Risorse aggiuntive

Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Connessione del servizio Web in ricerca federata di Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate seguenti in ricerca federata di Windows](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca nella ricerca federata di Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 




