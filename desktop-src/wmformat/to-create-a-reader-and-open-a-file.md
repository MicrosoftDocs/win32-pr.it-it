---
title: Per creare un reader e aprire un file
description: Per creare un reader e aprire un file
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- ASF (Advanced Systems Format), creazione di Reader
- ASF (formato avanzato dei sistemi), creazione di Reader
- ASF (Advanced Systems Format), apertura di file
- ASF (Advanced Systems Format), apertura di file
- Reader asincroni, creazione
- Reader asincroni, apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724092"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="6a9a7-109">Per creare un reader e aprire un file</span><span class="sxs-lookup"><span data-stu-id="6a9a7-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="6a9a7-110">Prima di poter eseguire qualsiasi operazione con il lettore, sarà necessario creare un oggetto Reader e caricare un file per la lettura.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="6a9a7-111">Per inizializzare il Reader e aprire un file, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="6a9a7-112">Creare un oggetto Reader chiamando la funzione [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) .</span><span class="sxs-lookup"><span data-stu-id="6a9a7-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="6a9a7-113">È necessario specificare il livello desiderato di Rights Management per il nuovo oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="6a9a7-114">Le modalità disponibili sono elencate nel tipo di enumerazione [**WMT \_ Rights**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="6a9a7-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="6a9a7-115">Specificare un file da leggere chiamando [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span><span class="sxs-lookup"><span data-stu-id="6a9a7-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="6a9a7-116">È necessario specificare un'interfaccia di callback Reader per il lettore da usare.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="6a9a7-117">Per ulteriori informazioni sul callback del lettore, vedere [per implementare i messaggi del lettore nel callback OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="6a9a7-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="6a9a7-118">Attendere che il lettore Apra il file.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="6a9a7-119">Quando si chiama **Open** per caricare un file, viene restituito quasi immediatamente e continua l'elaborazione in un altro thread.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="6a9a7-120">È necessario attendere il completamento delle operazioni segnalando un evento quando il callback **OnStatus** riceve il \_ messaggio di stato WMT aperto.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="6a9a7-121">Il lettore supporta inoltre l'utilizzo dell'interfaccia com **IStream** per l'apertura di file.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="6a9a7-122">È possibile implementare l'interfaccia **IStream** come desiderato.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="6a9a7-123">Una volta aperto il file desiderato in **IStream**, è possibile seguire la procedura sopra indicata, ad eccezione del fatto che è necessario chiamare [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) anziché **IWMReader:: Open** nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a9a7-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a9a7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a9a7-125">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="6a9a7-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="6a9a7-126">**Interfaccia IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="6a9a7-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="6a9a7-127">**Interfaccia IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="6a9a7-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="6a9a7-128">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="6a9a7-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="6a9a7-129">**Utilizzo dei metodi di callback**</span><span class="sxs-lookup"><span data-stu-id="6a9a7-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




