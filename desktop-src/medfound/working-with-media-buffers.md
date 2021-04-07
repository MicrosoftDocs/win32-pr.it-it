---
description: Uso dei buffer multimediali
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Uso dei buffer multimediali (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886000"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a><span data-ttu-id="4e31e-103">Uso dei buffer multimediali (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="4e31e-103">Working with Media Buffers (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4e31e-104">In questo argomento viene descritto come utilizzare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) per accedere ai dati in un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="4e31e-104">This topic describes how to use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface to access the data in a media buffer.</span></span> <span data-ttu-id="4e31e-105">Tutti i buffer multimediali espongono **IMFMediaBuffer**, progettato per qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="4e31e-105">All media buffers expose **IMFMediaBuffer**, which is designed for any type of data.</span></span> <span data-ttu-id="4e31e-106">I frame video non compressi costituiscono un caso speciale, descritti nell'argomento [buffer video non compressi](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="4e31e-106">Uncompressed video frames are a special case, described in the topic [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="buffer-size"></a><span data-ttu-id="4e31e-107">Dimensione buffer</span><span class="sxs-lookup"><span data-stu-id="4e31e-107">Buffer Size</span></span>

<span data-ttu-id="4e31e-108">A un buffer multimediale sono associate due dimensioni:</span><span class="sxs-lookup"><span data-stu-id="4e31e-108">A media buffer has two sizes associated with it:</span></span>

-   <span data-ttu-id="4e31e-109">La *lunghezza massima* corrisponde alla dimensione fisica della memoria allocata per il buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-109">The *maximum length* is the physical size of the memory that is allocated for the buffer.</span></span> <span data-ttu-id="4e31e-110">Questo valore viene impostato quando il buffer viene creato e non viene modificato durante il ciclo di vita del buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-110">This value is set when the buffer is created and does not change during the lifetime of the buffer.</span></span> <span data-ttu-id="4e31e-111">La lunghezza massima indica la quantità di dati che è possibile archiviare nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-111">The maximum length indicates how much data can be stored in the buffer.</span></span> <span data-ttu-id="4e31e-112">Per trovare le dimensioni massime, chiamare [**IMFMediaBuffer:: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span><span class="sxs-lookup"><span data-stu-id="4e31e-112">To find the maximum size, call [**IMFMediaBuffer::GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).</span></span>

