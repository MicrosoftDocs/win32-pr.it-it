---
description: Buffer video non compressi
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Buffer video non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310183"
---
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="b0182-103">Buffer video non compressi</span><span class="sxs-lookup"><span data-stu-id="b0182-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="b0182-104">Questo articolo descrive come usare i buffer multimediali che contengono frame video non compressi.</span><span class="sxs-lookup"><span data-stu-id="b0182-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="b0182-105">In ordine di preferenza sono disponibili le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0182-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="b0182-106">Non tutti i buffer multimediali supportano ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="b0182-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="b0182-107">Utilizzare la superficie Direct3D sottostante.</span><span class="sxs-lookup"><span data-stu-id="b0182-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="b0182-108">(Si applica solo ai frame video archiviati nelle superfici Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="b0182-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="b0182-109">Usare l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="b0182-110">Usare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="b0182-111">Usare la superficie Direct3D sottostante</span><span class="sxs-lookup"><span data-stu-id="b0182-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="b0182-112">Il fotogramma video potrebbe essere archiviato all'interno di una superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b0182-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="b0182-113">In tal caso, è possibile ottenere un puntatore all'area chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) o [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sull'oggetto buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="b0182-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="b0182-114">Usare il servizio buffer di identificazione del servizio \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b0182-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="b0182-115">Questo approccio è consigliato quando il componente che accede al frame video è progettato per l'uso di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b0182-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="b0182-116">Ad esempio, un decodificatore video che supporta l'accelerazione video DirectX deve usare questo approccio.</span><span class="sxs-lookup"><span data-stu-id="b0182-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="b0182-117">Il codice seguente illustra come ottenere il puntatore **IDirect3DSurface9** da un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="b0182-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



<span data-ttu-id="b0182-118">Gli oggetti seguenti supportano il servizio del **\_ \_ servizio buffer di Mr** :</span><span class="sxs-lookup"><span data-stu-id="b0182-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="b0182-119">Buffer della superficie DirectX</span><span class="sxs-lookup"><span data-stu-id="b0182-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="b0182-120">Esempi video</span><span class="sxs-lookup"><span data-stu-id="b0182-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="b0182-121">Usare l'interfaccia IMF2DBuffer</span><span class="sxs-lookup"><span data-stu-id="b0182-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="b0182-122">Se il fotogramma video non è archiviato in una superficie Direct3D o il componente non è progettato per l'utilizzo di Direct3D, il successivo metodo consigliato per accedere al frame video consiste nell'eseguire una query sul buffer per l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="b0182-123">Questa interfaccia è progettata specificamente per i dati di immagine.</span><span class="sxs-lookup"><span data-stu-id="b0182-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="b0182-124">Per ottenere un puntatore a questa interfaccia, chiamare **QueryInterface** sul buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="b0182-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="b0182-125">Non tutti gli oggetti buffer multimediali espongono questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b0182-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="b0182-126">Tuttavia, se un buffer multimediale espone l'interfaccia **IMF2DBuffer** , è consigliabile usare tale interfaccia per accedere ai dati, se possibile, invece di usare [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span><span class="sxs-lookup"><span data-stu-id="b0182-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="b0182-127">È comunque possibile usare l'interfaccia **IMFMediaBuffer** , ma potrebbe essere meno efficiente.</span><span class="sxs-lookup"><span data-stu-id="b0182-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="b0182-128">Chiamare **QueryInterface** sul buffer multimediale per ottenere l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="b0182-129">Chiamare [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) per accedere alla memoria per il buffer.</span><span class="sxs-lookup"><span data-stu-id="b0182-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="b0182-130">Questo metodo restituisce un puntatore al primo byte della prima riga di pixel.</span><span class="sxs-lookup"><span data-stu-id="b0182-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="b0182-131">Restituisce anche lo stride dell'immagine, ovvero il numero di byte dall'inizio di una riga di pixel all'inizio della riga successiva.</span><span class="sxs-lookup"><span data-stu-id="b0182-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="b0182-132">Il buffer potrebbe contenere byte di riempimento dopo ogni riga di pixel, quindi lo stride potrebbe essere più ampio della larghezza dell'immagine in byte.</span><span class="sxs-lookup"><span data-stu-id="b0182-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="b0182-133">Lo stride può anche essere negativo se l'immagine è orientata dal basso verso l'alto nella memoria.</span><span class="sxs-lookup"><span data-stu-id="b0182-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="b0182-134">Per ulteriori informazioni, vedere [Image stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="b0182-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="b0182-135">Mantieni il buffer bloccato solo quando devi accedere alla memoria.</span><span class="sxs-lookup"><span data-stu-id="b0182-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="b0182-136">Sbloccare il buffer chiamando [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span><span class="sxs-lookup"><span data-stu-id="b0182-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="b0182-137">Non tutti i buffer multimediali implementano l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="b0182-138">Se il buffer multimediale non implementa questa interfaccia, ovvero l'oggetto buffer restituisce E \_ nointerface nel passaggio 1, è necessario usare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) Interface, descritta di seguito.</span><span class="sxs-lookup"><span data-stu-id="b0182-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="b0182-139">Usare l'interfaccia IMFMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="b0182-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="b0182-140">Se un buffer multimediale non espone l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , usare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="b0182-141">La semantica generale di questa interfaccia è descritta nell'argomento [uso dei buffer multimediali](working-with-media-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="b0182-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="b0182-142">Chiamare **QueryInterface** sul buffer multimediale per ottenere l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="b0182-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="b0182-143">Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per accedere alla memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="b0182-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="b0182-144">Questo metodo restituisce un puntatore alla memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="b0182-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="b0182-145">Quando si usa il metodo **Lock** , lo stride è sempre lo stride minimo per il formato video in questione, senza ulteriori byte di riempimento.</span><span class="sxs-lookup"><span data-stu-id="b0182-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="b0182-146">Mantieni il buffer bloccato solo quando devi accedere alla memoria.</span><span class="sxs-lookup"><span data-stu-id="b0182-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="b0182-147">Sbloccare il buffer chiamando [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="b0182-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="b0182-148">È sempre consigliabile evitare di chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) se il buffer espone [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), perché il metodo **Lock** può forzare l'oggetto buffer sul frame video in un blocco di memoria contiguo e quindi nuovamente.</span><span class="sxs-lookup"><span data-stu-id="b0182-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="b0182-149">D'altra parte, se il buffer non supporta **IMF2DBuffer**, **IMFMediaBuffer:: Lock** probabilmente non genererà una copia.</span><span class="sxs-lookup"><span data-stu-id="b0182-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="b0182-150">Calcolare lo stride minimo dal tipo di supporto come segue:</span><span class="sxs-lookup"><span data-stu-id="b0182-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="b0182-151">Lo stride minimo potrebbe essere archiviato nell'attributo [**\_ \_ \_ stride predefinito di MF mt**](mf-mt-default-stride-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b0182-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="b0182-152">Se l' **attributo \_ \_ \_ stride predefinito di MF mt** non è impostato, chiamare la funzione [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) per calcolare lo stride per i formati video più comuni.</span><span class="sxs-lookup"><span data-stu-id="b0182-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="b0182-153">Se la funzione [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) non riconosce il formato, è necessario calcolare lo stride in base alla definizione del formato.</span><span class="sxs-lookup"><span data-stu-id="b0182-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="b0182-154">In tal caso, non esiste alcuna regola generale; è necessario avere informazioni dettagliate sulla definizione del formato.</span><span class="sxs-lookup"><span data-stu-id="b0182-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="b0182-155">Il codice seguente illustra come ottenere lo stride predefinito per i formati video più comuni.</span><span class="sxs-lookup"><span data-stu-id="b0182-155">The following code shows how to get the default stride for the most common video formats.</span></span>


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



<span data-ttu-id="b0182-156">A seconda dell'applicazione, è possibile sapere in anticipo se un determinato buffer multimediale supporta [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , ad esempio se è stato creato il buffer.</span><span class="sxs-lookup"><span data-stu-id="b0182-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="b0182-157">In caso contrario, è necessario essere pronti a utilizzare una delle due interfacce del buffer.</span><span class="sxs-lookup"><span data-stu-id="b0182-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="b0182-158">Nell'esempio seguente viene illustrata una classe helper che nasconde alcuni di questi dettagli.</span><span class="sxs-lookup"><span data-stu-id="b0182-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="b0182-159">Questa classe dispone di un metodo LockBuffer che chiama [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) o [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) e restituisce un puntatore all'inizio della prima riga di pixel.</span><span class="sxs-lookup"><span data-stu-id="b0182-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="b0182-160">Questo comportamento corrisponde al metodo **Lock2D** . Il metodo LockBuffer accetta lo stride predefinito come parametro di input e restituisce lo stride effettivo come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="b0182-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a><span data-ttu-id="b0182-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0182-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0182-162">Stride immagine</span><span class="sxs-lookup"><span data-stu-id="b0182-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="b0182-163">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="b0182-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



