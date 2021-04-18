---
description: Panoramica di DXVA 2 e relativa relazione con DXVA 1.
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: Informazioni su DXVA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307523"
---
# <a name="about-dxva-20"></a><span data-ttu-id="b0e78-103">Informazioni su DXVA 2,0</span><span class="sxs-lookup"><span data-stu-id="b0e78-103">About DXVA 2.0</span></span>

<span data-ttu-id="b0e78-104">DirectX Video Acceleration (DXVA) è un'API e un DDI corrispondente per l'uso dell'accelerazione hardware per velocizzare l'elaborazione dei video.</span><span class="sxs-lookup"><span data-stu-id="b0e78-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware acceleration to speed up video processing.</span></span> <span data-ttu-id="b0e78-105">I codec software e i processori video software possono usare DXVA per eseguire l'offload di alcune operazioni con utilizzo intensivo della CPU nella GPU.</span><span class="sxs-lookup"><span data-stu-id="b0e78-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="b0e78-106">Un decodificatore software, ad esempio, può eseguire l'offload della trasformazione iDCT (discrete coseno) inversa nella GPU.</span><span class="sxs-lookup"><span data-stu-id="b0e78-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="b0e78-107">In DXVA alcune operazioni di decodifica sono implementate dal driver hardware grafico.</span><span class="sxs-lookup"><span data-stu-id="b0e78-107">In DXVA, some decoding operations are implemented by the graphics hardware driver.</span></span> <span data-ttu-id="b0e78-108">Questo set di funzionalità viene definito tasto di *scelta rapida*.</span><span class="sxs-lookup"><span data-stu-id="b0e78-108">This set of functionality is termed the *accelerator*.</span></span> <span data-ttu-id="b0e78-109">Altre operazioni di decodifica sono implementate dal software dell'applicazione in modalità utente, denominato *decoder host* o decodificatore *software*.</span><span class="sxs-lookup"><span data-stu-id="b0e78-109">Other decoding operations are implemented by user-mode application software, called the *host decoder* or *software decoder*.</span></span> <span data-ttu-id="b0e78-110">I termini decodificatore *host* e *software decodificatore* sono equivalenti. L'elaborazione eseguita dall'acceleratore viene chiamata *elaborazione fuori host*.</span><span class="sxs-lookup"><span data-stu-id="b0e78-110">(The terms *host decoder* and *software decoder* are equivalent.) Processing performed by the accelerator is called *off-host processing*.</span></span> <span data-ttu-id="b0e78-111">In genere l'acceleratore usa la GPU per velocizzare alcune operazioni.</span><span class="sxs-lookup"><span data-stu-id="b0e78-111">Typically the accelerator uses the GPU to speed up some operations.</span></span> <span data-ttu-id="b0e78-112">Ogni volta che l'acceleratore esegue un'operazione di decodifica, il decodificatore host deve fornire i buffer dell'acceleratore contenenti le informazioni necessarie per eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="b0e78-112">Whenever the accelerator performs a decoding operation, the host decoder must convey to the accelerator buffers containing the information needed to perform the operation</span></span>

<span data-ttu-id="b0e78-113">L'API DXVA 2 richiede Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b0e78-113">The DXVA 2 API requires Windows Vista or later.</span></span> <span data-ttu-id="b0e78-114">L'API DXVA 1 è ancora supportata in Windows Vista per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b0e78-114">The DXVA 1 API is still supported in Windows Vista for backward compatibility.</span></span> <span data-ttu-id="b0e78-115">Viene fornito un livello di emulazione che esegue la conversione tra una versione dell'API e la versione opposta di DDI:</span><span class="sxs-lookup"><span data-stu-id="b0e78-115">An emulation layer is provided that converts between either version of the API and the opposite version of the DDI:</span></span>

-   <span data-ttu-id="b0e78-116">Se il driver di grafica è conforme a Windows Display Driver Model (WDDM), le chiamate API DXVA 1 vengono convertite in chiamate DDI DXVA 2.</span><span class="sxs-lookup"><span data-stu-id="b0e78-116">If the graphics driver conforms to the Windows Display Driver Model (WDDM), DXVA 1 API calls are converted to DXVA 2 DDI calls.</span></span>
-   <span data-ttu-id="b0e78-117">Se i driver della grafica utilizzano il modello di driver di visualizzazione di Windows XP precedente (XPDM), le chiamate API DXVA 2 vengono convertite in chiamate DDI DXVA 1.</span><span class="sxs-lookup"><span data-stu-id="b0e78-117">If the graphics drivers uses the older Windows XP Display Driver Model (XPDM), DXVA 2 API calls are converted to DXVA 1 DDI calls.</span></span>

