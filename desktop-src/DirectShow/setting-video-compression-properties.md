---
description: Impostazione delle proprietà di compressione video
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Impostazione delle proprietà di compressione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401235"
---
# <a name="setting-video-compression-properties"></a><span data-ttu-id="31d6b-103">Impostazione delle proprietà di compressione video</span><span class="sxs-lookup"><span data-stu-id="31d6b-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="31d6b-104">I filtri di compressione video possono supportare l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) nei pin di output.</span><span class="sxs-lookup"><span data-stu-id="31d6b-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="31d6b-105">Usare questa interfaccia per impostare le proprietà di compressione, ad esempio la frequenza dei fotogrammi chiave, il numero di frame stimati (P) per fotogramma chiave e la qualità di compressione relativa.</span><span class="sxs-lookup"><span data-stu-id="31d6b-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="31d6b-106">Chiamare innanzitutto il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) per trovare il pin di output del filtro ed eseguire una query sul pin per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="31d6b-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="31d6b-107">Alcuni filtri potrebbero non supportare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="31d6b-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="31d6b-108">Altri possono esporre l'interfaccia ma non supportare ogni proprietà di compressione.</span><span class="sxs-lookup"><span data-stu-id="31d6b-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="31d6b-109">Per determinare quali proprietà sono supportate, chiamare [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="31d6b-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="31d6b-110">Questo metodo restituisce diverse informazioni:</span><span class="sxs-lookup"><span data-stu-id="31d6b-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="31d6b-111">Un set di flag di funzionalità</span><span class="sxs-lookup"><span data-stu-id="31d6b-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="31d6b-112">Stringa descrittiva e stringa di numero di versione</span><span class="sxs-lookup"><span data-stu-id="31d6b-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="31d6b-113">Valori predefiniti per la frequenza dei fotogrammi chiave, la frequenza dei fotogrammi P e la qualità (se supportata)</span><span class="sxs-lookup"><span data-stu-id="31d6b-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="31d6b-114">Il metodo presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="31d6b-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="31d6b-115">I parametri *pszVersion* e *pszDesc* sono buffer a caratteri wide che ricevono la stringa di versione e la stringa di descrizione.</span><span class="sxs-lookup"><span data-stu-id="31d6b-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="31d6b-116">I parametri *cbVersion* e *cbDesc* ricevono le dimensioni del buffer richieste in byte (non caratteri).</span><span class="sxs-lookup"><span data-stu-id="31d6b-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="31d6b-117">I parametri *lKeyFrame*, *lPFrame* e *dblQuality* ricevono i valori predefiniti per la frequenza dei fotogrammi chiave, la frequenza dei fotogrammi P e la qualità.</span><span class="sxs-lookup"><span data-stu-id="31d6b-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="31d6b-118">La qualità è espressa come numero a virgola mobile compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="31d6b-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="31d6b-119">Il parametro *lCap* riceve **un operatore OR** bit per bit dei flag capabilities, definiti dal tipo enumerato [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) .</span><span class="sxs-lookup"><span data-stu-id="31d6b-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="31d6b-120">Uno di questi parametri può essere **null**, nel qual caso il metodo ignora il parametro.</span><span class="sxs-lookup"><span data-stu-id="31d6b-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="31d6b-121">Per allocare i buffer per le stringhe di versione e descrizione, ad esempio, chiamare prima il metodo con **null** nel primo e nel terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="31d6b-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="31d6b-122">Usare i valori restituiti per *cbVersion* e *cbDesc* per allocare i buffer e quindi chiamare di nuovo il metodo:</span><span class="sxs-lookup"><span data-stu-id="31d6b-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



<span data-ttu-id="31d6b-123">Il valore di *lCap* indica gli altri metodi **IAMVideoCompression** supportati dal filtro.</span><span class="sxs-lookup"><span data-stu-id="31d6b-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="31d6b-124">Se, ad esempio, *lCap* contiene il \_ flag CompressionCaps CanKeyFrame, è possibile chiamare [**IAMVideoCompression:: Get \_ framerate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) per ottenere la frequenza dei fotogrammi chiave e [**IAMVideoCompression::p la frequenza dei \_ fotogrammi**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) chiave per impostare la frequenza del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="31d6b-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="31d6b-125">Un valore negativo indica che il filtro utilizzerà il valore predefinito, come ottenuto da [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="31d6b-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="31d6b-126">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="31d6b-126">For example:</span></span>


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



<span data-ttu-id="31d6b-127">L'esempio di codice seguente tenta di trovare l'interfaccia **IAMVideoCompression** sul pin di output.</span><span class="sxs-lookup"><span data-stu-id="31d6b-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="31d6b-128">Se ha esito positivo, recupera i valori predefiniti e effettivi per le proprietà di compressione:</span><span class="sxs-lookup"><span data-stu-id="31d6b-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="31d6b-129">Se si usa l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) per compilare il grafo, è possibile ottenere l'interfaccia **IAMVideoCompression** chiamando [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), invece di usare **IBaseFilter:: EnumPins**.</span><span class="sxs-lookup"><span data-stu-id="31d6b-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="31d6b-130">Il metodo **FindInterface** è un metodo helper che cerca filtri e pin nel grafico per un'interfaccia specificata.</span><span class="sxs-lookup"><span data-stu-id="31d6b-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



