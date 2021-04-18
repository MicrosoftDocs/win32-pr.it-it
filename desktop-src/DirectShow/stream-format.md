---
description: Formato flusso
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316299"
---
# <a name="stream-format"></a><span data-ttu-id="10246-103">Formato flusso</span><span class="sxs-lookup"><span data-stu-id="10246-103">Stream Format</span></span>

<span data-ttu-id="10246-104">Sia MSDV che il driver UVC possono restituire due formati DV: audio-video interleaved o solo video.</span><span class="sxs-lookup"><span data-stu-id="10246-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="10246-105">Audio-video con interfoliazione è il formato originale dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10246-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="10246-106">Il formato solo video contiene gli stessi dati, ma gli esempi sono contrassegnati come privi di dati audio.</span><span class="sxs-lookup"><span data-stu-id="10246-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="10246-107">Il formato solo video è disponibile principalmente per la compatibilità con le applicazioni che utilizzano video per Windows.</span><span class="sxs-lookup"><span data-stu-id="10246-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="10246-108">Per ulteriori informazioni, vedere la pagina relativa ai [file AVI DV](type-1-vs--type-2-dv-avi-files.md)di tipo 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="10246-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="10246-109">**Driver MSDV**</span><span class="sxs-lookup"><span data-stu-id="10246-109">**MSDV Driver**</span></span>

<span data-ttu-id="10246-110">Il driver MSDV ha due pin di output.</span><span class="sxs-lookup"><span data-stu-id="10246-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="10246-111">Il primo pin di output invia dati con interfoliazione e il secondo pin di output invia dati di solo video.</span><span class="sxs-lookup"><span data-stu-id="10246-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="10246-112">È possibile connettere solo un pin di output alla volta.</span><span class="sxs-lookup"><span data-stu-id="10246-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="10246-113">Per selezionare un formato, connettere il pin di output appropriato.</span><span class="sxs-lookup"><span data-stu-id="10246-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="10246-114">Per trovare il formato, è possibile usare l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sul pin di output.</span><span class="sxs-lookup"><span data-stu-id="10246-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="10246-115">**Driver UVC**</span><span class="sxs-lookup"><span data-stu-id="10246-115">**UVC Driver**</span></span>

<span data-ttu-id="10246-116">Diversamente dal driver MSDV, il driver UVC fornisce entrambi i formati dallo stesso pin.</span><span class="sxs-lookup"><span data-stu-id="10246-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="10246-117">Il formato predefinito è solo video.</span><span class="sxs-lookup"><span data-stu-id="10246-117">The default format is video-only.</span></span> <span data-ttu-id="10246-118">Per selezionare il formato, usare l'interfaccia **IAMStreamConfig** sul pin di output.</span><span class="sxs-lookup"><span data-stu-id="10246-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="10246-119">Chiamare il metodo **GetStreamCaps** per enumerare i tipi di supporto sul pin di output.</span><span class="sxs-lookup"><span data-stu-id="10246-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="10246-120">Per ogni tipo di supporto, se il tipo principale corrisponde al formato desiderato, chiamare **Seformatt** e passare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="10246-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="10246-121">Formato</span><span class="sxs-lookup"><span data-stu-id="10246-121">Format</span></span>                      | <span data-ttu-id="10246-122">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="10246-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="10246-123">Audio e video con interfoliazione</span><span class="sxs-lookup"><span data-stu-id="10246-123">Interleaved audio and video</span></span> | <span data-ttu-id="10246-124">MEDIATYPE con \_ interfoliazione</span><span class="sxs-lookup"><span data-stu-id="10246-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="10246-125">Solo video</span><span class="sxs-lookup"><span data-stu-id="10246-125">Video only</span></span>                  | <span data-ttu-id="10246-126">Video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="10246-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="10246-127">La funzione seguente imposta il formato in base al GUID di tipo principale.</span><span class="sxs-lookup"><span data-stu-id="10246-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="10246-128">Il driver MSDV supporta anche **IAMStreamConfig**, quindi è possibile scrivere codice che funziona per entrambi i tipi di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10246-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10246-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10246-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10246-130">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="10246-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



