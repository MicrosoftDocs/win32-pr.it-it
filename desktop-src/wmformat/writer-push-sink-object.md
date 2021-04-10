---
title: Oggetto sink push writer
description: Oggetto sink push writer
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media Format SDK, oggetti sink push writer
- ASF (Advanced Systems Format), oggetti sink push writer
- ASF (Advanced Systems Format), oggetti sink push writer
- oggetti, oggetti sink push writer
- oggetti sink push writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956181"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="df319-108">Oggetto sink push writer</span><span class="sxs-lookup"><span data-stu-id="df319-108">Writer Push Sink Object</span></span>

<span data-ttu-id="df319-109">L'oggetto sink push writer distribuisce i supporti digitali ai punti di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="df319-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="df319-110">Ad esempio, un concerto Live può essere codificato da un singolo server e quindi recapitato, o *push*, a diversi altri server che eseguiranno effettivamente lo streaming del contenuto agli utenti.</span><span class="sxs-lookup"><span data-stu-id="df319-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="df319-111">Un oggetto sink push writer viene creato dalla funzione [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), che imposta un puntatore a un'interfaccia **IWMWriterPushSink** .</span><span class="sxs-lookup"><span data-stu-id="df319-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="df319-112">Le altre interfacce supportate dall'oggetto, elencate nella tabella seguente, possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="df319-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="df319-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="df319-113">Interface</span></span>                                          | <span data-ttu-id="df319-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df319-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df319-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="df319-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="df319-116">Consente all'applicazione di ottenere i messaggi di stato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df319-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="df319-117">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="df319-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="df319-118">Gestisce una sessione di distribuzione push.</span><span class="sxs-lookup"><span data-stu-id="df319-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="df319-119">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="df319-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="df319-120">Alloca memoria, determina se il sink funziona in tempo reale ed espone diverse funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="df319-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="df319-121">L'interfaccia di callback seguente può essere implementata dall'applicazione per tenere traccia dello stato di avanzamento di un oggetto sink push writer.</span><span class="sxs-lookup"><span data-stu-id="df319-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="df319-122">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="df319-122">Interface</span></span>                                      | <span data-ttu-id="df319-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df319-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="df319-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="df319-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="df319-125">Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="df319-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df319-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df319-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df319-127">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="df319-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="df319-128">**Invio di dati ASF a un punto di pubblicazione**</span><span class="sxs-lookup"><span data-stu-id="df319-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="df319-129">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="df319-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




