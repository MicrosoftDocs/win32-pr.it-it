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
# <a name="enabling-your-data-store-in-windows-federated-search"></a><span data-ttu-id="0b5f9-103">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-103">Enabling Your Data Store in Windows Federated Search</span></span>

<span data-ttu-id="0b5f9-104">Viene illustrato come abilitare l'accesso all'archivio dati da un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) e come evitare potenziali barriere.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-104">Explains how to enable your data store to be accessed by an [OpenSearch](https://github.com/dewitt/opensearch) web service, and how to avoid potential barriers for doing so.</span></span>

<span data-ttu-id="0b5f9-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0b5f9-106">Condizioni per l'accettazione della richiesta di ricerca</span><span class="sxs-lookup"><span data-stu-id="0b5f9-106">Conditions for Search Request Acceptance</span></span>](#conditions-for-search-request-acceptance)
    -   [<span data-ttu-id="0b5f9-107">Sintassi di query supportata</span><span class="sxs-lookup"><span data-stu-id="0b5f9-107">Supported Query Syntax</span></span>](#supported-query-syntax)
    -   [<span data-ttu-id="0b5f9-108">Protocolli di autenticazione supportati</span><span class="sxs-lookup"><span data-stu-id="0b5f9-108">Supported Authentication Protocols</span></span>](#supported-authentication-protocols)
-   [<span data-ttu-id="0b5f9-109">Invio di query e restituzione di risultati della ricerca in formato RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="0b5f9-109">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [<span data-ttu-id="0b5f9-110">Esempio di output di un feed RSS</span><span class="sxs-lookup"><span data-stu-id="0b5f9-110">Example of an RSS Feed Output</span></span>](#example-of-an-rss-feed-output)
-   [<span data-ttu-id="0b5f9-111">Mapping automatico a proprietà della shell di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-111">Automatic Mapping to Windows Shell Properties</span></span>](#automatic-mapping-to-windows-shell-properties)
-   [<span data-ttu-id="0b5f9-112">Informazioni sul modo in cui Windows mappa gli elementi ai tipi di file</span><span class="sxs-lookup"><span data-stu-id="0b5f9-112">Understanding How Windows Maps Items to File Types</span></span>](#understanding-how-windows-maps-items-to-file-types)
-   [<span data-ttu-id="0b5f9-113">Evitare potenziali barriere per l'abilitazione di un archivio dati</span><span class="sxs-lookup"><span data-stu-id="0b5f9-113">Avoiding Potential Barriers to Enabling a Data Store</span></span>](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [<span data-ttu-id="0b5f9-114">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="0b5f9-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="0b5f9-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b5f9-115">Related topics</span></span>](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a><span data-ttu-id="0b5f9-116">Condizioni per l'accettazione della richiesta di ricerca</span><span class="sxs-lookup"><span data-stu-id="0b5f9-116">Conditions for Search Request Acceptance</span></span>

<span data-ttu-id="0b5f9-117">Il servizio Web [OpenSearch](https://github.com/dewitt/opensearch) creato nel server Web **deve** soddisfare i due requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-117">The [OpenSearch](https://github.com/dewitt/opensearch) web service you create on your web server **must** fulfill the following two requirements:</span></span>

-   <span data-ttu-id="0b5f9-118">Essere in grado di accettare una `GET URL` query dal client.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-118">Be able to accept a `GET URL` query from the client.</span></span>
-   <span data-ttu-id="0b5f9-119">Consente di incorporare i termini di ricerca nell'URL.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-119">Permit the search terms to be embedded in the URL.</span></span>

    <span data-ttu-id="0b5f9-120">Nell'esempio seguente viene illustrato come un termine di ricerca può essere incorporato in un URL.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-120">The following example shows how a search term can be embedded in a URL.</span></span>

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> <span data-ttu-id="0b5f9-121">La ricerca federata non supporta l'invio `POST` di richieste a un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-121">Federated search does not support sending `POST` requests to a web service.</span></span>

 

<span data-ttu-id="0b5f9-122">Per ulteriori informazioni sulla creazione di un URL, vedere la sezione relativa ai parametri dei modelli URL nella pagina relativa alla [creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-122">For more information about constructing a URL, see "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

### <a name="supported-query-syntax"></a><span data-ttu-id="0b5f9-123">Sintassi di query supportata</span><span class="sxs-lookup"><span data-stu-id="0b5f9-123">Supported Query Syntax</span></span>

<span data-ttu-id="0b5f9-124">In Windows 7 non è prevista una sintassi di query specifica.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-124">There is no specific query syntax expected in Windows 7.</span></span> <span data-ttu-id="0b5f9-125">Il provider OpenSearch accetta tutti i termini immessi dall'utente nella casella di input in Esplora risorse e li codifica nell'URL.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-125">The OpenSearch provider accepts whatever terms the user enters in the input box in Windows Explorer, and encodes it into the URL.</span></span> <span data-ttu-id="0b5f9-126">Questa operazione viene eseguita in base al modello di URL descritto in "parametri modello URL" in [creazione di un file di descrizione OpenSearch in ricerca federata di Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-126">It does so according to the URL template described in "URL Template Parameters" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

<span data-ttu-id="0b5f9-127">Gli utenti si aspettano che i termini separati vengano considerati in modo implicito individuato insieme.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-127">Users expect that separate terms are treated as implicitly ANDed together.</span></span> <span data-ttu-id="0b5f9-128">Ad esempio, una query per "Microsoft Windows" deve restituire solo i risultati che contengono sia "Windows" che "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="0b5f9-128">For example, a query for "Microsoft Windows" should return only results that contain both "Windows" and "Microsoft".</span></span>

### <a name="supported-authentication-protocols"></a><span data-ttu-id="0b5f9-129">Protocolli di autenticazione supportati</span><span class="sxs-lookup"><span data-stu-id="0b5f9-129">Supported Authentication Protocols</span></span>

<span data-ttu-id="0b5f9-130">La ricerca federata Windows supporta l'autenticazione basata su Windows e può fornire le credenziali ai servizi Web tramite i protocolli seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-130">Windows Federated Search supports Windows-based authentication, and can provide credentials to web services via the following protocols:</span></span>

-   <span data-ttu-id="0b5f9-131">NTLM.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-131">NTLM.</span></span>
-   <span data-ttu-id="0b5f9-132">Autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-132">Kerberos.</span></span>
-   <span data-ttu-id="0b5f9-133">Basic (solo su HTTPS).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-133">Basic (only over https).</span></span>
-   <span data-ttu-id="0b5f9-134">Altri SSP (Security Support Provider) installati in Windows che forniscono capacità di query aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-134">Other Security Support Providers (SSPs) installed on Windows that provide additional querying capacity.</span></span> <span data-ttu-id="0b5f9-135">Vedere la documentazione di [SSP Interface](../secauthn/sspi.md) SDK per gestire la potenziale aggiunta di altri SSP.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-135">See the [SSP Interface](../secauthn/sspi.md) SDK documentation to keep abreast of the potential addition of other SSPs.</span></span>

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="0b5f9-136">Invio di query e restituzione di risultati della ricerca in formato RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="0b5f9-136">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="0b5f9-137">Il provider [OpenSearch](https://github.com/dewitt/opensearch) è responsabile del mapping dei valori degli elementi XML alle proprietà di sistema della shell di Windows che possono essere utilizzate dalle applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-137">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span> <span data-ttu-id="0b5f9-138">Tuttavia, non si è limitati ai mapping predefiniti di elementi RSS o Atom standard e possono includere elementi XML personalizzati nello spazio dei nomi Windows per ciascuna proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-138">But you are not limited to the default mappings of standard RSS or Atom elements, and can include custom XML elements in the Windows namespace for each of the properties.</span></span> <span data-ttu-id="0b5f9-139">È ad esempio possibile aggiungere elementi XML personalizzati all'interno dell'elemento **Item** per fornire metadati aggiuntivi a Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-139">For example, you can add your own custom XML elements within the **item** element to provide additional metadata to Windows.</span></span> <span data-ttu-id="0b5f9-140">È anche possibile eseguire il mapping di elementi da altri spazi dei nomi XML, ad esempio iTunes</span><span class="sxs-lookup"><span data-stu-id="0b5f9-140">You can also map elements from other XML namespaces, such as iTunes</span></span>

### <a name="example-of-an-rss-feed-output"></a><span data-ttu-id="0b5f9-141">Esempio di output di un feed RSS</span><span class="sxs-lookup"><span data-stu-id="0b5f9-141">Example of an RSS Feed Output</span></span>

<span data-ttu-id="0b5f9-142">L'output del feed RSS di esempio seguente restituisce un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-142">The following example RSS feed output returns one item.</span></span>


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



<span data-ttu-id="0b5f9-143">Per informazioni più dettagliate sul mapping delle proprietà, vedere le sezioni "elementi estesi in ricerca federata di WIndows" e "mapping di proprietà personalizzate" in [creazione di un file di descrizione OpenSearch in ricerca federata di Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-143">For more detailed information about property mapping, see the "Extended Elements in WIndows Federated Search" and "Custom Property Mappings" sections in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="automatic-mapping-to-windows-shell-properties"></a><span data-ttu-id="0b5f9-144">Mapping automatico a proprietà della shell di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-144">Automatic Mapping to Windows Shell Properties</span></span>

<span data-ttu-id="0b5f9-145">Negli elementi del feed RSS è possibile scegliere di includere altri elementi XML che vengono mappati automaticamente alle proprietà del sistema della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-145">Within the items in your RSS feed, you can choose to include other XML elements that automatically map to Windows Shell system properties.</span></span> <span data-ttu-id="0b5f9-146">A tale scopo, includere un elemento denominato dopo la proprietà della shell di Windows e preceduto dallo spazio dei nomi System Shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-146">To do so, include an element named after the Windows Shell property and prefixed with the Windows Shell system namespace.</span></span> <span data-ttu-id="0b5f9-147">Nell'esempio seguente viene illustrata la dichiarazione dello spazio dei nomi `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` e l'inclusione di un elemento per il mapping delle proprietà `win:System.Contact.PrimaryEmailAddress` :</span><span class="sxs-lookup"><span data-stu-id="0b5f9-147">The following example illustrates the namespace declaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` and the inclusion of an element for the property mapping `win:System.Contact.PrimaryEmailAddress`:</span></span>


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



<span data-ttu-id="0b5f9-148">Il prefisso dello spazio dei nomi usato qui ( `"win"` ) è un suggerimento. è possibile usare qualsiasi prefisso.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-148">The namespace prefix used here (`"win"`) is a suggestion; you can use any prefix.</span></span> <span data-ttu-id="0b5f9-149">Tuttavia, è necessario usare i nomi esatti delle proprietà della shell di Windows e deve includere l'esatta Uniform Resource Identifier (URI), come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-149">However, you must use the exact Windows Shell property names, and must include the exact Uniform Resource Identifier (URI), as shown in the following example:</span></span>


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



<span data-ttu-id="0b5f9-150">**Informazioni sulle proprietà di sistema della shell di Windows**</span><span class="sxs-lookup"><span data-stu-id="0b5f9-150">**About Windows Shell System Properties**</span></span>

<span data-ttu-id="0b5f9-151">Windows definisce un elenco completo delle [proprietà di sistema](../properties/props.md) e il formato del tipo di valore necessario per ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-151">Windows defines a complete list of [System Properties](../properties/props.md) and the value type format required for each property.</span></span> <span data-ttu-id="0b5f9-152">La documentazione relativa alla proprietà della shell della finestra [System. FileExtension](../properties/props-system-fileextension.md) , ad esempio, specifica che il valore deve contenere il punto principale (". docx" e non "docx").</span><span class="sxs-lookup"><span data-stu-id="0b5f9-152">The documentation for the [System.FileExtension](../properties/props-system-fileextension.md) Window Shell property, for example, specifies that the value must contain the leading dot (".docx" and not "docx").</span></span>

<span data-ttu-id="0b5f9-153">**Valori di data e ora**</span><span class="sxs-lookup"><span data-stu-id="0b5f9-153">**Date and Time Values**</span></span>

<span data-ttu-id="0b5f9-154">Il formato di data e ora preferito è ISO-8601, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-154">The preferred date and time format is ISO-8601, as shown in the following example:</span></span>


```
2008-01-16T 19:20:30:.45+01:00
```



<span data-ttu-id="0b5f9-155">Gli sviluppatori .NET devono usare la classe DateTime con `ToString("R") ` per restituire il formato corretto.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-155">.NET developers should use the DateTime class with `ToString("R") `to output the correct format.</span></span>

<span data-ttu-id="0b5f9-156">Per informazioni più dettagliate sul mapping delle proprietà, vedere "elementi estesi in ricerca federata di Windows" in [creazione di un file di descrizione OpenSearch in ricerca federata di Windows](-search-federated-search-osdx-file.md).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-156">For more detailed information about property mapping, see "Extended Elements in Windows Federated Search" in [Creating an OpenSearch Description File in Windows Federated Search](-search-federated-search-osdx-file.md).</span></span>

## <a name="understanding-how-windows-maps-items-to-file-types"></a><span data-ttu-id="0b5f9-157">Informazioni sul modo in cui Windows mappa gli elementi ai tipi di file</span><span class="sxs-lookup"><span data-stu-id="0b5f9-157">Understanding How Windows Maps Items to File Types</span></span>

<span data-ttu-id="0b5f9-158">La ricerca all'interno dell'interfaccia utente di Esplora risorse consente agli utenti di trattare i risultati come file quando un elemento RSS punta a un file archiviato in remoto.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-158">Searching within the Windows Explorer UI permits users to treat results as files when an RSS item points to a file stored remotely.</span></span> <span data-ttu-id="0b5f9-159">L'utente può trascinare e rilasciare elementi sul desktop e l'interfaccia utente di Esplora risorse Visualizza l'icona corretta e fornisce il menu di scelta rapida appropriato.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-159">The user can drag and drop items to the desktop, and the Windows Explorer UI displays the correct icon and provides the appropriate shortcut menu.</span></span> <span data-ttu-id="0b5f9-160">Se l'elemento RSS non punta a un file archiviato in modalità remota, il file viene considerato come un collegamento e gli utenti possono eseguire azioni su di esso, ad esempio creare un collegamento o aprirlo nel browser.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-160">If the RSS item does not point to a remotely stored file, the file is treated as a link, and users can perform actions on it such as creating a shortcut or opening it in the browser.</span></span>

<span data-ttu-id="0b5f9-161">Il diagramma di flusso seguente mostra in che modo Windows determina il tipo di file di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-161">The following flowchart shows how Windows determines an item's file type.</span></span>

![diagramma di flusso che mostra i percorsi da un elemento alle decisioni per considerarlo come un elemento del tipo di collegamento Web o come tipo di file](images/determineanitemfiletype.png)

<span data-ttu-id="0b5f9-163">Il provider [OpenSearch](https://github.com/dewitt/opensearch) esegue i passaggi seguenti per eseguire il mapping di un elemento a un tipo di file:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-163">The [OpenSearch](https://github.com/dewitt/opensearch) provider performs the following steps to map an item to a file type:</span></span>

-   <span data-ttu-id="0b5f9-164">Determinare se l'elemento deve essere trattato come un file o un collegamento Web.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-164">Identify whether the item should be treated as a file or a web link.</span></span>
-   <span data-ttu-id="0b5f9-165">Identificare l'estensione del nome file corretta da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-165">Identify the correct file name extension to use.</span></span>

<span data-ttu-id="0b5f9-166">Ad esempio, se l'elemento ha un URL di collegamento che usa un percorso di file system (ad esempio `file:///\\server\share\etc\item.ext` ), il provider [OpenSearch](https://github.com/dewitt/opensearch) considera il collegamento come un file e determina il tipo in base all'estensione del nome file usata nel percorso (. ext in questo esempio).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-166">For example, if the item has a link URL that uses a file system path (such as `file:///\\server\share\etc\item.ext`), the [OpenSearch](https://github.com/dewitt/opensearch) provider treats the link as a file and determines the type by the file name extension used in the path (.ext in this example).</span></span>

<span data-ttu-id="0b5f9-167">Se l'elemento usa lo chassis RSS standard o **MediaRSS media: content** , il provider [OpenSearch](https://github.com/dewitt/opensearch) presuppone che l'elemento sia un file e identifichi l'estensione del nome file come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-167">If the item uses the standard RSS enclosure or **MediaRSS media:content** element, the [OpenSearch](https://github.com/dewitt/opensearch) provider assumes that the item is a file and identifies the file name extension as follows:</span></span>

-   <span data-ttu-id="0b5f9-168">Se è stato eseguito il mapping della proprietà della shell di Windows [System. FileExtension](../properties/props-system-fileextension.md) per l'elemento, il provider usa tale estensione di file.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-168">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has been mapped for the item, the provider uses that file name extension.</span></span>
-   <span data-ttu-id="0b5f9-169">Se non è stato eseguito il mapping della proprietà della shell di Windows [System. FileExtension](../properties/props-system-fileextension.md) , il provider utilizza l'attributo **Type** specificato nell'enclosure o nell'elemento Content.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-169">If the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property has not been mapped, the provider uses the **Type** attribute specified in the enclosure or content element.</span></span> <span data-ttu-id="0b5f9-170">Questo elemento deve contenere una `MIMEType` stringa, ad esempio `"image/jpeg"` .</span><span class="sxs-lookup"><span data-stu-id="0b5f9-170">This element should contain a `MIMEType` string, such as `"image/jpeg"`.</span></span> <span data-ttu-id="0b5f9-171">Se `MIMEType` è associato a un'estensione di file registrata nel computer client, l'elemento viene considerato come un file di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-171">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the item is regarded as a file of that type.</span></span> <span data-ttu-id="0b5f9-172">Se `MIMEType` non è associato a un'estensione di file registrata nel computer client, l'elemento viene considerato come un tipo di collegamento Web.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-172">If the `MIMEType` is not associated with a file name extension registered on the client computer, the item is treated as a web link type.</span></span> <span data-ttu-id="0b5f9-173">Il provider [OpenSearch](https://github.com/dewitt/opensearch) non tenta di analizzare l'attributo **URL** per individuare l'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-173">The [OpenSearch](https://github.com/dewitt/opensearch) provider does not attempt to parse the **Url** attribute to locate the file name extension.</span></span>
-   <span data-ttu-id="0b5f9-174">Se `MIMEType` è associato a un'estensione di file registrata nel computer client, il provider determina se l'estensione del nome file è un tipo di file Web noto (htm, HTML, ASP, aspx, php, SWF, STM).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-174">If the `MIMEType` is associated with a file name extension that is registered on the client computer, the provider determines whether the file name extension is a known web file type (.htm, .html, .asp, .aspx, .php, .swf, .stm).</span></span> <span data-ttu-id="0b5f9-175">In tal caso, il tipo di file viene considerato come un tipo di collegamento Web; in caso contrario, viene considerato come un tipo di file.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-175">If so, the file type is regarded as a web link type; otherwise, it is regarded as a file type.</span></span> <span data-ttu-id="0b5f9-176">Ad esempio, se l' `MIMEType "text/html"` oggetto è associato all'estensione del nome di file htm, tale elemento viene considerato come un collegamento Web anziché come un tipo di file htm.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-176">For example, if the `MIMEType "text/html"` is associated with the .htm file name extension, that item is regarded as a web link instead of as an .htm file type.</span></span>

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a><span data-ttu-id="0b5f9-177">Evitare potenziali barriere per l'abilitazione di un archivio dati</span><span class="sxs-lookup"><span data-stu-id="0b5f9-177">Avoiding Potential Barriers to Enabling a Data Store</span></span>

<span data-ttu-id="0b5f9-178">Alcuni archivi dati non forniscono un servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch), ma possono comunque essere connessi alla ricerca federata di Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-178">Some data stores do not provide an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service but can still be connected to Windows Federated Search.</span></span> <span data-ttu-id="0b5f9-179">Tali archivi dati includono:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-179">Such data stores include:</span></span>

-   <span data-ttu-id="0b5f9-180">Indici remoti con metodi di autenticazione non supportati nella ricerca federata di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-180">Remote indexes with authentication methods that are not supported in Windows 7 Federated Search.</span></span>

    <span data-ttu-id="0b5f9-181">Gli esempi includono l'autenticazione basata su moduli e altri metodi di autenticazione personalizzati.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-181">Examples include forms-based authentication and other custom authentication methods.</span></span>

-   <span data-ttu-id="0b5f9-182">Se un archivio pubblico di valore elevato ha API Web pubbliche, chiunque può scrivere un altro servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch)e chiama tali API in background.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-182">If a high-value public store has public web APIs, anyone can write another web service that is [OpenSearch](https://github.com/dewitt/opensearch)-compatible and calls those APIs behind the scenes.</span></span>

    <span data-ttu-id="0b5f9-183">Gli esempi includono la libreria del Congresso e i database di ricerca medica.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-183">Examples include the Library of Congress, and medical research databases.</span></span>

-   <span data-ttu-id="0b5f9-184">Gli archivi dati aziendali o gli indici proprietari e gli archivi di gestione del contenuto legacy, per i quali potrebbe essere Impossibile implementare un front-end.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-184">Proprietary enterprise data stores or indexes, and legacy content management stores, for which it might be impossible to implement a front end.</span></span>

<span data-ttu-id="0b5f9-185">Tuttavia, esistono alternative che possono evitare barriere per l'abilitazione di un archivio dati.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-185">However, there are alternatives that can avoid barriers to enabling a data store.</span></span> <span data-ttu-id="0b5f9-186">Di seguito sono riportate alcune alternative:</span><span class="sxs-lookup"><span data-stu-id="0b5f9-186">The following are some of those alternatives:</span></span>

<span data-ttu-id="0b5f9-187">**Per scrivere un servizio Web di tipo intermedio quando non è possibile modificare il servizio Web per l'origine dati esistente o il servizio Web fornisce un'API personalizzata:**</span><span class="sxs-lookup"><span data-stu-id="0b5f9-187">**To write a middle-man web service when you cannot modify the web service for the existing data source, or the web service provides a custom API:**</span></span>

1.  <span data-ttu-id="0b5f9-188">Scrivere un servizio Web di tipo intermedio che può accettare una query di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-188">Write a middle-man web service that can accept a Windows 7 query.</span></span>
2.  <span data-ttu-id="0b5f9-189">Connettersi all'origine dati e recuperare i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-189">Connect to your data source, and retrieve the query results.</span></span>
3.  <span data-ttu-id="0b5f9-190">Riformattare i risultati in formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-190">Reformat the results in RSS or Atom format.</span></span>
4.  <span data-ttu-id="0b5f9-191">Restituisce i risultati al client Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-191">Return the results to the Windows 7 client.</span></span>
5.  <span data-ttu-id="0b5f9-192">Si noti che per Enterprise Data Services e molti servizi dati Internet, potrebbe essere necessario passare le credenziali utente tramite per conto del servizio Web per eseguire il taglio dei risultati in base alle autorizzazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-192">Note that for enterprise data services and many Internet data services, you may need to pass the user credentials through on behalf of the web service to perform result trimming based on the user's permissions.</span></span>

<span data-ttu-id="0b5f9-193">**Per usare un motore di ricerca esistente quando non è possibile abilitare un archivio dati pubblico:**</span><span class="sxs-lookup"><span data-stu-id="0b5f9-193">**To use an existing search engine when you cannot enable a public data store:**</span></span>

1.  <span data-ttu-id="0b5f9-194">Usare un motore di ricerca pubblico che supporta già [OpenSearch](https://github.com/dewitt/opensearch) con RSS.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-194">Use a public search engine that already supports [OpenSearch](https://github.com/dewitt/opensearch) with RSS.</span></span> <span data-ttu-id="0b5f9-195">A tale scopo, è possibile fornire agli utenti un file con estensione osdx che dispone di un modello di URL che limita i risultati solo a quelli per il dominio specifico.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-195">You can do so by providing your users with an .osdx file that has a URL template that restricts results to only those for your specific domain.</span></span>
2.  <span data-ttu-id="0b5f9-196">Vedere l'esempio seguente di una descrizione di [OpenSearch](https://github.com/dewitt/opensearch) per la ricerca solo nel contenuto della Guida per Windows tramite una query su Live.com.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-196">See the following example of an [OpenSearch](https://github.com/dewitt/opensearch) description for searching only the Help content for Windows by using a query against live.com.</span></span>

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

    

<span data-ttu-id="0b5f9-197">**Per utilizzare un server di indicizzazione esistente che supporta OpenSearch quando non è possibile abilitare gli archivi dati aziendali o gli indici proprietari:**</span><span class="sxs-lookup"><span data-stu-id="0b5f9-197">**To use an existing indexing server that supports OpenSearch when you cannot enable proprietary enterprise data stores or indexes:**</span></span>

1.  <span data-ttu-id="0b5f9-198">Consente di selezionare un server di indicizzazione esistente che supporta [OpenSearch](https://github.com/dewitt/opensearch) per indicizzare il contenuto, ad esempio il server di ricerca di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-198">Select an existing indexing server that supports [OpenSearch](https://github.com/dewitt/opensearch) to index your content, such as the SharePoint Search Server.</span></span>
2.  <span data-ttu-id="0b5f9-199">Creare un file con estensione osdx che limiti i risultati dall'indice di SharePoint solo a quelli del server usando la relativa sintassi delle parole chiave nel modello di URL.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-199">Create an .osdx file that restricts the results from the SharePoint index to only those from your server by using their KeyWord syntax within the URL template.</span></span>

<span data-ttu-id="0b5f9-200">**Per scrivere un archivio dati lato client se una soluzione solo sul lato server non funziona:**</span><span class="sxs-lookup"><span data-stu-id="0b5f9-200">**To write a client-side data store if a server-side-only solution does not work:**</span></span>

1.  <span data-ttu-id="0b5f9-201">Scrivere un'origine dati [OpenSearch](https://github.com/dewitt/opensearch) sul lato client che risiede tra il provider [OpenSearch](https://github.com/dewitt/opensearch) Windows e l'origine dati esterna.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-201">Write a client-side [OpenSearch](https://github.com/dewitt/opensearch) data source that sits between the Windows [OpenSearch](https://github.com/dewitt/opensearch) provider and the external data source.</span></span>
2.  <span data-ttu-id="0b5f9-202">Usare l'API dell' [interfaccia IOpenSearchSource](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) nel Windows SDK per creare un file con estensione searchconnector-ms configurato in modo appropriato tramite cui Esplora risorse può chiamare l'implementazione con i parametri di query.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-202">Use the [IOpenSearchSource Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) API in the Windows SDK to create an appropriately configured .searchconnector-ms file through which Windows Explorer can call your implementation with the query parameters.</span></span> <span data-ttu-id="0b5f9-203">L'implementazione può quindi restituire i risultati formattati in formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-203">Your implementation can then return results formatted in RSS or Atom format.</span></span> <span data-ttu-id="0b5f9-204">Questa operazione consente all'implementazione di fornire un'interfaccia utente personalizzata per l'autenticazione e di connettersi all'origine dati usando l'API proprietaria.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-204">Doing so enables your implementation to provide custom authentication UI and to connect to the data source using its proprietary API.</span></span>

> [!Note]  
> <span data-ttu-id="0b5f9-205">Se si apre un file con estensione osdx, viene creato un file con estensione searchconnector-ms (connettore di ricerca) nella directory% UserProfile%/Searches e viene inserito un collegamento nella directory% UserProfile%/Links.</span><span class="sxs-lookup"><span data-stu-id="0b5f9-205">Opening an .osdx file creates a .searchconnector-ms file (search connector) in the %userprofile%/searches directory and places a link to it in the %userprofile%/links directory.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="0b5f9-206">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="0b5f9-206">Additional Resources</span></span>

<span data-ttu-id="0b5f9-207">Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b5f9-207">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b5f9-208">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b5f9-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b5f9-209">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-209">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="0b5f9-210">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-210">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="0b5f9-211">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-211">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="0b5f9-212">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-212">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="0b5f9-213">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-213">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="0b5f9-214">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="0b5f9-214">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
