---
description: Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in un filtro del decodificatore DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Supporto di DXVA 2,0 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880050"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="72f28-103">Supporto di DXVA 2,0 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="72f28-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="72f28-104">Questo argomento descrive come supportare l'accelerazione video DirectX (DXVA) 2,0 in un filtro del decodificatore DirectShow.</span><span class="sxs-lookup"><span data-stu-id="72f28-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="72f28-105">In particolare, descrive la comunicazione tra il decodificatore e il renderer video.</span><span class="sxs-lookup"><span data-stu-id="72f28-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="72f28-106">In questo argomento non viene descritto come implementare la decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="72f28-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="72f28-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="72f28-108">Note sulla migrazione</span><span class="sxs-lookup"><span data-stu-id="72f28-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="72f28-109">Ricerca di una configurazione del decodificatore</span><span class="sxs-lookup"><span data-stu-id="72f28-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="72f28-110">Notifica al renderer video</span><span class="sxs-lookup"><span data-stu-id="72f28-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="72f28-111">Allocazione di buffer non compressi</span><span class="sxs-lookup"><span data-stu-id="72f28-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="72f28-112">Decodifica</span><span class="sxs-lookup"><span data-stu-id="72f28-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="72f28-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72f28-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="72f28-114">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="72f28-114">Prerequisites</span></span>

<span data-ttu-id="72f28-115">In questo argomento si presuppone che l'utente abbia familiarità con la scrittura di filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="72f28-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="72f28-116">Per ulteriori informazioni, vedere l'argomento relativo alla [scrittura dei filtri DirectShow](../directshow/writing-directshow-filters.md) nella documentazione di DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="72f28-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="72f28-117">Gli esempi di codice in questo argomento presuppongono che il filtro decodificatore sia derivato dalla classe [**CTransformFilter**](../directshow/ctransformfilter.md) , con la definizione di classe seguente:</span><span class="sxs-lookup"><span data-stu-id="72f28-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="72f28-118">Nella parte restante di questo argomento, il termine *decodificatore* indica il filtro del decodificatore, che riceve video compresso e genera video non compressi.</span><span class="sxs-lookup"><span data-stu-id="72f28-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="72f28-119">Il termine *dispositivo decodificatore* si riferisce a un acceleratore video hardware implementato dal driver Graphics.</span><span class="sxs-lookup"><span data-stu-id="72f28-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="72f28-120">Ecco i passaggi di base che devono essere eseguiti da un filtro decodificatore per supportare DXVA 2,0:</span><span class="sxs-lookup"><span data-stu-id="72f28-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="72f28-121">Negoziare un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="72f28-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="72f28-122">Trovare una configurazione del decodificatore DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="72f28-123">Notifica al renderer video che il decodificatore usa la decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="72f28-124">Fornire un allocatore personalizzato che alloca superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="72f28-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="72f28-125">Questi passaggi sono descritti in modo più dettagliato nella parte restante di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="72f28-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="72f28-126">Note sulla migrazione</span><span class="sxs-lookup"><span data-stu-id="72f28-126">Migration Notes</span></span>

