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
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="36ed3-103">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="36ed3-104">Il supporto di Windows 7 per la Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch consente agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="36ed3-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="36ed3-105">È possibile creare un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante ricerca federata di Windows e abilitare l'integrazione avanzata delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice lato client Windows.</span><span class="sxs-lookup"><span data-stu-id="36ed3-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="36ed3-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="36ed3-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="36ed3-107">Che cos'è la ricerca federata?</span><span class="sxs-lookup"><span data-stu-id="36ed3-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="36ed3-108">Passaggi per la compilazione della ricerca federata</span><span class="sxs-lookup"><span data-stu-id="36ed3-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="36ed3-109">Funzionamento della ricerca federata</span><span class="sxs-lookup"><span data-stu-id="36ed3-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="36ed3-110">Invio di query e restituzione di risultati della ricerca in formato RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="36ed3-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="36ed3-111">Esempi di ricerca federati</span><span class="sxs-lookup"><span data-stu-id="36ed3-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="36ed3-112">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="36ed3-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="36ed3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36ed3-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="36ed3-114">Che cos'è la ricerca federata?</span><span class="sxs-lookup"><span data-stu-id="36ed3-114">What is Federated Search?</span></span>

<span data-ttu-id="36ed3-115">Windows 7 supporta la connessione di origini esterne al client Windows tramite il protocollo [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="36ed3-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="36ed3-116">Ciò consente agli utenti di eseguire ricerche in un archivio dati remoto e visualizzare i risultati da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="36ed3-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="36ed3-117">Lo standard [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 definisce formati di file semplici che possono essere utilizzati per descrivere il modo in cui un client deve eseguire una query sul servizio Web per l'archivio dati e il modo in cui il servizio deve restituire i risultati per il rendering da parte del client.</span><span class="sxs-lookup"><span data-stu-id="36ed3-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="36ed3-118">La ricerca federata Windows si connette ai servizi Web che ricevono query [OpenSearch](https://github.com/dewitt/opensearch) e restituisce i risultati in formato XML Atom o RSS.</span><span class="sxs-lookup"><span data-stu-id="36ed3-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="36ed3-119">Lo screenshot seguente illustra i risultati della ricerca ottenuti dopo la ricerca remota in un sito di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="36ed3-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![screenshot che mostra i risultati della ricerca da un sito di SharePoint come visualizzato in Esplora risorse](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="36ed3-121">Passaggi per la compilazione della ricerca federata</span><span class="sxs-lookup"><span data-stu-id="36ed3-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="36ed3-122">Per compilare la ricerca federata, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="36ed3-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="36ed3-123">Consente di eseguire la ricerca nell'archivio dati da Esplora risorse fornendo un servizio Web compatibile con [OpenSearch](https://github.com/dewitt/opensearch)che può restituire risultati in formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="36ed3-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="36ed3-124">Creare un file di descrizione OpenSearch (con estensione osdx) che descriva come connettersi al servizio Web e come eseguire il mapping di eventuali elementi personalizzati nel codice XML Atom o RSS.</span><span class="sxs-lookup"><span data-stu-id="36ed3-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="36ed3-125">Distribuire i connettori di ricerca nei computer client Windows con un file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="36ed3-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="36ed3-126">Il diagramma seguente illustra i passaggi per la compilazione della ricerca federata.</span><span class="sxs-lookup"><span data-stu-id="36ed3-126">The following diagram illustrates the steps for building federated search.</span></span>

![diagramma del processo per la compilazione della ricerca federata](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="36ed3-128">Funzionamento della ricerca federata</span><span class="sxs-lookup"><span data-stu-id="36ed3-128">How Federated Search Works</span></span>

<span data-ttu-id="36ed3-129">La comunicazione tra Esplora risorse e il servizio Web [OpenSearch](https://github.com/dewitt/opensearch) viene eseguita tramite il livello dati di Windows.</span><span class="sxs-lookup"><span data-stu-id="36ed3-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="36ed3-130">Il livello dati di Windows è in grado di comunicare con diversi tipi di archivi dati tramite i provider di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="36ed3-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="36ed3-131">Ogni provider è specializzato nella comunicazione con archivi dati che supportano un determinato protocollo e hanno funzionalità specifiche.</span><span class="sxs-lookup"><span data-stu-id="36ed3-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="36ed3-132">Nella figura seguente, ad esempio, viene illustrato il modo in cui il provider [OpenSearch](https://github.com/dewitt/opensearch) comunica con gli archivi dati che forniscono un servizio Web che supporta lo standard [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="36ed3-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![diagramma che illustra la comunicazione da Esplora risorse sul client tramite l'archivio dati OpenSearch nel server remoto](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="36ed3-134">Per consentire all'archivio dati di supportare la ricerca federata in Windows 7, è necessario eseguire una serie di attività.</span><span class="sxs-lookup"><span data-stu-id="36ed3-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="36ed3-135">La tabella seguente elenca le attività per l'abilitazione dell'archivio dati, gli elementi necessari per eseguire ogni attività e la posizione in cui trovare la documentazione.</span><span class="sxs-lookup"><span data-stu-id="36ed3-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="36ed3-136">Attività</span><span class="sxs-lookup"><span data-stu-id="36ed3-136">Task</span></span>                                                                                                     | <span data-ttu-id="36ed3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="36ed3-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="36ed3-138">Documentazione</span><span class="sxs-lookup"><span data-stu-id="36ed3-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ed3-139">Consente di eseguire la ricerca in Esplora risorse dell'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="36ed3-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="36ed3-140">Compilare un servizio Web compatibile con OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="36ed3-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="36ed3-141">Creare un file di descrizione OpenSearch (con estensione osdx).</span><span class="sxs-lookup"><span data-stu-id="36ed3-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="36ed3-142">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="36ed3-143">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="36ed3-144">Distribuisci attivamente il servizio Web agli utenti all'interno di un'azienda.</span><span class="sxs-lookup"><span data-stu-id="36ed3-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="36ed3-145">Fornire un file con estensione osdx agli utenti, copiarlo localmente e renderlo accessibile all'utente tramite un collegamento.</span><span class="sxs-lookup"><span data-stu-id="36ed3-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="36ed3-146">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="36ed3-147">Enumerare i risultati della ricerca in Esplora risorse in risposta a una query.</span><span class="sxs-lookup"><span data-stu-id="36ed3-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="36ed3-148">Implementare un servizio Web che accetta una stringa di query e restituisce i risultati in formato RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="36ed3-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="36ed3-149">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="36ed3-150">Consentire agli utenti di aggiungere l'archivio dati alla finestra Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="36ed3-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="36ed3-151">Creare un file con estensione osdx e fornirlo agli utenti.</span><span class="sxs-lookup"><span data-stu-id="36ed3-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="36ed3-152">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="36ed3-153">Visualizza gli elementi come elementi di tipo file in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="36ed3-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="36ed3-154">Restituire un URL al file o al flusso di contenuto usando l' **enclosure** o i **supporti:** elementi di contenuto</span><span class="sxs-lookup"><span data-stu-id="36ed3-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="36ed3-155">Specificare un'estensione di file o un tipo MIME riconosciuto dal computer client.</span><span class="sxs-lookup"><span data-stu-id="36ed3-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="36ed3-156">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="36ed3-157">Visualizzare le proprietà personalizzate in Esplora risorse, oltre a quelle definite negli standard RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="36ed3-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="36ed3-158">Fornire metadati aggiuntivi usando un altro spazio dei nomi XML nell'output RSS/Atom.</span><span class="sxs-lookup"><span data-stu-id="36ed3-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="36ed3-159">Aggiungere una mappa di proprietà al file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="36ed3-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="36ed3-160">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="36ed3-161">Personalizzare le proprietà visualizzate per gli elementi in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="36ed3-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="36ed3-162">Aggiungere i mapping di proprietà di un file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="36ed3-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="36ed3-163">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="36ed3-164">Visualizza una visualizzazione pagina Web personalizzata degli elementi nel riquadro di anteprima.</span><span class="sxs-lookup"><span data-stu-id="36ed3-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="36ed3-165">Restituisce valori di collegamento e enclosure distinti.</span><span class="sxs-lookup"><span data-stu-id="36ed3-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="36ed3-166">Eseguire il mapping di un valore URL alla proprietà della shell di Windows **System. WebPreviewUrl** .</span><span class="sxs-lookup"><span data-stu-id="36ed3-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="36ed3-167">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="36ed3-168">Consente di visualizzare un pulsante della barra dei comandi in Esplora risorse che esegue il rollforward della query nel sito Web.</span><span class="sxs-lookup"><span data-stu-id="36ed3-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="36ed3-169">Fornire un `Url format="text/html"` modello nel file con estensione osdx.</span><span class="sxs-lookup"><span data-stu-id="36ed3-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="36ed3-170">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="36ed3-171">Invio di query e restituzione di risultati della ricerca in formato RSS o Atom</span><span class="sxs-lookup"><span data-stu-id="36ed3-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="36ed3-172">Quando l'utente digita un termine nella casella di ricerca nell'angolo superiore destro di Esplora risorse, la query viene inviata al provider [OpenSearch](https://github.com/dewitt/opensearch) , che quindi Invia la query all'archivio dati remoto.</span><span class="sxs-lookup"><span data-stu-id="36ed3-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="36ed3-173">Il servizio Web remoto risponde alla query fornendo i risultati in un documento XML, in genere definito feed, in uno dei due formati supportati (RSS o Atom).</span><span class="sxs-lookup"><span data-stu-id="36ed3-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="36ed3-174">Ogni elemento di risultato nel feed include elementi figlio XML per rappresentare o descrivere i metadati degli elementi, ad esempio titolo, URL, descrizione, immagine di anteprima e così via.</span><span class="sxs-lookup"><span data-stu-id="36ed3-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="36ed3-175">Il provider [OpenSearch](https://github.com/dewitt/opensearch) è responsabile del mapping dei valori degli elementi XML alle proprietà di sistema della shell di Windows che possono essere utilizzate dalle applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="36ed3-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="36ed3-176">Esempi di ricerca federati</span><span class="sxs-lookup"><span data-stu-id="36ed3-176">Federated Search Examples</span></span>

<span data-ttu-id="36ed3-177">Il file di descrizione OpenSearch (con estensione osdx) di esempio seguente è costituito da `ShortName` `Url` elementi e, che sono gli elementi figlio minimi necessari per connettere un archivio dati esterno al client Windows tramite il protocollo OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="36ed3-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="36ed3-178">Nell'esempio seguente viene illustrato come creare un archivio dati abilitato per il Web in formato RSS e come specificare che venga restituito un elemento di ricerca:</span><span class="sxs-lookup"><span data-stu-id="36ed3-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


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



<span data-ttu-id="36ed3-179">Nell'esempio seguente viene illustrato come eseguire il mapping delle proprietà alle proprietà di sistema predefinite in modo che gli elementi visualizzati siano ordinati e raggruppati:</span><span class="sxs-lookup"><span data-stu-id="36ed3-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="36ed3-180">Nell'esempio seguente viene illustrato come aggiungere una visualizzazione dell'immagine di anteprima a ogni elemento in Esplora risorse:</span><span class="sxs-lookup"><span data-stu-id="36ed3-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="36ed3-181">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="36ed3-181">Additional Resources</span></span>

<span data-ttu-id="36ed3-182">Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36ed3-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36ed3-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36ed3-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36ed3-184">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="36ed3-185">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="36ed3-186">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="36ed3-187">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="36ed3-188">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="36ed3-189">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="36ed3-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




