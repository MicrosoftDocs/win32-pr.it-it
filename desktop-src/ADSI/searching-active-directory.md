---
title: Ricerca di Active Directory
description: Una funzione importante di Active Directory consiste nel risolvere le query sui dati degli utenti, nonché i dati di configurazione per i computer e i servizi.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Ricerca di Active Directory ADSI
- ADSI ADSI, ricerca in Active Directory
- query ADSI, ricerca Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328356"
---
# <a name="searching-active-directory"></a><span data-ttu-id="a6f4b-106">Ricerca di Active Directory</span><span class="sxs-lookup"><span data-stu-id="a6f4b-106">Searching Active Directory</span></span>

<span data-ttu-id="a6f4b-107">Una funzione importante di Active Directory consiste nel risolvere le query sui dati degli utenti, nonché i dati di configurazione per i computer e i servizi.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="a6f4b-108">Per scrivere query efficienti per Active Directory, è utile acquisire familiarità con quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a6f4b-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="a6f4b-109">Determinazione dell'ambito della query: è necessario che il client trovi proprietà per oggetti che potrebbero trovarsi in qualsiasi punto all'interno di una foresta o solo all'interno di un dominio o in una determinata unità organizzativa (OU)?</span><span class="sxs-lookup"><span data-stu-id="a6f4b-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="a6f4b-110">Determinazione della profondità della query: è necessario che la query cerchi un solo livello o possa incrociare altre directory LDAP?</span><span class="sxs-lookup"><span data-stu-id="a6f4b-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="a6f4b-111">Prestazioni e gestione di set di risultati di grandi dimensioni: in che modo il client può gestire efficacemente il potenziale di un set di risultati di grandi dimensioni?</span><span class="sxs-lookup"><span data-stu-id="a6f4b-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="a6f4b-112">Determinazione delle query migliori: quale tipo di query fornisce i risultati più efficienti?</span><span class="sxs-lookup"><span data-stu-id="a6f4b-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="a6f4b-113">Quale tipo di query lo sviluppatore deve evitare?</span><span class="sxs-lookup"><span data-stu-id="a6f4b-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="a6f4b-114">Informazioni sulla sintassi della query: ADSI supporta sia la sintassi LDAP come documentata in RFC 2254, sia un subset di SQL.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="a6f4b-115">Scelta delle interfacce: ADSI offre supporto OLE DB e un'interfaccia C/C++ denominata [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="a6f4b-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="a6f4b-116">Poiché ADSI funziona per più spazi dei nomi, è possibile utilizzare queste interfacce per eseguire query in altri spazi dei nomi, ad esempio Exchange, nonché Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="a6f4b-117">Poiché ADO (ActiveX Data Object) è un semplice modello a oggetti di accesso ai dati con script in OLE DB, le interfacce OLE DB sono ideali per Visual Basic programmatori e writer di script di pagine Web.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="a6f4b-118">Le nuove funzionalità di accesso ai dati in Visual Studio e nelle applicazioni di Office che sfruttano i vantaggi di ADO e OLE DB possono ora accedere ai dati di Active Directory in modo analogo all'accesso ai dati da altri provider OLE DB, ad esempio SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="a6f4b-119">Tuttavia, se uno sviluppatore C/C++ deve eseguire una semplice ricerca di directory, l'interfaccia **IDirectorySearch** potrebbe essere più appropriata delle interfacce OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a6f4b-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="a6f4b-120">Negli argomenti seguenti viene descritto come eseguire la ricerca Active Directory per assicurarsi che l'applicazione rilascia la query più efficiente, in base ai requisiti del client:</span><span class="sxs-lookup"><span data-stu-id="a6f4b-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="a6f4b-121">Ambito della query</span><span class="sxs-lookup"><span data-stu-id="a6f4b-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="a6f4b-122">Prestazioni e gestione di set di risultati di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="a6f4b-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="a6f4b-123">Sintassi del filtro di ricerca</span><span class="sxs-lookup"><span data-stu-id="a6f4b-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="a6f4b-124">Interfacce di query</span><span class="sxs-lookup"><span data-stu-id="a6f4b-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="a6f4b-125">Ricerca di dati binari</span><span class="sxs-lookup"><span data-stu-id="a6f4b-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="a6f4b-126">Query distribuite</span><span class="sxs-lookup"><span data-stu-id="a6f4b-126">Distributed Query</span></span>](distributed-query.md)

 

 




