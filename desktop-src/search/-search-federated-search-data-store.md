---
description: Viene illustrato come abilitare l'accesso all'archivio dati da un servizio Web OpenSearch e come evitare potenziali barriere.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Abilitazione dell'archivio dati in ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306174"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Abilitazione dell'archivio dati in ricerca federata di Windows

Viene illustrato come abilitare l'accesso all'archivio dati da un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) e come evitare potenziali barriere.

Questo argomento è organizzato nel modo seguente:

-   [Condizioni per l'accettazione della richiesta di ricerca](#conditions-for-search-request-acceptance)
    -   [Sintassi di query supportata](#supported-query-syntax)
    -   [Protocolli di autenticazione supportati](#supported-authentication-protocols)
-   [Invio di query e restituzione di risultati della ricerca in formato RSS o Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Esempio di output di un feed RSS](#example-of-an-rss-feed-output)
-   [Mapping automatico a proprietà della shell di Windows](#automatic-mapping-to-windows-shell-properties)
-   [Informazioni sul modo in cui Windows mappa gli elementi ai tipi di file](#understanding-how-windows-maps-items-to-file-types)
-   [Evitare potenziali barriere per l'abilitazione di un archivio dati](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Condizioni per l'accettazione della richiesta di ricerca

Il servizio Web [OpenSearch](https://github.com/dewitt/opensearch) creato nel server Web **deve** soddisfare i due requisiti seguenti:

-   Essere in grado di accettare una `GET URL` query dal client.
-   Consente di incorporare i termini di ricerca nell'URL.

    Nell'esempio seguente viene illustrato come un termine di ricerca può essere incorporato in un URL.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> La ricerca federata non supporta l'invio `POST` di richieste a un servizio Web.

 

Per ulteriori informazioni sulla creazione di un URL, vedere la sezione relativa ai parametri dei modelli URL nella pagina relativa alla [creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Sintassi di query supportata

In Windows 7 non è prevista una sintassi di query specifica. Il provider OpenSearch accetta tutti i termini immessi dall'utente nella casella di input in Esplora risorse e li codifica nell'URL. Questa operazione viene eseguita in base al modello di URL descritto in "parametri modello URL" in [creazione di un file di descrizione OpenSearch in ricerca federata di Windows](-search-federated-search-osdx-file.md).

Gli utenti si aspettano che i termini separati vengano considerati in modo implicito individuato insieme. Ad esempio, una query per "Microsoft Windows" deve restituire solo i risultati che contengono sia "Windows" che "Microsoft".

### <a name="supported-authentication-protocols"></a>Protocolli di autenticazione supportati

La ricerca federata Windows supporta l'autenticazione basata su Windows e può fornire le credenziali ai servizi Web tramite i protocolli seguenti:

-   NTLM.
-   Autenticazione Kerberos.
-   Basic (solo su HTTPS).
-   Altri SSP (Security Support Provider) installati in Windows che forniscono capacità di query aggiuntive. Vedere la documentazione di [SSP Interface](../secauthn/sspi.md) SDK per gestire la potenziale aggiunta di altri SSP.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Invio di query e restituzione di risultati della ricerca in formato RSS o Atom

Il provider [OpenSearch](https://github.com/dewitt/opensearch) è responsabile del mapping dei valori degli elementi XML alle proprietà di sistema della shell di Windows che possono essere utilizzate dalle applicazioni Windows. Tuttavia, non si è limitati ai mapping predefiniti di elementi RSS o Atom standard e possono includere elementi XML personalizzati nello spazio dei nomi Windows per ciascuna proprietà. È ad esempio possibile aggiungere elementi XML personalizzati all'interno dell'elemento **Item** per fornire metadati aggiuntivi a Windows. È anche possibile eseguire il mapping di elementi da altri spazi dei nomi XML, ad esempio iTunes

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



Per informazioni più dettagliate sul mapping delle proprietà, vedere le sezioni "elementi estesi in ricerca federata di WIndows" e "mapping di proprietà personalizzate" in [creazione di un file di descrizione OpenSearch in ricerca federata di Windows](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Mapping automatico a proprietà della shell di Windows

Negli elementi del feed RSS è possibile scegliere di includere altri elementi XML che vengono mappati automaticamente alle proprietà del sistema della shell di Windows. A tale scopo, includere un elemento denominato dopo la proprietà della shell di Windows e preceduto dallo spazio dei nomi System Shell di Windows. Nell'esempio seguente viene illustrata la dichiarazione dello spazio dei nomi `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e l'inclusione di un elemento per il mapping delle proprietà `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



Il prefisso dello spazio dei nomi usato qui ( `"win"` ) è un suggerimento. è possibile usare qualsiasi prefisso. Tuttavia, è necessario usare i nomi esatti delle proprietà della shell di Windows e deve includere l'esatta Uniform Resource Identifier (URI), come illustrato nell'esempio seguente:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Informazioni sulle proprietà di sistema della shell di Windows**

Windows definisce un elenco completo delle [proprietà di sistema](../properties/props.md) e il formato del tipo di valore necessario per ogni proprietà. La documentazione relativa alla proprietà della shell della finestra [System. FileExtension](../properties/props-system-fileextension.md) , ad esempio, specifica che il valore deve contenere il punto principale (". docx" e non "docx").

**Valori di data e ora**

Il formato di data e ora preferito è ISO-8601, come illustrato nell'esempio seguente:


```
2008-01-16T 19:20:30:.45+01:00
```



Gli sviluppatori .NET devono usare la classe DateTime con `ToString("R") ` per restituire il formato corretto.

Per informazioni più dettagliate sul mapping delle proprietà, vedere "elementi estesi in ricerca federata di Windows" in [creazione di un file di descrizione OpenSearch in ricerca federata di Windows](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Informazioni sul modo in cui Windows mappa gli elementi ai tipi di file

La ricerca all'interno dell'interfaccia utente di Esplora risorse consente agli utenti di trattare i risultati come file quando un elemento RSS punta a un file archiviato in remoto. L'utente può trascinare e rilasciare elementi sul desktop e l'interfaccia utente di Esplora risorse Visualizza l'icona corretta e fornisce il menu di scelta rapida appropriato. Se l'elemento RSS non punta a un file archiviato in modalità remota, il file viene considerato come un collegamento e gli utenti possono eseguire azioni su di esso, ad esempio creare un collegamento o aprirlo nel browser.

Il diagramma di flusso seguente mostra in che modo Windows determina il tipo di file di un elemento.

![diagramma di flusso che mostra i percorsi da un elemento alle decisioni per considerarlo come un elemento del tipo di collegamento Web o come tipo di file](images/determineanitemfiletype.png)

Il provider [OpenSearch](https://github.com/dewitt/opensearch) esegue i passaggi seguenti per eseguire il mapping di un elemento a un tipo di file:

-   Determinare se l'elemento deve essere trattato come un file o un collegamento Web.
-   Identificare l'estensione del nome file corretta da utilizzare.

Ad esempio, se l'elemento ha un URL di collegamento che usa un percorso di file system (ad esempio `file:///\\server\share\etc\item.ext` ), il provider [OpenSearch](https://github.com/dewitt/opensearch) considera il collegamento come un file e determina il tipo in base all'estensione del nome file usata nel percorso (. ext in questo esempio).

Se l'elemento usa lo chassis RSS standard o **MediaRSS media: content** , il provider [OpenSearch](https://github.com/dewitt/opensearch) presuppone che l'elemento sia un file e identifichi l'estensione del nome file come indicato di seguito:

-   Se è stato eseguito il mapping della proprietà della shell di Windows [System. FileExtension](../properties/props-system-fileextension.md) per l'elemento, il provider usa tale estensione di file.
-   Se non è stato eseguito il mapping della proprietà della shell di Windows [System. FileExtension](../properties/props-system-fileextension.md) , il provider utilizza l'attributo **Type** specificato nell'enclosure o nell'elemento Content. Questo elemento deve contenere una `MIMEType` stringa, ad esempio `"image/jpeg"` . Se `MIMEType` è associato a un'estensione di file registrata nel computer client, l'elemento viene considerato come un file di quel tipo. Se `MIMEType` non è associato a un'estensione di file registrata nel computer client, l'elemento viene considerato come un tipo di collegamento Web. Il provider [OpenSearch](https://github.com/dewitt/opensearch) non tenta di analizzare l'attributo **URL** per individuare l'estensione del nome file.
-   Se `MIMEType` è associato a un'estensione di file registrata nel computer client, il provider determina se l'estensione del nome file è un tipo di file Web noto (htm, HTML, ASP, aspx, php, SWF, STM). In tal caso, il tipo di file viene considerato come un tipo di collegamento Web; in caso contrario, viene considerato come un tipo di file. Ad esempio, se l' `MIMEType "text/html"` oggetto è associato all'estensione del nome di file htm, tale elemento viene considerato come un collegamento Web anziché come un tipo di file htm.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Evitare potenziali barriere per l'abilitazione di un archivio dati

Alcuni archivi dati non forniscono un servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch), ma possono comunque essere connessi alla ricerca federata di Windows. Tali archivi dati includono:

-   Indici remoti con metodi di autenticazione non supportati nella ricerca federata di Windows 7.

    Gli esempi includono l'autenticazione basata su moduli e altri metodi di autenticazione personalizzati.

-   Se un archivio pubblico di valore elevato ha API Web pubbliche, chiunque può scrivere un altro servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch)e chiama tali API in background.

    Gli esempi includono la libreria del Congresso e i database di ricerca medica.

-   Gli archivi dati aziendali o gli indici proprietari e gli archivi di gestione del contenuto legacy, per i quali potrebbe essere Impossibile implementare un front-end.

Tuttavia, esistono alternative che possono evitare barriere per l'abilitazione di un archivio dati. Di seguito sono riportate alcune alternative:

**Per scrivere un servizio Web di tipo intermedio quando non è possibile modificare il servizio Web per l'origine dati esistente o il servizio Web fornisce un'API personalizzata:**

1.  Scrivere un servizio Web di tipo intermedio che può accettare una query di Windows 7.
2.  Connettersi all'origine dati e recuperare i risultati della query.
3.  Riformattare i risultati in formato RSS o Atom.
4.  Restituisce i risultati al client Windows 7.
5.  Si noti che per Enterprise Data Services e molti servizi dati Internet, potrebbe essere necessario passare le credenziali utente tramite per conto del servizio Web per eseguire il taglio dei risultati in base alle autorizzazioni dell'utente.

**Per usare un motore di ricerca esistente quando non è possibile abilitare un archivio dati pubblico:**

1.  Usare un motore di ricerca pubblico che supporta già [OpenSearch](https://github.com/dewitt/opensearch) con RSS. A tale scopo, è possibile fornire agli utenti un file con estensione osdx che dispone di un modello di URL che limita i risultati solo a quelli per il dominio specifico.
2.  Vedere l'esempio seguente di una descrizione di [OpenSearch](https://github.com/dewitt/opensearch) per la ricerca solo nel contenuto della Guida per Windows tramite una query su Live.com.

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

    

**Per utilizzare un server di indicizzazione esistente che supporta OpenSearch quando non è possibile abilitare gli archivi dati aziendali o gli indici proprietari:**

1.  Consente di selezionare un server di indicizzazione esistente che supporta [OpenSearch](https://github.com/dewitt/opensearch) per indicizzare il contenuto, ad esempio il server di ricerca di SharePoint.
2.  Creare un file con estensione osdx che limiti i risultati dall'indice di SharePoint solo a quelli del server usando la relativa sintassi delle parole chiave nel modello di URL.

**Per scrivere un archivio dati lato client se una soluzione solo sul lato server non funziona:**

1.  Scrivere un'origine dati [OpenSearch](https://github.com/dewitt/opensearch) sul lato client che risiede tra il provider [OpenSearch](https://github.com/dewitt/opensearch) Windows e l'origine dati esterna.
2.  Usare l'API dell' [interfaccia IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) nel Windows SDK per creare un file con estensione searchconnector-ms configurato in modo appropriato tramite cui Esplora risorse può chiamare l'implementazione con i parametri di query. L'implementazione può quindi restituire i risultati formattati in formato RSS o Atom. Questa operazione consente all'implementazione di fornire un'interfaccia utente personalizzata per l'autenticazione e di connettersi all'origine dati usando l'API proprietaria.

> [!Note]  
> Se si apre un file con estensione osdx, viene creato un file con estensione searchconnector-ms (connettore di ricerca) nella directory% UserProfile%/Searches e viene inserito un collegamento nella directory% UserProfile%/Links.

 

## <a name="additional-resources"></a>Risorse aggiuntive

Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introduzione con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in ricerca federata di Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Procedure consigliate seguenti in ricerca federata di Windows](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca nella ricerca federata di Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
