---
description: Viene illustrato come abilitare l'accesso all'archivio dati da un servizio Web OpenSearch e come evitare potenziali barriere per questa operazione.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Abilitazione dell'archivio dati Windows ricerca federata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26feb231f17dbaacb9656f2ef91e1cdb64bc598831a1e4808327dff7e5787bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456757"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Abilitazione dell'archivio dati Windows ricerca federata

Viene illustrato come abilitare l'accesso all'archivio dati da un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) e come evitare potenziali barriere per questa operazione.

Questo argomento è organizzato come segue:

-   [Condizioni per l'accettazione della richiesta di ricerca](#conditions-for-search-request-acceptance)
    -   [Sintassi di query supportata](#supported-query-syntax)
    -   [Protocolli di autenticazione supportati](#supported-authentication-protocols)
-   [Invio di query e restituzione dei risultati della ricerca in RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Esempio di output di un feed RSS](#example-of-an-rss-feed-output)
-   [Mapping automatico alle Windows shell](#automatic-mapping-to-windows-shell-properties)
-   [Informazioni su come Mappe Windows elementi ai tipi di file](#understanding-how-windows-maps-items-to-file-types)
-   [Evitare potenziali barriere all'abilitazione di un archivio dati](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condizioni per l'accettazione della richiesta di ricerca

Il [OpenSearch](https://github.com/dewitt/opensearch) web creato nel server Web **deve** soddisfare i due requisiti seguenti:

-   Essere in grado di accettare `GET URL` una query dal client.
-   Consente di incorporare i termini di ricerca nell'URL.

    Nell'esempio seguente viene illustrato come incorporare un termine di ricerca in un URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> La ricerca federata non supporta l'invio `POST` di richieste a un servizio Web.

 

Per altre informazioni sulla costruzione di un URL, vedere "Parametri del modello URL" in Creazione di un [file di descrizione](-search-federated-search-osdx-file.md)OpenSearch in Windows Ricerca federata .

### <a name="supported-query-syntax"></a>Sintassi di query supportata

Non è prevista alcuna sintassi di query specifica Windows 7. Il provider OpenSearch accetta i termini immessi dall'utente nella casella di input in Windows Explorer e lo codifica nell'URL. A tale scopo, in base al modello di URL descritto in "Parametri del modello URL" in Creazione di un file di descrizione OpenSearch in Windows [Ricerca federata](-search-federated-search-osdx-file.md).

Gli utenti prevedono che termini separati siano considerati implicitamente anDed insieme. Ad esempio, una query per "Microsoft Windows" deve restituire solo i risultati che contengono sia "Windows" che "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolli di autenticazione supportati

Windows La ricerca federata supporta Windows basata su autenticazione e può fornire credenziali ai servizi Web tramite i protocolli seguenti:

-   NTLM.
-   Autenticazione Kerberos.
-   Basic (solo su https).
-   Altri provider di supporto per la sicurezza (SSP) installati in Windows che forniscono capacità di query aggiuntiva. Per informazioni sulla potenziale aggiunta di altri provider di servizi condivisi, vedere la documentazione di [SSP Interface](../secauthn/sspi.md) SDK.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Invio di query e restituzione dei risultati della ricerca in RSS o Atom

Il [OpenSearch](https://github.com/dewitt/opensearch) provider è responsabile del mapping dei valori degli elementi XML Windows proprietà di sistema shell che possono essere usate dalle Windows applicazioni. Tuttavia, non si è limitati ai mapping predefiniti degli elementi RSS o Atom standard e possono includere elementi XML personalizzati nello spazio dei nomi Windows per ognuna delle proprietà. È ad esempio possibile aggiungere elementi XML personalizzati all'interno dell'elemento **item** per fornire metadati aggiuntivi Windows. È anche possibile eseguire il mapping di elementi da altri spazi dei nomi XML, ad esempio iTunes

### <a name="example-of-an-rss-feed-output"></a>Esempio di output di un feed RSS

L'output del feed RSS di esempio seguente restituisce un elemento.


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



Per informazioni più dettagliate sul mapping delle proprietà, vedere le sezioni "Elementi estesi nella ricerca federata WIndows" e "Mapping delle proprietà personalizzate" in Creazione di un file di descrizione [OpenSearch in ricerca](-search-federated-search-osdx-file.md)federata Windows .

## <a name="automatic-mapping-to-windows-shell-properties"></a>Mapping automatico alle Windows shell

All'interno degli elementi nel feed RSS è possibile scegliere di includere altri elementi XML che eseere automaticamente il mapping Windows proprietà di sistema di Shell. A tale scopo, includere un elemento denominato dopo la proprietà shell Windows e preceduto dal prefisso Windows dello spazio dei nomi di sistema shell. L'esempio seguente illustra la dichiarazione dello spazio dei nomi `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e l'inclusione di un elemento per il mapping della proprietà `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



Il prefisso dello spazio dei nomi usato qui ( `"win"` ) è un suggerimento. È possibile usare qualsiasi prefisso. Tuttavia, è necessario usare i nomi Windows proprietà shell e includere l'URI (Exact Uniform Resource Identifier), come illustrato nell'esempio seguente:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Informazioni Windows di sistema della shell**

Windows definisce un elenco completo di Proprietà di [sistema e](../properties/props.md) il formato del tipo di valore richiesto per ogni proprietà. La documentazione per la proprietà Shell della finestra [System.FileExtension,](../properties/props-system-fileextension.md) ad esempio, specifica che il valore deve contenere il punto iniziale (".docx" e non "docx").

**Valori di data e ora**

Il formato di data e ora preferito è ISO-8601, come illustrato nell'esempio seguente:


```
2008-01-16T 19:20:30:.45+01:00
```



Gli sviluppatori .NET devono usare la classe DateTime con `ToString("R") ` per ottenere il formato corretto.

Per informazioni più dettagliate sul mapping delle proprietà, vedere "Elementi estesi nella ricerca federata Windows" in Creazione di un file di descrizione OpenSearch [in Windows Ricerca federata](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Informazioni su come Mappe Windows elementi ai tipi di file

La ricerca all'interno Windows'interfaccia utente di Esplora risorse consente agli utenti di considerare i risultati come file quando un elemento RSS punta a un file archiviato in remoto. L'utente può trascinare e rilasciare elementi sul desktop e l'interfaccia Windows Explorer visualizza l'icona corretta e fornisce il menu di scelta rapida appropriato. Se l'elemento RSS non punta a un file archiviato in remoto, il file viene considerato come un collegamento e gli utenti possono eseguire azioni su di esso, ad esempio la creazione di un collegamento o l'apertura nel browser.

Il diagramma di flusso seguente illustra Windows il tipo di file di un elemento.

![Diagramma di flusso che mostra i percorsi da un elemento alle decisioni di considerarlo come un elemento di tipo collegamento Web o come tipo di file](images/determineanitemfiletype.png)

Il [provider OpenSearch](https://github.com/dewitt/opensearch) esegue la procedura seguente per eseguire il mapping di un elemento a un tipo di file:

-   Identificare se l'elemento deve essere considerato come un file o un collegamento Web.
-   Identificare l'estensione di file corretta da usare.

Ad esempio, se l'elemento ha un URL di collegamento che usa un percorso file system (ad esempio ), il provider OpenSearch considera il collegamento come file e determina il tipo in base all'estensione di file usata nel percorso `file:///\\server\share\etc\item.ext` (.ext in questo esempio). [](https://github.com/dewitt/opensearch)

Se l'elemento usa l'enclosure RSS standard o l'elemento **media:content mediaRSS,** il provider [OpenSearch](https://github.com/dewitt/opensearch) presuppone che l'elemento sia un file e identifichi l'estensione di file come indicato di seguito:

-   Se è stato eseguito il mapping della proprietà Windows Shell di [System.FileExtension](../properties/props-system-fileextension.md) per l'elemento, il provider usa tale estensione di file.
-   Se non è stato eseguito il mapping della proprietà Windows Shell di [System.FileExtension,](../properties/props-system-fileextension.md) il provider usa **l'attributo Type** specificato nell'elemento enclosure o content. Questo elemento deve contenere `MIMEType` una stringa, ad esempio `"image/jpeg"` . Se è associato a un'estensione di file registrata nel computer client, l'elemento viene considerato come `MIMEType` un file di quel tipo. Se non `MIMEType` è associato a un'estensione di file registrata nel computer client, l'elemento viene considerato come un tipo di collegamento Web. Il [OpenSearch](https://github.com/dewitt/opensearch) non tenta di analizzare **l'attributo URL** per individuare l'estensione del nome file.
-   Se è associato a un'estensione di file registrata nel computer client, il provider determina se l'estensione è un tipo di file Web noto `MIMEType` (.htm, .html, asp, aspx, php, swf, stm). In tal caso, il tipo di file viene considerato un tipo di collegamento Web. in caso contrario, viene considerato come un tipo di file. Ad esempio, se è associato all'estensione .htm file, tale elemento viene considerato come collegamento Web anziché come .htm `MIMEType "text/html"` di file.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitare potenziali barriere all'abilitazione di un archivio dati

Alcuni archivi dati non forniscono un [servizio Web OpenSearch](https://github.com/dewitt/opensearch)compatibile con il servizio, ma possono comunque essere connessi Windows ricerca federata. Tali archivi dati includono:

-   Indici remoti con metodi di autenticazione non supportati in Windows 7 Ricerca federata.

    Ad esempio, l'autenticazione basata su moduli e altri metodi di autenticazione personalizzati.

-   Se un archivio pubblico di alto valore ha API Web pubbliche, chiunque può scrivere un altro servizio Web compatibile con OpenSearch e chiama tali API [in](https://github.com/dewitt/opensearch)background.

    Ad esempio, la Library of Congress e i database di ricerca sanitaria.

-   Archivi dati aziendali proprietari o indici e archivi di gestione dei contenuti legacy, per i quali potrebbe essere impossibile implementare un front-end.

Esistono tuttavia alternative che possono evitare barriere all'abilitazione di un archivio dati. Di seguito sono riportate alcune di queste alternative:

**Per scrivere un servizio Web middle-man quando non è possibile modificare il servizio Web per l'origine dati esistente oppure il servizio Web fornisce un'API personalizzata:**

1.  Scrivere un servizio Web middle-man in grado di accettare una query Windows 7.
2.  Connessione'origine dati e recuperare i risultati della query.
3.  Riformattare i risultati in formato RSS o Atom.
4.  Restituire i risultati al client Windows 7.
5.  Si noti che per i servizi dati aziendali e molti servizi dati Internet potrebbe essere necessario passare le credenziali utente per conto del servizio Web per eseguire la rimozione dei risultati in base alle autorizzazioni dell'utente.

**Per usare un motore di ricerca esistente quando non è possibile abilitare un archivio dati pubblico:**

1.  Usare un motore di ricerca pubblico che supporta già OpenSearch [con](https://github.com/dewitt/opensearch) RSS. A tale scopo, fornire agli utenti un file con estensione osdx con un modello di URL che limita i risultati solo a quelli per il dominio specifico.
2.  Vedere l'esempio seguente di [una OpenSearch](https://github.com/dewitt/opensearch) per cercare solo il contenuto della Guida per Windows usando una query su live.com.

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

**Per usare un server di indicizzazione esistente che supporta OpenSearch quando non è possibile abilitare indici o archivi dati aziendali proprietari:**

1.  Selezionare un server di indicizzazione esistente che supporti OpenSearch [indicizzare](https://github.com/dewitt/opensearch) il contenuto, ad esempio SharePoint Search Server.
2.  Creare un file con estensione osdx che limita i risultati dell'indice SharePoint solo a quelli del server usando la sintassi KeyWord all'interno del modello di URL.

**Per scrivere un archivio dati sul lato client se una soluzione solo lato server non funziona:**

1.  Scrivere un'origine [OpenSearch](https://github.com/dewitt/opensearch) client che si trova tra il provider Windows [OpenSearch](https://github.com/dewitt/opensearch) e l'origine dati esterna.
2.  Usare l'API dell'interfaccia [IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) in Windows SDK per creare un file con estensione searchconnector-ms configurato in modo appropriato tramite il quale Windows Explorer può chiamare l'implementazione con i parametri di query. L'implementazione può quindi restituire risultati formattati in formato RSS o Atom. Questa operazione consente all'implementazione di fornire un'interfaccia utente di autenticazione personalizzata e di connettersi all'origine dati usando l'API proprietaria.

> [!Note]  
> L'apertura di un file con estensione osdx crea un file con estensione searchconnector-ms (connettore di ricerca) nella directory %userprofile%/searches e inserisce un collegamento nella directory %userprofile%/links.

 

## <a name="additional-resources"></a>Risorse aggiuntive

Per altre informazioni sull'implementazione della federazione della ricerca negli archivi dati remoti usando le tecnologie OpenSearch in Windows 7 e versioni successive, vedere "Risorse aggiuntive" in Ricerca federata [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Attività iniziali con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in Windows federata](-search-federated-search-web-service.md)
</dt> <dt>

[Creazione di un OpenSearch file di descrizione Windows ricerca federata](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate per la ricerca Windows federata](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca Windows ricerca federata](-search-federated-search-deploying.md)
</dt> </dl>

 

 
