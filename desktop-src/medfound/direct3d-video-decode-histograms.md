---
description: Questo articolo contiene istruzioni per la generazione di istogrammi durante la decodifica di video usando le API video Direct3D 11 o 12.
ms.assetid: ''
title: Istogrammi decodifica video Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305403"
---
# <a name="direct3d-video-decode-histograms"></a><span data-ttu-id="9464e-103">Istogrammi decodifica video Direct3D</span><span class="sxs-lookup"><span data-stu-id="9464e-103">Direct3D video decode histograms</span></span>

<span data-ttu-id="9464e-104">Questo articolo contiene istruzioni per la generazione di istogrammi durante la decodifica di video usando le API video Direct3D 11 o 12.</span><span class="sxs-lookup"><span data-stu-id="9464e-104">This article contains guidance for generating histograms while decoding video using Direct3D 11 or 12 video APIs.</span></span>

## <a name="checking-the-video-device-for-histogram-capabilities"></a><span data-ttu-id="9464e-105">Controllo del dispositivo video per le funzionalità istogramma</span><span class="sxs-lookup"><span data-stu-id="9464e-105">Checking the video device for histogram capabilities</span></span>

<span data-ttu-id="9464e-106">Prima di provare a generare istogrammi, è necessario verificare se il dispositivo video corrente supporta la funzionalità di decodifica video istogramma.</span><span class="sxs-lookup"><span data-stu-id="9464e-106">Before attempting to generated histograms, you must check to see if the current video device supports the video decode histogram feature.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="9464e-107">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9464e-107">Direct3D 12</span></span>

<span data-ttu-id="9464e-108">Chiamare [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) per verificare i dettagli del supporto per le operazioni di decodifica video di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9464e-108">Call [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) to check for the support details for Direct3D 12 video decoding operations.</span></span> <span data-ttu-id="9464e-109">Passare il valore **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** dall'enumerazione [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) per specificare che si richiede il supporto per gli istogrammi di decodifica video.</span><span class="sxs-lookup"><span data-stu-id="9464e-109">Pass the **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** value from the [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify that you are requesting support for video decode histograms.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="9464e-110">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9464e-110">Direct3D 11</span></span>

<span data-ttu-id="9464e-111">Chiamare [ID3D11VideoDevice2:: CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) e passare il valore **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** della [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) per determinare se gli istogrammi sono supportati per il dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="9464e-111">Call [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) and pass in the **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** value of the [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) to determine if histograms are supported for the current device.</span></span>

## <a name="enabling-histogram-during-decode"></a><span data-ttu-id="9464e-112">Abilitazione dell'istogramma durante la decodifica</span><span class="sxs-lookup"><span data-stu-id="9464e-112">Enabling histogram during decode</span></span>

<span data-ttu-id="9464e-113">La raccolta di dati dell'istogramma viene abilitata dal chiamante che fornisce i buffer in cui vengono archiviati i dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="9464e-113">The collection of histogram data is enabled by the caller providing the buffers in which the histogram data is stored.</span></span>  <span data-ttu-id="9464e-114">Un buffer di output con istogramma null per un determinato componente indica che la raccolta di istogrammi è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="9464e-114">A null histogram output buffer for a given component indicates that histogram collection is disabled.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="9464e-115">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9464e-115">Direct3D 12</span></span>

<span data-ttu-id="9464e-116">Per fornire i buffer di output per ricevere i dati dell'istogramma usando Direct3D 12, è necessario creare l'elenco di comandi Decode usando il metodo [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) .</span><span class="sxs-lookup"><span data-stu-id="9464e-116">In order to provide output buffers to receive histogram data using Direct3D 12, you should create your decode command list using the [ID3D12VideoDecodeCommandList1::DecodeFrame1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) method.</span></span> <span data-ttu-id="9464e-117">Questo metodo accetta una struttura [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) come argomento.</span><span class="sxs-lookup"><span data-stu-id="9464e-117">This method takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure as an argument.</span></span> <span data-ttu-id="9464e-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** dispone di un campo di tipo [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), che consente di specificare un [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) in cui vengono restituiti i dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="9464e-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** has a field of type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), which allows you to specify an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) into which histogram data is output.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="9464e-119">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="9464e-119">Direct3D 11</span></span>

