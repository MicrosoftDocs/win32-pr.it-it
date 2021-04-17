---
description: Introduce lo schema di descrizione del connettore di ricerca utilizzato dalle librerie di Esplora risorse e dai provider di ricerca federati.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Cerca nello schema di descrizione del connettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306068"
---
# <a name="search-connector-description-schema"></a><span data-ttu-id="4fb29-103">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="4fb29-103">Search Connector Description Schema</span></span>

<span data-ttu-id="4fb29-104">Introduce lo schema di descrizione del connettore di ricerca utilizzato dalle librerie di Esplora risorse e dai provider di ricerca federati.</span><span class="sxs-lookup"><span data-stu-id="4fb29-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="4fb29-105">Lo schema specifica la struttura e i requisiti per i file di descrizione del connettore di ricerca (con \* estensione searchConnector-MS) e per gli elementi **searchConnectorDescriptionType** dei file di descrizione della libreria della shell ( \* libreria-MS).</span><span class="sxs-lookup"><span data-stu-id="4fb29-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="4fb29-106">In questo argomento viene descritto lo schema correlato ai connettori di ricerca federati.</span><span class="sxs-lookup"><span data-stu-id="4fb29-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="4fb29-107">Per ulteriori informazioni sulle librerie e sullo schema di descrizione della libreria, vedere [Library Description schema](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="4fb29-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="4fb29-108">Questo argomento include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fb29-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="4fb29-109">Che cosa sono i connettori di ricerca?</span><span class="sxs-lookup"><span data-stu-id="4fb29-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="4fb29-110">Come funzionano i file di descrizione del connettore di ricerca?</span><span class="sxs-lookup"><span data-stu-id="4fb29-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="4fb29-111">Che cos'è lo schema di descrizione del connettore di ricerca?</span><span class="sxs-lookup"><span data-stu-id="4fb29-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="4fb29-112">Quali sono le parti principali dello schema?</span><span class="sxs-lookup"><span data-stu-id="4fb29-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="4fb29-113">Esempi di file di descrizione del connettore di ricerca</span><span class="sxs-lookup"><span data-stu-id="4fb29-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="4fb29-114">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="4fb29-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="4fb29-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fb29-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="4fb29-116">Che cosa sono i connettori di ricerca?</span><span class="sxs-lookup"><span data-stu-id="4fb29-116">What Are Search Connectors?</span></span>

