---
title: Informazioni su IMediaObject
description: Informazioni su IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IMediaObject
- plug-in, interfaccia IMediaObject
- plug-in per l'elaborazione di segnali digitali, interfaccia IMediaObject
- Plug-in DSP, interfaccia IMediaObject
- Interfaccia IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708047"
---
# <a name="about-imediaobject"></a><span data-ttu-id="acd0d-113">Informazioni su IMediaObject</span><span class="sxs-lookup"><span data-stu-id="acd0d-113">About IMediaObject</span></span>

<span data-ttu-id="acd0d-114">L'interfaccia **IMediaObject** è l'interfaccia necessaria per DMOS.</span><span class="sxs-lookup"><span data-stu-id="acd0d-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="acd0d-115">**IMediaObject** contiene i metodi usati da un plug-in di Windows Media Player DSP per recuperare i dati da Windows Media Player, per elaborare i dati e per restituire i dati elaborati a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="acd0d-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="acd0d-116">Per la documentazione completa dell'interfaccia **IMediaObject** , vedere la sezione relativa a DirectShow del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="acd0d-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="acd0d-117">I metodi di **IMediaObject** possono essere categorizzati come segue:</span><span class="sxs-lookup"><span data-stu-id="acd0d-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="acd0d-118">Metodi che gestiscono la negoziazione del formato</span><span class="sxs-lookup"><span data-stu-id="acd0d-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="acd0d-119">Questi sono i metodi che Windows Media Player chiama per ottenere informazioni sui formati di dati supportati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="acd0d-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="acd0d-120">Questi metodi includono:</span><span class="sxs-lookup"><span data-stu-id="acd0d-120">These methods include:</span></span>

-   <span data-ttu-id="acd0d-121">**GetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="acd0d-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="acd0d-122">**GetInputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="acd0d-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="acd0d-123">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="acd0d-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="acd0d-124">**GetInputType**</span><span class="sxs-lookup"><span data-stu-id="acd0d-124">**GetInputType**</span></span>
-   <span data-ttu-id="acd0d-125">**GetOutputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="acd0d-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="acd0d-126">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="acd0d-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="acd0d-127">**GetOutputType**</span><span class="sxs-lookup"><span data-stu-id="acd0d-127">**GetOutputType**</span></span>
-   <span data-ttu-id="acd0d-128">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="acd0d-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="acd0d-129">**SetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="acd0d-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="acd0d-130">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="acd0d-130">**SetInputType**</span></span>
-   <span data-ttu-id="acd0d-131">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="acd0d-131">**SetOutputType**</span></span>

<span data-ttu-id="acd0d-132">Molti di questi metodi, ad esempio **GetInputType** e **SetInputType**, usano la struttura del **\_ \_ tipo di supporto DMO** per descrivere il formato dei dati usati da un flusso.</span><span class="sxs-lookup"><span data-stu-id="acd0d-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="acd0d-133">Quando Windows Media Player chiama questi metodi, fornisce un puntatore a una struttura **del \_ \_ tipo di supporto DMO** .</span><span class="sxs-lookup"><span data-stu-id="acd0d-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="acd0d-134">Se un metodo come **SetInputType** specifica le informazioni sul tipo di supporto, il plug-in deve copiare la struttura del **\_ \_ tipo di supporto DMO** in una variabile membro ed esaminare i relativi membri dati per determinare il tipo di dati che Windows Media Player fornirà nel buffer di input.</span><span class="sxs-lookup"><span data-stu-id="acd0d-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="acd0d-135">Se un metodo come **GetInputType** recupera le informazioni sul tipo di supporto, il plug-in deve copiare l'indirizzo della variabile membro contenente la struttura del **\_ \_ tipo di supporto DMO** nel puntatore fornito da Windows Media Player nell'elenco dei parametri.</span><span class="sxs-lookup"><span data-stu-id="acd0d-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="acd0d-136">Windows Media Player utilizza principalmente due membri della struttura **del \_ \_ tipo di supporto DMO** :</span><span class="sxs-lookup"><span data-stu-id="acd0d-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="acd0d-137">**majortype**: identificatore univoco globale (Guid) che specifica la categoria complessiva del supporto, ad esempio audio o video.</span><span class="sxs-lookup"><span data-stu-id="acd0d-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="acd0d-138">**sottotipo**: GUID che specifica una descrizione più dettagliata del supporto, ad esempio audio PCM.</span><span class="sxs-lookup"><span data-stu-id="acd0d-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="acd0d-139">Questi GUID sono disponibili nell'intestazione denominata UUIDs. h, inclusa nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="acd0d-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="acd0d-140">I metodi come **GetInputSizeInfo** forniscono informazioni a Windows Media Player sulla quantità di memoria necessaria per allocare i buffer di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="acd0d-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="acd0d-141">I metodi come **GetStreamCount** e **GetOutputStreamInfo** forniscono informazioni a Windows Media Player sul numero e sul carattere dei flussi supportati dal plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="acd0d-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="acd0d-142">**GetInputMaxLatency** e **SetInputMaxLatency** sono implementati da DMOS in casi speciali.</span><span class="sxs-lookup"><span data-stu-id="acd0d-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="acd0d-143">I plug-in di Windows Media Player DSP devono restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="acd0d-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="acd0d-144">Metodi che specificano o recuperano informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="acd0d-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="acd0d-145">Questi sono i metodi che Windows Media Player chiama per ottenere o impostare i valori correlati allo stato corrente del plug-in.</span><span class="sxs-lookup"><span data-stu-id="acd0d-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="acd0d-146">Questi metodi includono:</span><span class="sxs-lookup"><span data-stu-id="acd0d-146">These methods include:</span></span>

