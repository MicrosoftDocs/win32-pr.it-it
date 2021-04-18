---
title: Per creare un reader sincrono e aprire un file
description: Per creare un reader sincrono e aprire un file
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), creazione di Reader
- ASF (formato avanzato dei sistemi), creazione di Reader
- ASF (Advanced Systems Format), apertura di file
- ASF (Advanced Systems Format), apertura di file
- lettori sincroni, creazione
- lettori sincroni, apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299515"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="7c44c-109">Per creare un reader sincrono e aprire un file</span><span class="sxs-lookup"><span data-stu-id="7c44c-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="7c44c-110">Prima di poter eseguire qualsiasi operazione con il lettore sincrono, sarà necessario creare un oggetto Reader sincrono e caricare un file per la lettura.</span><span class="sxs-lookup"><span data-stu-id="7c44c-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="7c44c-111">Per inizializzare il lettore sincrono e aprire un file, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="7c44c-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="7c44c-112">Creare un oggetto Reader sincrono chiamando la funzione [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .</span><span class="sxs-lookup"><span data-stu-id="7c44c-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="7c44c-113">È necessario specificare il livello desiderato di Rights Management per il nuovo oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="7c44c-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="7c44c-114">Le modalità disponibili sono elencate nel tipo di enumerazione **WMT \_ Rights** .</span><span class="sxs-lookup"><span data-stu-id="7c44c-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="7c44c-115">Specificare un file da leggere chiamando [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span><span class="sxs-lookup"><span data-stu-id="7c44c-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="7c44c-116">Il lettore sincrono supporta inoltre l'utilizzo dell'interfaccia com **IStream** per l'apertura di file.</span><span class="sxs-lookup"><span data-stu-id="7c44c-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="7c44c-117">È possibile implementare l'interfaccia **IStream** come desiderato.</span><span class="sxs-lookup"><span data-stu-id="7c44c-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="7c44c-118">Una volta aperto il file desiderato in **IStream**, è possibile seguire la procedura sopra indicata, ad eccezione del fatto che è necessario chiamare [**IWMSyncReader:: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) anziché **IWMSyncReader:: Open** nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="7c44c-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c44c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c44c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c44c-120">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="7c44c-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="7c44c-121">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="7c44c-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




