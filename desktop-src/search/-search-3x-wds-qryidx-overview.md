---
description: Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Esecuzione di query sull'indice a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306176"
---
# <a name="querying-the-index-programmatically"></a><span data-ttu-id="3e72f-103">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="3e72f-103">Querying the Index Programmatically</span></span>

<span data-ttu-id="3e72f-104">Sono disponibili diversi modi per utilizzare la ricerca di Windows per eseguire una query sull'indice.</span><span class="sxs-lookup"><span data-stu-id="3e72f-104">There are several ways to use Windows Search to query the index.</span></span>

<span data-ttu-id="3e72f-105">Questa sezione fornisce il framework concettuale per l'esecuzione di query sull'indice a livello di codice:</span><span class="sxs-lookup"><span data-stu-id="3e72f-105">This section provides the conceptual framework for querying the index programmatically:</span></span>

-   [<span data-ttu-id="3e72f-106">Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice</span><span class="sxs-lookup"><span data-stu-id="3e72f-106">Using SQL and AQS Approaches to Query the Index</span></span>](using-sql-and-aqs-to-query-the-index.md)
-   [<span data-ttu-id="3e72f-107">Esecuzione di query sull'indice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="3e72f-107">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [<span data-ttu-id="3e72f-108">Esecuzione di query sull'indice con il protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="3e72f-108">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
-   [<span data-ttu-id="3e72f-109">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="3e72f-109">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
-   [<span data-ttu-id="3e72f-110">Uso della sintassi avanzata delle query a livello di codice</span><span class="sxs-lookup"><span data-stu-id="3e72f-110">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)

> [!Note]  
> <span data-ttu-id="3e72f-111">Compatibilità di Microsoft Windows Desktop Search (WDS) 2x: nei computer che eseguono Windows XP e versioni successive [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) è deprecato.</span><span class="sxs-lookup"><span data-stu-id="3e72f-111">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="3e72f-112">Gli sviluppatori devono invece usare [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) per ottenere una stringa di connessione e analizzare la query dell'utente in Structured Query Language (SQL), quindi eseguire una query tramite il collegamento all'oggetto e il database di incorporamento (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="3e72f-112">Instead, developers should use [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string and to parse the user's query into Structured Query Language (SQL), and then query through Object Linking and Embedding Database (OLE DB).</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="3e72f-113">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3e72f-113">Additional Resources</span></span>

-   <span data-ttu-id="3e72f-114">Per informazioni su OLE DB, vedere [Cenni preliminari sulla programmazione OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="3e72f-114">For information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span></span> <span data-ttu-id="3e72f-115">Per informazioni sul provider di dati di .NET Framework per OLE DB, vedere lo [spazio dei nomi System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span><span class="sxs-lookup"><span data-stu-id="3e72f-115">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span></span>
-   <span data-ttu-id="3e72f-116">Per ulteriori informazioni sull'utilizzo delle proprietà nell'esecuzione di query, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e72f-116">For additional background on using properties in querying, see the following topics:</span></span>
    -   [<span data-ttu-id="3e72f-117">Sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="3e72f-117">Property System</span></span>](../properties/building-property-handlers.md)
    -   <span data-ttu-id="3e72f-118">[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="3e72f-118">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
-   <span data-ttu-id="3e72f-119">Per informazioni su come creare e modificare le cartelle di ricerca, vedere [**interfaccia ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span><span class="sxs-lookup"><span data-stu-id="3e72f-119">For information on how to create and modify search folders, see [**ISearchFolderItemFactory Interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span></span>
-   <span data-ttu-id="3e72f-120">Per le bacheche dei messaggi di discussione e domande supportate dalla community sulle tecnologie di ricerca, vedere il [Forum MSDN relativo allo sviluppo per Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="3e72f-120">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
-   <span data-ttu-id="3e72f-121">Per scaricare gli esempi di codice dell'SDK di ricerca:</span><span class="sxs-lookup"><span data-stu-id="3e72f-121">To download the Search SDK Code Samples:</span></span>
    -   <span data-ttu-id="3e72f-122">Per Windows 7: [esempi di Windows Search su GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span><span class="sxs-lookup"><span data-stu-id="3e72f-122">For Windows 7: [Windows Search Samples on GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span></span>
    -   <span data-ttu-id="3e72f-123">Per Windows Vista: [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span><span class="sxs-lookup"><span data-stu-id="3e72f-123">For Windows Vista: [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span></span>
-   <span data-ttu-id="3e72f-124">Per scaricare il Windows SDK:</span><span class="sxs-lookup"><span data-stu-id="3e72f-124">To download the Windows SDK:</span></span>
    -   <span data-ttu-id="3e72f-125">Per Windows 7: [Windows SDK per Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e72f-125">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>
    -   <span data-ttu-id="3e72f-126">Per Windows Vista: [Windows SDK per Windows Vista e .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span><span class="sxs-lookup"><span data-stu-id="3e72f-126">For Windows Vista: [Windows SDK for Windows Vista and .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e72f-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e72f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e72f-128">Guida allo sviluppo di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3e72f-128">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="3e72f-129">Gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="3e72f-129">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3e72f-130">Estensione dell'indice di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="3e72f-130">Extending the Windows Search Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[<span data-ttu-id="3e72f-131">Estensione delle risorse della lingua</span><span class="sxs-lookup"><span data-stu-id="3e72f-131">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
