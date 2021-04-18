---
description: Passaggio 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Passaggio 3A. Implementare il metodo CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316327"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="8d609-104">Passaggio 3A.</span><span class="sxs-lookup"><span data-stu-id="8d609-104">Step 3A.</span></span> <span data-ttu-id="8d609-105">Implementare il metodo CheckInputType</span><span class="sxs-lookup"><span data-stu-id="8d609-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="8d609-106">Questo è il passaggio 3A dell'esercitazione [scrittura dei filtri di trasformazione](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8d609-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="8d609-107">Il metodo [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) viene chiamato quando il filtro upstream propone un tipo di supporto al filtro di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="8d609-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="8d609-108">Questo metodo accetta un puntatore a un oggetto [**CMediaType**](cmediatype.md) , che è un wrapper sottile per la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="8d609-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="8d609-109">In questo metodo, è necessario esaminare ogni campo pertinente della struttura del **\_ \_ tipo di supporto am** , inclusi i campi nel blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="8d609-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="8d609-110">È possibile usare i metodi della funzione di accesso definiti in **CMediaType** o fare riferimento direttamente ai membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="8d609-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="8d609-111">Se un campo non è valido, restituire il \_ tipo VFW E \_ \_ non \_ accettato.</span><span class="sxs-lookup"><span data-stu-id="8d609-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="8d609-112">Se l'intero tipo di supporto è valido, restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d609-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="8d609-113">Nel filtro del codificatore RLE, ad esempio, il tipo di input deve essere un video RGB non compresso a 8 bit o a 4 bit.</span><span class="sxs-lookup"><span data-stu-id="8d609-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="8d609-114">Non esiste alcun motivo per supportare altri formati di input, ad esempio a 16 o a 24 bit RGB, perché il filtro avrebbe dovuto convertirli in una profondità di bit inferiore e DirectShow fornisce già un filtro del [convertitore dello spazio dei colori](color-space-converter-filter.md) a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="8d609-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="8d609-115">Nell'esempio seguente si presuppone che il codificatore supporti video a 8 bit, ma non video a 4 bit:</span><span class="sxs-lookup"><span data-stu-id="8d609-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="8d609-116">In questo esempio, il metodo controlla prima di tutto il tipo principale e il sottotipo.</span><span class="sxs-lookup"><span data-stu-id="8d609-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="8d609-117">Quindi controlla il tipo di formato, per assicurarsi che il blocco di formato sia una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="8d609-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="8d609-118">Il filtro può inoltre supportare [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), ma in questo caso non esiste alcun vantaggio reale.</span><span class="sxs-lookup"><span data-stu-id="8d609-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="8d609-119">La struttura **VIDEOINFOHEADER2** aggiunge il supporto per l'interlacciamento e i pixel non quadrati, che probabilmente non saranno rilevanti nei video a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="8d609-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="8d609-120">Se il tipo di formato è corretto, nell'esempio vengono controllati i membri **biBitCount** e **biCompression** della struttura **VIDEOINFOHEADER** per verificare che il formato sia RGB non compresso a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="8d609-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="8d609-121">Come illustrato in questo esempio, è necessario forzare il</span><span class="sxs-lookup"><span data-stu-id="8d609-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="8d609-122">puntatore alla struttura corretta, in base al tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="8d609-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="8d609-123">Controllare sempre il tipo di formato GUID (**formatType**) e le dimensioni del blocco di formato (**cbFormat**) prima di eseguire il cast del puntatore.</span><span class="sxs-lookup"><span data-stu-id="8d609-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="8d609-124">Nell'esempio viene inoltre verificato che il numero di voci della tavolozza è compatibile con la profondità del bit e il blocco di formato è sufficientemente grande da poter essere utilizzato per le voci della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="8d609-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="8d609-125">Se tutte le informazioni sono corrette, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d609-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="8d609-126">[Passaggio 3b. implementare il metodo GetMediaType](step-3b--implement-the-getmediatype-method.md).</span><span class="sxs-lookup"><span data-stu-id="8d609-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d609-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d609-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d609-128">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="8d609-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



