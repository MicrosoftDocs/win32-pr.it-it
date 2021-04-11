---
description: Windows Search SDK fornisce un assembly di interoperabilità che consente di utilizzare gli oggetti Component Object Model (COM) esposti da ricerca di Windows e altri programmi rispetto alle interfacce e alle classi utilizzando codice gestito.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Uso di codice gestito con i dati della shell e Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128607"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="0cbcb-103">Uso di codice gestito con i dati della shell e Windows Search</span><span class="sxs-lookup"><span data-stu-id="0cbcb-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="0cbcb-104">Windows Search SDK fornisce un assembly di interoperabilità che consente di utilizzare gli oggetti Component Object Model (COM) esposti da ricerca di Windows e altri programmi rispetto alle interfacce e alle classi utilizzando codice gestito.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="0cbcb-105">L'assembly di interoperabilità è firmato digitalmente da Microsoft e può essere trovato con gli [esempi di Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="0cbcb-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="0cbcb-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="0cbcb-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0cbcb-107">Uso del codepack API Windows</span><span class="sxs-lookup"><span data-stu-id="0cbcb-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="0cbcb-108">Accesso ai risultati dell'indice</span><span class="sxs-lookup"><span data-stu-id="0cbcb-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="0cbcb-109">Applicazione di esempio con il codepack API Windows</span><span class="sxs-lookup"><span data-stu-id="0cbcb-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="0cbcb-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cbcb-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="0cbcb-111">Uso del codepack API Windows</span><span class="sxs-lookup"><span data-stu-id="0cbcb-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="0cbcb-112">Se si lavora nell'ambiente Microsoft .NET, usare il pacchetto di [codice dell'API Windows per Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) per ottenere i risultati della ricerca o semplicemente esplorare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="0cbcb-113">Il [pacchetto di codice API Windows per Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) fornisce una raccolta di elementi della shell che sono essenzialmente wrapper intorno all' [interfaccia IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)nativa.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="0cbcb-114">È possibile eseguire l'iterazione di questa raccolta e ottenere i diversi valori di proprietà in modo analogo a come si enumerano i risultati in una tabella da una query di collegamento e incorporamento di un database (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="0cbcb-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="0cbcb-115">Il frammento di codice seguente illustra come eseguire l'iterazione degli elementi di ricerca e ottenere i valori delle proprietà per ognuno.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="0cbcb-116">Accesso ai risultati dell'indice</span><span class="sxs-lookup"><span data-stu-id="0cbcb-116">Accessing Index Results</span></span>

<span data-ttu-id="0cbcb-117">È possibile accedere ai risultati degli indici tramite OLE DB o il modello di dati della shell.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="0cbcb-118">Uno dei due approcci presenta vantaggi e svantaggi.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="0cbcb-119">Un vantaggio è che OLE DB e Structured Query Language (SQL) sono familiari ai programmatori di database.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="0cbcb-120">Altri vantaggi sono il controllo migliore sulle prestazioni quando si eseguono query solo nell'indicizzatore e l'accesso a funzionalità aggiuntive, ad esempio la possibilità di individuare rapidamente i risultati precedenti in un nuovo set di righe.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="0cbcb-121">I vantaggi del modello di dati della shell sono l'astrazione tra diverse fonti di informazioni, ad esempio OpenSearch, e fornisce l'accesso a funzionalità aggiuntive, ad esempio anteprime e gestori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="0cbcb-122">Il modello a oggetti della shell, inoltre, richiede un supporto speciale per i risultati non filename, ad esempio gli elementi di posta e i risultati di OneNote, né per gli elementi che si trovano nell'indice dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="0cbcb-123">Si noti che nella shell [KNOWNFOLDERID](../shell/knownfolderid.md) è l'ambito di cartella noto per il contenuto indicizzato locale.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="0cbcb-124">Per ulteriori informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0cbcb-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="0cbcb-125">Le origini dati OpenSearch non vengono esposte tramite OLE DB per la ricerca federata in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="0cbcb-126">Per questo motivo, è consigliabile prendere in considerazione la scrittura di un provider LINQ per lo spazio dei nomi della shell invece di usare OLE DB per accedere ai risultati dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="0cbcb-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="0cbcb-127">Per ulteriori informazioni, vedere [procedura dettagliata: creazione di un provider LINQ IQueryable](/previous-versions/bb546158(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="0cbcb-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="0cbcb-128">Applicazione di esempio con il codepack API Windows</span><span class="sxs-lookup"><span data-stu-id="0cbcb-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="0cbcb-129">Lo screenshot seguente rappresenta una simulazione di un'applicazione di esempio creata con il [pacchetto di codice API Windows per Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span><span class="sxs-lookup"><span data-stu-id="0cbcb-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![screenshot dell'applicazione Media Player che mostra i messaggi di posta elettronica](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="0cbcb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cbcb-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0cbcb-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0cbcb-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0cbcb-133">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="0cbcb-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="0cbcb-134">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="0cbcb-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0cbcb-135">[Interoperabilità tra linguaggi diversi](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="0cbcb-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
