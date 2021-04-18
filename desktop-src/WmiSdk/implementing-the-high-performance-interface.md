---
description: Poiché WMI carica un provider a prestazioni elevate in-process in WMI o in un'applicazione client, è necessario progettare il provider a prestazioni elevate come server in-process.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315217"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="d60db-103">Implementazione dell'interfaccia High-Performance</span><span class="sxs-lookup"><span data-stu-id="d60db-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="d60db-104">Poiché WMI carica un provider a prestazioni elevate in-process in WMI o in un'applicazione client, è necessario progettare il provider a prestazioni elevate come server in-process.</span><span class="sxs-lookup"><span data-stu-id="d60db-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="d60db-105">Inoltre, è necessario implementare i metodi del provider a prestazioni elevate nelle interfacce [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .</span><span class="sxs-lookup"><span data-stu-id="d60db-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="d60db-106">È necessario implementare un provider a prestazioni elevate come server in-process.</span><span class="sxs-lookup"><span data-stu-id="d60db-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="d60db-107">Una funzionalità da tenere presente quando si implementa la sicurezza di un server in-process è il modo in cui il provider identifica il proprio percorso.</span><span class="sxs-lookup"><span data-stu-id="d60db-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="d60db-108">Quando viene caricato in-process in WMI, WMI crea un'istanza del provider utilizzando un CLSID.</span><span class="sxs-lookup"><span data-stu-id="d60db-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="d60db-109">Quando viene caricato in un processo in un'applicazione client, l'applicazione client crea un'istanza del provider con la proprietà **ClientLoadableCLSID** .</span><span class="sxs-lookup"><span data-stu-id="d60db-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="d60db-110">Se si assegnano valori diversi a un CLSID e a **ClientLoadableCLSID**, si consente al provider di determinare se viene caricato in-process in WMI o in un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d60db-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="d60db-111">Se si trova in un processo WMI, il provider deve eseguire la rappresentazione client necessaria usando **ClientLoadableCLSID**.</span><span class="sxs-lookup"><span data-stu-id="d60db-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="d60db-112">Se si trova in un processo client, il provider eredita il token di accesso del thread su cui è stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="d60db-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="d60db-113">Per ulteriori informazioni sull'implementazione di un server in-process, vedere la [sezione com](https://msdn.microsoft.com/library/aa139695.aspx) di MSDN.</span><span class="sxs-lookup"><span data-stu-id="d60db-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="d60db-114">Come server in-process, un provider a prestazioni elevate utilizza un oggetto di aggiornamento per garantire la presenza di dati correnti per il client remoto.</span><span class="sxs-lookup"><span data-stu-id="d60db-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="d60db-115">Nella tabella seguente sono elencati i metodi che è necessario implementare per un provider a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="d60db-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="d60db-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="d60db-116">Method</span></span>                                                                                              | <span data-ttu-id="d60db-117">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="d60db-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="d60db-118">**IWbemHiPerfProvider::QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="d60db-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="d60db-119">Query</span><span class="sxs-lookup"><span data-stu-id="d60db-119">Queries</span></span>                                           |
| [<span data-ttu-id="d60db-120">**IWbemHiPerfProvider:: GetObjects**</span><span class="sxs-lookup"><span data-stu-id="d60db-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="d60db-121">Recupero di oggetti</span><span class="sxs-lookup"><span data-stu-id="d60db-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="d60db-122">**IWbemHiPerfProvider::CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="d60db-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="d60db-123">Consente di creare un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d60db-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="d60db-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="d60db-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="d60db-125">Crea un oggetto istanza aggiornabile</span><span class="sxs-lookup"><span data-stu-id="d60db-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="d60db-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="d60db-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="d60db-127">Crea un enumeratore aggiornabile</span><span class="sxs-lookup"><span data-stu-id="d60db-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="d60db-128">**IWbemHiPerfProvider::StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="d60db-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="d60db-129">Interrompe l'aggiornamento di un oggetto enumeratore o istanza</span><span class="sxs-lookup"><span data-stu-id="d60db-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="d60db-130">**IWbemRefresher:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="d60db-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="d60db-131">Consente di creare un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d60db-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="d60db-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d60db-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d60db-133">Creazione di un provider di istanze in un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="d60db-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



