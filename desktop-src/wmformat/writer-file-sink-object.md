---
title: Oggetto file sink del writer
description: Oggetto file sink del writer
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media Format SDK, oggetti sink di file del writer
- ASF (Advanced Systems Format), oggetti sink di file writer
- ASF (Advanced Systems Format), oggetti sink di file writer
- oggetti, oggetti sink di file writer
- oggetti sink di file writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046442"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="a6adf-108">Oggetto file sink del writer</span><span class="sxs-lookup"><span data-stu-id="a6adf-108">Writer File Sink Object</span></span>

<span data-ttu-id="a6adf-109">L'oggetto sink di file del writer viene usato durante la scrittura dell'output di Windows Media in un file.</span><span class="sxs-lookup"><span data-stu-id="a6adf-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="a6adf-110">L'oggetto sink di file del writer viene creato dalla funzione [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), che imposta un puntatore a un'interfaccia **IWMWriterFileSink** .</span><span class="sxs-lookup"><span data-stu-id="a6adf-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="a6adf-111">Le altre interfacce dell'oggetto sink di file del writer possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="a6adf-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="a6adf-112">Le interfacce seguenti sono supportate dall'oggetto sink di file del writer.</span><span class="sxs-lookup"><span data-stu-id="a6adf-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="a6adf-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a6adf-113">Interface</span></span>                                          | <span data-ttu-id="a6adf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6adf-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6adf-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="a6adf-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="a6adf-116">Consente all'applicazione di ottenere i messaggi di stato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6adf-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="a6adf-117">**IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="a6adf-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="a6adf-118">Apre un file in cui l'oggetto writer può scrivere i dati.</span><span class="sxs-lookup"><span data-stu-id="a6adf-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="a6adf-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="a6adf-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="a6adf-120">Fornisce la gestione estesa di un oggetto sink di file.</span><span class="sxs-lookup"><span data-stu-id="a6adf-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="a6adf-121">Eredita tutti i metodi di **IWMWriterFileSink**.</span><span class="sxs-lookup"><span data-stu-id="a6adf-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="a6adf-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="a6adf-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="a6adf-123">Fornisce opzioni aggiuntive per la scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="a6adf-123">Provides additional options for writing files.</span></span> <span data-ttu-id="a6adf-124">Eredita tutti i metodi di **IWMWriterFileSink** e **IWMWriterFileSink2**.</span><span class="sxs-lookup"><span data-stu-id="a6adf-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="a6adf-125">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="a6adf-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="a6adf-126">Alloca memoria, determina se il sink funziona in tempo reale e gestisce diverse funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="a6adf-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="a6adf-127">L'interfaccia di callback seguente deve essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink di file del writer.</span><span class="sxs-lookup"><span data-stu-id="a6adf-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="a6adf-128">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a6adf-128">Interface</span></span>                                      | <span data-ttu-id="a6adf-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6adf-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a6adf-130">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="a6adf-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="a6adf-131">Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="a6adf-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a6adf-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6adf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6adf-133">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="a6adf-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="a6adf-134">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="a6adf-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




