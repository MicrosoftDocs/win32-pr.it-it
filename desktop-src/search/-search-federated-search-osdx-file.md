---
description: Viene descritto come creare un file OpenSearch Description (con estensione osdx) per connettere archivi dati esterni al client Windows tramite il protocollo OpenSearch.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Creazione di un OpenSearch di descrizione Windows ricerca federata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f58b29a860c7d53583b7fd17ddd942bb21b08d649ea7e54d5b2278be2f8d4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456861"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Creazione di un OpenSearch di descrizione Windows ricerca federata

Viene descritto come creare un file OpenSearch description (con estensione osdx) per connettere archivi dati esterni al client Windows tramite il [protocollo OpenSearch.](https://github.com/dewitt/opensearch) La ricerca federata consente agli utenti di eseguire ricerche in un archivio dati remoto e visualizzare i risultati dall'Windows Explorer.

In questo argomento sono incluse le sezioni seguenti:

-   [OpenSearch File di descrizione](#opensearch-description-file)
    -   [Mininum Elementi figlio obbligatori](#mininum-required-child-elements)
-   [Elementi standard nella Windows federata](#standard-elements-in-windows-federated-search)
    -   [Nome breve](#shortname)
    -   [Descrizione](#description)
    -   [Modello DI URL per i risultati RSS/Atom](#url-template-for-rssatom-results)
    -   [Modello DI URL per i risultati Web](#url-template-for-web-results)
    -   [Parametri del modello URL](#url-template-parameters)
    -   [Risultati di cui è stato fatto il paged](#paged-results)
    -   [Paging con l'indice degli elementi](#paging-using-the-item-index)
    -   [Paging con l'indice di pagina](#paging-using-the-page-index)
    -   [Dimensioni pagina](#page-size)
-   [Elementi estesi nella Windows federata](#extended-elements-in-windows-federated-search)
    -   [Numero massimo di risultati](#maximum-result-count)
    -   [Mapping di proprietà](#property-mapping)
-   [Anteprime](#previews)
-   [Voce di menu Apri percorso file](#open-file-location-menu-item)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="opensearch-description-file"></a>OpenSearch File di descrizione

Un file OpenSearch description (con estensione osdx) per Windows ricerca federata deve rispettare le regole seguenti:

-   Essere un documento OpenSearch description valido, come definito dalla specifica [OpenSearch](https://github.com/dewitt/opensearch) 1.1.
-   Specificare un modello di URL con un tipo di formato RSS o Atom.
-   Usare l'estensione OSDX o essere associato all'estensione OSDX durante il download dal Web. Ad esempio, non è necessario un server per usare .osdx. Un server può restituire il file con qualsiasi estensione di file, ad esempio .xml, e considerato come se fosse un file con estensione osdx se usa il tipo MIME corretto per i documenti di descrizione OpenSearch (file con estensione osdx).
-   Specificare un **valore dell'elemento ShortName** (scelta consigliata).

### <a name="mininum-required-child-elements"></a>Mininum Elementi figlio obbligatori

Il file OSDX di esempio seguente è costituito da **ShortName** e da elementi , che `Url` sono gli elementi figlio minimi necessari.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Elementi standard nella Windows federata

Oltre agli elementi figlio minimi, la ricerca federata supporta gli elementi standard seguenti.

### <a name="shortname"></a>Nome breve

Windows il valore **dell'elemento ShortName** per assegnare un nome al file con estensione searchconnector-ms (connettore di ricerca) creato quando l'utente apre il file con estensione osdx. Windows che il nome file generato usi solo i caratteri consentiti nei Windows file. Se non viene specificato alcun valore **ShortName,** il file con estensione searchconnector-ms tenta invece di usare il nome file del file con estensione osdx.

Il codice seguente illustra come usare **l'elemento ShortName** in un file con estensione osdx.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>Descrizione

Windows il valore **dell'elemento Description** per popolare la descrizione del file visualizzata nel riquadro dei dettagli di Windows Explorer quando un utente seleziona un file con estensione searchconnector-ms.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>Modello DI URL per i risultati RSS/Atom

Il file con estensione osdx deve  includere un elemento di formato **URL** e un attributo modello (un modello URL) che restituisce i risultati in formato RSS o Atom. L'attributo format deve essere impostato su per i risultati in formato RSS o per i risultati in formato `application/rss+xml` `application/atom+xml` Atom, come illustrato nel codice seguente.

> [!Note]  
> **L'elemento di formato URL** e **l'attributo** del modello sono comunemente noti come modello di URL.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>Modello DI URL per i risultati Web

Se è presente una versione dei risultati della ricerca che può essere visualizzata in un Web browser, è necessario specificare un elemento **Url format=** e un attributo modello, come illustrato nel `text/html` codice seguente. 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Se si specifica un elemento **url format="text/html"** e un attributo modello, nella barra dei comandi di Esplora Windows viene visualizzato un pulsante, come illustrato nella schermata seguente, che consente all'utente di aprire un Web browser per visualizzare i risultati della ricerca quando l'utente esegue una query. 

![Screenshot che mostra il pulsante di roll over della ricerca Web.](images/websearchroll-overcommandbarbutton.png)

Il roll-over della query nell'interfaccia utente Web dell'archivio dati è importante in alcuni scenari. Ad esempio, un utente potrebbe voler visualizzare più di 100 risultati (il numero predefinito di elementi OpenSearch richieste del provider). In tal caso, l'utente potrebbe anche voler usare funzionalità di ricerca disponibili solo nel sito Web dell'archivio dati, ad esempio la nuova query con un ordinamento diverso o il pivot e il filtro della query con metadati correlati.

### <a name="url-template-parameters&quot;></a>Parametri del modello URL

Il provider OpenSearch esegue sempre le azioni seguenti:

1.  Usa il modello di URL per inviare la richiesta al servizio Web.
2.  Tenta di sostituire i token trovati nel modello di URL prima di inviare la richiesta al servizio Web, come indicato di seguito:
    -   Sostituisce i token OpenSearch standard elencati nella tabella seguente.
    -   Rimuove tutti i token non elencati nella tabella seguente.



| Token supportato  | Come viene usato dal provider OpenSearch                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Sostituiti con i termini di ricerca che l'utente digitare nella casella Windows di input di ricerca di Esplora risorse.<br/>                                         |
| {startIndex}     | Usato per ottenere i risultati in &quot;pages&quot;.<br/> Sostituito con l'indice per il primo elemento del risultato da restituire.<br/>                        |
| {startPage}      | Usato per ottenere i risultati in &quot;pages&quot;.<br/> Sostituito con il numero di pagina del set di risultati della ricerca da restituire.<br/>               |
| {count}          | Usato per ottenere i risultati in &quot;pages&quot;.<br/> Sostituito con il numero di risultati della ricerca per pagina che Windows Explorer.<br/> |
| {language}       | Sostituito con una stringa che indica la lingua della query inviata.<br/>                                                          |
| {inputEncoding}  | Sostituito con una stringa (ad esempio &quot;UTF-16") che indica la codifica dei caratteri della query inviata.<br/>                                |
| {outputEncoding} | Sostituito con una stringa (ad esempio "UTF-16") che indica la codifica dei caratteri desiderata per la risposta dal servizio Web.<br/>       |



 

### <a name="paged-results"></a>Risultati di cui è stato fatto il paged

È possibile limitare il numero di risultati restituiti per ogni richiesta. È possibile scegliere di restituire una "pagina" di risultati alla volta o fare in modo che il provider OpenSearch otterrà pagine aggiuntive di risultati in base al numero di elemento o di pagina. Ad esempio, se si inviano venti risultati per pagina, la prima pagina che si invia inizia in corrispondenza dell'indice dell'elemento 1 e alla pagina 1; la seconda pagina che si invia inizia in corrispondenza dell'indice dell'elemento 21 e della pagina 2. È possibile definire il modo in cui il provider OpenSearch richiedere gli elementi usando o il `{startItem}` token nel modello di `{startPage}` URL.

### <a name="paging-using-the-item-index"></a>Paging con l'indice degli elementi

Un indice di elemento identifica il primo elemento del risultato in una pagina di risultati. Se si vuole che i client inviino richieste usando un indice di elemento, è possibile usare il token nell'attributo del modello di elemento `{startIndex}` **Url,** come illustrato nel codice seguente. 


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



Il [OpenSearch](https://github.com/dewitt/opensearch) quindi sostituisce il token nell'URL con un valore di indice iniziale. La prima richiesta inizia con il primo elemento, come illustrato nell'esempio seguente:


```
https://example.com/rss.php?query=frogs&start=1
```



Il provider OpenSearch può ottenere elementi aggiuntivi modificando il valore del parametro ed `{startIndex}` emettendo una nuova richiesta. Il provider ripete questo processo finché non ottiene risultati sufficienti per soddisfare il limite o raggiunge la fine dei risultati. Il OpenSearch provider esamina il numero di elementi restituiti dal servizio Web nella prima pagina di risultati e imposta le dimensioni della pagina previste su tale numero. Usa tale numero per incrementare il `{startIndex}` valore per le richieste successive. Ad esempio, se il servizio Web restituisce 20 risultati nella prima richiesta, il provider imposta le dimensioni della pagina previste su 20. Per la richiesta successiva, il provider sostituisce `{startIndex}` con il valore 21 per ottenere i 20 elementi successivi.

> [!Note]  
> Se una pagina di risultati restituita dal servizio Web ha meno elementi rispetto alle dimensioni di pagina previste, il provider OpenSearch presuppone che abbia ricevuto l'ultima pagina di risultati e arresti l'esecuzione di richieste.

 

### <a name="paging-using-the-page-index"></a>Paging con l'indice di pagina

Un indice di pagina identifica la pagina di risultati specificata. Se si vuole che i client inviino richieste usando un numero di pagina, è possibile usare il token nell'attributo del modello dell'elemento di formato URL per indicar questo, come illustrato `{startPage}` nell'esempio  seguente: 


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



Il provider OpenSearch sostituisce quindi il token nell'URL con un parametro del numero di pagina. La prima richiesta inizia con la prima pagina, come illustrato nell'esempio seguente:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Se una pagina di risultati restituita dal servizio Web contiene meno elementi rispetto alle dimensioni di pagina previste, il provider OpenSearch presuppone che abbia ricevuto l'ultima pagina di risultati e arresti le richieste.

 

### <a name="page-size"></a>Dimensioni pagina

È possibile configurare il servizio Web per consentire a una richiesta di specificare le dimensioni delle pagine usando un parametro nell'URL. È necessario specificare una richiesta nel file con estensione osdx usando il `{count}` token , come indicato di seguito:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



Il [provider OpenSearch](https://github.com/dewitt/opensearch) può quindi impostare le dimensioni della pagina desiderate, in numero di risultati per pagina, come illustrato nell'esempio seguente:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Per impostazione predefinita, OpenSearch provider effettua richieste usando una dimensione di pagina di 50. Se si desidera una dimensione di pagina diversa, non fornire un token e inserire invece il numero desiderato direttamente `{count}` **nell'elemento del modello** URL.

Il provider OpenSearch determina le dimensioni della pagina in base al numero di risultati restituiti alla prima richiesta. Se la prima pagina di risultati ricevuta contiene meno elementi rispetto al conteggio richiesto, il provider reimposta le dimensioni della pagina per le richieste di pagina successive. Se le richieste di pagina successive restituiscono un numero di elementi inferiore a quello richiesto, il provider OpenSearch presuppone che abbia raggiunto la fine dei risultati.

## <a name="extended-elements-in-windows-federated-search"></a>Elementi estesi nella Windows federata

Oltre agli elementi standard, la ricerca federata supporta gli elementi estesi **seguenti: MaximumResultCount** e **ResultsProcessing.**

Poiché questi elementi figlio estesi non sono supportati nella [specifica OpenSearch](https://github.com/dewitt/opensearch) 1.1, devono essere aggiunti usando lo spazio dei nomi seguente:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Numero massimo di risultati

Per impostazione predefinita, i connettori di ricerca sono limitati a 100 risultati per ogni query utente. Questo limite può essere personalizzato includendo **l'elemento MaximumResultCount** all'interno del file OSD, come illustrato nell'esempio seguente:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



L'esempio precedente dichiara il prefisso dello spazio dei nomi nell'elemento OpenSearchDescription di primo livello e quindi lo usa come prefisso `ms-ose` nel nome  dell'elemento. Questa dichiarazione è obbligatoria perché **MaximumResultCount** non è supportato nella [specifica OpenSearch](https://github.com/dewitt/opensearch) versione 1.1.

### <a name="property-mapping"></a>Mapping di proprietà

Quando i risultati vengono restituiti dal servizio Web come feed RSS o Atom, il provider OpenSearch deve eseguire il mapping dei metadati degli elementi nei feed alle proprietà che possono essere usate da Windows Shell. Lo screenshot seguente illustra come il provider OpenSearch esegue il mapping di alcuni degli elementi RSS predefiniti.

![Screenshot che mostra i mapping delle proprietà rss-to-windows-shell predefiniti](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Mapping predefiniti

I mapping predefiniti degli elementi XML RSS alle Windows di sistema della shell sono elencati nella tabella seguente. I percorsi XML sono relativi all'elemento item. Il `"media:"` prefisso è definito dallo spazio dei nomi Yahoo [Search.](https://www.rssboard.org/media-rss)



| Percorso XML RSS                  | Windows Proprietà shell (nome canonico) |
|-------------------------------|-----------------------------------------|
| Collegamento                          | System.ItemUrl                          |
| Title                         | System.ItemName                         |
| Autore                        | System.Author                           |
| pubDate                       | System.DateModified                     |
| Descrizione                   | System.AutoSummary                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System.MIMEType                         |
| enclosure/@length             | System.Size                             |
| enclosure/@url                | System.ContentUrl                       |
| media:category                | System.Keywords                         |
| media:content/@fileSize       | System.Size                             |
| media:content/@type           | System.MIMEType                         |
| media:content/@url            | System.ContentUrl                       |
| media:group/content/@fileSize | System.Size                             |
| media:group/content/@type     | System.MIMEType                         |
| media:group/content/@url      | System.ContentUrl                       |
| media:thumbnail/@url          | System.ItemThumbnailUrl                 |



 

> [!Note]  
> Oltre ai mapping predefiniti degli elementi RSS o Atom standard, è possibile eseguire il mapping di altre proprietà di sistema della shell Windows includendo elementi XML aggiuntivi nello spazio dei nomi Windows per ognuna delle proprietà. È anche possibile eseguire il mapping di elementi da altri spazi dei nomi XML esistenti, ad esempio MediaRSS, iTunes e così via, aggiungendo il mapping di proprietà personalizzate nel file con estensione osdx.

 

### <a name="custom-property-mappings"></a>Mapping di proprietà personalizzate

È possibile personalizzare il mapping degli elementi dall'output RSS Windows proprietà di sistema della shell specificando il mapping nel file con estensione osdx.

L'output RSS specifica:

-   Uno spazio dei nomi XML e
-   Per qualsiasi elemento figlio di un elemento, nome di elemento su cui eseguire il mapping.

Il file con estensione osdx identifica una Windows shell per ogni nome di elemento in uno spazio dei nomi. I mapping delle proprietà definiti nel file con estensione osdx eseguono l'override dei mapping predefiniti, se esistenti, per le proprietà specificate.

Il diagramma seguente illustra il mapping di un'estensione RSS Windows proprietà (nome canonico).

![Diagramma che mostra che la combinazione dello spazio dei nomi xml e del percorso xml produce il nome canonico](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Risultati RSS di esempio e mapping delle proprietà OSD

L'output RSS di esempio seguente `https://example.com/schema/2009` identifica come spazio dei nomi XML con il prefisso "example". Questo prefisso deve essere visualizzato di nuovo prima **dell'elemento email.**


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



Nel file OSDX di esempio seguente l'elemento di posta elettronica **XML** esegue il mapping alla proprietà Windows Shell [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md).


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



Alcune proprietà non possono essere mappate perché i relativi valori vengono sottoposti a override in un secondo momento o non sono modificabili. Non è ad esempio possibile eseguire il mapping di [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) o [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) perché vengono calcolati in base al valore dell'URL specificato negli elementi link o enclosure.

### <a name="thumbnails"></a>Anteprime

Gli URL delle immagini di anteprima possono essere forniti per qualsiasi elemento usando **l'elemento media:thumbnail url="".** La risoluzione ideale è 150 x 150 pixel. Le anteprime più grandi supportate sono 256 x 256 pixel. Fornire immagini di dimensioni maggiori richiede più larghezza di banda senza alcun vantaggio aggiuntivo per l'utente.

### <a name="open-file-location-context-menu"></a>Menu di scelta rapida Apri percorso file

Windows un menu di scelta rapida denominato **Apri percorso file per** gli elementi dei risultati. Se l'utente seleziona un elemento da tale menu, viene aperto l'URL "padre" per l'elemento selezionato. Se l'URL è un URL Web, ad esempio , il Web browser viene `https://...` aperto e si passa a tale URL. Il feed deve fornire un URL personalizzato per ogni elemento per assicurarsi che Windows apra un URL valido. Questa operazione può essere eseguita includendo l'URL all'interno di un elemento all'interno del codice XML dell'elemento, come illustrato nell'esempio seguente:


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



Se questa proprietà non è impostata in modo esplicito nel codice XML dell'elemento, il provider OpenSearch la imposta sulla cartella padre dell'URL dell'elemento. Nell'esempio precedente il provider OpenSearch usa il valore del collegamento e imposta il valore della proprietà [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell su `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Personalizzare le Windows Explorer con elenchi di descrizioni delle proprietà

Alcuni Windows layout di visualizzazione di Explorer sono definiti da elenchi di descrizione delle proprietà o proplist. Un proplist è un elenco di proprietà delimitato da punto e virgola, ad esempio , usato per controllare la modalità di visualizzazione dei `"prop:System.ItemName; System.Author"` risultati in Windows Explorer.

Le aree dell'interfaccia utente Windows Explorer che possono essere personalizzate usando proplist sono illustrate nello screenshot seguente:

![Screenshot che mostra le aree dell'interfaccia utente di Esplora risorse che possono essere personalizzate tramite proplist](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

A ogni area Windows Explorer è associato un set di proplist, che a loro volta vengono specificati come proprietà. È possibile specificare proplist personalizzati per singoli elementi nei set di risultati o per tutti gli elementi in un set di risultati.



| Area dell'interfaccia utente da personalizzare               | Windows Proprietà della shell che implementa la personalizzazione |
|------------------------------------|----------------------------------------------------------|
| Modalità di visualizzazione del contenuto (durante la ricerca) | System.PropList.ContentViewModeForSearch                 |
| Modalità di visualizzazione del contenuto (durante l'esplorazione)  | System.PropList.ContentViewModeForBrowse                 |
| Modalità di visualizzazione affiancata                     | System.PropList.TileInfo                                 |
| Riquadro dei dettagli                       | System.PropList.PreviewDetails                           |
| Descrizione comando (descrizione comando al passaggio del mouse dell'elemento)     | System.PropList.Infotip                                  |



 

 

**Per specificare un proplist univoco per un singolo elemento:**

1.  Nell'output RSS aggiungere un elemento personalizzato che rappresenta l'elenco di proprietà da personalizzare. Ad esempio, nell'esempio seguente viene impostato l'elenco per il riquadro dei dettagli:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Per applicare una proprietà a ogni elemento nei risultati della ricerca senza modificare l'output RSS, specificare un proplist all'interno di un elemento **ms-ose:PropertyDefaultValues** nel file con estensione osdx, come illustrato nell'esempio seguente:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Layout delle proprietà in modalità visualizzazione contenuto

L'elenco delle proprietà specificate nei proplist **System.PropList.ContentViewModeForSearch** e **System.PropList.ContentViewModeForBrowse** determina ciò che viene visualizzato in modalità di visualizzazione contenuto. Per altre informazioni sugli elenchi di proprietà, vedere [PropList.](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)

Le proprietà vengono disposte in base ai numeri mostrati nel modello di layout seguente:

![Screenshot che mostra il modello di layout predefinito nella visualizzazione contenuto](images/propertiesnumberslayoutpattern.png)

Se si usa l'elenco di proprietà seguente,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



Viene quindi visualizzata la visualizzazione seguente:

![Screenshot che mostra il layout delle proprietà di esempio.](images/samplepropertylayout.png)

> [!Note]  
> Per una migliore leggibilità, le proprietà visualizzate nella colonna più a destra devono essere etichettate.

 

### <a name="property-list-flags"></a>Flag di elenco delle proprietà

Solo uno dei flag definiti nella documentazione relativa ai proplist si applica alla visualizzazione degli elementi nei layout in modalità visualizzazione contenuto: ` "~"` . Negli esempi precedenti la visualizzazione Windows Explorer etichetta alcune delle proprietà, ad esempio `Tags: animals; zoo; lion` . Si tratta del comportamento predefinito quando si specifica una proprietà nell'elenco. Ad esempio, il proplist ha `"System.Author"` che viene visualizzato come `"Authors: value"` . Quando si vuole nascondere l'etichetta della proprietà, posizionare un `"~"` davanti al nome della proprietà. Ad esempio, se il proplist ha , la proprietà viene visualizzata come solo `"~System.Size"` un valore, senza l'etichetta .

## <a name="previews"></a>Anteprime

Quando l'utente seleziona un elemento del risultato in Windows Explorer e il riquadro di anteprima è aperto, il contenuto dell'elemento viene visualizzato in anteprima.

Il contenuto da visualizzare nell'anteprima viene specificato da un URL, determinato come segue:

1.  Se la **proprietà System.WebPreviewUrl** Windows Shell è impostata per l'elemento, usare tale URL.
    > [!Note]  
    > La proprietà deve essere fornita nel formato RSS usando lo spazio dei nomi Windows Shell oppure deve essere mappata in modo esplicito nel file con estensione osdx.

     

2.  In caso contrario, usare invece l'URL del collegamento.

Il diagramma di flusso seguente illustra questa logica.

![Diagramma di flusso che illustra come Esplora risorse seleziona l'URL da usare per le anteprime](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

È possibile usare un URL diverso per l'anteprima rispetto all'elemento stesso. Ciò significa che se si specificano URL diversi per l'URL del collegamento e l'enclosure o , Windows Explorer usa l'URL del collegamento per le anteprime dell'elemento, ma usa l'altro URL per il rilevamento del tipo di file, l'apertura, il download e `media:content URL` così via.

Come Windows Explorer determina l'URL da usare:

1.  Se si specifica un mapping a [System.ItemFolderPathDisplay,](../properties/props-system-itemfolderpathdisplay.md)Windows Explorer usa tale URL
2.  Se non si specifica un mapping, Windows Explorer identifica se gli URL del collegamento e dello chassis sono diversi. In questo caso, Windows Explorer usa l'URL del collegamento.
3.  Se gli URL sono uguali o se è presente solo un URL di collegamento, Windows Explorer analizza il collegamento per trovare il contenitore padre rimuovendo il nome del file dall'URL completo.
    > [!Note]  
    > Se si riconosce che l'analisi dell'URL comporta collegamenti non disponibili per il servizio, è necessario fornire un mapping esplicito per la proprietà .

     

## <a name="open-file-location-menu-item"></a>Voce di menu Apri percorso file

Quando si fa clic con il pulsante destro del mouse su un elemento, viene **visualizzato** il comando di menu Apri percorso file. Questo comando consente all'utente di accedere al contenitore per o alla posizione dell'elemento. In una ricerca SharePoint, ad esempio, la selezione di questa opzione per un file in una raccolta documenti aprirà la radice della raccolta documenti nel Web browser.

Quando un utente fa clic su Apri **percorso file**, Windows Explorer tenta di trovare un contenitore padre, usando la logica illustrata nel diagramma di flusso seguente:

![Diagramma di flusso che illustra come Esplora risorse identifica un contenitore padre](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Risorse aggiuntive

Per altre informazioni sull'implementazione della federazione della ricerca in archivi dati remoti tramite tecnologie OpenSearch in Windows 7 e versioni successive, vedere "Risorse aggiuntive" in Ricerca federata [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Attività iniziali con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in Windows ricerca federata](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati Windows ricerca federata](-search-federated-search-data-store.md)
</dt> <dt>

[Procedure consigliate seguenti per Windows ricerca federata](-search-fedsearch-best.md)
</dt> <dt>

[Distribuzione di connettori di ricerca Windows ricerca federata](-search-federated-search-deploying.md)
</dt> </dl>

 

 
