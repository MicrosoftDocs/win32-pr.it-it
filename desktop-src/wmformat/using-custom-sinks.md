---
title: Uso di sink personalizzati
description: Uso di sink personalizzati
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- ASF (Advanced Systems Format), sink personalizzati
- ASF (formato avanzato dei sistemi), sink personalizzati
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, sink personalizzati
- sink personalizzati, informazioni
- sink writer, sink personalizzati
- sink personalizzati, interfaccia IWMWriterSink
- IWMWriterSink
- sink writer, interfaccia IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723479"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="9bdb2-113">Uso di sink personalizzati</span><span class="sxs-lookup"><span data-stu-id="9bdb2-113">Using Custom Sinks</span></span>

<span data-ttu-id="9bdb2-114">Se si ha una speciale necessità di scrittura, è possibile creare sink di writer personalizzati.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="9bdb2-115">Il writer gestisce una comunicazione unidirezionale con un sink effettuando chiamate ai metodi di [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span><span class="sxs-lookup"><span data-stu-id="9bdb2-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="9bdb2-116">Per creare un sink personalizzato, implementare l'interfaccia **IWMWriterSink** in una classe nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="9bdb2-117">Questo processo è molto simile all'implementazione di qualsiasi altra interfaccia di callback utilizzata dagli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="9bdb2-118">Per ulteriori informazioni sui callback, vedere [utilizzo dei metodi di callback](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9bdb2-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="9bdb2-119">Il buffer ricevuto in [**IWMWriterSink:: Onheader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) deve essere scritto all'inizio del file e tutti i buffer ricevuti in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) devono essere scritti in sequenza.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="9bdb2-120">**Onheader** verrà chiamato all'inizio, ma potrebbe essere chiamato anche in altri momenti. in tal caso, è necessario, se possibile, sovrascrivere l'intestazione originale.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="9bdb2-121">Se l'applicazione non è in grado di eseguire questa operazione per qualche motivo, è sufficiente ignorare le chiamate **Onheader** successive.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="9bdb2-122">Il sink personalizzato deve comunicare lo stato all'applicazione di scrittura effettuando chiamate al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="9bdb2-123">Se si implementa il sink come oggetto COM, potrebbe essere necessario esporre l'interfaccia [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="9bdb2-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="9bdb2-124">Tuttavia, è possibile passare l'indirizzo del callback **OnStatus** al sink e impostare un contesto nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="9bdb2-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bdb2-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bdb2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bdb2-126">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="9bdb2-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