<span data-ttu-id="9464e-120">L'interfaccia [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) fornisce il metodo [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) , che consente di fornire una o più interfacce [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) in cui verranno restituiti i dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="9464e-120">The [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) interface provides the [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) method, which allows you to provide one or more [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interfaces into which the histogram data will be output.</span></span> <span data-ttu-id="9464e-121">[D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) per specificare i componenti per i quali si desidera che vengano generati i dati dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="9464e-121">The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) to specify the components for which you want histogram data to be generated.</span></span>


## <a name="buffer-format"></a><span data-ttu-id="9464e-122">Formato buffer</span><span class="sxs-lookup"><span data-stu-id="9464e-122">Buffer format</span></span>

<span data-ttu-id="9464e-123">L'output dell'istogramma Decode viene scritto in un buffer come contatore integer per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="9464e-123">The decode histogram output is written to a buffer as an integer counter per component.</span></span>  <span data-ttu-id="9464e-124">Il formato del buffer è un valore a 32 bit per bin.</span><span class="sxs-lookup"><span data-stu-id="9464e-124">The buffer format is a 32-bit value per bin.</span></span>  <span data-ttu-id="9464e-125">Un dispositivo può usare una profondità di bit del contatore integer inferiore A 32 bit, ma deve essere pari A 16, 24 o 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9464e-125">A device may use an integer counter bit depth that is smaller than 32 bits, but must be 16, 24, or 32 bits.</span></span>  <span data-ttu-id="9464e-126">In tal caso, il valore del contatore viene archiviato nei bit inferiori e i bit inutilizzati superiori sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="9464e-126">If so, the counter value is stored in the lower bits and the upper unused bits are zero.</span></span>  <span data-ttu-id="9464e-127">Quando il conteggio per un cestino supera il valore massimo, il dispositivo imposta invece il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="9464e-127">When the count for a bin would exceed the max value, the device sets the max value instead.</span></span> <span data-ttu-id="9464e-128">I dispositivi segnalano il numero di contenitori supportati, che deve essere un valore che è una potenza di 2.</span><span class="sxs-lookup"><span data-stu-id="9464e-128">Devices report the number of bins supported, which must be a value that is a power of 2.</span></span>  <span data-ttu-id="9464e-129">Il numero minimo di contenitori necessari per i dispositivi che supportano questa funzionalità è 64.</span><span class="sxs-lookup"><span data-stu-id="9464e-129">The minimum number of bins required for devices that support this feature is 64.</span></span> 

<span data-ttu-id="9464e-130">È necessario fornire un buffer con un offset allineato a 256 byte e una dimensione che corrisponde al numero supportato di contenitori moltiplicato per le dimensioni del cestino (4 byte) per ogni componente richiesto.</span><span class="sxs-lookup"><span data-stu-id="9464e-130">You must supply a buffer with a 256-byte aligned offset and a size that is the supported number of bins multiplied by the bin size (4 bytes) for each component requested.</span></span>  <span data-ttu-id="9464e-131">Il posizionamento del contenitore è determinato da:</span><span class="sxs-lookup"><span data-stu-id="9464e-131">Bin placement is determined by:</span></span>

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


<span data-ttu-id="9464e-132">Quando un formato definisce i bit utili di un componente come inferiore al numero di bit di archiviazione (ad esempio, P010 usa i primi 10 bit di 16 bit di archiviazione componenti), vengono considerati solo i bit utili (P010 viene considerato come valore a 10 bit).</span><span class="sxs-lookup"><span data-stu-id="9464e-132">When a format defines the useful bits of a component as less than the number of storage bits (for example, P010 uses the top 10 bits of 16 bits of component storage), only the useful bits are considered (P010 is treated as a 10 bit value).</span></span> 

<span data-ttu-id="9464e-133">Il dispositivo video segnala i componenti supportati.</span><span class="sxs-lookup"><span data-stu-id="9464e-133">The video device reports which components are supported.</span></span>  <span data-ttu-id="9464e-134">Se il chiamante non desidera un istogramma per un determinato componente, viene specificato nullptr.</span><span class="sxs-lookup"><span data-stu-id="9464e-134">If the caller does not want a histogram for a given component, they specify nullptr.</span></span>  <span data-ttu-id="9464e-135">Se il driver non supporta un istogramma per un determinato componente, il buffer dell'istogramma del componente deve essere nullptr.</span><span class="sxs-lookup"><span data-stu-id="9464e-135">If the driver does not support a histogram for a given component, that component's histogram buffer must be nullptr.</span></span>

