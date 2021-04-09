---
description: Viene descritto come creare un file di descrizione OpenSearch (con estensione osdx) per connettere archivi dati esterni al client Windows tramite il protocollo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966536"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows

Viene descritto come creare un file di descrizione OpenSearch (con estensione osdx) per connettere archivi dati esterni al client Windows tramite il protocollo [OpenSearch](https://github.com/dewitt/opensearch) . La ricerca federata consente agli utenti di eseguire ricerche in un archivio dati remoto e di visualizzare i risultati da Esplora risorse.

In questo argomento sono incluse le sezioni seguenti:

-   [File di descrizione OpenSearch](#opensearch-description-file)
    -   [Minima elementi figlio obbligatori](#mininum-required-child-elements)
-   [Elementi standard in ricerca federata di Windows](#standard-elements-in-windows-federated-search)
    -   [Nome breve](#shortname)
    -   [Descrizione](#description)
    -   [Modello di URL per i risultati RSS/Atom](#url-template-for-rssatom-results)
    -   [Modello di URL per i risultati Web](#url-template-for-web-results)
    -   [Parametri del modello URL](#url-template-parameters)
    -   [Risultati di paging](#paged-results)
    -   [Paging mediante l'indice dell'elemento](#paging-using-the-item-index)
    -   [Paging tramite l'indice della pagina](#paging-using-the-page-index)
    -   [Dimensioni pagina](#page-size)
-   [Elementi estesi in ricerca federata di Windows](#extended-elements-in-windows-federated-search)
    -   [Numero massimo di risultati](#maximum-result-count)
    -   [Mapping di proprietà](#property-mapping)
-   [Anteprime](#previews)
-   [Voce di menu Apri percorso file](#open-file-location-menu-item)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="opensearch-description-file"></a>File di descrizione OpenSearch

Un file di descrizione OpenSearch (. osdx) per la ricerca federata di Windows deve rispettare le regole seguenti:

-   Essere un documento OpenSearch Description valido, come definito dalla specifica [OpenSearch](https://github.com/dewitt/opensearch) 1,1.
-   Fornire un modello di URL con un tipo di formato RSS o Atom.
-   Utilizzare l'estensione del nome di file. osdx o associarla all'estensione di file osdx durante il download dal Web. Ad esempio, non è necessario che un server usi. osdx. Un server può restituire il file con qualsiasi estensione di file, ad esempio. XML, e considerato come se fosse un file. osdx se usa il tipo MIME corretto per i documenti di descrizione OpenSearch (file con estensione osdx).
-   Fornire un valore di elemento **ShortName** (scelta consigliata).

### <a name="mininum-required-child-elements"></a>Minima elementi figlio obbligatori

Il file osdx di esempio seguente è costituito da **ShortName** e `Url` Elements, che sono gli elementi figlio minimi richiesti.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Elementi standard in ricerca federata di Windows

Oltre agli elementi figlio minimi, la ricerca federata supporta i seguenti elementi standard.

### <a name="shortname"></a>Nome breve

Windows usa il valore dell'elemento **ShortName** per denominare il file. searchconnector-ms (connettore di ricerca) che viene creato quando l'utente apre il file. osdx. Windows garantisce che il nome file generato usi solo i caratteri consentiti nei nomi file di Windows. Se non viene specificato alcun valore **ShortName** , il file. searchconnector-ms tenta di usare invece il nome file del file con estensione osdx.

Il codice seguente illustra come usare l'elemento **ShortName** in un file con estensione osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Descrizione

Windows utilizza il valore dell'elemento **Description** per popolare la descrizione del file visualizzata nel riquadro dei dettagli di Esplora risorse quando un utente seleziona un file con estensione searchconnector-ms.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Modello di URL per i risultati RSS/Atom

Il file. osdx deve includere un elemento del **formato dell'URL** e un attributo di **modello** (un modello di URL) che restituisce i risultati in formato RSS o Atom. L'attributo Format deve essere impostato su `application/rss+xml` per i risultati in formato RSS o `application/atom+xml` per i risultati in formato Atom, come illustrato nel codice seguente.

> [!Note]  
> L'elemento **formato URL** e l'attributo **modello** sono comunemente noti come modello di URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Modello di URL per i risultati Web

Se è presente una versione dei risultati della ricerca che può essere visualizzata in un Web browser, è necessario specificare un **URL Format =** `text/html` Element e **template** Attribute, come illustrato nel codice seguente.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Se si specifica un elemento **URL Format = "text/html"** e un attributo **template** , viene visualizzato un pulsante nella barra dei comandi di Esplora risorse, come illustrato nello screenshot seguente, che consente all'utente di aprire un Web browser per visualizzare i risultati della ricerca quando l'utente esegue una query.

![screenshot che mostra il pulsante di ricerca Web.](images/websearchroll-overcommandbarbutton.png)

Il rollup della query all'interfaccia utente Web dell'archivio dati è importante in alcuni scenari. Ad esempio, è possibile che un utente desideri visualizzare più di 100 risultati (il numero predefinito di elementi richiesti dal provider OpenSearch). In tal caso, è possibile che l'utente desideri utilizzare anche le funzionalità di ricerca disponibili solo sul sito Web dell'archivio dati, ad esempio l'esecuzione di una nuova query con un ordinamento diverso, oppure la trasformazione e il filtraggio della query con i metadati correlati.

### <a name="url-template-parameters&quot;></a>Parametri del modello URL

Il provider OpenSearch esegue sempre le azioni seguenti:

1.  Usa il modello di URL per inviare la richiesta al servizio Web.
2.  Tenta di sostituire i token trovati nel modello di URL prima di inviare la richiesta al servizio Web, come indicato di seguito:
    -   Sostituisce i token OpenSearch standard elencati nella tabella seguente.
    -   Rimuove tutti i token non elencati nella tabella seguente.



| Token supportato  | Modalità di utilizzo del provider OpenSearch                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| searchTerms    | Sostituito con i termini di ricerca che l'utente digita nella casella di input di ricerca di Esplora risorse.<br/>                                         |
| startIndex     | Utilizzato quando si recuperano i risultati in &quot;Pages&quot;.<br/> Sostituito con l'indice per il primo elemento di risultato da restituire.<br/>                        |
| Startpage      | Utilizzato quando si recuperano i risultati in &quot;Pages&quot;.<br/> Sostituito con il numero di pagina del set di risultati della ricerca da restituire.<br/>               |
| conteggio          | Utilizzato quando si recuperano i risultati in &quot;Pages&quot;.<br/> Sostituito con il numero di risultati della ricerca per ogni pagina richiesta da Esplora risorse.<br/> |
| linguaggio       | Sostituito con una stringa che indica il linguaggio della query inviata.<br/>                                                          |
| InputEncoding  | Sostituito con una stringa (ad esempio &quot;UTF-16") che indica la codifica dei caratteri della query inviata.<br/>                                |
| OutputEncoding | Sostituito con una stringa (ad esempio "UTF-16") che indica la codifica dei caratteri desiderata per la risposta del servizio Web.<br/>       |



 

### <a name="paged-results"></a>Risultati di paging

È possibile che si desideri limitare il numero di risultati restituiti per ogni richiesta. È possibile scegliere di restituire una "pagina" di risultati alla volta oppure di fare in modo che il provider OpenSearch ottenga ulteriori pagine di risultati in base al numero di elemento o al numero di pagina. Se, ad esempio, si inviano venti risultati per pagina, la prima pagina inviata inizia in corrispondenza dell'indice dell'elemento 1 e della pagina 1; la seconda pagina inviata inizia in corrispondenza dell'indice degli elementi 21 e della pagina 2. È possibile definire il modo in cui si vuole che il provider OpenSearch richieda elementi usando il `{startItem}` `{startPage}` token o nel modello di URL.

### <a name="paging-using-the-item-index"></a>Paging mediante l'indice dell'elemento

Un indice di elemento identifica il primo elemento di risultato in una pagina di risultati. Se si vuole che i client inviino richieste usando un indice di elemento, è possibile usare il `{startIndex}` token nell'attributo del **modello** di elemento **URL** , come illustrato nel codice seguente.


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



Il provider [OpenSearch](https://github.com/dewitt/opensearch) sostituisce quindi il token nell'URL con un valore di indice iniziale. La prima richiesta inizia con il primo elemento, come illustrato nell'esempio seguente:


```
https://example.com/rss.php?query=frogs&start=1
```



Il provider OpenSearch può ottenere elementi aggiuntivi modificando il `{startIndex}` valore del parametro ed eseguendo una nuova richiesta. Il provider ripete questo processo fino a ottenere risultati sufficienti per soddisfare il limite o raggiunge la fine dei risultati. Il provider OpenSearch esamina il numero di elementi restituiti dal servizio Web nella prima pagina di risultati e imposta la dimensione di pagina prevista su tale numero. USA tale numero per incrementare il `{startIndex}` valore delle richieste successive. Se, ad esempio, il servizio Web restituisce 20 risultati nella prima richiesta, il provider imposta la dimensione di pagina prevista su 20. Per la richiesta successiva, il provider sostituisce `{startIndex}` con il valore 21 per ottenere i successivi 20 elementi.

> [!Note]  
> Se una pagina di risultati restituiti dal servizio Web dispone di un numero inferiore di elementi rispetto alle dimensioni di pagina previste, il provider OpenSearch presuppone che abbia ricevuto l'ultima pagina di risultati e interrompa l'esecuzione delle richieste.

 

### <a name="paging-using-the-page-index"></a>Paging tramite l'indice della pagina

Un indice di pagina identifica la pagina di risultati specificata. Se si vuole che i client inviino richieste usando un numero di pagina, è possibile usare il `{startPage}` token nell'attributo del **modello** di elemento **formato URL** per indicare che, come illustrato nell'esempio seguente:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



Il provider OpenSearch sostituisce quindi il token nell'URL con un parametro di numero di pagina. La prima richiesta inizia con la prima pagina, come illustrato nell'esempio seguente:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Se una pagina di risultati restituiti dal servizio Web dispone di un numero inferiore di elementi rispetto alle dimensioni di pagina previste, il provider OpenSearch presuppone che abbia ricevuto l'ultima pagina di risultati e interrompa l'esecuzione delle richieste.

 

### <a name="page-size"></a>Dimensioni pagina

È possibile configurare il servizio Web per consentire a una richiesta di specificare le dimensioni delle pagine usando un parametro nell'URL. È necessario specificare una richiesta nel file con estensione osdx usando il `{count}` token, come indicato di seguito:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



Il provider [OpenSearch](https://github.com/dewitt/opensearch) può quindi impostare le dimensioni di pagina desiderate, in numero di risultati per pagina, come illustrato nell'esempio seguente:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Per impostazione predefinita, il provider OpenSearch esegue richieste usando una dimensione di pagina di 50. Se si desiderano dimensioni di pagina diverse, non fornire un `{count}` token e inserire invece il numero desiderato direttamente nell'elemento del **modello URL** .

Il provider OpenSearch determina le dimensioni della pagina in base al numero di risultati restituiti alla prima richiesta. Se la prima pagina di risultati ricevuta ha un numero di elementi inferiore al numero richiesto, il provider Reimposta le dimensioni di pagina per tutte le richieste di pagina successive. Se le richieste di pagina successive restituiscono un numero di elementi inferiore a quello richiesto, il provider OpenSearch presuppone che abbia raggiunto la fine dei risultati.

## <a name="extended-elements-in-windows-federated-search"></a>Elementi estesi in ricerca federata di Windows

Oltre agli elementi standard, la ricerca federata supporta gli elementi estesi seguenti: **MaximumResultCount** e **ResultsProcessing**.

Poiché questi elementi figlio estesi non sono supportati nella specifica [OpenSearch](https://github.com/dewitt/opensearch) v 1.1, è necessario aggiungerli usando lo spazio dei nomi seguente:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Numero massimo di risultati

Per impostazione predefinita, i connettori di ricerca sono limitati a 100 risultati per query utente. Questo limite può essere personalizzato includendo l'elemento **MaximumResultCount** all'interno del file OSD, come illustrato nell'esempio seguente:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



Nell'esempio precedente viene dichiarato il prefisso dello spazio dei nomi `ms-ose` nell'elemento **OpenSearchDescription** di primo livello, che viene quindi utilizzato come prefisso nel nome dell'elemento. Questa dichiarazione è obbligatoria perché **MaximumResultCount** non è supportato nella specifica [OpenSearch](https://github.com/dewitt/opensearch) v 1.1.

### <a name="property-mapping"></a>Mapping di proprietà

Quando i risultati vengono restituiti dal servizio Web come feed RSS o Atom, il provider OpenSearch deve eseguire il mapping dei metadati degli elementi nei feed alle proprietà che possono essere utilizzate dalla shell di Windows. Lo screenshot seguente illustra il modo in cui il provider OpenSearch esegue il mapping di alcuni degli elementi RSS predefiniti.

![screenshot che mostra i mapping incorporati di proprietà da RSS a Windows Shell](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Mapping predefiniti

I mapping predefiniti degli elementi XML RSS alle proprietà di sistema della shell di Windows sono elencati nella tabella seguente. I percorsi XML sono relativi all'elemento Item. Il `"media:"` prefisso viene definito dallo spazio dei nomi dello [spazio dei nomi di Yahoo Search](https://www.rssboard.org/media-rss) .



| Percorso XML RSS                  | Proprietà della shell di Windows (nome canonico) |
|-------------------------------|-----------------------------------------|
| Collegamento                          | System. ItemUrl                          |
| Titolo                         | System. ItemName                         |
| Autore                        | System.Author                           |
| pubDate                       | System. DateModified                     |
| Descrizione                   | System. AutoSummary                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System. MIMEType                         |
| enclosure/@length             | System. size                             |
| enclosure/@url                | System. ContentUrl                       |
| supporto: Categoria                | System.Keywords                         |
| media:content/@fileSize       | System. size                             |
| media:content/@type           | System. MIMEType                         |
| media:content/@url            | System. ContentUrl                       |
| media:group/content/@fileSize | System. size                             |
| media:group/content/@type     | System. MIMEType                         |
| media:group/content/@url      | System. ContentUrl                       |
| media:thumbnail/@url          | System. ItemThumbnailUrl                 |



 

> [!Note]  
> Oltre ai mapping predefiniti degli elementi RSS o Atom standard, è possibile eseguire il mapping di altre proprietà di sistema della shell di Windows includendo elementi XML aggiuntivi nello spazio dei nomi Windows per ciascuna proprietà. È anche possibile eseguire il mapping di elementi da altri spazi dei nomi XML esistenti, ad esempio MediaRSS, iTunes e così via, aggiungendo un mapping personalizzato delle proprietà nel file. osdx.

 

### <a name="custom-property-mappings"></a>Mapping di proprietà personalizzate

È possibile personalizzare il mapping degli elementi dall'output RSS alle proprietà di sistema della shell di Windows specificando il mapping nel file con estensione osdx.

L'output RSS specifica:

-   Uno spazio dei nomi XML e
-   Per qualsiasi elemento figlio di un elemento, il nome di un elemento su cui eseguire il mapping.

Il file con estensione osdx identifica una proprietà della shell di Windows per ogni nome di elemento in uno spazio dei nomi. I mapping di proprietà definiti nel file con estensione osdx sostituiscono i mapping predefiniti, se esistenti, per le proprietà specificate.

Il diagramma seguente illustra come viene eseguito il mapping di un'estensione RSS alle proprietà di Windows (nome canonico).

![diagramma che mostra che la combinazione di spazio dei nomi XML e percorso XML produce il nome canonico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Risultati RSS di esempio e mapping di proprietà OSD

L'output RSS di esempio seguente identifica lo `https://example.com/schema/2009` spazio dei nomi XML con il prefisso "example". Questo prefisso deve essere visualizzato di nuovo prima dell'elemento di **posta elettronica** .


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



Nel file osdx di esempio seguente l'elemento di **posta elettronica** XML viene mappato alla proprietà della shell di Windows [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md).


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



Alcune proprietà non possono essere mappate perché i valori per esse sono sostituiti in un secondo momento o non sono modificabili. Non è ad esempio possibile eseguire il mapping di [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) o [System. ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) perché vengono calcolati dal valore dell'URL fornito negli elementi del collegamento o dell'enclosure.

### <a name="thumbnails"></a>Anteprime

Gli URL dell'immagine di anteprima possono essere forniti per qualsiasi elemento usando l'elemento **media: thumbnail URL = ""** . La risoluzione ideale è 150 x 150 pixel. Le anteprime più grandi supportate sono 256 x 256 pixel. Fornire immagini più grandi richiede una maggiore larghezza di banda senza alcun vantaggio aggiuntivo per l'utente.

### <a name="open-file-location-context-menu"></a>Apri il menu di scelta rapida percorso file

In Windows è disponibile un menu di scelta rapida denominato **Apri percorso file** per gli elementi dei risultati. Se l'utente seleziona un elemento da tale menu, viene aperto l'URL "padre" per l'elemento selezionato. Se l'URL è un URL Web, ad esempio `https://...` , il Web browser viene aperto e passa a tale URL. Il feed deve fornire un URL personalizzato per ogni elemento per assicurarsi che Windows apra un URL valido. Questa operazione può essere eseguita includendo l'URL all'interno di un elemento all'interno del codice XML dell'elemento, come illustrato nell'esempio seguente:


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



Se questa proprietà non è impostata in modo esplicito nel codice XML dell'elemento, il provider OpenSearch lo imposta sulla cartella padre dell'URL dell'elemento. Nell'esempio precedente il provider OpenSearch usa il valore del collegamento e imposta il valore della proprietà della shell di Windows [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) su `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personalizzare le visualizzazioni di Esplora risorse con elenchi di descrizioni delle proprietà

Alcuni layout di visualizzazione di Esplora risorse sono definiti da elenchi di descrizioni delle proprietà, o proplists. Un oggetto prop è un elenco delimitato da punti e virgola di proprietà, ad esempio `"prop:System.ItemName; System.Author"` , usato per controllare la modalità di visualizzazione dei risultati in Esplora risorse.

Le aree dell'interfaccia utente di Esplora risorse che possono essere personalizzate tramite proplists sono illustrate nella schermata seguente:

![screenshot che mostra le aree dell'interfaccia utente di Esplora risorse che possono essere personalizzate mediante proplists](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

A ogni area di Esplora risorse è associato un set di proplists, che vengono specificati come proprietà. È possibile specificare proplists personalizzati per i singoli elementi nei set di risultati o per tutti gli elementi di un set di risultati.



| Area dell'interfaccia utente da personalizzare               | Proprietà della shell di Windows che implementa la personalizzazione |
|------------------------------------|----------------------------------------------------------|
| Modalità di visualizzazione contenuto (durante la ricerca) | System. Propin. ContentViewModeForSearch                 |
| Modalità di visualizzazione contenuto (quando si Esplora)  | System. Propin. ContentViewModeForBrowse                 |
| Modalità visualizzazione affiancata                     | System. Propin. TileInfo                                 |
| Riquadro dei dettagli                       | System. Propin. PreviewDetails                           |
| Infotip (descrizione comando hover dell'elemento)     | System. Propin. infotip                                  |



 

 

**Per specificare un oggetto univoco per un singolo elemento:**

1.  Nell'output RSS aggiungere un elemento personalizzato che rappresenta l'oggetto di proprietà che si desidera personalizzare. Nell'esempio seguente viene impostato l'elenco per il riquadro Dettagli:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Per applicare una proprietà a ogni elemento nei risultati della ricerca senza modificare l'output RSS, specificare un oggetto prop all'interno di un elemento **MS-OSE: PropertyDefaultValues** nel file con estensione osdx, come illustrato nell'esempio seguente:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Layout della modalità di visualizzazione contenuto delle proprietà

L'elenco delle proprietà specificate in **System. propt. ContentViewModeForSearch** e **System. propName. ContentViewModeForBrowse** proplists determina ciò che viene visualizzato in modalità di visualizzazione contenuto. Per ulteriori informazioni sugli elenchi di proprietà, [vedere l'](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)elenco delle proprietà.

Le proprietà sono disposte in base ai numeri mostrati nel modello di layout seguente:

![screenshot che mostra il modello di layout predefinito nella visualizzazione contenuto](images/propertiesnumberslayoutpattern.png)

Se si usa l'elenco di proprietà seguente,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



Viene visualizzata la schermata seguente:

![screenshot che mostra il layout delle proprietà di esempio.](images/samplepropertylayout.png)

> [!Note]  
> Per una migliore leggibilità, è necessario etichettare le proprietà visualizzate nella colonna a destra.

 

### <a name="property-list-flags"></a>Flag elenco proprietà

Solo uno dei flag definiti nella documentazione di proplists si applica alla visualizzazione degli elementi nei layout della modalità di visualizzazione del contenuto: ` "~"` . Negli esempi precedenti, la visualizzazione Esplora risorse di Windows etichetta alcune proprietà, ad esempio `Tags: animals; zoo; lion` . Questo è il comportamento predefinito quando si specifica una proprietà nell'elenco. Ad esempio, l'oggetto di proprietà `"System.Author"` è visualizzato come `"Authors: value"` . Quando si vuole nascondere l'etichetta della proprietà, posizionare un oggetto `"~"` davanti al nome della proprietà. Se, ad esempio, la proprietà contiene `"~System.Size"` , la proprietà viene visualizzata come un solo valore, senza l'etichetta.

## <a name="previews"></a>Anteprime

Quando l'utente seleziona un elemento di risultato in Esplora risorse e il riquadro di anteprima è aperto, il contenuto dell'elemento viene visualizzato in anteprima.

Il contenuto da visualizzare nell'anteprima viene specificato da un URL, determinato nel modo seguente:

1.  Se la proprietà della shell di Windows **System. WebPreviewUrl** è impostata per l'elemento, usare tale URL.
    > [!Note]  
    > La proprietà deve essere fornita nel feed RSS usando lo spazio dei nomi della shell di Windows o il mapping esplicito nel file. osdx.

     

2.  In caso contrario, usare invece l'URL del collegamento.

Il diagramma di flusso seguente illustra questa logica.

![diagramma di flusso che illustra in che modo Esplora risorse seleziona l'URL da usare per le anteprime](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

È possibile usare un URL diverso per l'anteprima rispetto all'elemento stesso. Ciò significa che se si specificano URL diversi per l'URL del collegamento e l'enclosure oppure `media:content URL` , Esplora risorse utilizza l'URL del collegamento per le anteprime dell'elemento, ma utilizza l'altro URL per il rilevamento del tipo di file, l'apertura, il download e così via.

Modalità di determinazione dell'URL da utilizzare in Esplora risorse:

1.  Se si fornisce un mapping a [System. ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md), Esplora risorse usa tale URL
2.  Se non si specifica un mapping, Esplora risorse indica se gli URL del collegamento e dell'enclosure sono diversi. In tal caso, Esplora risorse utilizza l'URL del collegamento.
3.  Se gli URL sono uguali o se è presente solo un URL di collegamento, Esplora risorse analizza il collegamento per trovare il contenitore padre rimuovendo il nome del file dall'URL completo.
    > [!Note]  
    > Se si riconosce che l'analisi degli URL comporterebbe collegamenti non recapitabili per il servizio, è necessario fornire un mapping esplicito per la proprietà.

     

## <a name="open-file-location-menu-item"></a>Voce di menu Apri percorso file

Quando si fa clic con il pulsante destro del mouse su un elemento, viene visualizzato il comando di menu **Apri percorso file** . Questo comando porta l'utente al contenitore per la posizione o dell'elemento. Ad esempio, in una ricerca di SharePoint, la selezione di questa opzione per un file in una raccolta documenti apre la radice della raccolta documenti nel Web browser.

Quando un utente fa clic su **Apri percorso file**, Esplora risorse tenta di trovare un contenitore padre, usando la logica mostrata nel diagramma di flusso seguente:

![diagramma di flusso che illustra come Windows Explorer identifica un contenitore padre](images/howwindowsexploreridentifiesaparentcontainer.png)

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

[Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Procedure consigliate seguenti in ricerca federata di Windows](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca nella ricerca federata di Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
