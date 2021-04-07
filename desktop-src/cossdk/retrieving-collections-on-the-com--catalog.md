---
description: Recupero di raccolte nel catalogo COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recupero di raccolte nel catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748031"
---
# <a name="retrieving-collections-on-the-com-catalog"></a><span data-ttu-id="eaf80-103">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="eaf80-103">Retrieving Collections on the COM+ Catalog</span></span>

<span data-ttu-id="eaf80-104">I dati nel catalogo COM+ vengono archiviati all'interno di una gerarchia di raccolte.</span><span class="sxs-lookup"><span data-stu-id="eaf80-104">Data on the COM+ catalog is stored within a hierarchy of collections.</span></span> <span data-ttu-id="eaf80-105">Nello strumento di amministrazione Servizi componenti, molte di queste raccolte vengono visualizzate come cartelle nell'albero della console.</span><span class="sxs-lookup"><span data-stu-id="eaf80-105">In the Component Services administrative tool, many of these collections appear as folders in the console tree.</span></span> <span data-ttu-id="eaf80-106">È possibile accedere alle raccolte che non sono visualizzate come cartelle solo a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="eaf80-106">Collections that don't appear as folders can be accessed only programmatically.</span></span> <span data-ttu-id="eaf80-107">Le raccolte vengono utilizzate come contenitori per gli elementi.</span><span class="sxs-lookup"><span data-stu-id="eaf80-107">Collections serve as containers for items.</span></span> <span data-ttu-id="eaf80-108">Gli elementi di una raccolta specifica sono tutti di un tipo coerente; ovvero tutti rappresentano lo stesso tipo di elemento e può essere presente un numero arbitrario di elementi in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="eaf80-108">The items in a given collection are all of a consistent type; that is, they all represent the same kind of element, and there can be an arbitrary number of items in a collection.</span></span> <span data-ttu-id="eaf80-109">La raccolta [**Applications**](applications.md) , ad esempio, contiene un elemento per ogni applicazione com+ installata nel computer.</span><span class="sxs-lookup"><span data-stu-id="eaf80-109">For example, the [**Applications**](applications.md) collection contains an item for each COM+ application that is installed on the machine.</span></span> <span data-ttu-id="eaf80-110">Questa raccolta viene visualizzata nello strumento di amministrazione come cartella **applicazioni com+** .</span><span class="sxs-lookup"><span data-stu-id="eaf80-110">This collection appears in the administrative tool as the **COM+ Applications** folder.</span></span>

<span data-ttu-id="eaf80-111">Le raccolte si verificano in una struttura gerarchica perché gli elementi che contengono seguono un ordine di inclusione innato.</span><span class="sxs-lookup"><span data-stu-id="eaf80-111">The collections occur in a hierarchical structure because the elements they contain follow an innate order of inclusion.</span></span> <span data-ttu-id="eaf80-112">Poiché, ad esempio, i componenti vengono installati in un'applicazione COM+, la raccolta [**Components**](components.md) viene configurata logicamente nella raccolta di [**applicazioni**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf80-112">For example, because components are installed into a COM+ application, the [**Components**](components.md) collection is logically subsumed under the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="eaf80-113">In particolare, per conservare i componenti installati in un'applicazione specifica, è presente una raccolta di **componenti** distinti per ogni elemento nella raccolta di **applicazioni** .</span><span class="sxs-lookup"><span data-stu-id="eaf80-113">More particularly, to hold the components installed into that particular application, there is a distinct **Components** collection for each item in the **Applications** collection.</span></span>

<span data-ttu-id="eaf80-114">È necessario ottenere una raccolta nel catalogo quando si desidera recuperare un elemento e impostare le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="eaf80-114">You must get a collection on the catalog whenever you want to retrieve an item and set properties on it.</span></span> <span data-ttu-id="eaf80-115">Nel caso generale, è necessario eseguire diverse raccolte per ottenere l'elemento desiderato.</span><span class="sxs-lookup"><span data-stu-id="eaf80-115">In the general case, you need to step through several collections to get to the element you want.</span></span> <span data-ttu-id="eaf80-116">Per la procedura per eseguire questa operazione, vedere [esplorazione della gerarchia della raccolta com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="eaf80-116">For the procedure for doing this, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="eaf80-117">Dopo aver recuperato una raccolta e prima di poter utilizzare direttamente gli elementi in esso contenuti, è necessario popolare la raccolta, che recupera i dati per il contenuto della raccolta dal catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="eaf80-117">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection, which fetches data for the collection's contents from the COM+ catalog.</span></span> <span data-ttu-id="eaf80-118">Per informazioni dettagliate, vedere [popolamento di raccolte com+](populating-com--collections.md).</span><span class="sxs-lookup"><span data-stu-id="eaf80-118">For details, see [Populating COM+ Collections](populating-com--collections.md).</span></span>

<span data-ttu-id="eaf80-119">Inoltre, è possibile usare una funzionalità che consente di eseguire query in modo dinamico per vedere quali raccolte correlate sono disponibili da una determinata raccolta che si sta mantenendo.</span><span class="sxs-lookup"><span data-stu-id="eaf80-119">Additionally, there is a facility you can use that enables you to dynamically query to see what related collections are available from a given collection you are holding.</span></span> <span data-ttu-id="eaf80-120">Per informazioni dettagliate, vedere [esecuzione di query per le raccolte correlate disponibili](querying-for-available-related-collections.md).</span><span class="sxs-lookup"><span data-stu-id="eaf80-120">For details, see [Querying for Available Related Collections](querying-for-available-related-collections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaf80-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaf80-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf80-122">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="eaf80-122">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
</dt> <dt>

[<span data-ttu-id="eaf80-123">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="eaf80-123">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="eaf80-124">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="eaf80-124">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="eaf80-125">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="eaf80-125">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="eaf80-126">Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="eaf80-126">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