<span data-ttu-id="9464e-136">Quando sono supportati più componenti, l'applicazione può richiedere qualsiasi combinazione di componenti per ogni decodifica di frame.</span><span class="sxs-lookup"><span data-stu-id="9464e-136">When multiple components are supported, the application may request any combination of components per frame decode.</span></span>  <span data-ttu-id="9464e-137">Se, ad esempio, i rapporti hardware supportano i componenti Y, U e V, l'applicazione può richiedere l'istogramma Y solo per il frame uno, l'istogramma U solo per il frame due e l'istogramma V solo per il frame 3.</span><span class="sxs-lookup"><span data-stu-id="9464e-137">For example,if the hardware reports support for Y, U, and V components, the application may request the Y histogram only for frame one, the U histogram only for frame two, and the V histogram only for frame 3.</span></span>  <span data-ttu-id="9464e-138">Possono anche richiedere qualsiasi combinazione di due componenti o di tutti e tre i componenti.</span><span class="sxs-lookup"><span data-stu-id="9464e-138">They may also request any combination of two components or all three components.</span></span>

<span data-ttu-id="9464e-139">Le applicazioni forniscono un offset separato e un puntatore/handle del buffer per ogni componente richiesto.</span><span class="sxs-lookup"><span data-stu-id="9464e-139">Applications supply a separate offset and buffer pointer/handle for each component requested.</span></span>  <span data-ttu-id="9464e-140">Questo puntatore può puntare alla stessa risorsa di un altro componente o di una risorsa separata.</span><span class="sxs-lookup"><span data-stu-id="9464e-140">This pointer may point to the same resource as another component or a separate resource.</span></span>  <span data-ttu-id="9464e-141">L'offset consente l'inserimento di più componenti nello stesso buffer, ma l'area di output specificata dall'offset e le dimensioni dell'istogramma non devono sovrapporsi a un altro output del componente dell'istogramma.</span><span class="sxs-lookup"><span data-stu-id="9464e-141">The offset allows placing multiple components in the same buffer, but the output region specified by the offset and the histogram size must not overlap another histogram component output.</span></span>  <span data-ttu-id="9464e-142">L'istogramma può anche essere scritto nello stesso buffer di altri contenuti non correlati, ad esempio quando viene usato in una strategia di sottoallocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9464e-142">The histogram may also be written to the same buffer as other unrelated content such as when being used in a resource sub-allocation strategy.</span></span>


<span data-ttu-id="9464e-143">Il runtime D3D verifica che i chiamanti consentano solo l'istogramma per i componenti supportati, che l'offset del buffer sia allineato e che le dimensioni del buffer siano sufficienti per il numero di contenitori segnalato.</span><span class="sxs-lookup"><span data-stu-id="9464e-143">The D3D runtime validates that callers only enable histogram for supported components, that the buffer offset is aligned, and that buffer size is sufficient for the reported number of bins.</span></span>


## <a name="protected-content"></a><span data-ttu-id="9464e-144">Contenuto protetto</span><span class="sxs-lookup"><span data-stu-id="9464e-144">Protected content</span></span>

<span data-ttu-id="9464e-145">I buffer dell'istogramma devono avere la stessa protezione della superficie di output della decodifica.</span><span class="sxs-lookup"><span data-stu-id="9464e-145">The Histogram buffers are required to have the same surface protection as the decode output surface.</span></span> <span data-ttu-id="9464e-146">Se la superficie di output della decodifica non è una risorsa protetta, il buffer dell'istogramma non deve essere una risorsa protetta.</span><span class="sxs-lookup"><span data-stu-id="9464e-146">If the decode output surface is not a protected resource, the histogram buffer must not be a protected resource.</span></span> <span data-ttu-id="9464e-147">Se la superficie di output della decodifica è protetta, l'istogramma deve essere una risorsa protetta.</span><span class="sxs-lookup"><span data-stu-id="9464e-147">If the decode output surface is protected resource, the histogram must be a protected resource.</span></span>








## <a name="related-topics"></a><span data-ttu-id="9464e-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9464e-148">Related topics</span></span>

<dl> <span data-ttu-id="9464e-149"><dt>API video Direct3D 
[12](direct3d-12-video-apis.md) 
 [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="9464e-149"><dt>
[Direct3D 12 Video APIs](direct3d-12-video-apis.md)
[Media Foundation Programming Guide](media-foundation-programming-guide.md)
</dt> </span></span></dl>

 

 