-   <span data-ttu-id="4e31e-113">La *lunghezza corrente* corrisponde alla quantità di dati validi attualmente presenti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-113">The *current length* is the amount of valid data that is currently in the buffer.</span></span> <span data-ttu-id="4e31e-114">Quando il buffer viene allocato per la prima volta, la lunghezza corrente è zero, perché non sono presenti dati validi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-114">When the buffer is first allocated, the current length is zero, because there is no valid data in the buffer.</span></span> <span data-ttu-id="4e31e-115">Se si scrivono dati nel buffer, è necessario aggiornare la lunghezza corrente chiamando [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span><span class="sxs-lookup"><span data-stu-id="4e31e-115">If you write any data to the buffer, you must update the current length by calling [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength).</span></span> <span data-ttu-id="4e31e-116">Se, ad esempio, si scrivono 100 byte di dati nel buffer, chiamare **SetCurrentLength** con il valore 100.</span><span class="sxs-lookup"><span data-stu-id="4e31e-116">For example, if you write 100 bytes of data into the buffer, call **SetCurrentLength** with the value 100.</span></span> <span data-ttu-id="4e31e-117">Se si leggono i dati da un buffer multimediale, chiamare [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) per determinare la quantità di dati attualmente presenti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-117">If you read data from a media buffer, call [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) to find out how much data is currently in the buffer.</span></span> <span data-ttu-id="4e31e-118">Non leggere oltre la lunghezza corrente.</span><span class="sxs-lookup"><span data-stu-id="4e31e-118">Do not read past the current length.</span></span> <span data-ttu-id="4e31e-119">La lunghezza corrente non può mai superare la lunghezza massima del buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-119">The current length can never exceed the maximum length of the buffer.</span></span>

## <a name="accessing-the-buffer-memory"></a><span data-ttu-id="4e31e-120">Accesso alla memoria del buffer</span><span class="sxs-lookup"><span data-stu-id="4e31e-120">Accessing the Buffer Memory</span></span>

<span data-ttu-id="4e31e-121">Per accedere alla memoria nel buffer, chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="4e31e-121">To access the memory in the buffer, call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="4e31e-122">Questo metodo restituisce un puntatore all'inizio del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="4e31e-122">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="4e31e-123">Restituisce anche la lunghezza massima e la lunghezza corrente.</span><span class="sxs-lookup"><span data-stu-id="4e31e-123">It also returns the maximum length and the current length.</span></span> <span data-ttu-id="4e31e-124">Al termine dell'utilizzo del puntatore, chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="4e31e-124">When you are done using the pointer, call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="4e31e-125">Per scrivere i dati in un buffer multimediale:</span><span class="sxs-lookup"><span data-stu-id="4e31e-125">To write data into a media buffer:</span></span>

1.  <span data-ttu-id="4e31e-126">Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore alla memoria.</span><span class="sxs-lookup"><span data-stu-id="4e31e-126">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="4e31e-127">Il metodo restituisce anche la lunghezza massima del buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-127">The method also returns the buffer's maximum length.</span></span>
2.  <span data-ttu-id="4e31e-128">Scrivere i dati nella memoria, fino alla lunghezza massima del buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-128">Write your data into the memory, up to the buffer's maximum length.</span></span>
3.  <span data-ttu-id="4e31e-129">Chiamare [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) per aggiornare la lunghezza corrente.</span><span class="sxs-lookup"><span data-stu-id="4e31e-129">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the current length.</span></span> <span data-ttu-id="4e31e-130">Impostare la lunghezza corrente uguale alla quantità di dati scritti nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="4e31e-130">Set the current length equal to the amount of data that you wrote in step 2.</span></span>
4.  <span data-ttu-id="4e31e-131">Chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-131">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

<span data-ttu-id="4e31e-132">Per leggere i dati da un buffer multimediale:</span><span class="sxs-lookup"><span data-stu-id="4e31e-132">To read data from a media buffer:</span></span>

1.  <span data-ttu-id="4e31e-133">Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per ottenere un puntatore alla memoria.</span><span class="sxs-lookup"><span data-stu-id="4e31e-133">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the memory.</span></span> <span data-ttu-id="4e31e-134">Il metodo restituisce anche la lunghezza corrente del buffer (la quantità di dati validi nel buffer).</span><span class="sxs-lookup"><span data-stu-id="4e31e-134">The method also returns the buffer's current length (the amount of valid data in the buffer).</span></span>
2.  <span data-ttu-id="4e31e-135">Leggere il contenuto della memoria, fino alla lunghezza corrente.</span><span class="sxs-lookup"><span data-stu-id="4e31e-135">Read the contents of the memory, up to the current length.</span></span>
3.  <span data-ttu-id="4e31e-136">Chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-136">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>

## <a name="creating-system-memory-buffers"></a><span data-ttu-id="4e31e-137">Creazione di buffer di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="4e31e-137">Creating System Memory Buffers</span></span>

<span data-ttu-id="4e31e-138">Il buffer di memoria di sistema è un buffer multimediale che gestisce un blocco di memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e31e-138">The system memory buffer is a media buffer that manages a block of system memory.</span></span> <span data-ttu-id="4e31e-139">Per creare un'istanza di questo oggetto, chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) o [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) e specificare una dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-139">To create an instance of this object, call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) or [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) and specify a buffer size.</span></span> <span data-ttu-id="4e31e-140">Entrambe le funzioni allocano un blocco di memoria e restituiscono un puntatore [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="4e31e-140">Both functions allocate a block of memory and return an [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) pointer.</span></span> <span data-ttu-id="4e31e-141">La memoria viene rilasciata automaticamente quando il conteggio dei riferimenti del buffer multimediale raggiunge lo zero e l'oggetto viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="4e31e-141">The memory is automatically released when the media buffer's reference count reaches zero and the object is destroyed.</span></span>

<span data-ttu-id="4e31e-142">Nell'esempio seguente viene illustrato come creare un buffer di memoria di sistema e scrivere nel buffer.</span><span class="sxs-lookup"><span data-stu-id="4e31e-142">The following example shows how to create a system memory buffer and write to the buffer.</span></span>


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4e31e-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e31e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e31e-144">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="4e31e-144">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="4e31e-145">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e31e-145">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



