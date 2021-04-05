---
title: Per implementare i messaggi del lettore nel callback OnStatus
description: Per implementare i messaggi del lettore nel callback OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- ASF (Advanced Systems Format), implementazione di messaggi Reader
- ASF (Advanced Systems Format), implementazione di messaggi Reader
- ASF (Advanced Systems Format), callback di OnStatus
- ASF (formato avanzato dei sistemi), callback OnStatus
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, implementazione di messaggi Reader
- Metodo di callback OnStatus, implementazione dei messaggi del lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046296"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="767cd-111">Per implementare i messaggi del lettore nel callback OnStatus</span><span class="sxs-lookup"><span data-stu-id="767cd-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="767cd-112">Per utilizzare il Reader asincrono per recapitare contenuto da un file ASF, è necessario implementare almeno due metodi di callback, [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) e [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="767cd-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="767cd-113">In questa sezione viene descritto come implementare **IWMStatusCallback:: OnStatus** per ricevere e rispondere ai messaggi di stato inviati dal lettore.</span><span class="sxs-lookup"><span data-stu-id="767cd-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="767cd-114">**OnStatus** viene usato da altri oggetti in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="767cd-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="767cd-115">Per informazioni generali su **OnStatus**, vedere [utilizzo del callback OnStatus](using-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="767cd-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="767cd-116">Quando si usa il Reader asincrono, è necessario intercettare i messaggi seguenti in **IWMStatusCallback:: OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="767cd-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="767cd-117">Messaggio di stato</span><span class="sxs-lookup"><span data-stu-id="767cd-117">Status message</span></span> | <span data-ttu-id="767cd-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="767cd-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="767cd-119">WMT \_ aperto</span><span class="sxs-lookup"><span data-stu-id="767cd-119">WMT\_OPENED</span></span>    | <span data-ttu-id="767cd-120">Inviato al completamento delle operazioni di apertura del file.</span><span class="sxs-lookup"><span data-stu-id="767cd-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="767cd-121">WMT \_ chiuso</span><span class="sxs-lookup"><span data-stu-id="767cd-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="767cd-122">Inviato al completamento delle operazioni di chiusura del file.</span><span class="sxs-lookup"><span data-stu-id="767cd-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="767cd-123">È necessario usare i messaggi di stato elencati sopra per controllare l'esecuzione dell'applicazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="767cd-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="767cd-124">Ad esempio, è necessario attendere fino a quando non si riceve il messaggio **WMT \_ aperto** per avviare il Reader o chiamare altri metodi che richiedono che il lettore disponga di un file pronto.</span><span class="sxs-lookup"><span data-stu-id="767cd-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="767cd-125">Spesso, le applicazioni compilate con il Reader asincrono utilizzano un evento per segnalare il completamento delle chiamate asincrone e continuare l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="767cd-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="767cd-126">Per altre informazioni sull'uso di eventi per la segnalazione del completamento delle operazioni, vedere [uso di eventi con chiamate asincrone](using-events-with-asynchronous-calls.md).</span><span class="sxs-lookup"><span data-stu-id="767cd-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="767cd-127">Molti altri messaggi vengono inviati a **OnStatus** dall'oggetto Reader per consentire all'applicazione di rispondere allo stato delle operazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="767cd-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="767cd-128">I valori dei messaggi di stato possibili sono definiti nel tipo di enumerazione [**\_ dello stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="767cd-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="767cd-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="767cd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="767cd-130">**IWMStatusCallback:: OnStatus**</span><span class="sxs-lookup"><span data-stu-id="767cd-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="767cd-131">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="767cd-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="767cd-132">**Uso del callback di OnStatus**</span><span class="sxs-lookup"><span data-stu-id="767cd-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




