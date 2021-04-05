---
title: Oggetto configurazione del flusso
description: Oggetto configurazione del flusso
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media Format SDK, oggetti di configurazione di flusso
- ASF (Advanced Systems Format), oggetti di configurazione di flusso
- ASF (formato avanzato dei sistemi), oggetti di configurazione di flusso
- oggetti, flusso di oggetti di configurazione
- oggetti di configurazione di flusso
- flussi, oggetti di configurazione di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117458"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="54a30-109">Oggetto configurazione del flusso</span><span class="sxs-lookup"><span data-stu-id="54a30-109">Stream Configuration Object</span></span>

<span data-ttu-id="54a30-110">Per specificare le proprietà di un flusso multimediale in un file ASF, viene usato un oggetto di configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="54a30-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="54a30-111">Gli oggetti di configurazione del flusso possono essere creati per i flussi esistenti in un profilo oppure possono essere creati vuoti, pronti per la ricezione di nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="54a30-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="54a30-112">Gli oggetti di configurazione del flusso non possono esistere indipendentemente da un oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="54a30-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="54a30-113">Per salvare il contenuto di un oggetto di configurazione del flusso, è necessario chiamare [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) per aggiungere un nuovo flusso o [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) per salvare le modifiche apportate a un flusso esistente.</span><span class="sxs-lookup"><span data-stu-id="54a30-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="54a30-114">Per creare un oggetto di configurazione del flusso, usare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="54a30-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="54a30-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="54a30-115">Method</span></span>                                                                | <span data-ttu-id="54a30-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54a30-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54a30-117">**IWMProfile::CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="54a30-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="54a30-118">Crea un oggetto di configurazione del flusso senza dati.</span><span class="sxs-lookup"><span data-stu-id="54a30-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="54a30-119">**IWMProfile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="54a30-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="54a30-120">Crea un oggetto di configurazione del flusso popolato con i dati di un profilo.</span><span class="sxs-lookup"><span data-stu-id="54a30-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="54a30-121">Usa l'indice del flusso per identificare il flusso desiderato.</span><span class="sxs-lookup"><span data-stu-id="54a30-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="54a30-122">**IWMProfile::GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="54a30-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="54a30-123">Crea un oggetto di configurazione del flusso popolato con i dati di un profilo.</span><span class="sxs-lookup"><span data-stu-id="54a30-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="54a30-124">Usa il numero di flusso per identificare il flusso desiderato.</span><span class="sxs-lookup"><span data-stu-id="54a30-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="54a30-125">Tutti i metodi della tabella precedente impostano un puntatore a un'interfaccia **IWMStreamConfig** .</span><span class="sxs-lookup"><span data-stu-id="54a30-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="54a30-126">Le altre interfacce dell'oggetto di configurazione del flusso possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="54a30-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="54a30-127">Le interfacce seguenti sono supportate dall'oggetto di configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="54a30-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="54a30-128">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="54a30-128">Interface</span></span>                                        | <span data-ttu-id="54a30-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54a30-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54a30-130">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="54a30-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="54a30-131">Imposta e recupera la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="54a30-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="54a30-132">**IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="54a30-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="54a30-133">Imposta e recupera le proprietà che non sono necessarie per tutti i flussi, ad esempio le impostazioni della velocità in bit (VBR) della variabile.</span><span class="sxs-lookup"><span data-stu-id="54a30-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="54a30-134">**IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="54a30-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="54a30-135">Imposta e recupera tutte le informazioni di base su un flusso.</span><span class="sxs-lookup"><span data-stu-id="54a30-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="54a30-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="54a30-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="54a30-137">Configura i tipi di estensioni di unità dati associate al flusso.</span><span class="sxs-lookup"><span data-stu-id="54a30-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="54a30-138">Eredita tutti i metodi di **IWMStreamConfig**.</span><span class="sxs-lookup"><span data-stu-id="54a30-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="54a30-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="54a30-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="54a30-140">Imposta e recupera la lingua per il flusso.</span><span class="sxs-lookup"><span data-stu-id="54a30-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="54a30-141">Eredita tutti i metodi di **IWMStreamConfig** e **IWMStreamConfig2**.</span><span class="sxs-lookup"><span data-stu-id="54a30-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="54a30-142">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="54a30-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="54a30-143">Gestisce le proprietà di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="54a30-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="54a30-144">Si tratta di un'interfaccia facoltativa ed è disponibile solo per i flussi video.</span><span class="sxs-lookup"><span data-stu-id="54a30-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="54a30-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54a30-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54a30-146">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="54a30-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="54a30-147">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="54a30-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="54a30-148">**Oggetto Gestione profili**</span><span class="sxs-lookup"><span data-stu-id="54a30-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




