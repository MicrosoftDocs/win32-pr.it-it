---
description: Il supporto di Windows 7 per la Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch consente agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse.
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Ricerca federata in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484436"
---
# <a name="federated-search-in-windows"></a><span data-ttu-id="29492-103">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="29492-103">Federated Search in Windows</span></span>

<span data-ttu-id="29492-104">Il supporto di Windows 7 per la Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch consente agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="29492-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span>

<span data-ttu-id="29492-105">Nell'elenco di argomenti riportato di seguito viene descritto come creare un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante la ricerca federata di Windows e come abilitare l'integrazione completa delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice sul lato client di Windows.</span><span class="sxs-lookup"><span data-stu-id="29492-105">The following list of topics describe how you can build a web-based data store that can be searched using Windows federated search, and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

-   [<span data-ttu-id="29492-106">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="29492-106">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
-   [<span data-ttu-id="29492-107">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="29492-107">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
-   [<span data-ttu-id="29492-108">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="29492-108">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
-   [<span data-ttu-id="29492-109">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="29492-109">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
-   [<span data-ttu-id="29492-110">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="29492-110">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
-   [<span data-ttu-id="29492-111">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="29492-111">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
-   [<span data-ttu-id="29492-112">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="29492-112">Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a><span data-ttu-id="29492-113">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="29492-113">Additional Resources</span></span>

-   <span data-ttu-id="29492-114">Nell'esempio di codice [OpenSearch](-search-sample-opensearch.md) viene illustrato come creare un servizio di ricerca federato utilizzando il protocollo [OpenSearch](https://github.com/dewitt/opensearch) e un file descrittore OpenSearch (con estensione osdx) (un connettore di ricerca).</span><span class="sxs-lookup"><span data-stu-id="29492-114">The [OpenSearch](-search-sample-opensearch.md) code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>
-   <span data-ttu-id="29492-115">Per una dimostrazione video della creazione di un servizio Web [OpenSearch](https://github.com/dewitt/opensearch) per un database SQL, vedere [Windows 7: consentire agli utenti di trovare, visualizzare e organizzare i dati con librerie e Esplora risorse](https://channel9.msdn.com/pdc2008/PC16/).</span><span class="sxs-lookup"><span data-stu-id="29492-115">For a video demonstration of creating an [OpenSearch](https://github.com/dewitt/opensearch) web service for a SQL database, see [Windows 7: Empower Users to Find, Visualize and Organize their Data with Libraries and the Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span></span>
-   <span data-ttu-id="29492-116">Se si sta scrivendo un provider [OpenSearch](https://github.com/dewitt/opensearch) sul lato client, vedere:</span><span class="sxs-lookup"><span data-stu-id="29492-116">If you are writing a client-side [OpenSearch](https://github.com/dewitt/opensearch) provider, see:</span></span>
    -   <span data-ttu-id="29492-117">Guida per gli [sviluppatori di OpenSearch](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) per altre informazioni sulla connessione a un provider lato client usando i protocolli o le API di un archivio dati proprietario.</span><span class="sxs-lookup"><span data-stu-id="29492-117">The [OpenSearch Developer How To Guide](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) for more information on connecting to a client-side provider by using a proprietary data store's protocols or APIs.</span></span>
    -   <span data-ttu-id="29492-118">Panoramica della documentazione dello schema della [Descrizione del connettore di ricerca](search-sconn-desc-schema-entry.md) (. searchconnector-ms).</span><span class="sxs-lookup"><span data-stu-id="29492-118">The [Overview of the Search Connector Description Schema](search-sconn-desc-schema-entry.md) (.searchconnector-ms) schema documentation.</span></span>
-   <span data-ttu-id="29492-119">Visitare il sito Web [area download Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) per la seguente risorsa scaricabile: esempio di ricerca Server 2008: connettore di ricerca federata.</span><span class="sxs-lookup"><span data-stu-id="29492-119">See the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) website for the following downloadable resource: Search Server 2008 Sample: Federated Search Connector Sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29492-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29492-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29492-121">Panoramica di Windows Search</span><span class="sxs-lookup"><span data-stu-id="29492-121">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="29492-122">Guida per gli sviluppatori di Windows Search</span><span class="sxs-lookup"><span data-stu-id="29492-122">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="29492-123">Informazioni di riferimento su Windows Search</span><span class="sxs-lookup"><span data-stu-id="29492-123">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="29492-124">Esempi di codice di Windows Search</span><span class="sxs-lookup"><span data-stu-id="29492-124">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="29492-125">Tecnologie di ricerca correlate</span><span class="sxs-lookup"><span data-stu-id="29492-125">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)
</dt> <dt>

[<span data-ttu-id="29492-126">Glossario di Windows Search</span><span class="sxs-lookup"><span data-stu-id="29492-126">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 



