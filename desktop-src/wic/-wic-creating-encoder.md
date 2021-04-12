---
description: Un codificatore scrive i dati dell'immagine in un flusso. I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Panoramica della codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233542"
---
# <a name="encoding-overview"></a><span data-ttu-id="f5e38-104">Panoramica della codifica</span><span class="sxs-lookup"><span data-stu-id="f5e38-104">Encoding Overview</span></span>

<span data-ttu-id="f5e38-105">Un codificatore scrive i dati dell'immagine in un flusso.</span><span class="sxs-lookup"><span data-stu-id="f5e38-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="f5e38-106">I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso.</span><span class="sxs-lookup"><span data-stu-id="f5e38-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="f5e38-107">L'uso di alcuni codificatori comporta compromessi, ad esempio JPEG, che commercia le informazioni sui colori per una migliore compressione.</span><span class="sxs-lookup"><span data-stu-id="f5e38-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="f5e38-108">Gli altri codificatori non generano tali perdite, ad esempio bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="f5e38-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="f5e38-109">Poiché molti codec usano la tecnologia proprietaria per ottenere una migliore compressione e fedeltà delle immagini, i dettagli sul modo in cui un'immagine viene codificata sono gli sviluppatori di codec.</span><span class="sxs-lookup"><span data-stu-id="f5e38-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="f5e38-110">In questo argomento sono incluse le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5e38-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="f5e38-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="f5e38-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="f5e38-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="f5e38-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="f5e38-113">Esempio di codifica TIFF</span><span class="sxs-lookup"><span data-stu-id="f5e38-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="f5e38-114">Utilizzo delle opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="f5e38-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="f5e38-115">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="f5e38-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="f5e38-116">Esempi di opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="f5e38-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="f5e38-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5e38-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="f5e38-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="f5e38-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="f5e38-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) è l'interfaccia principale per la codifica di un'immagine nel formato di destinazione e usata per serializzare i componenti di un'immagine, ad esempio l'anteprima ([**dithumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) e i frame ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="f5e38-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="f5e38-120">Il modo e il momento in cui viene eseguita la serializzazione viene lasciato allo sviluppatore di codec.</span><span class="sxs-lookup"><span data-stu-id="f5e38-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="f5e38-121">Ogni singolo blocco di dati nel formato di file di destinazione deve essere in grado di impostare in modo indipendente dall'ordine, ma anche in questo caso si tratta della decisione dello sviluppatore di codec.</span><span class="sxs-lookup"><span data-stu-id="f5e38-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="f5e38-122">Quando viene chiamato il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) , tuttavia, le modifiche all'immagine non devono essere consentite e il flusso deve essere chiuso.</span><span class="sxs-lookup"><span data-stu-id="f5e38-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="f5e38-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="f5e38-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="f5e38-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) è l'interfaccia per la codifica dei singoli frame di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f5e38-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="f5e38-125">Fornisce metodi per l'impostazione di singoli componenti per la creazione di immagini di frame, ad esempio anteprime e frame, oltre a formati di dimensioni immagine, DPI e pixel.</span><span class="sxs-lookup"><span data-stu-id="f5e38-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="f5e38-126">I singoli frame possono essere codificati con metadati specifici del frame, in modo che [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) fornisca l'accesso a un writer di metadati tramite il metodo [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="f5e38-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="f5e38-127">Il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del frame consente di eseguire il commit di tutte le modifiche apportate al singolo frame e indica che le modifiche apportate al frame non devono essere più accettate.</span><span class="sxs-lookup"><span data-stu-id="f5e38-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="f5e38-128">Esempio di codifica TIFF</span><span class="sxs-lookup"><span data-stu-id="f5e38-128">TIFF Encoding Example</span></span>