-   <span data-ttu-id="acd0d-147">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="acd0d-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="acd0d-148">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="acd0d-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="acd0d-149">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="acd0d-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="acd0d-150">**GetInputCurrentType** e **GetOutputCurrentType** usano la struttura del **\_ \_ tipo di supporto DMO** per restituire informazioni a Windows Media Player sui tipi di supporto impostati in precedenza per i flussi di input e di output.</span><span class="sxs-lookup"><span data-stu-id="acd0d-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="acd0d-151">**GetInputStatus** restituisce un flag che indica a Windows Media Player se il plug-in DSP può accettare i dati di input.</span><span class="sxs-lookup"><span data-stu-id="acd0d-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="acd0d-152">Metodi che gestiscono il buffering e l'elaborazione dei dati</span><span class="sxs-lookup"><span data-stu-id="acd0d-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="acd0d-153">Questi sono i metodi che Windows Media Player chiama per avviare i vari processi eseguiti dal plug-in per eseguire l'elaborazione del segnale digitale.</span><span class="sxs-lookup"><span data-stu-id="acd0d-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="acd0d-154">Questi metodi includono:</span><span class="sxs-lookup"><span data-stu-id="acd0d-154">These methods include:</span></span>

-   <span data-ttu-id="acd0d-155">**AllocateStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="acd0d-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="acd0d-156">**Discontinuità**</span><span class="sxs-lookup"><span data-stu-id="acd0d-156">**Discontinuity**</span></span>
-   <span data-ttu-id="acd0d-157">**Svuotamento**</span><span class="sxs-lookup"><span data-stu-id="acd0d-157">**Flush**</span></span>
-   <span data-ttu-id="acd0d-158">**FreeStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="acd0d-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="acd0d-159">**Lock**</span><span class="sxs-lookup"><span data-stu-id="acd0d-159">**Lock**</span></span>
-   <span data-ttu-id="acd0d-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="acd0d-160">**ProcessInput**</span></span>
-   <span data-ttu-id="acd0d-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="acd0d-161">**ProcessOutput**</span></span>

<span data-ttu-id="acd0d-162">Windows Media Player chiama **AllocateStreamingResources** e **FreeStreamingResources** per fornire al plug-in DSP la possibilità di configurare o rilasciare eventuali buffer aggiuntivi che il plug-in può richiedere per l'elaborazione interna.</span><span class="sxs-lookup"><span data-stu-id="acd0d-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="acd0d-163">Non è necessario che i plug-in Windows Media Player DSP usino il metodo di **discontinuità** DMO.</span><span class="sxs-lookup"><span data-stu-id="acd0d-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="acd0d-164">Windows Media Player chiama **Flush** per indirizzare il plug-in DSP allo scaricamento di tutti i dati memorizzati nel buffer internamente.</span><span class="sxs-lookup"><span data-stu-id="acd0d-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="acd0d-165">Il plug-in deve rilasciare tutti i riferimenti alle interfacce **IMediaBuffer** , cancellare tutti i valori che specificano il timestamp o la lunghezza del campione per il buffer multimediale e reinizializzare gli Stati interni che dipendono dal contenuto dell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="acd0d-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="acd0d-166">Windows Media Player chiama ProcessInput per passare un puntatore a un'interfaccia **IMediaBuffer** al plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="acd0d-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="acd0d-167">Questa interfaccia fornisce l'accesso al buffer di input allocato da Windows Media Player per fornire i dati al plug-in.</span><span class="sxs-lookup"><span data-stu-id="acd0d-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="acd0d-168">Windows Media Player successivamente chiama **ProcessOutput** per passare un puntatore a un'interfaccia **IMediaBuffer** che fornisce l'accesso al buffer di output allocato da Windows Media Player per ricevere i dati elaborati dal plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="acd0d-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="acd0d-169">L'interfaccia **IMediaObject** include un metodo denominato **Lock**.</span><span class="sxs-lookup"><span data-stu-id="acd0d-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="acd0d-170">Questo metodo è progettato per acquisire o rilasciare un blocco su DMO per lasciare serializzare DMO durante l'esecuzione di più operazioni.</span><span class="sxs-lookup"><span data-stu-id="acd0d-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="acd0d-171">La versione di **IMediaObject:: Lock** nel codice della procedura guidata sostituisce l'implementazione ATL del **blocco**.</span><span class="sxs-lookup"><span data-stu-id="acd0d-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="acd0d-172">Poiché Windows Media Player serializza le chiamate effettuate all'interfaccia DMO di un plug-in DSP, l'implementazione del **blocco** restituisce semplicemente S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="acd0d-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="acd0d-173">Per informazioni dettagliate su come creare un DMO multithread, vedere la sezione relativa a DirectShow del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="acd0d-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acd0d-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acd0d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acd0d-175">**Interfacce obbligatorie**</span><span class="sxs-lookup"><span data-stu-id="acd0d-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




