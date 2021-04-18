---
description: Passaggio 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Passaggio 3B. Implementare il metodo GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530499"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="47c2d-104">Passaggio 3B.</span><span class="sxs-lookup"><span data-stu-id="47c2d-104">Step 3B.</span></span> <span data-ttu-id="47c2d-105">Implementare il metodo GetMediaType</span><span class="sxs-lookup"><span data-stu-id="47c2d-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="47c2d-106">Questo è il passaggio 3B dell'esercitazione sulla [scrittura dei filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="47c2d-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="47c2d-107">Questo passaggio non è necessario per i filtri che derivano da **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="47c2d-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="47c2d-108">Il metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) restituisce uno dei tipi di output preferiti del filtro, a cui fa riferimento il numero di indice.</span><span class="sxs-lookup"><span data-stu-id="47c2d-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="47c2d-109">Questo metodo non viene mai chiamato a meno che il pin di input del filtro non sia già connesso.</span><span class="sxs-lookup"><span data-stu-id="47c2d-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="47c2d-110">Pertanto, è possibile utilizzare il tipo di supporto della connessione upstream per determinare i tipi di output preferiti.</span><span class="sxs-lookup"><span data-stu-id="47c2d-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="47c2d-111">Un codificatore offre in genere un singolo tipo preferito, che rappresenta il formato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="47c2d-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="47c2d-112">I decodificatori in genere supportano una gamma di formati di output e li offrono in ordine di qualità o efficienza decrescente.</span><span class="sxs-lookup"><span data-stu-id="47c2d-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="47c2d-113">Ad esempio, l'elenco potrebbe essere UYVY, Y211, RGB-24, RGB-565, RGB-555 e RGB-8, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="47c2d-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="47c2d-114">I filtri effetti possono richiedere una corrispondenza esatta tra il formato di output e il formato di input.</span><span class="sxs-lookup"><span data-stu-id="47c2d-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="47c2d-115">Nell'esempio seguente viene restituito un singolo tipo di output, che viene costruito modificando il tipo di input per specificare la compressione RLE8:</span><span class="sxs-lookup"><span data-stu-id="47c2d-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



<span data-ttu-id="47c2d-116">In questo esempio, il metodo chiama [**Ipin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) per ottenere il tipo di input dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="47c2d-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="47c2d-117">Modifica quindi alcuni campi per indicare il formato di compressione, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="47c2d-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="47c2d-118">Assegna un nuovo GUID del sottotipo, costruito dal codice FOURCC ' MRLE ', usando la classe [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="47c2d-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="47c2d-119">Chiama il metodo [**CMediaType:: SetVariableSize**](cmediatype-setvariablesize.md) , che imposta il flag **bFixedSizeSamples** su **false** e il membro **lSampleSize** su zero, indicando esempi di dimensioni variabili.</span><span class="sxs-lookup"><span data-stu-id="47c2d-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="47c2d-120">Chiama il metodo [**CMediaType:: SetTemporalCompression**](cmediatype-settemporalcompression.md) con il valore **false**, a indicare che ogni frame è un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="47c2d-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="47c2d-121">(Questo campo è solo informativo, pertanto è possibile ignorarlo in modo sicuro).</span><span class="sxs-lookup"><span data-stu-id="47c2d-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="47c2d-122">Imposta il campo **biCompression** su bi \_ RLE8.</span><span class="sxs-lookup"><span data-stu-id="47c2d-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="47c2d-123">Imposta il campo **biSizeImage** sulla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="47c2d-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="47c2d-124">[Passaggio 3c: implementare il metodo CheckTransform](step-3c--implement-the-checktransform-method.md).</span><span class="sxs-lookup"><span data-stu-id="47c2d-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47c2d-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47c2d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47c2d-126">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="47c2d-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



