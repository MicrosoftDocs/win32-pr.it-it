---
title: Panoramica delle interfacce di rete
description: Panoramica delle interfacce di rete
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media Format SDK, interfacce di rete
- Windows Media Format SDK, interfacce
- ASF (Advanced Systems Format), interfacce di rete
- ASF (formato avanzato dei sistemi), interfacce di rete
- ASF (Advanced Systems Format), elenco di interfacce per le funzionalità di rete
- ASF (Advanced Systems Format), elenco di interfacce per le funzionalità di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724132"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="84bc1-109">Panoramica delle interfacce di rete</span><span class="sxs-lookup"><span data-stu-id="84bc1-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="84bc1-110">Le funzionalità di rete di questo SDK sono supportate tramite i metodi delle interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="84bc1-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="84bc1-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="84bc1-111">Interface</span></span>                                                  | <span data-ttu-id="84bc1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84bc1-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84bc1-113">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="84bc1-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="84bc1-114">Ottiene informazioni sui client connessi a un sink di rete.</span><span class="sxs-lookup"><span data-stu-id="84bc1-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="84bc1-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="84bc1-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="84bc1-116">Fornisce un metodo per ottenere informazioni su un client collegato a un sink di rete del writer.</span><span class="sxs-lookup"><span data-stu-id="84bc1-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="84bc1-117">Questa interfaccia estende l'interfaccia **IWMClientConnections** .</span><span class="sxs-lookup"><span data-stu-id="84bc1-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="84bc1-118">**IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="84bc1-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="84bc1-119">Fornisce un metodo di callback per acquisire le credenziali utente quando si accede a un sito remoto.</span><span class="sxs-lookup"><span data-stu-id="84bc1-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="84bc1-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="84bc1-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="84bc1-121">Fornisce metodi avanzati per l'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="84bc1-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="84bc1-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="84bc1-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="84bc1-123">Estende l'interfaccia **IWMReaderAdvanced2** .</span><span class="sxs-lookup"><span data-stu-id="84bc1-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="84bc1-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="84bc1-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="84bc1-125">Estende l'interfaccia **IWMReaderAdvanced3** .</span><span class="sxs-lookup"><span data-stu-id="84bc1-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="84bc1-126">**IWMReaderNetworkConfig**</span><span class="sxs-lookup"><span data-stu-id="84bc1-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="84bc1-127">Configura le impostazioni di rete nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="84bc1-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="84bc1-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="84bc1-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="84bc1-129">Configura impostazioni di rete aggiuntive nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="84bc1-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="84bc1-130">Questa interfaccia estende l'interfaccia **IWMReaderNetworkConfig** .</span><span class="sxs-lookup"><span data-stu-id="84bc1-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="84bc1-131">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="84bc1-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="84bc1-132">Configura l'oggetto sink di rete, utilizzato per scrivere supporti digitali in una rete.</span><span class="sxs-lookup"><span data-stu-id="84bc1-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="84bc1-133">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="84bc1-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="84bc1-134">Configura l'oggetto sink di push, usato per distribuire i supporti digitali nei punti di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="84bc1-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="84bc1-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84bc1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84bc1-136">**Implementazione della funzionalità di rete**</span><span class="sxs-lookup"><span data-stu-id="84bc1-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