<span data-ttu-id="4fb29-117">I connettori di ricerca connettono gli utenti con i dati archiviati in servizi Web o posizioni di archiviazione remota.</span><span class="sxs-lookup"><span data-stu-id="4fb29-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="4fb29-118">Con Windows 7, gli utenti possono installare i connettori di ricerca per le posizioni, ad esempio i servizi Web, in modo da cercare tali percorsi direttamente da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="4fb29-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="4fb29-119">I connettori di ricerca sono file di descrizione del connettore di ricerca (con \* estensione searchConnector-MS) che specificano come connettersi, inviare query a e ricevere i risultati dal percorso.</span><span class="sxs-lookup"><span data-stu-id="4fb29-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="4fb29-120">Oltre ai servizi Web, è possibile usare i connettori di ricerca per eseguire ricerche negli ambiti degli indici locali creati dai gestori del protocollo.</span><span class="sxs-lookup"><span data-stu-id="4fb29-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="4fb29-121">Ad esempio, gli utenti possono eseguire ricerche nella posta elettronica indicizzata localmente con il gestore del protocollo MAPI usando un connettore di ricerca per l'archivio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4fb29-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="4fb29-122">Come funzionano i file di descrizione del connettore di ricerca?</span><span class="sxs-lookup"><span data-stu-id="4fb29-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="4fb29-123">Quando i file di descrizione del connettore di ricerca sono installati nei sistemi degli utenti, gli utenti possono aprire Esplora risorse, fare clic sul connettore Cerca nel riquadro di spostamento e immettere una query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="4fb29-124">Esplora risorse Invia la query usando le informazioni del file di descrizione del connettore di ricerca, ad esempio il provider da usare e l'ambito della ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="4fb29-125">I risultati vengono restituiti come elementi feed RSS o Atom e visualizzati agli utenti come se fossero elementi normali della shell.</span><span class="sxs-lookup"><span data-stu-id="4fb29-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="4fb29-126">La modalità di distribuzione del file di descrizione del connettore di ricerca dipende dal tipo di posizione supportata dal connettore di ricerca:</span><span class="sxs-lookup"><span data-stu-id="4fb29-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="4fb29-127">In un file di configurazione di OpenSearch (con \* estensione osdx) per il servizio Web</span><span class="sxs-lookup"><span data-stu-id="4fb29-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="4fb29-128">Come parte dell'installazione del gestore di protocollo</span><span class="sxs-lookup"><span data-stu-id="4fb29-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="4fb29-129">È necessario assicurarsi che si verifichi quanto segue quando un utente apre il file con estensione osdx o installa il gestore di protocollo:</span><span class="sxs-lookup"><span data-stu-id="4fb29-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="4fb29-130">Il file con estensione searchconnector-ms viene creato nella cartella **ricerche di Windows** degli utenti (% USERPROFILE%/Searches).</span><span class="sxs-lookup"><span data-stu-id="4fb29-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="4fb29-131">Viene creato un collegamento al file. searchconnector-ms nella cartella **collegamenti** degli utenti (% USERPROFILE%/Links).</span><span class="sxs-lookup"><span data-stu-id="4fb29-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="4fb29-132">Che cos'è lo schema di descrizione del connettore di ricerca?</span><span class="sxs-lookup"><span data-stu-id="4fb29-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="4fb29-133">Lo schema di descrizione del connettore di ricerca è un XML Schema che definisce la struttura dei file di descrizione del connettore di ricerca (con \* estensione searchConnector-MS).</span><span class="sxs-lookup"><span data-stu-id="4fb29-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="4fb29-134">Ogni connettore di ricerca deve avere un file di descrizione del connettore di ricerca che specifichi come connettersi, inviare query a e ricevere i risultati dal percorso.</span><span class="sxs-lookup"><span data-stu-id="4fb29-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="4fb29-135">Quali sono le parti principali dello schema?</span><span class="sxs-lookup"><span data-stu-id="4fb29-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="4fb29-136">Nella tabella seguente sono elencate le parti principali dello schema.</span><span class="sxs-lookup"><span data-stu-id="4fb29-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="4fb29-137">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4fb29-137">Child elements</span></span>                                                                         | <span data-ttu-id="4fb29-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb29-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fb29-139">isSearchOnlyItem</span><span class="sxs-lookup"><span data-stu-id="4fb29-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="4fb29-140">Indica se i percorsi supportati dal connettore di ricerca sono di sola ricerca o di ricerca ed esplorazione.</span><span class="sxs-lookup"><span data-stu-id="4fb29-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="4fb29-141">isDefaultSaveLocation</span><span class="sxs-lookup"><span data-stu-id="4fb29-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="4fb29-142">Solo per l'uso della libreria.</span><span class="sxs-lookup"><span data-stu-id="4fb29-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="4fb29-143">isDefaultNonOwnerSaveLocation</span><span class="sxs-lookup"><span data-stu-id="4fb29-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="4fb29-144">Solo per l'uso della libreria.</span><span class="sxs-lookup"><span data-stu-id="4fb29-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="4fb29-145">description</span><span class="sxs-lookup"><span data-stu-id="4fb29-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="4fb29-146">Descrive il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="4fb29-147">iconReference</span><span class="sxs-lookup"><span data-stu-id="4fb29-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="4fb29-148">Identifica la posizione di un'icona personalizzata per il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="4fb29-149">Collegamentoimmagine</span><span class="sxs-lookup"><span data-stu-id="4fb29-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="4fb29-150">Identifica la posizione di un'anteprima personalizzata per il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="4fb29-151">autore</span><span class="sxs-lookup"><span data-stu-id="4fb29-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="4fb29-152">Identifica l'autore del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="4fb29-153">dateCreated</span><span class="sxs-lookup"><span data-stu-id="4fb29-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="4fb29-154">Identifica la data di creazione del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="4fb29-155">templateInfo</span><span class="sxs-lookup"><span data-stu-id="4fb29-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="4fb29-156">Specifica un tipo di cartella per il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="4fb29-157">locationProvider</span><span class="sxs-lookup"><span data-stu-id="4fb29-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="4fb29-158">Specifica il provider di ricerca che deve essere usato da questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="4fb29-159">ambito</span><span class="sxs-lookup"><span data-stu-id="4fb29-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="4fb29-160">Specifica i percorsi da includere ed escludere dall'ambito di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="4fb29-161">propertyStore</span><span class="sxs-lookup"><span data-stu-id="4fb29-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="4fb29-162">Specifica il percorso di un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basato su XML per questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="4fb29-163">Il **IPropertyStore** supporta i metadati aperti del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="4fb29-164">includeInStartMenuScope</span><span class="sxs-lookup"><span data-stu-id="4fb29-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="4fb29-165">Specifica se la posizione rappresentata dal connettore di ricerca deve essere inclusa nell'ambito di ricerca del menu Start.</span><span class="sxs-lookup"><span data-stu-id="4fb29-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="4fb29-166">dominio</span><span class="sxs-lookup"><span data-stu-id="4fb29-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="4fb29-167">Identifica il dominio di primo livello del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4fb29-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="4fb29-168">supportsAdvancedQuerySyntax</span><span class="sxs-lookup"><span data-stu-id="4fb29-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="4fb29-169">Specifica se il connettore di ricerca supporta la sintassi di query avanzata (AQS).</span><span class="sxs-lookup"><span data-stu-id="4fb29-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="4fb29-170">isIndexed</span><span class="sxs-lookup"><span data-stu-id="4fb29-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="4fb29-171">Specifica se la posizione rappresentata dal connettore di ricerca è indicizzata.</span><span class="sxs-lookup"><span data-stu-id="4fb29-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="4fb29-172">Esempi di file di descrizione del connettore di ricerca</span><span class="sxs-lookup"><span data-stu-id="4fb29-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="4fb29-173">Di seguito è riportato un esempio di un file di descrizione del connettore di ricerca per un servizio Web di ricerca federata.</span><span class="sxs-lookup"><span data-stu-id="4fb29-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="4fb29-174">Di seguito è riportato un esempio di un file di descrizione del connettore di ricerca per un gestore di protocollo MAPI.</span><span class="sxs-lookup"><span data-stu-id="4fb29-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a><span data-ttu-id="4fb29-175">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="4fb29-175">Additional Resources</span></span>

-   <span data-ttu-id="4fb29-176">Per ulteriori informazioni sullo schema di descrizione della libreria, vedere [Library Description schema](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="4fb29-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="4fb29-177">Per altre informazioni sull'installazione di un connettore di ricerca, vedere [ricerca federata in Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4fb29-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fb29-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fb29-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4fb29-179">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4fb29-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4fb29-180">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="4fb29-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="4fb29-181">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4fb29-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4fb29-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="4fb29-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="4fb29-183">Area download Microsoft</span><span class="sxs-lookup"><span data-stu-id="4fb29-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
