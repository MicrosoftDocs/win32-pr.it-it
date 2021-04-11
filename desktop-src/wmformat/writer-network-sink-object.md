---
title: Oggetto sink di rete writer
description: Oggetto sink di rete writer
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media Format SDK, oggetti sink di rete writer
- ASF (Advanced Systems Format), oggetti sink di rete writer
- ASF (formato avanzato dei sistemi), oggetti sink di rete writer
- oggetti, oggetti sink di rete writer
- oggetti sink di rete writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117462"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="16caf-108">Oggetto sink di rete writer</span><span class="sxs-lookup"><span data-stu-id="16caf-108">Writer Network Sink Object</span></span>

<span data-ttu-id="16caf-109">L'oggetto sink di rete writer viene utilizzato per scrivere supporti digitali in una rete.</span><span class="sxs-lookup"><span data-stu-id="16caf-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="16caf-110">L'oggetto sink di rete writer viene creato dalla funzione [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), che imposta un puntatore a un'interfaccia **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="16caf-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="16caf-111">Le altre interfacce dell'oggetto sink di rete del writer possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="16caf-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="16caf-112">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="16caf-112">Interface</span></span>                                              | <span data-ttu-id="16caf-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16caf-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16caf-114">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="16caf-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="16caf-115">Raccoglie informazioni sui client connessi.</span><span class="sxs-lookup"><span data-stu-id="16caf-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="16caf-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="16caf-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="16caf-117">Recupera informazioni client avanzate.</span><span class="sxs-lookup"><span data-stu-id="16caf-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="16caf-118">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="16caf-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="16caf-119">Consente all'applicazione di ottenere i messaggi di stato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="16caf-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="16caf-120">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="16caf-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="16caf-121">Apre e chiude le porte, imposta e recupera il numero massimo di client che è in grado di connettersi all'oggetto sink, imposta il protocollo di rete che deve essere utilizzato dall'oggetto writer ed esegue altre funzioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="16caf-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="16caf-122">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="16caf-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="16caf-123">Alloca memoria, determina se il sink funziona in tempo reale e gestisce diverse funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="16caf-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="16caf-124">L'interfaccia di callback seguente può essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink di rete del writer.</span><span class="sxs-lookup"><span data-stu-id="16caf-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="16caf-125">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="16caf-125">Interface</span></span>                                      | <span data-ttu-id="16caf-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16caf-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="16caf-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="16caf-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="16caf-128">Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="16caf-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="16caf-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16caf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16caf-130">**Trasmissione di dati ASF**</span><span class="sxs-lookup"><span data-stu-id="16caf-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="16caf-131">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="16caf-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="16caf-132">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="16caf-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




