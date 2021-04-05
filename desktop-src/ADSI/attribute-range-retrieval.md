---
title: Recupero intervallo attributi
description: Un attributo multivalore può contenere quasi un numero qualsiasi di valori. In molti casi può essere vantaggioso, o addirittura necessario, limitare l'intervallo di valori recuperati da una query.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI recupero intervallo attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955113"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="80b30-105">Recupero intervallo attributi</span><span class="sxs-lookup"><span data-stu-id="80b30-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="80b30-106">Un attributo multivalore può contenere quasi un numero qualsiasi di valori.</span><span class="sxs-lookup"><span data-stu-id="80b30-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="80b30-107">In molti casi può essere vantaggioso, o addirittura necessario, limitare l'intervallo di valori recuperati da una query.</span><span class="sxs-lookup"><span data-stu-id="80b30-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="80b30-108">Il recupero di intervalli implica la richiesta di un numero limitato di valori di attributo in una singola query.</span><span class="sxs-lookup"><span data-stu-id="80b30-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="80b30-109">Il numero di valori richiesti deve essere minore o uguale al numero massimo di valori supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="80b30-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="80b30-110">Per ridurre il numero di volte in cui la query deve contattare il server, il numero di valori richiesti dovrebbe essere il più vicino possibile al massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="80b30-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="80b30-111">Per consentire a un'applicazione di funzionare correttamente con tutti i server Windows, è necessario usare un numero massimo di 1000.</span><span class="sxs-lookup"><span data-stu-id="80b30-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="80b30-112">Gli identificatori di intervallo per una query di proprietà richiedono il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="80b30-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="80b30-113">dove " &lt; intervallo minimo &gt; " è l'indice in base zero del primo valore della proprietà da recuperare e " &lt; intervallo elevato &gt; " è l'indice in base zero dell'ultimo valore della proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="80b30-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="80b30-114">Per &lt; &gt; specificare la prima voce, viene utilizzato zero per "intervallo minimo".</span><span class="sxs-lookup"><span data-stu-id="80b30-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="80b30-115">Il carattere jolly ( \* ) può essere usato per " &lt; intervallo elevato &gt; " per specificare tutte le voci rimanenti.</span><span class="sxs-lookup"><span data-stu-id="80b30-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="80b30-116">Nella tabella seguente sono elencati esempi di identificatori di intervallo.</span><span class="sxs-lookup"><span data-stu-id="80b30-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="80b30-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="80b30-117">Example</span></span>      | <span data-ttu-id="80b30-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80b30-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b30-119">intervallo = 0-\*</span><span class="sxs-lookup"><span data-stu-id="80b30-119">range=0-\*</span></span>   | <span data-ttu-id="80b30-120">Recuperare tutti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="80b30-120">Retrieve all property values.</span></span> <span data-ttu-id="80b30-121">Questa operazione è soggetta ai limiti imposti dal server.</span><span class="sxs-lookup"><span data-stu-id="80b30-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="80b30-122">intervallo = 0-500</span><span class="sxs-lookup"><span data-stu-id="80b30-122">range=0-500</span></span>  | <span data-ttu-id="80b30-123">Recuperare da 1 a 501st valori inclusivi.</span><span class="sxs-lookup"><span data-stu-id="80b30-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="80b30-124">intervallo = 2-3</span><span class="sxs-lookup"><span data-stu-id="80b30-124">range=2-3</span></span>    | <span data-ttu-id="80b30-125">Recuperare i valori 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="80b30-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="80b30-126">intervallo = 501-\*</span><span class="sxs-lookup"><span data-stu-id="80b30-126">range=501-\*</span></span> | <span data-ttu-id="80b30-127">Recuperare 502nd e tutti i valori rimanenti.</span><span class="sxs-lookup"><span data-stu-id="80b30-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="80b30-128">Questa operazione è soggetta ai limiti imposti dal server.</span><span class="sxs-lookup"><span data-stu-id="80b30-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="80b30-129">Esistono diversi modi per recuperare un intervallo di valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="80b30-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="80b30-130">Il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) può essere usato in un linguaggio di automazione o in C++.</span><span class="sxs-lookup"><span data-stu-id="80b30-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="80b30-131">Il metodo **IADs. GetInfoEx** è il metodo preferito per eseguire il recupero di intervalli.</span><span class="sxs-lookup"><span data-stu-id="80b30-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="80b30-132">Per ulteriori informazioni sull'utilizzo di **IADs. GetInfoEx** per il recupero di intervalli, vedere [utilizzo di IADs:: GetInfoEx per il recupero di intervalli](using-iads--getinfoex-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="80b30-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="80b30-133">Se viene utilizzato un linguaggio di automazione, è possibile utilizzare ADO (ActiveX Directory Objects) per recuperare un intervallo di valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="80b30-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="80b30-134">Per ulteriori informazioni sull'utilizzo di ADO per il recupero di intervalli, vedere [utilizzo di ADO per il recupero di intervalli](using-ado-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="80b30-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="80b30-135">Se si usa C++, le interfacce [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) possono essere usate per recuperare un intervallo di valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="80b30-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="80b30-136">Per altre informazioni sull'uso di **IDirectorySearch** e **IDirectoryObject** per il recupero di intervalli, vedere [uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="80b30-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




