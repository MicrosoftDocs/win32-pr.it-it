---
description: Impostazione dei tipi di supporto in un DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Impostazione dei tipi di supporto in un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320744"
---
# <a name="setting-media-types-on-a-dmo"></a><span data-ttu-id="227d1-103">Impostazione dei tipi di supporto in un DMO</span><span class="sxs-lookup"><span data-stu-id="227d1-103">Setting Media Types on a DMO</span></span>

<span data-ttu-id="227d1-104">Prima che un DMO possa elaborare i dati, il client deve impostare il tipo di supporto per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="227d1-104">Before a DMO can process any data, the client must set the media type for each stream.</span></span> <span data-ttu-id="227d1-105">Esiste una sola eccezione secondaria a questa regola. vedere [flussi facoltativi](optional-streams.md). Per trovare il numero di flussi, chiamare il metodo [**IMediaObject:: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :</span><span class="sxs-lookup"><span data-stu-id="227d1-105">(There is one minor exception to this rule; see [Optional Streams](optional-streams.md).) To find the number of streams, call the [**IMediaObject::GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) method:</span></span>


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



<span data-ttu-id="227d1-106">Questo metodo restituisce due valori, il numero di input e il numero di output.</span><span class="sxs-lookup"><span data-stu-id="227d1-106">This method returns two values, the number of inputs and the number of outputs.</span></span> <span data-ttu-id="227d1-107">Questi valori sono corretti per la durata di DMO.</span><span class="sxs-lookup"><span data-stu-id="227d1-107">These values are fixed for the lifetime of the DMO.</span></span>

<span data-ttu-id="227d1-108">**Tipi preferiti**</span><span class="sxs-lookup"><span data-stu-id="227d1-108">**Preferred Types**</span></span>

<span data-ttu-id="227d1-109">Per ogni flusso, DMO assegna un elenco di tipi di supporti possibili, in ordine di preferenza.</span><span class="sxs-lookup"><span data-stu-id="227d1-109">For every stream, the DMO assigns a list of possible media types, in order of preference.</span></span> <span data-ttu-id="227d1-110">Ad esempio, i tipi preferiti possono essere 32-RGB, RGB a 24 bit e RGB a 16 bit, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="227d1-110">For example, the preferred types might be 32-RGB, 24-bit RGB, and 16-bit RGB, in that order.</span></span> <span data-ttu-id="227d1-111">Quando il client imposta i tipi di supporto, può utilizzare questi elenchi come hint.</span><span class="sxs-lookup"><span data-stu-id="227d1-111">When the client sets the media types, it can use these lists as a hint.</span></span> <span data-ttu-id="227d1-112">Per recuperare un tipo preferito per un flusso, chiamare il metodo [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) o [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="227d1-112">To retrieve a preferred type for a stream, call the [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) method or [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) method.</span></span> <span data-ttu-id="227d1-113">Specificare il numero di flusso e un valore di indice per il tipo (a partire da zero).</span><span class="sxs-lookup"><span data-stu-id="227d1-113">Specify the stream number and an index value for the type (starting from zero).</span></span> <span data-ttu-id="227d1-114">Il codice seguente, ad esempio, recupera il primo tipo preferito dal primo flusso di input:</span><span class="sxs-lookup"><span data-stu-id="227d1-114">For example, the following code retrieves the first preferred type from the first input stream:</span></span>


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="227d1-115">Per enumerare tutti i tipi di supporto preferiti in un determinato flusso, usare un ciclo che incrementa l'indice del tipo fino a quando il metodo non restituisce DMO \_ E \_ nessun \_ altro \_ elemento, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="227d1-115">To enumerate all of the preferred media types on a given stream, use a loop that increments the type index until the method returns DMO\_E\_NO\_MORE\_ITEMS, as shown in the following example:</span></span>


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



<span data-ttu-id="227d1-116">Si notino i seguenti punti sui tipi preferiti:</span><span class="sxs-lookup"><span data-stu-id="227d1-116">You should note the following points about preferred types:</span></span>

-   <span data-ttu-id="227d1-117">DMO potrebbe restituire un tipo senza blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="227d1-117">The DMO might return a type that has no format block.</span></span> <span data-ttu-id="227d1-118">Ad esempio, un DMO potrebbe specificare un tipo video, ad esempio RGB a 24 bit, senza fornire la larghezza e l'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="227d1-118">For example, a DMO could specify a video type, such as 24-bit RGB, without providing the width and height of the image.</span></span> <span data-ttu-id="227d1-119">Quando si imposta il tipo, tuttavia, è necessario fornire un blocco di formato completo.</span><span class="sxs-lookup"><span data-stu-id="227d1-119">When you set the type, however, you must provide a complete format block.</span></span> <span data-ttu-id="227d1-120">(Alcuni tipi di supporti, ad esempio MIDI, non richiedono mai un blocco di formato. in tal caso, questo contrassegno non è applicabile).</span><span class="sxs-lookup"><span data-stu-id="227d1-120">(Some media types, such as MIDI, never require a format block, in which case this remark does not apply.)</span></span>
-   <span data-ttu-id="227d1-121">Non è necessario che DMO supporti ogni combinazione di tipi preferiti restituiti.</span><span class="sxs-lookup"><span data-stu-id="227d1-121">The DMO is not required to support every combination of preferred types that it returns.</span></span> <span data-ttu-id="227d1-122">Se, ad esempio, in un DMO sono presenti due flussi e ogni flusso dispone di quattro tipi preferiti, sono disponibili 16 combinazioni, ma non tutte sono sicuramente valide.</span><span class="sxs-lookup"><span data-stu-id="227d1-122">For example, if a DMO has two streams, and each stream has four preferred types, there are 16 possible combinations, but not all of them are guaranteed to be valid.</span></span>
-   <span data-ttu-id="227d1-123">Quando il client imposta il tipo di supporto per un flusso, DMO potrebbe aggiornare i tipi preferiti affinché altri flussi riflettano il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="227d1-123">When the client sets the media type for one stream, the DMO might update the preferred types for other streams to reflect the new state.</span></span> <span data-ttu-id="227d1-124">Tuttavia, non è necessario eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="227d1-124">It is not required to do so, however.</span></span>
-   <span data-ttu-id="227d1-125">Per alcuni flussi, DMO potrebbe non offrire i tipi preferiti.</span><span class="sxs-lookup"><span data-stu-id="227d1-125">For some streams, the DMO might not offer any preferred types.</span></span> <span data-ttu-id="227d1-126">In genere, un DMO dovrebbe offrire almeno alcuni tipi preferiti in alcuni flussi.</span><span class="sxs-lookup"><span data-stu-id="227d1-126">Typically, a DMO should offer at least some preferred types on some streams.</span></span>
-   <span data-ttu-id="227d1-127">Non è necessario che DMO offra un elenco completo dei tipi di supporti che può accettare.</span><span class="sxs-lookup"><span data-stu-id="227d1-127">The DMO is not required to offer a complete list of the media types it can accept.</span></span> <span data-ttu-id="227d1-128">Potrebbero essere presenti tipi "non pubblicizzati" supportati da DMO ma che non sono disponibili come tipi preferiti.</span><span class="sxs-lookup"><span data-stu-id="227d1-128">There might be "unadvertised" types that the DMO supports but does not offer as preferred types.</span></span>

<span data-ttu-id="227d1-129">In breve, il client deve considerare i tipi preferiti solo come linee guida.</span><span class="sxs-lookup"><span data-stu-id="227d1-129">In short, the client should treat the preferred types as guidelines only.</span></span> <span data-ttu-id="227d1-130">L'unico modo per stabilire quali tipi sono supportati consiste nel testarli, come descritto nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="227d1-130">The only way to know for certain which types are supported is to test them, as described in the next section.</span></span>

<span data-ttu-id="227d1-131">**Impostazione del tipo di supporto in un flusso**</span><span class="sxs-lookup"><span data-stu-id="227d1-131">**Setting the Media Type on a Stream**</span></span>

<span data-ttu-id="227d1-132">Usare i metodi [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) per impostare il tipo per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="227d1-132">Use the [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) and [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) methods to set the type for each stream.</span></span> <span data-ttu-id="227d1-133">È necessario fornire una struttura del **\_ \_ tipo di supporto DMO** che contiene una descrizione completa del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="227d1-133">You must provide a **DMO\_MEDIA\_TYPE** structure that contains a complete description of the media type.</span></span> <span data-ttu-id="227d1-134">L'esempio seguente imposta il tipo di supporto nel flusso di input 0, usando audio PCM stereo a 16 bit 44,1-kHz:</span><span class="sxs-lookup"><span data-stu-id="227d1-134">The following example sets the media type on input stream 0, using 44.1-kHz 16-bit stereo PCM audio:</span></span>


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



<span data-ttu-id="227d1-135">Per testare un tipo di supporto senza impostarlo, chiamare **SetInputType** o **SetOutputType** con il \_ flag DMO set \_ TYPEF \_ test \_ only.</span><span class="sxs-lookup"><span data-stu-id="227d1-135">To test a media type without setting it, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_TEST\_ONLY flag.</span></span> <span data-ttu-id="227d1-136">Il metodo restituisce \_ OK se il tipo è accettabile oppure s \_ false in caso contrario:</span><span class="sxs-lookup"><span data-stu-id="227d1-136">The method returns S\_OK if the type is acceptable, or S\_FALSE otherwise:</span></span>


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



<span data-ttu-id="227d1-137">Poiché le impostazioni in un flusso possono influire su un altro flusso, potrebbe essere necessario cancellare il tipo di supporto di un flusso.</span><span class="sxs-lookup"><span data-stu-id="227d1-137">Because the settings on one stream can affect another stream, you might need to clear a stream's media type.</span></span> <span data-ttu-id="227d1-138">A tale scopo, chiamare **SetInputType** o **SetOutputType** con il \_ flag DMO set \_ TYPEF \_ Clear.</span><span class="sxs-lookup"><span data-stu-id="227d1-138">To do this, call **SetInputType** or **SetOutputType** with the DMO\_SET\_TYPEF\_CLEAR flag.</span></span>

<span data-ttu-id="227d1-139">Per un decodificatore DMO, il client in genere imposta innanzitutto il tipo di input e quindi sceglie un tipo di output.</span><span class="sxs-lookup"><span data-stu-id="227d1-139">For a decoder DMO, the client would typically set the input type first, and then choose an output type.</span></span> <span data-ttu-id="227d1-140">Per un codificatore DMO, il client imposterà prima il tipo di output e quindi il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="227d1-140">For an encoder DMO, the client would set the output type first, and then the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="227d1-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="227d1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="227d1-142">Hosting diretto di un DMO</span><span class="sxs-lookup"><span data-stu-id="227d1-142">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



