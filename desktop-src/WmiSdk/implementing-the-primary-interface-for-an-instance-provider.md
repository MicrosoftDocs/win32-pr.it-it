---
title: Implementazione di un'interfaccia primaria del provider di istanze
description: Un provider di istanze usa i metodi asincroni di IWbemServices come interfaccia principale di WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315212"
---
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="7e115-103">Implementazione di un'interfaccia primaria del provider di istanze</span><span class="sxs-lookup"><span data-stu-id="7e115-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="7e115-104">Un provider di istanze usa i metodi asincroni di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia principale di WMI.</span><span class="sxs-lookup"><span data-stu-id="7e115-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="7e115-105">Implementando solo i metodi che soddisfano le esigenze del provider di istanze, è possibile ridurre la quantità di risorse di cui si dedica la codifica.</span><span class="sxs-lookup"><span data-stu-id="7e115-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="7e115-106">Tuttavia, implementando metodi riservati per altri tipi di provider, è possibile ridurre il numero di provider scritti.</span><span class="sxs-lookup"><span data-stu-id="7e115-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="7e115-107">Poiché è usato anche da applicazioni e provider per richiedere servizi di WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contiene molti metodi irrilevanti per un provider di istanze.</span><span class="sxs-lookup"><span data-stu-id="7e115-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="7e115-108">Nella tabella seguente sono elencati i metodi **IWbemServices** che è possibile implementare per un provider di istanze.</span><span class="sxs-lookup"><span data-stu-id="7e115-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="7e115-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="7e115-109">Method</span></span>                                                                   | <span data-ttu-id="7e115-110">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="7e115-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="7e115-111">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="7e115-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="7e115-112">Recupero</span><span class="sxs-lookup"><span data-stu-id="7e115-112">Retrieval</span></span>        |
| [<span data-ttu-id="7e115-113">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="7e115-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="7e115-114">Modifica</span><span class="sxs-lookup"><span data-stu-id="7e115-114">Modification</span></span>     |
| [<span data-ttu-id="7e115-115">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="7e115-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="7e115-116">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="7e115-116">Deletion</span></span>         |
| [<span data-ttu-id="7e115-117">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="7e115-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="7e115-118">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="7e115-118">Enumeration</span></span>      |
| [<span data-ttu-id="7e115-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="7e115-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="7e115-120">Elaborazione di query</span><span class="sxs-lookup"><span data-stu-id="7e115-120">Query processing</span></span> |



 

<span data-ttu-id="7e115-121">Per i metodi che non vengono usati, il provider può fornire un'implementazione stub che restituisce **il \_ provider WBEM E che \_ non è \_ \_ in grado** di supportare.</span><span class="sxs-lookup"><span data-stu-id="7e115-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="7e115-122">Sono inclusi tutti i metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) non elencati nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="7e115-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="7e115-123">Un singolo provider può agire simultaneamente come provider di classi, istanze e metodi mediante la registrazione e l'implementazione appropriate di tutti i metodi pertinenti.</span><span class="sxs-lookup"><span data-stu-id="7e115-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="7e115-124">Per ulteriori informazioni, vedere [scrittura di un provider di classi](writing-a-class-provider.md) e [scrittura di un provider di metodi](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7e115-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