<span data-ttu-id="b0e78-118">La tabella seguente illustra i requisiti del sistema operativo e i renderer video supportati per ogni versione dell'API DXVA.</span><span class="sxs-lookup"><span data-stu-id="b0e78-118">The following table shows the operating system requirements and the supported video renderers for each version of the DXVA API.</span></span>



| <span data-ttu-id="b0e78-119">Versione API</span><span class="sxs-lookup"><span data-stu-id="b0e78-119">API Version</span></span> | <span data-ttu-id="b0e78-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0e78-120">Requirements</span></span>          | <span data-ttu-id="b0e78-121">Supporto renderer video</span><span class="sxs-lookup"><span data-stu-id="b0e78-121">Video Renderer Support</span></span>                        |
|-------------|-----------------------|-----------------------------------------------|
| <span data-ttu-id="b0e78-122">DXVA 1</span><span class="sxs-lookup"><span data-stu-id="b0e78-122">DXVA 1</span></span>      | <span data-ttu-id="b0e78-123">Windows 2000 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b0e78-123">Windows 2000 or later</span></span> | <span data-ttu-id="b0e78-124">Mixer overlay, VMR-7, VMR-9 (solo DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b0e78-124">Overlay Mixer, VMR-7, VMR-9 (DirectShow only)</span></span> |
| <span data-ttu-id="b0e78-125">DXVA 2</span><span class="sxs-lookup"><span data-stu-id="b0e78-125">DXVA 2</span></span>      | <span data-ttu-id="b0e78-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0e78-126">Windows Vista</span></span>         | <span data-ttu-id="b0e78-127">EVR (DirectShow e Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="b0e78-127">EVR (DirectShow and Media Foundation)</span></span>         |



 

<span data-ttu-id="b0e78-128">In DXVA 1, il decodificatore software deve accedere all'API tramite il renderer video.</span><span class="sxs-lookup"><span data-stu-id="b0e78-128">In DXVA 1, the software decoder must access the API through the video renderer.</span></span> <span data-ttu-id="b0e78-129">Non è possibile usare l'API DXVA 1 senza chiamare il renderer video.</span><span class="sxs-lookup"><span data-stu-id="b0e78-129">There is no way to use the DXVA 1 API without calling into the video renderer.</span></span> <span data-ttu-id="b0e78-130">Questa limitazione è stata rimossa con DXVA 2.</span><span class="sxs-lookup"><span data-stu-id="b0e78-130">This limitation has been removed with DXVA 2.</span></span> <span data-ttu-id="b0e78-131">Usando DXVA 2, il decodificatore host (o qualsiasi applicazione) può accedere direttamente all'API tramite l'interfaccia [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="b0e78-131">Using DXVA 2, the host decoder (or any application) can access the API directly, through the [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>

<span data-ttu-id="b0e78-132">La documentazione di DXVA 1 descrive le strutture di decodifica usate per gli standard video seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0e78-132">The DXVA 1 documentation describes the decoding structures used for the following video standards:</span></span>

-   <span data-ttu-id="b0e78-133">ITU-T REC. H. 261</span><span class="sxs-lookup"><span data-stu-id="b0e78-133">ITU-T Rec. H.261</span></span>
-   <span data-ttu-id="b0e78-134">ITU-T REC. H. 263</span><span class="sxs-lookup"><span data-stu-id="b0e78-134">ITU-T Rec. H.263</span></span>
-   <span data-ttu-id="b0e78-135">Video MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b0e78-135">MPEG-1 video</span></span>
-   <span data-ttu-id="b0e78-136">Video del profilo principale MPEG-2</span><span class="sxs-lookup"><span data-stu-id="b0e78-136">MPEG-2 Main Profile video</span></span>

<span data-ttu-id="b0e78-137">Le specifiche seguenti definiscono le estensioni DXVA per altri standard video:</span><span class="sxs-lookup"><span data-stu-id="b0e78-137">The following specifications define DXVA extensions for other video standards:</span></span>

-   [<span data-ttu-id="b0e78-138">Specifica DXVA per la decodifica H. 264/AVC</span><span class="sxs-lookup"><span data-stu-id="b0e78-138">DXVA Specification for H.264/AVC Decoding</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [<span data-ttu-id="b0e78-139">Specifica DXVA per la codifica video (MVC) H. 264/MPEG-4 AVC, incluso il profilo High stereo</span><span class="sxs-lookup"><span data-stu-id="b0e78-139">DXVA Specification for H.264/MPEG-4 AVC Multiview Video Coding (MVC), Including the Stereo High Profile</span></span>](https://www.microsoft.com/download/details.aspx?id=25200)
-   <span data-ttu-id="b0e78-140">[Specifica DXVA per MPEG-1 VLD e decodifica video combinata MPEG-1/MPEG-2 VLD](https://www.microsoft.com/download/details.aspx?id=9374).</span><span class="sxs-lookup"><span data-stu-id="b0e78-140">[DXVA Specification for MPEG-1 VLD and Combined MPEG-1/MPEG-2 VLD Video Decoding](https://www.microsoft.com/download/details.aspx?id=9374).</span></span>
-   [<span data-ttu-id="b0e78-141">Specifica DXVA per la decodifica del video MPEG-4 Part 2 in modalità VLD Off-Host</span><span class="sxs-lookup"><span data-stu-id="b0e78-141">DXVA Specification for Off-Host VLD Mode for MPEG-4 Part 2 Video Decoding</span></span>](https://www.microsoft.com/download/details.aspx?id=21100)
-   [<span data-ttu-id="b0e78-142">Specifica DXVA per la decodifica Windows Media Video® V8, V9 e vA (incluso SMPTE 421M "VC-1")</span><span class="sxs-lookup"><span data-stu-id="b0e78-142">DXVA Specification for Windows Media Video® v8, v9 and vA Decoding (Including SMPTE 421M "VC-1")</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [<span data-ttu-id="b0e78-143">Specifica DXVA (DirectX Video Acceleration) per la codifica video scalabile H. 264/MPEG-4 (SVC) Off-Host la decodifica in modalità VLD</span><span class="sxs-lookup"><span data-stu-id="b0e78-143">DirectX Video Acceleration (DXVA) Specification for H.264/MPEG-4 Scalable Video Coding (SVC) Off-Host VLD Mode Decoding</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [<span data-ttu-id="b0e78-144">Specifica di accelerazione video DirectX per la codifica video VP8 e VP9</span><span class="sxs-lookup"><span data-stu-id="b0e78-144">DirectX Video Acceleration Specification for VP8 and VP9 Video Coding</span></span>](https://www.microsoft.com/download/details.aspx?id=49188)

<span data-ttu-id="b0e78-145">DXVA 1 e DXVA 2 usano le stesse strutture di dati per la decodifica.</span><span class="sxs-lookup"><span data-stu-id="b0e78-145">DXVA 1 and DXVA 2 use the same data structures for decoding.</span></span> <span data-ttu-id="b0e78-146">Tuttavia, la procedura per la configurazione della sessione di decodifica è cambiata.</span><span class="sxs-lookup"><span data-stu-id="b0e78-146">However, the procedure for configuring the decoding session has changed.</span></span> <span data-ttu-id="b0e78-147">DXVA 1 usa un meccanismo di probe e blocco, in cui il decodificatore host può testare diverse configurazioni prima di impostare la configurazione desiderata nell'acceleratore.</span><span class="sxs-lookup"><span data-stu-id="b0e78-147">DXVA 1 uses a "probe and lock" mechanism, wherein the host decoder can test various configurations before setting the desired configuration on the accelerator.</span></span> <span data-ttu-id="b0e78-148">In DXVA 2 il tasto di scelta rapida restituisce un elenco di configurazioni supportate e il decodificatore host ne seleziona uno dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="b0e78-148">In DXVA 2, the accelerator returns a list of supported configurations and the host decoder selects one from the list.</span></span> <span data-ttu-id="b0e78-149">I dettagli sono forniti nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0e78-149">Details are given in the following sections:</span></span>

-   [<span data-ttu-id="b0e78-150">Supporto di DXVA 2,0 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0e78-150">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)
-   [<span data-ttu-id="b0e78-151">Supporto di DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0e78-151">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a><span data-ttu-id="b0e78-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0e78-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e78-153">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="b0e78-153">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="b0e78-154">Specifica DXVA 1,0</span><span class="sxs-lookup"><span data-stu-id="b0e78-154">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