<span data-ttu-id="72f28-127">Se si esegue la migrazione da DXVA 1,0, è necessario tenere presenti alcune differenze significative tra le due versioni:</span><span class="sxs-lookup"><span data-stu-id="72f28-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="72f28-128">DXVA 2,0 non usa le interfacce [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) e [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , perché il decodificatore può accedere alle API DXVA 2,0 direttamente tramite l'interfaccia [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="72f28-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="72f28-129">Durante la negoziazione del tipo di supporto, il decodificatore non usa un GUID di accelerazione video come sottotipo.</span><span class="sxs-lookup"><span data-stu-id="72f28-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="72f28-130">Il sottotipo è invece solo il formato video non compresso, ad esempio NV12, come per la decodifica software.</span><span class="sxs-lookup"><span data-stu-id="72f28-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="72f28-131">La procedura per la configurazione dell'acceleratore è cambiata.</span><span class="sxs-lookup"><span data-stu-id="72f28-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="72f28-132">In DXVA 1,0, il decodificatore chiama **Execute** con una struttura **\_ ConfigPictureDecode di DXVA** per configurare il accerlator.</span><span class="sxs-lookup"><span data-stu-id="72f28-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="72f28-133">In DXVA 2,0, il decodificatore usa l'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , come descritto nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="72f28-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="72f28-134">Il decodificatore alloca i buffer non compressi.</span><span class="sxs-lookup"><span data-stu-id="72f28-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="72f28-135">Il renderer video non li alloca più.</span><span class="sxs-lookup"><span data-stu-id="72f28-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="72f28-136">Anziché chiamare [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) per visualizzare il frame decodificato, il decodificatore recapita il frame al renderer chiamando [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), come con la decodifica software.</span><span class="sxs-lookup"><span data-stu-id="72f28-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="72f28-137">Il decodificatore non è più responsabile del controllo quando i buffer dei dati sono sicuri per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="72f28-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="72f28-138">Pertanto DXVA 2,0 non dispone di alcun metodo equivalente a [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span><span class="sxs-lookup"><span data-stu-id="72f28-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="72f28-139">Il renderer video esegue la fusione di sottoimmagini, usando le API del processore video DXVA 2.0.</span><span class="sxs-lookup"><span data-stu-id="72f28-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="72f28-140">I decodificatori che forniscono le immagini secondarie (ad esempio, i decodificatori DVD) devono inviare i dati di un'immagine in un pin di output separato.</span><span class="sxs-lookup"><span data-stu-id="72f28-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="72f28-141">Per le operazioni di decodifica, DXVA 2,0 usa le stesse strutture di dati di DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="72f28-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="72f28-142">Il filtro EVR (Enhanced video renderer) supporta DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="72f28-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="72f28-143">I filtri renderer di video mixing (VMR-7 e VMR-9) supportano solo DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="72f28-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="72f28-144">Ricerca di una configurazione del decodificatore</span><span class="sxs-lookup"><span data-stu-id="72f28-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="72f28-145">Una volta negoziato il tipo di supporto di output, il decodificatore deve trovare una configurazione compatibile per il dispositivo DXVA decoder.</span><span class="sxs-lookup"><span data-stu-id="72f28-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="72f28-146">È possibile eseguire questo passaggio all'interno del metodo [**CBaseOutputPin:: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="72f28-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="72f28-147">Questo passaggio garantisce che il driver di grafica supporti le funzionalità richieste dal decodificatore, prima del commit del decodificatore nell'uso di DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="72f28-148">Per trovare una configurazione per il dispositivo di decodificatore, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="72f28-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="72f28-149">Eseguire una query sul pin di input del renderer per l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="72f28-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="72f28-150">Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="72f28-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="72f28-151">Il GUID del servizio è \_ il \_ servizio accelerazione video \_ .</span><span class="sxs-lookup"><span data-stu-id="72f28-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="72f28-152">Chiamare [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un handle per il dispositivo Direct3D del renderer.</span><span class="sxs-lookup"><span data-stu-id="72f28-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="72f28-153">Chiamare [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passare l'handle del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72f28-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="72f28-154">Questo metodo restituisce un puntatore all'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="72f28-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="72f28-155">Chiamare [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span><span class="sxs-lookup"><span data-stu-id="72f28-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="72f28-156">Questo metodo restituisce una matrice di GUID del dispositivo del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="72f28-157">Scorrere la matrice dei GUID del decodificatore per trovare quelli supportati dal filtro del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="72f28-158">Per un decodificatore MPEG-2, ad esempio, si cercherà **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ ModeMPEG2 \_ VLD.**</span><span class="sxs-lookup"><span data-stu-id="72f28-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="72f28-159">Quando si trova un GUID del dispositivo del decodificatore candidato, passare il GUID al metodo [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) .</span><span class="sxs-lookup"><span data-stu-id="72f28-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="72f28-160">Questo metodo restituisce una matrice di formati di destinazione di rendering, specificati come valori **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="72f28-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="72f28-161">Scorrere i formati della destinazione di rendering e cercarne uno corrispondente al formato di output.</span><span class="sxs-lookup"><span data-stu-id="72f28-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="72f28-162">In genere, un dispositivo di decodificatore supporta un unico formato di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="72f28-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="72f28-163">Il filtro del decodificatore deve connettersi al renderer usando questo sottotipo.</span><span class="sxs-lookup"><span data-stu-id="72f28-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="72f28-164">Nella prima chiamata a [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), il decodificatore può denominare il formato della destinazione di rendering e quindi restituire questo formato come tipo di output preferito.</span><span class="sxs-lookup"><span data-stu-id="72f28-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="72f28-165">Chiamare [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span><span class="sxs-lookup"><span data-stu-id="72f28-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="72f28-166">Passare lo stesso GUID del dispositivo di decodificatore, insieme a una struttura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) che descrive il formato proposto.</span><span class="sxs-lookup"><span data-stu-id="72f28-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="72f28-167">Il metodo restituisce una matrice di [**strutture \_ ConfigPictureDecode di DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) .</span><span class="sxs-lookup"><span data-stu-id="72f28-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="72f28-168">Ogni struttura descrive una possibile configurazione per il dispositivo di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="72f28-169">Supponendo che i passaggi precedenti abbiano esito positivo, archiviare l'handle del dispositivo Direct3D, il GUID del dispositivo del decodificatore e la struttura di configurazione.</span><span class="sxs-lookup"><span data-stu-id="72f28-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="72f28-170">Il filtro utilizzerà queste informazioni per creare il dispositivo di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="72f28-171">Il codice seguente illustra come trovare una configurazione del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="72f28-172">Poiché questo esempio è generico, alcune della logica sono state inserite in funzioni helper che devono essere implementate dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="72f28-173">Nel codice seguente vengono illustrate le dichiarazioni per queste funzioni:</span><span class="sxs-lookup"><span data-stu-id="72f28-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="72f28-174">Notifica al renderer video</span><span class="sxs-lookup"><span data-stu-id="72f28-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="72f28-175">Se il decodificatore trova una configurazione del decodificatore, il passaggio successivo consiste nel notificare al renderer video che il decodificatore userà l'accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="72f28-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="72f28-176">È possibile eseguire questo passaggio all'interno del metodo [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="72f28-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="72f28-177">Questo passaggio deve verificarsi prima che l'allocatore venga selezionato, perché influiscono sulla modalità di selezione dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="72f28-178">Eseguire una query sul pin di input del renderer per l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="72f28-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="72f28-179">Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere un puntatore all'interfaccia [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="72f28-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="72f28-180">Il GUID del servizio è il **\_ \_ \_ servizio accelerazione video**.</span><span class="sxs-lookup"><span data-stu-id="72f28-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="72f28-181">Chiamare [**IDirectXVideoMemoryConfiguration:: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in un ciclo, incrementando la variabile *dwTypeIndex* da zero.</span><span class="sxs-lookup"><span data-stu-id="72f28-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="72f28-182">Arrestare quando il metodo restituisce il valore **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** nel parametro *pdwType* .</span><span class="sxs-lookup"><span data-stu-id="72f28-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="72f28-183">Questo passaggio garantisce che il renderer video supporti la decodifica con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="72f28-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="72f28-184">Questo passaggio avrà sempre esito positivo per il filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="72f28-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="72f28-185">Se il passaggio precedente ha avuto esito positivo, chiamare [**IDirectXVideoMemoryConfiguration:: SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) con il valore DXVA2 \_ SurfaceType \_ DecoderRenderTarget.</span><span class="sxs-lookup"><span data-stu-id="72f28-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="72f28-186">La chiamata di **SetSurfaceType** con questo valore inserisce il renderer video in modalità DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="72f28-187">Quando il renderer video è in questa modalità, il decodificatore deve fornire il proprio allocatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="72f28-188">Il codice seguente illustra come inviare una notifica al renderer video.</span><span class="sxs-lookup"><span data-stu-id="72f28-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="72f28-189">Se il decodificatore trova una configurazione valida e invia una notifica al renderer video, il decodificatore può usare DXVA per la decodifica.</span><span class="sxs-lookup"><span data-stu-id="72f28-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="72f28-190">Il decodificatore deve implementare un allocatore personalizzato per il pin di output, come descritto nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="72f28-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="72f28-191">Allocazione di buffer non compressi</span><span class="sxs-lookup"><span data-stu-id="72f28-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="72f28-192">In DXVA 2,0, il decodificatore è responsabile dell'allocazione di superfici Direct3D da usare come buffer video non compressi.</span><span class="sxs-lookup"><span data-stu-id="72f28-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="72f28-193">Pertanto, il decodificatore deve implementare un allocatore personalizzato che creerà le superfici.</span><span class="sxs-lookup"><span data-stu-id="72f28-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="72f28-194">Gli esempi di supporti forniti da questo allocatore conterranno i puntatori alle superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="72f28-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="72f28-195">EVR recupera un puntatore all'area chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="72f28-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="72f28-196">L'identificatore del servizio è il **\_ \_ servizio buffer** di.</span><span class="sxs-lookup"><span data-stu-id="72f28-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="72f28-197">Per fornire l'allocatore personalizzato, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="72f28-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="72f28-198">Definire una classe per gli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="72f28-198">Define a class for the media samples.</span></span> <span data-ttu-id="72f28-199">Questa classe può derivare dalla classe [**CMediaSample**](../directshow/cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="72f28-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="72f28-200">All'interno di questa classe, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="72f28-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="72f28-201">Archiviare un puntatore alla superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="72f28-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="72f28-202">Implementare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="72f28-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="72f28-203">Nel metodo [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , se il GUID del servizio è **il \_ \_ servizio buffer**, eseguire una query sulla superficie Direct3D per l'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="72f28-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="72f28-204">In caso contrario, **GetService** può restituire il **\_ \_ \_ servizio MF E non supportato**.</span><span class="sxs-lookup"><span data-stu-id="72f28-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="72f28-205">Eseguire l'override del metodo [**CMediaSample:: Getpointer**](../directshow/cmediasample-getpointer.md) per restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="72f28-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="72f28-206">Definire una classe per l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-206">Define a class for the allocator.</span></span> <span data-ttu-id="72f28-207">L'allocatore può derivare dalla classe [**CBaseAllocator**](../directshow/cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="72f28-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="72f28-208">All'interno di questa classe, eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="72f28-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="72f28-209">Eseguire l'override del metodo [**CBaseAllocator:: Alloc**](../directshow/cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="72f28-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="72f28-210">All'interno di questo metodo, chiamare [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) per creare le superfici.</span><span class="sxs-lookup"><span data-stu-id="72f28-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="72f28-211">(L'interfaccia [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) eredita questo metodo da [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)).</span><span class="sxs-lookup"><span data-stu-id="72f28-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="72f28-212">Eseguire l'override del metodo [**CBaseAllocator:: Free**](../directshow/cbaseallocator-free.md) per rilasciare le superfici.</span><span class="sxs-lookup"><span data-stu-id="72f28-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="72f28-213">Nel pin di output del filtro, eseguire l'override del metodo [**CBaseOutputPin:: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="72f28-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="72f28-214">All'interno di questo metodo, creare un'istanza dell'allocatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="72f28-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="72f28-215">Nel filtro implementare il metodo [**CTransformFilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="72f28-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="72f28-216">Il parametro *pProperties* indica il numero di superfici necessarie per il EVR.</span><span class="sxs-lookup"><span data-stu-id="72f28-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="72f28-217">Aggiungere a questo valore il numero di superfici richieste dal decodificatore e chiamare [**IMemAllocator::**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) SetValue nell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="72f28-218">Il codice seguente illustra come implementare la classe di esempio media:</span><span class="sxs-lookup"><span data-stu-id="72f28-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="72f28-219">Nel codice seguente viene illustrato come implementare il metodo [**Alloc**](../directshow/cbaseallocator-alloc.md) nell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="72f28-220">Ecco il codice per il metodo [**gratuito**](../directshow/cbaseallocator-free.md) :</span><span class="sxs-lookup"><span data-stu-id="72f28-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="72f28-221">Per ulteriori informazioni sull'implementazione di allocatori personalizzati, vedere l'argomento relativo alla [fornitura di un allocatore personalizzato](../directshow/providing-a-custom-allocator.md) nella documentazione di DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="72f28-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="72f28-222">Decodifica</span><span class="sxs-lookup"><span data-stu-id="72f28-222">Decoding</span></span>

<span data-ttu-id="72f28-223">Per creare il dispositivo di decodificatore, chiamare [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span><span class="sxs-lookup"><span data-stu-id="72f28-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="72f28-224">Il metodo restituisce un puntatore all'interfaccia [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="72f28-225">In ogni frame, chiamare [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) per testare l'handle del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72f28-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="72f28-226">Se il dispositivo è stato modificato, il metodo restituisce \_ il \_ nuovo \_ dispositivo video DXVA2 E \_ .</span><span class="sxs-lookup"><span data-stu-id="72f28-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="72f28-227">In tal caso, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="72f28-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="72f28-228">Chiudere l'handle del dispositivo chiamando [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span><span class="sxs-lookup"><span data-stu-id="72f28-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="72f28-229">Rilasciare i puntatori [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="72f28-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="72f28-230">Aprire un nuovo handle di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72f28-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="72f28-231">Negoziare una nuova configurazione del decodificatore, come descritto nella sezione [ricerca di una configurazione del decodificatore](#finding-a-decoder-configuration).</span><span class="sxs-lookup"><span data-stu-id="72f28-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="72f28-232">Creare un nuovo dispositivo di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="72f28-232">Create a new decoder device.</span></span>

<span data-ttu-id="72f28-233">Supponendo che l'handle del dispositivo sia valido, il processo di decodifica funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="72f28-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="72f28-234">Chiamare [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span><span class="sxs-lookup"><span data-stu-id="72f28-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="72f28-235">Eseguire le operazioni seguenti una o più volte:</span><span class="sxs-lookup"><span data-stu-id="72f28-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="72f28-236">Chiamare [**IDirectXVideoDecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) per ottenere un buffer del decodificatore DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="72f28-237">Riempire il buffer.</span><span class="sxs-lookup"><span data-stu-id="72f28-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="72f28-238">Chiamare [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span><span class="sxs-lookup"><span data-stu-id="72f28-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="72f28-239">Chiamare [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) per eseguire le operazioni di decodifica sul frame.</span><span class="sxs-lookup"><span data-stu-id="72f28-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="72f28-240">DXVA 2,0 usa le stesse strutture di dati di DXVA 1,0 per le operazioni di decodifica.</span><span class="sxs-lookup"><span data-stu-id="72f28-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="72f28-241">Per il set originale di profili DXVA (per H. 261, H. 263 e MPEG-2), queste strutture di dati sono descritte nella [specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="72f28-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="72f28-242">All'interno di ogni [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)coppia di chiamate di / [**esecuzione**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) BeginFrame, è possibile chiamare più volte [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) , ma solo una volta per ogni tipo di buffer DXVA.</span><span class="sxs-lookup"><span data-stu-id="72f28-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="72f28-243">Se viene chiamato due volte con lo stesso tipo di buffer, i dati vengono sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="72f28-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="72f28-244">Dopo la chiamata a [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), chiamare [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) per recapitare il frame al renderer video, come per la decodifica del software.</span><span class="sxs-lookup"><span data-stu-id="72f28-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="72f28-245">Il metodo **Receive** è asincrono. una volta restituito, il decodificatore può continuare a decodificare il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="72f28-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="72f28-246">Il driver di visualizzazione impedisce a tutti i comandi di decodifica di sovrascrivere il buffer mentre il buffer è in uso.</span><span class="sxs-lookup"><span data-stu-id="72f28-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="72f28-247">Il decodificatore non deve riutilizzare una superficie per decodificare un altro frame finché il renderer non ha rilasciato l'esempio.</span><span class="sxs-lookup"><span data-stu-id="72f28-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="72f28-248">Quando il renderer rilascia l'esempio, l'allocatore riporta l'esempio al relativo pool di esempi disponibili.</span><span class="sxs-lookup"><span data-stu-id="72f28-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="72f28-249">Per ottenere il successivo esempio disponibile, chiamare [**CBaseOutputPin:: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), che a sua volta chiama [**IMemAllocator:: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="72f28-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="72f28-250">Per ulteriori informazioni, vedere l'argomento [Cenni preliminari sul flusso di dati in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) nella documentazione di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="72f28-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72f28-251">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72f28-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72f28-252">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="72f28-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