<span data-ttu-id="f5e38-129">Nell'esempio seguente viene codificata un'immagine Tagged Image File Format (TIFF) utilizzando [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e un [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="f5e38-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="f5e38-130">L'output TIFF è personalizzato con [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) e il frame bitmap viene inizializzato usando le opzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="f5e38-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="f5e38-131">Dopo che l'immagine è stata creata con [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), il frame viene sottoposto a commit tramite [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) e l'immagine viene salvata tramite [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span><span class="sxs-lookup"><span data-stu-id="f5e38-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a><span data-ttu-id="f5e38-132">Utilizzo delle opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="f5e38-132">Encoder Options Usage</span></span>

<span data-ttu-id="f5e38-133">Codificatori diversi per formati diversi devono esporre opzioni diverse per la modalità di codifica di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f5e38-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="f5e38-134">Windows Imaging Component (WIC) fornisce un meccanismo coerente per esprimere se le opzioni di codifica sono necessarie pur continuando a consentire alle applicazioni di usare più codificatori senza richiedere la conoscenza di un particolare formato.</span><span class="sxs-lookup"><span data-stu-id="f5e38-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="f5e38-135">Questa operazione viene eseguita fornendo un parametro [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) nel metodo [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) e nel metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="f5e38-135">This is accomplished by providing an [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="f5e38-136">Il componente Factory fornisce un semplice punto di creazione per la creazione di un contenitore delle proprietà Opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="f5e38-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="f5e38-137">I codec possono utilizzare questo servizio se è necessario fornire un set semplice, intuitivo e non in conflitto di opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="f5e38-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="f5e38-138">Il contenitore delle proprietà di imaging deve essere inizializzato durante la creazione con tutte le opzioni del codificatore rilevanti per il codec.</span><span class="sxs-lookup"><span data-stu-id="f5e38-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="f5e38-139">Per le opzioni del codificatore dal set canonico, l'intervallo di valori verrà applicato durante la scrittura.</span><span class="sxs-lookup"><span data-stu-id="f5e38-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="f5e38-140">Per esigenze più avanzate, i codec devono scrivere la propria implementazione del contenitore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5e38-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="f5e38-141">Un'applicazione riceve il contenitore delle opzioni del codificatore durante la creazione del frame e deve configurare tutti i valori prima dell'inizializzazione del frame del codificatore.</span><span class="sxs-lookup"><span data-stu-id="f5e38-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="f5e38-142">Per un'applicazione basata su interfaccia utente, può offrire un'interfaccia utente fissa per le opzioni del codificatore canonico e una visualizzazione avanzata per le opzioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f5e38-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="f5e38-143">Le modifiche possono essere apportate una alla volta tramite il metodo Write e tutti gli errori vengono segnalati tramite IErrorLog.</span><span class="sxs-lookup"><span data-stu-id="f5e38-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="f5e38-144">L'applicazione dell'interfaccia utente deve sempre rileggere e visualizzare tutte le opzioni dopo avere apportato una modifica nel caso in cui la modifica abbia causato un effetto a cascata.</span><span class="sxs-lookup"><span data-stu-id="f5e38-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="f5e38-145">Un'applicazione deve essere preparata per gestire l'inizializzazione non riuscita dei frame per i codec che forniscono solo una segnalazione minima degli errori tramite il contenitore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5e38-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="f5e38-146">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="f5e38-146">Encoder Options</span></span>

<span data-ttu-id="f5e38-147">Si può prevedere che un'applicazione riscontri il set di opzioni del codificatore seguente.</span><span class="sxs-lookup"><span data-stu-id="f5e38-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="f5e38-148">Le opzioni del codificatore riflettono le funzionalità di un codificatore e il formato del contenitore sottostante e pertanto sono di natura non indipendenti dal codec.</span><span class="sxs-lookup"><span data-stu-id="f5e38-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="f5e38-149">Quando possibile, è necessario normalizzare le nuove opzioni in modo che possano essere applicate ai nuovi codec che emergono.</span><span class="sxs-lookup"><span data-stu-id="f5e38-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="f5e38-150">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="f5e38-150">Property Name</span></span>      | <span data-ttu-id="f5e38-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f5e38-151">VARTYPE</span></span>  | <span data-ttu-id="f5e38-152">Valore</span><span class="sxs-lookup"><span data-stu-id="f5e38-152">Value</span></span>                                                                     | <span data-ttu-id="f5e38-153">Codec applicabili</span><span class="sxs-lookup"><span data-stu-id="f5e38-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="f5e38-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="f5e38-154">ImageQuality</span></span>       | <span data-ttu-id="f5e38-155">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-155">VT\_R4</span></span>   | <span data-ttu-id="f5e38-156">0-1.0</span><span class="sxs-lookup"><span data-stu-id="f5e38-156">0-1.0</span></span>                                                                     | <span data-ttu-id="f5e38-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="f5e38-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="f5e38-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="f5e38-158">CompressionQuality</span></span> | <span data-ttu-id="f5e38-159">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-159">VT\_R4</span></span>   | <span data-ttu-id="f5e38-160">0-1.0</span><span class="sxs-lookup"><span data-stu-id="f5e38-160">0-1.0</span></span>                                                                     | <span data-ttu-id="f5e38-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="f5e38-161">TIFF</span></span>              |
| <span data-ttu-id="f5e38-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="f5e38-162">Lossless</span></span>           | <span data-ttu-id="f5e38-163">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-163">VT\_BOOL</span></span> | <span data-ttu-id="f5e38-164">**true**, **false**</span><span class="sxs-lookup"><span data-stu-id="f5e38-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="f5e38-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="f5e38-165">HDPhoto</span></span>           |
| <span data-ttu-id="f5e38-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="f5e38-166">BitmapTransform</span></span>    | <span data-ttu-id="f5e38-167">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-167">VT\_UI1</span></span>  | [<span data-ttu-id="f5e38-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="f5e38-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="f5e38-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="f5e38-169">JPEG</span></span>              |



 

<span data-ttu-id="f5e38-170">ImageQualty di 0,0 indica il livello di fedeltà più basso possibile e 1,0 significa la massima fedeltà, che può implicare anche la perdita di perdite a seconda del codec.</span><span class="sxs-lookup"><span data-stu-id="f5e38-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="f5e38-171">CompressionQuality 0,0 indica lo schema di compressione meno efficiente disponibile, in genere con un output di codifica veloce ma di dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="f5e38-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="f5e38-172">Il valore 1,0 indica lo schema più efficiente disponibile, che richiede in genere più tempo per la codifica, ma produce un output ridotto.</span><span class="sxs-lookup"><span data-stu-id="f5e38-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="f5e38-173">A seconda delle funzionalità del codec, questo intervallo può essere mappato su un set discreto di metodi di compressione disponibili.</span><span class="sxs-lookup"><span data-stu-id="f5e38-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="f5e38-174">Lossless significa che il codec codifica l'immagine come perdita di dati senza perdita di dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f5e38-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="f5e38-175">Se il lossless è abilitato, ImageQuality viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f5e38-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="f5e38-176">Oltre alle opzioni del codificatore generico sopra indicate, i codec forniti con WIC supportano le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5e38-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="f5e38-177">Se un codec ha la necessità di supportare un'opzione coerente con l'utilizzo in questi codec forniti, è consigliabile farlo.</span><span class="sxs-lookup"><span data-stu-id="f5e38-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="f5e38-178">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="f5e38-178">Property Name</span></span>           | <span data-ttu-id="f5e38-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f5e38-179">VARTYPE</span></span>           | <span data-ttu-id="f5e38-180">Valore</span><span class="sxs-lookup"><span data-stu-id="f5e38-180">Value</span></span>                                                                             | <span data-ttu-id="f5e38-181">Codec applicabili</span><span class="sxs-lookup"><span data-stu-id="f5e38-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="f5e38-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="f5e38-182">InterlaceOption</span></span>         | <span data-ttu-id="f5e38-183">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-183">VT\_BOOL</span></span>          | <span data-ttu-id="f5e38-184">Attivato/Disattivato</span><span class="sxs-lookup"><span data-stu-id="f5e38-184">On/Off</span></span>                                                                            | <span data-ttu-id="f5e38-185">PNG</span><span class="sxs-lookup"><span data-stu-id="f5e38-185">PNG</span></span>               |
| <span data-ttu-id="f5e38-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="f5e38-186">FilterOption</span></span>            | <span data-ttu-id="f5e38-187">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-187">VT\_UI1</span></span>           | [<span data-ttu-id="f5e38-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="f5e38-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="f5e38-189">PNG</span><span class="sxs-lookup"><span data-stu-id="f5e38-189">PNG</span></span>               |
| <span data-ttu-id="f5e38-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="f5e38-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="f5e38-191">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-191">VT\_UI1</span></span>           | [<span data-ttu-id="f5e38-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="f5e38-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="f5e38-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="f5e38-193">TIFF</span></span>              |
| <span data-ttu-id="f5e38-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="f5e38-194">Luminance</span></span>               | <span data-ttu-id="f5e38-195">\_Array VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="f5e38-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="f5e38-196">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="f5e38-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="f5e38-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="f5e38-197">JPEG</span></span>              |
| <span data-ttu-id="f5e38-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="f5e38-198">Chrominance</span></span>             | <span data-ttu-id="f5e38-199">\_Array VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="f5e38-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="f5e38-200">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="f5e38-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="f5e38-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="f5e38-201">JPEG</span></span>              |
| <span data-ttu-id="f5e38-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="f5e38-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="f5e38-203">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-203">VT\_UI1</span></span>           | [<span data-ttu-id="f5e38-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="f5e38-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="f5e38-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="f5e38-205">JPEG</span></span>              |
| <span data-ttu-id="f5e38-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="f5e38-206">SuppressApp0</span></span>            | <span data-ttu-id="f5e38-207">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="f5e38-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="f5e38-208">JPEG</span></span>              |
| <span data-ttu-id="f5e38-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="f5e38-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="f5e38-210">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="f5e38-210">VT\_BOOL</span></span>          | <span data-ttu-id="f5e38-211">Attivato/Disattivato</span><span class="sxs-lookup"><span data-stu-id="f5e38-211">On/Off</span></span>                                                                            | <span data-ttu-id="f5e38-212">BMP</span><span class="sxs-lookup"><span data-stu-id="f5e38-212">BMP</span></span>               |



 

<span data-ttu-id="f5e38-213">Usare **VT \_ vuoto** per indicare che **\* non \* è impostato** come predefinito.</span><span class="sxs-lookup"><span data-stu-id="f5e38-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="f5e38-214">Se sono state impostate proprietà aggiuntive ma non supportate, il codificatore deve ignorarle; Ciò consente alle applicazioni di codificare meno logica se desiderano una funzionalità che può o non essere presente.</span><span class="sxs-lookup"><span data-stu-id="f5e38-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="f5e38-215">Esempi di opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="f5e38-215">Encoder Options Examples</span></span>

<span data-ttu-id="f5e38-216">Nell' [esempio di codifica TIFF](#tiff-encoding-example) precedente è impostata un'opzione specifica del codificatore.</span><span class="sxs-lookup"><span data-stu-id="f5e38-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="f5e38-217">Il membro *pstrName* della struttura Campo PROPBAG2 è impostato sul nome di proprietà appropriato e la variante è impostata sul VarType corrispondente e sul valore desiderato, in questo caso un membro dell'enumerazione [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .</span><span class="sxs-lookup"><span data-stu-id="f5e38-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="f5e38-218">Per usare le opzioni del codificatore predefinite, è sufficiente inizializzare il frame bitmap con l'elenco delle proprietà restituito al momento della creazione del frame.</span><span class="sxs-lookup"><span data-stu-id="f5e38-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="f5e38-219">È anche possibile eliminare il contenitore delle proprietà quando non vengono prese in considerazione opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="f5e38-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="f5e38-220">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5e38-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f5e38-221">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f5e38-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5e38-222">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="f5e38-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="f5e38-223">Panoramica della decodifica</span><span class="sxs-lookup"><span data-stu-id="f5e38-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="f5e38-224">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="f5e38-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f5e38-225">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="f5e38-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
