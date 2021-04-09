---
description: Esempi video
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Esempi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880569"
---
# <a name="video-samples"></a><span data-ttu-id="cc706-103">Esempi video</span><span class="sxs-lookup"><span data-stu-id="cc706-103">Video Samples</span></span>

<span data-ttu-id="cc706-104">L'oggetto di esempio video è un'implementazione specializzata dell'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per l'uso con il [renderer video avanzato](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="cc706-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="cc706-105">Per creare un'istanza di questo oggetto, chiamare la funzione [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) .</span><span class="sxs-lookup"><span data-stu-id="cc706-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="cc706-106">La funzione accetta un puntatore a una superficie Direct3D e restituisce un puntatore all'interfaccia **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="cc706-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="cc706-107">I tipi di oggetti seguenti devono allocare esempi utilizzando questa funzione:</span><span class="sxs-lookup"><span data-stu-id="cc706-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="cc706-108">Presenter EVR personalizzati.</span><span class="sxs-lookup"><span data-stu-id="cc706-108">Custom EVR presenters.</span></span> <span data-ttu-id="cc706-109">Un presentatore alloca gli esempi video e li invia al metodo [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) del mixer.</span><span class="sxs-lookup"><span data-stu-id="cc706-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="cc706-110">Per altre informazioni, vedere [How to write an EVR Presenter](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="cc706-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="cc706-111">Decodificatori video che supportano l'accelerazione video.</span><span class="sxs-lookup"><span data-stu-id="cc706-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="cc706-112">Per ulteriori informazioni, vedere [supporto di DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="cc706-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="cc706-113">L'oggetto di esempio video implementa le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc706-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="cc706-114">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="cc706-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="cc706-115">**IMFDesiredSample**</span><span class="sxs-lookup"><span data-stu-id="cc706-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="cc706-116">**IMFTrackedSample**</span><span class="sxs-lookup"><span data-stu-id="cc706-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="cc706-117">Se il parametro *pUnkSurface* di [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) è diverso da **null**, l'esempio video risultante contiene un singolo buffer multimediale che incapsula la superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc706-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="cc706-118">Questo oggetto buffer ha funzionalità limitate:</span><span class="sxs-lookup"><span data-stu-id="cc706-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="cc706-119">Il metodo [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) del buffer restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="cc706-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="cc706-120">Il buffer non implementa l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cc706-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="cc706-121">L'unico modo per accedere alla superficie dal buffer consiste nel chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), usando il servizio buffer di identificazione del servizio \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc706-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="cc706-122">Se il parametro *pUnkSurface* è **null**, l'esempio video viene creato con zero buffer multimediali.</span><span class="sxs-lookup"><span data-stu-id="cc706-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="cc706-123">Per aggiungere un buffer all'esempio, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc706-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="cc706-124">Creare una superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc706-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="cc706-125">Creare un buffer di superficie chiamando [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span><span class="sxs-lookup"><span data-stu-id="cc706-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="cc706-126">Per ulteriori informazioni, vedere la pagina relativa al [buffer della superficie DirectX](directx-surface-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="cc706-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="cc706-127">Aggiungere il buffer all'esempio chiamando [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="cc706-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="cc706-128">Utilizzare questo approccio se è necessario che la memoria della superficie sia accessibile tramite l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cc706-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc706-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc706-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc706-130">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="cc706-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="cc706-131">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="cc706-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
