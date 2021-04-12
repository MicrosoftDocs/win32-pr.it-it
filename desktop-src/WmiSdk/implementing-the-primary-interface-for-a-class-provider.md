---
description: "Esistono due modi per implementare un provider di classi: implementare l'interfaccia come provider di push o come provider di pull."
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346726"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="c8544-103">Implementazione dell'interfaccia primaria per un provider di classi</span><span class="sxs-lookup"><span data-stu-id="c8544-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="c8544-104">Esistono due modi per implementare un provider di classi: implementare l'interfaccia come provider di push o come provider di pull.</span><span class="sxs-lookup"><span data-stu-id="c8544-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="c8544-105">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="c8544-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c8544-106">Implementazione dell'interfaccia primaria per un provider di classi push</span><span class="sxs-lookup"><span data-stu-id="c8544-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="c8544-107">Implementazione dell'interfaccia primaria per un provider di classi pull</span><span class="sxs-lookup"><span data-stu-id="c8544-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="c8544-108">Implementazione dell'interfaccia primaria per un provider di classi push</span><span class="sxs-lookup"><span data-stu-id="c8544-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="c8544-109">Mentre tutti i provider implementano [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per l'inizializzazione e almeno un'altra interfaccia come interfaccia primaria, un provider di push implementa solo **IWbemProviderInit**.</span><span class="sxs-lookup"><span data-stu-id="c8544-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="c8544-110">Verificare che l'implementazione esegua le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8544-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="c8544-111">Recupera i dati della classe appropriati.</span><span class="sxs-lookup"><span data-stu-id="c8544-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="c8544-112">Inserisce i dati nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="c8544-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="c8544-113">Elimina i dati obsoleti.</span><span class="sxs-lookup"><span data-stu-id="c8544-113">Deletes obsolete data.</span></span>

<span data-ttu-id="c8544-114">Al termine del processo di inizializzazione, WMI gestisce tutte le richieste dell'applicazione per le classi appartenenti al provider di push senza ulteriori interazioni con i provider.</span><span class="sxs-lookup"><span data-stu-id="c8544-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="c8544-115">Successivamente, il provider di push funge da client di WMI anziché da provider.</span><span class="sxs-lookup"><span data-stu-id="c8544-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="c8544-116">Per ulteriori informazioni sull'implementazione di [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), vedere [inizializzazione di un provider](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c8544-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="c8544-117">Quando si chiama WMI per creare, aggiornare o rimuovere dati in un provider di push, impostare il parametro *è* in modo da includere il flag di **aggiornamento del proprietario del \_ flag \_ \_ WBEM** in tutte le chiamate ai metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="c8544-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="c8544-118">Implementazione dell'interfaccia primaria per un provider di classi pull</span><span class="sxs-lookup"><span data-stu-id="c8544-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="c8544-119">Un provider di pull della classe deve implementare [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia primaria.</span><span class="sxs-lookup"><span data-stu-id="c8544-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="c8544-120">L'interfaccia **IWbemServices** supporta il recupero dei dati, l'aggiornamento dei dati, la rimozione dei dati, l'enumerazione e l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="c8544-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="c8544-121">Tuttavia, poiché **IWbemServices** viene utilizzato anche da applicazioni e provider per richiedere servizi di WMI, **IWbemServices** contiene molti metodi irrilevanti per un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="c8544-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="c8544-122">L'implementazione deve supportare il recupero e l'enumerazione delle classi, rispettivamente tramite i metodi [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .</span><span class="sxs-lookup"><span data-stu-id="c8544-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="c8544-123">Nella tabella seguente sono elencati i metodi **IWbemServices** asincroni aggiuntivi che è possibile implementare per un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="c8544-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="c8544-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="c8544-124">Method</span></span>                                                     | <span data-ttu-id="c8544-125">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="c8544-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="c8544-126">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="c8544-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="c8544-127">Modifica</span><span class="sxs-lookup"><span data-stu-id="c8544-127">Modification</span></span> |
| [<span data-ttu-id="c8544-128">**DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="c8544-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="c8544-129">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="c8544-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="c8544-130">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="c8544-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="c8544-131">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c8544-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="c8544-132">Il provider di classi deve fornire un'implementazione dello stub che restituisce il **\_ provider WBEM E \_ \_ non \_ idoneo** per tutti gli altri metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che non supportano il set di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c8544-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="c8544-133">In particolare, WMI non supporta l'elaborazione di query per i provider di classi.</span><span class="sxs-lookup"><span data-stu-id="c8544-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="c8544-134">Di conseguenza, un provider di classi deve restituire il **\_ provider WBEM E \_ non è \_ \_ in grado** di eseguire l'implementazione di [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), impostare la proprietà di registrazione **QuerySupportLevels** su **null** o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c8544-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="c8544-135">Le interfacce implementate da un provider di classi sono molto simili alle interfacce per un provider di istanze e un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="c8544-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="c8544-136">Infatti, un singolo provider può fungere da tutti e tre i tipi di provider implementando tutti i metodi e la registrazione corretta.</span><span class="sxs-lookup"><span data-stu-id="c8544-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



