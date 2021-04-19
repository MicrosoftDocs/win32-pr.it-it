---
description: La stabilizzazione video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la stabilizzazione delle immagini in un flusso video.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Stabilizzazione video MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332596"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="c05f0-103">Stabilizzazione video MFT</span><span class="sxs-lookup"><span data-stu-id="c05f0-103">Video Stabilization MFT</span></span>

<span data-ttu-id="c05f0-104">La stabilizzazione video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la stabilizzazione delle immagini in un flusso video.</span><span class="sxs-lookup"><span data-stu-id="c05f0-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="c05f0-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="c05f0-105">CLSID</span></span>

<span data-ttu-id="c05f0-106">\_CMSVIDEODSPMFT CLSID</span><span class="sxs-lookup"><span data-stu-id="c05f0-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="c05f0-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="c05f0-107">Interfaces</span></span>

-   [<span data-ttu-id="c05f0-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="c05f0-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="c05f0-109">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="c05f0-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="c05f0-110">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="c05f0-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="c05f0-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="c05f0-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="c05f0-112">**IMediaExtension**</span><span class="sxs-lookup"><span data-stu-id="c05f0-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="c05f0-113">Formati di input</span><span class="sxs-lookup"><span data-stu-id="c05f0-113">Input Formats</span></span>

<span data-ttu-id="c05f0-114">Il tipo di supporto di input e le combinazioni di sottotipi accettati dalla MFT per la stabilizzazione video per i video non compressi sono:</span><span class="sxs-lookup"><span data-stu-id="c05f0-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="c05f0-115">**VIDEO di MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="c05f0-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="c05f0-116">**\_NV12 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="c05f0-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="c05f0-117">**\_YUY2 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="c05f0-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="c05f0-118">Formati di output</span><span class="sxs-lookup"><span data-stu-id="c05f0-118">Output Formats</span></span>

<span data-ttu-id="c05f0-119">Il tipo di supporto di output e le combinazioni di sottotipi accettati dalla MFT per la stabilizzazione video sono:</span><span class="sxs-lookup"><span data-stu-id="c05f0-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="c05f0-120">**VIDEO di MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="c05f0-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="c05f0-121">**\_NV12 MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="c05f0-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="c05f0-122">Il tipo di supporto di input deve essere impostato prima del tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="c05f0-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="c05f0-123">Nella maggior parte dei casi, il supporto per il formato limitato non è un problema perché la pipeline inserisce automaticamente le conversioni dei colori necessarie.</span><span class="sxs-lookup"><span data-stu-id="c05f0-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="c05f0-124">Il componente MFT per la stabilizzazione video è in grado di modificare il formato dinamico in caso di modifica dell'input.</span><span class="sxs-lookup"><span data-stu-id="c05f0-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="c05f0-125">Quando le dimensioni dell'immagine di input cambiano o il sottotipo viene modificato, viene attivata una modifica del formato dinamico nel flusso di output.</span><span class="sxs-lookup"><span data-stu-id="c05f0-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="c05f0-126">La stabilizzazione video MFT effettuerà la conversione dei colori nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c05f0-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="c05f0-127">Quando il formato di input è **MEDIASUBTYPE \_ YUY2**.</span><span class="sxs-lookup"><span data-stu-id="c05f0-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="c05f0-128">Quando viene utilizzata la modalità di compatibilità Microsoft DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="c05f0-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="c05f0-129">Attributi</span><span class="sxs-lookup"><span data-stu-id="c05f0-129">Attributes</span></span>

<span data-ttu-id="c05f0-130">Gli attributi seguenti sono supportati dalla stabilizzazione video MFT tramite l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c05f0-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="c05f0-131">L'attributo [MF \_ VIDEODSP \_ mode](mf-videodsp-mode.md) imposta la stabilizzazione video MFT in modalità di stabilizzazione o pass-through.</span><span class="sxs-lookup"><span data-stu-id="c05f0-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="c05f0-132">L'applicazione deve chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sul tipo GUID **MF \_ VIDEODSP \_** con un numero intero corrispondente a uno dei valori validi seguenti: **\_ stabilizzazione MFVideoDSPMode** = 4, **MFVideoDSPMode \_ PassThrough** = 1.</span><span class="sxs-lookup"><span data-stu-id="c05f0-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="c05f0-133">\_ \_ La modalità MF VIDEODSP può essere modificata in qualsiasi momento durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c05f0-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="c05f0-134">Questo comporta una modifica della modalità dinamica.</span><span class="sxs-lookup"><span data-stu-id="c05f0-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="c05f0-135">L'output passerà a stabilizzato o pass-through dopo 16 o 2 frame, a seconda della modalità di latenza, dopo la modifica dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="c05f0-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="c05f0-136">Con l'attributo [MF \_ bassa \_ latenza](mf-low-latency.md) , la stabilizzazione del video è in modalità a bassa latenza o alta qualità.</span><span class="sxs-lookup"><span data-stu-id="c05f0-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="c05f0-137">L'applicazione deve chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) sul GUID **MF \_ low \_ latenza** con un numero intero corrispondente a uno dei valori validi seguenti: latenza bassa = 1 alta qualità = 0</span><span class="sxs-lookup"><span data-stu-id="c05f0-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="c05f0-138">L'attributo [MF \_ sa \_ d3d11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) viene usato dalla pipeline per specificare i flag di associazione d3d11 per la creazione degli esempi di output con.</span><span class="sxs-lookup"><span data-stu-id="c05f0-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="c05f0-139">Qualsiasi combinazione di valori dall'enumerazione [**del \_ \_ flag di binding d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) è valida.</span><span class="sxs-lookup"><span data-stu-id="c05f0-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="c05f0-140">Il numero di campioni di **\_ \_ \_ output \_ \_ minimo dell'attributo MF SA** viene usato dalla pipeline per specificare il numero minimo di campioni che questo componente deve supportare nell'output.</span><span class="sxs-lookup"><span data-stu-id="c05f0-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="c05f0-141">L'attributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) viene impostato su ogni campione prodotto dalla stabilizzazione per indicare l' [effettiva \_ \_ modalità MF VIDEODSP](mf-videodsp-mode.md) applicata a tale campione (indipendentemente dal fatto che l'esempio sia stato stabilizzato).</span><span class="sxs-lookup"><span data-stu-id="c05f0-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="c05f0-142">In determinate condizioni, è possibile che gli esempi non siano stabilizzati (a causa del carico elevato del sistema o delle richieste da parte dell'utente).</span><span class="sxs-lookup"><span data-stu-id="c05f0-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="c05f0-143">Questo attributo ha gli stessi valori dell'attributo della \_ modalità MF VIDEODSP \_ (**\_ stabilizzazione MFVideoDSPMode** e **\_ PassThrough MFVideoDSPMode**).</span><span class="sxs-lookup"><span data-stu-id="c05f0-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="c05f0-144">Per ottenere il valore di questa applicazione di attributo, è necessario chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SETVALUE sul GUID **MFSampleExtension \_ VideoDSPMode**.</span><span class="sxs-lookup"><span data-stu-id="c05f0-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c05f0-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="c05f0-145">Remarks</span></span>

<span data-ttu-id="c05f0-146">È possibile creare un'istanza del DSP per la stabilizzazione video in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c05f0-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="c05f0-147">Chiamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="c05f0-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="c05f0-148">La stabilizzazione del video DSP è registrata nella categoria dell' **\_ \_ \_ effetto video della categoria MFT** .</span><span class="sxs-lookup"><span data-stu-id="c05f0-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="c05f0-149">Chiamando la funzione COM **CoCreateInstance** passando il CLSID CLSID **\_ CMSVideoDSPMFT**.</span><span class="sxs-lookup"><span data-stu-id="c05f0-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="c05f0-150">Per usare questo metodo, è necessario includere wmcodecdsp. h e il collegamento a wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c05f0-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="c05f0-151">Inoltre, la stabilizzazione video supporta la creazione di istanze utilizzando Windows Runtime come estensione per Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c05f0-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="c05f0-152">Viene definito in [**Windows. Media. VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)e il nome completo è "Windows. Media. VideoEffects. VideoStabilization".</span><span class="sxs-lookup"><span data-stu-id="c05f0-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="c05f0-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c05f0-153">Requirements</span></span>



| <span data-ttu-id="c05f0-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="c05f0-154">Requirement</span></span> | <span data-ttu-id="c05f0-155">Valore</span><span class="sxs-lookup"><span data-stu-id="c05f0-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c05f0-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c05f0-156">Header</span></span><br/> | <dl> <span data-ttu-id="c05f0-157"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="c05f0-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c05f0-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c05f0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c05f0-159">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="c05f0-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="c05f0-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="c05f0-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
