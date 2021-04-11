---
description: Buffer della superficie DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Buffer della superficie DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127903"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="94fcb-103">Buffer della superficie DirectX</span><span class="sxs-lookup"><span data-stu-id="94fcb-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="94fcb-104">L'oggetto buffer della superficie DirectX è un buffer multimediale che gestisce una superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="94fcb-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="94fcb-105">Per creare un'istanza di questo oggetto, chiamare [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) e passare un puntatore alla superficie DirectX.</span><span class="sxs-lookup"><span data-stu-id="94fcb-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="94fcb-106">Il buffer di superficie DirectX espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="94fcb-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="94fcb-107">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="94fcb-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="94fcb-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="94fcb-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="94fcb-109">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="94fcb-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="94fcb-110">Sono disponibili diversi modi per accedere alla memoria della superficie dall'oggetto buffer:</span><span class="sxs-lookup"><span data-stu-id="94fcb-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="94fcb-111">Consigliato: chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nel buffer.</span><span class="sxs-lookup"><span data-stu-id="94fcb-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="94fcb-112">Usare il **\_ \_ servizio buffer** di identificazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="94fcb-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="94fcb-113">Il metodo restituisce un puntatore alla superficie Direct3D sottostante.</span><span class="sxs-lookup"><span data-stu-id="94fcb-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="94fcb-114">Chiamare [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span><span class="sxs-lookup"><span data-stu-id="94fcb-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="94fcb-115">Questo metodo chiama **IDirect3DSurface9:: LockRect** direttamente sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="94fcb-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="94fcb-116">Il metodo [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) chiama **UnlockRect** sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="94fcb-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="94fcb-117">Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="94fcb-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="94fcb-118">In genere questa operazione non è consigliata, perché impone all'oggetto di copiare la memoria dall'area Direct3D e quindi di nuovo.</span><span class="sxs-lookup"><span data-stu-id="94fcb-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="94fcb-119">Il metodo [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="94fcb-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="94fcb-120">Sia [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) che [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) possono avere esito negativo se la superficie sottostante non è bloccabile.</span><span class="sxs-lookup"><span data-stu-id="94fcb-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="94fcb-121">Il buffer di superficie DirectX implementa questi due metodi principalmente per i componenti che non sono progettati per funzionare con le superfici Direct3D.</span><span class="sxs-lookup"><span data-stu-id="94fcb-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="94fcb-122">Il renderer video avanzato (EVR) crea buffer della superficie DirectX quando il decodificatore non è configurato per l'accelerazione video DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="94fcb-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="94fcb-123">Per ulteriori informazioni, vedere [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span><span class="sxs-lookup"><span data-stu-id="94fcb-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="94fcb-124">Recupero della superficie Direct3D</span><span class="sxs-lookup"><span data-stu-id="94fcb-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="94fcb-125">Per ottenere una superficie Direct3D da un esempio video, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="94fcb-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="94fcb-126">Chiamare [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) con un valore di indice pari a zero.</span><span class="sxs-lookup"><span data-stu-id="94fcb-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="94fcb-127">Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e specificare l'identificatore del servizio del **\_ \_ servizio di buffer** .</span><span class="sxs-lookup"><span data-stu-id="94fcb-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="94fcb-128">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="94fcb-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="94fcb-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94fcb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fcb-130">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="94fcb-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="94fcb-131">Esempi video</span><span class="sxs-lookup"><span data-stu-id="94fcb-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



