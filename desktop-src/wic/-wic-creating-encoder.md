---
description: Un codificatore scrive i dati dell'immagine in un flusso. I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Cenni preliminari sulla codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f938e184dee7fd9b3e5348365550615ee28de70d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549486"
---
# <a name="encoding-overview"></a><span data-ttu-id="1e13d-104">Cenni preliminari sulla codifica</span><span class="sxs-lookup"><span data-stu-id="1e13d-104">Encoding Overview</span></span>

<span data-ttu-id="1e13d-105">Un codificatore scrive i dati dell'immagine in un flusso.</span><span class="sxs-lookup"><span data-stu-id="1e13d-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="1e13d-106">I codificatori possono comprimere, crittografare e modificare i pixel dell'immagine in diversi modi prima di scriverli nel flusso.</span><span class="sxs-lookup"><span data-stu-id="1e13d-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="1e13d-107">L'uso di alcuni codificatori comporta compromessi, ad esempio JPEG, che scambia le informazioni sui colori per una migliore compressione.</span><span class="sxs-lookup"><span data-stu-id="1e13d-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="1e13d-108">Altri codificatori non comportano perdite di questo tipo, ad esempio bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="1e13d-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="1e13d-109">Poiché molti codec usano una tecnologia proprietaria per ottenere una migliore compressione e fedeltà delle immagini, i dettagli su come viene codificata un'immagine sono a responsabilità dello sviluppatore di codec.</span><span class="sxs-lookup"><span data-stu-id="1e13d-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="1e13d-110">In questo argomento sono incluse le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e13d-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="1e13d-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="1e13d-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="1e13d-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="1e13d-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="1e13d-113">Esempio di codifica TIFF</span><span class="sxs-lookup"><span data-stu-id="1e13d-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="1e13d-114">Utilizzo delle opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1e13d-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="1e13d-115">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1e13d-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="1e13d-116">Esempi di opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1e13d-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="1e13d-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e13d-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="1e13d-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="1e13d-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="1e13d-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) è l'interfaccia principale per la codifica di un'immagine nel formato di destinazione e viene usata per serializzare i componenti di un'immagine, ad esempio thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) e frame ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)) nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="1e13d-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="1e13d-120">La modalità e il momento in cui viene eseguita la serializzazione vengono lasciati allo sviluppatore di codec.</span><span class="sxs-lookup"><span data-stu-id="1e13d-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="1e13d-121">Ogni singolo blocco di dati all'interno del formato di file di destinazione deve essere in grado di impostare in modo indipendente dall'ordine, ma anche in questo caso, questa è la decisione dello sviluppatore del codec.</span><span class="sxs-lookup"><span data-stu-id="1e13d-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="1e13d-122">Una volta chiamato il metodo [**Commit,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) tuttavia, le modifiche all'immagine non devono essere consentite e il flusso deve essere chiuso.</span><span class="sxs-lookup"><span data-stu-id="1e13d-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="1e13d-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="1e13d-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="1e13d-124">[**IWICBitmapFrameEncode è**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) l'interfaccia per codificare i singoli fotogrammi di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1e13d-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="1e13d-125">Fornisce metodi per l'impostazione di singoli componenti di creazione di immagini di fotogrammi, ad esempio anteprime e fotogrammi, nonché dimensioni dell'immagine, formati DPI e pixel.</span><span class="sxs-lookup"><span data-stu-id="1e13d-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="1e13d-126">I singoli frame possono essere codificati con metadati specifici del frame, quindi [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) fornisce l'accesso a un writer di metadati tramite il [**metodo GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)</span><span class="sxs-lookup"><span data-stu-id="1e13d-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="1e13d-127">Il metodo [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) del frame esegue il commit di tutte le modifiche al singolo frame e indica che le modifiche a tale frame non devono più essere accettate.</span><span class="sxs-lookup"><span data-stu-id="1e13d-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="1e13d-128">Esempio di codifica TIFF</span><span class="sxs-lookup"><span data-stu-id="1e13d-128">TIFF Encoding Example</span></span>

<span data-ttu-id="1e13d-129">Nell'esempio seguente un'immagine Tagged Image File Format (TIFF) viene codificata [**usando IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="1e13d-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="1e13d-130">L'output TIFF viene personalizzato usando [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) e il frame bitmap viene inizializzato usando le opzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="1e13d-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="1e13d-131">Dopo aver creato l'immagine usando [**WritePixels,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)viene eseguito il commit del frame tramite [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) e l'immagine viene salvata usando [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span><span class="sxs-lookup"><span data-stu-id="1e13d-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


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
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride***/;
    UINT cbBufferSize = uiHeight * cbStride;

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



## <a name="encoder-options-usage"></a><span data-ttu-id="1e13d-132">Utilizzo delle opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1e13d-132">Encoder Options Usage</span></span>

<span data-ttu-id="1e13d-133">Codificatori diversi per formati diversi devono esporre opzioni diverse per la modalità di codifica di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1e13d-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="1e13d-134">Windows Imaging Component (WIC) fornisce un meccanismo coerente per indicare se le opzioni di codifica sono necessarie e allo stesso tempo consentire alle applicazioni di lavorare con più codificatori senza richiedere la conoscenza di un formato specifico.</span><span class="sxs-lookup"><span data-stu-id="1e13d-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="1e13d-135">Questa operazione viene eseguita fornendo un [parametro IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) nel [**metodo CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) e nel [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)</span><span class="sxs-lookup"><span data-stu-id="1e13d-135">This is accomplished by providing an [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="1e13d-136">La factory dei componenti fornisce un punto di creazione semplice per la creazione di un contenitore delle proprietà delle opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="1e13d-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="1e13d-137">I codec possono usare questo servizio se devono fornire un set semplice, intuitivo e non in conflitto di opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="1e13d-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="1e13d-138">Il contenitore delle proprietà di creazione dell'immagine deve essere inizializzato durante la creazione con tutte le opzioni del codificatore rilevanti per tale codec.</span><span class="sxs-lookup"><span data-stu-id="1e13d-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="1e13d-139">Per le opzioni del codificatore dal set canonico, l'intervallo di valori verrà applicato in scrittura.</span><span class="sxs-lookup"><span data-stu-id="1e13d-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="1e13d-140">Per esigenze più avanzate, i codec devono scrivere la propria implementazione del contenitore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e13d-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="1e13d-141">A un'applicazione viene assegnato il contenitore delle opzioni del codificatore durante la creazione del frame e è necessario configurare tutti i valori prima di inizializzare il frame del codificatore.</span><span class="sxs-lookup"><span data-stu-id="1e13d-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="1e13d-142">Per un'applicazione basata sull'interfaccia utente, può offrire un'interfaccia utente fissa per le opzioni del codificatore canonico e una visualizzazione avanzata per le opzioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="1e13d-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="1e13d-143">Le modifiche possono essere apportate una alla volta tramite il metodo Write e qualsiasi errore verrà segnalato tramite IErrorLog.</span><span class="sxs-lookup"><span data-stu-id="1e13d-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="1e13d-144">L'applicazione dell'interfaccia utente deve sempre ri-leggere e visualizzare tutte le opzioni dopo aver apportato una modifica nel caso in cui la modifica abbia causato un effetto a catena.</span><span class="sxs-lookup"><span data-stu-id="1e13d-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="1e13d-145">Un'applicazione deve essere preparata per gestire l'inizializzazione dei frame non riuscita per i codec che forniscono solo segnalazioni di errori minime tramite il contenitore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e13d-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="1e13d-146">Opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1e13d-146">Encoder Options</span></span>

<span data-ttu-id="1e13d-147">Un'applicazione può prevedere di riscontrare il set di opzioni del codificatore seguente.</span><span class="sxs-lookup"><span data-stu-id="1e13d-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="1e13d-148">Le opzioni del codificatore riflettono le funzionalità di un codificatore e il formato del contenitore sottostante e pertanto non sono per loro natura realmente indipendenti dal codec.</span><span class="sxs-lookup"><span data-stu-id="1e13d-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="1e13d-149">Quando possibile, le nuove opzioni devono essere normalizzate in modo che possano essere applicate ai nuovi codec che emergono.</span><span class="sxs-lookup"><span data-stu-id="1e13d-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="1e13d-150">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="1e13d-150">Property Name</span></span>      | <span data-ttu-id="1e13d-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1e13d-151">VARTYPE</span></span>  | <span data-ttu-id="1e13d-152">Valore</span><span class="sxs-lookup"><span data-stu-id="1e13d-152">Value</span></span>                                                                     | <span data-ttu-id="1e13d-153">Codec applicabili</span><span class="sxs-lookup"><span data-stu-id="1e13d-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="1e13d-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="1e13d-154">ImageQuality</span></span>       | <span data-ttu-id="1e13d-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="1e13d-155">VT\_R4</span></span>   | <span data-ttu-id="1e13d-156">0-1.0</span><span class="sxs-lookup"><span data-stu-id="1e13d-156">0-1.0</span></span>                                                                     | <span data-ttu-id="1e13d-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="1e13d-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="1e13d-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="1e13d-158">CompressionQuality</span></span> | <span data-ttu-id="1e13d-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="1e13d-159">VT\_R4</span></span>   | <span data-ttu-id="1e13d-160">0-1.0</span><span class="sxs-lookup"><span data-stu-id="1e13d-160">0-1.0</span></span>                                                                     | <span data-ttu-id="1e13d-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="1e13d-161">TIFF</span></span>              |
| <span data-ttu-id="1e13d-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="1e13d-162">Lossless</span></span>           | <span data-ttu-id="1e13d-163">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="1e13d-163">VT\_BOOL</span></span> | <span data-ttu-id="1e13d-164">**TRUE,** **FALSE**</span><span class="sxs-lookup"><span data-stu-id="1e13d-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="1e13d-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="1e13d-165">HDPhoto</span></span>           |
| <span data-ttu-id="1e13d-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="1e13d-166">BitmapTransform</span></span>    | <span data-ttu-id="1e13d-167">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="1e13d-167">VT\_UI1</span></span>  | [<span data-ttu-id="1e13d-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="1e13d-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="1e13d-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="1e13d-169">JPEG</span></span>              |



 

<span data-ttu-id="1e13d-170">ImageQualty di 0,0 indica la fedeltà più bassa possibile e 1.0 indica la massima fedeltà, che può anche implicare perdita a seconda del codec.</span><span class="sxs-lookup"><span data-stu-id="1e13d-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="1e13d-171">CompressionQuality di 0,0 indica lo schema di compressione meno efficiente disponibile, che in genere comporta una codifica veloce ma un output più grande.</span><span class="sxs-lookup"><span data-stu-id="1e13d-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="1e13d-172">Il valore 1.0 indica lo schema più efficiente disponibile, in genere richiede più tempo per la codifica, ma produce un output più piccolo.</span><span class="sxs-lookup"><span data-stu-id="1e13d-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="1e13d-173">A seconda delle funzionalità del codec, questo intervallo può essere mappato a un set discreto di metodi di compressione disponibili.</span><span class="sxs-lookup"><span data-stu-id="1e13d-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="1e13d-174">Senza perdita significa che il codec codifica l'immagine come senza perdita di dati senza perdita di dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1e13d-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="1e13d-175">Se Lossless è abilitato, ImageQuality viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1e13d-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="1e13d-176">Oltre alle opzioni del codificatore generico precedenti, i codec forniti con WIC supportano le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e13d-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="1e13d-177">Se un codec deve supportare un'opzione coerente con l'utilizzo di questi codec forniti, è consigliato farlo.</span><span class="sxs-lookup"><span data-stu-id="1e13d-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="1e13d-178">Nome della proprietà</span><span class="sxs-lookup"><span data-stu-id="1e13d-178">Property Name</span></span>           | <span data-ttu-id="1e13d-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1e13d-179">VARTYPE</span></span>           | <span data-ttu-id="1e13d-180">Valore</span><span class="sxs-lookup"><span data-stu-id="1e13d-180">Value</span></span>                                                                             | <span data-ttu-id="1e13d-181">Codec applicabili</span><span class="sxs-lookup"><span data-stu-id="1e13d-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="1e13d-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="1e13d-182">InterlaceOption</span></span>         | <span data-ttu-id="1e13d-183">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="1e13d-183">VT\_BOOL</span></span>          | <span data-ttu-id="1e13d-184">Attivato/Disattivato</span><span class="sxs-lookup"><span data-stu-id="1e13d-184">On/Off</span></span>                                                                            | <span data-ttu-id="1e13d-185">PNG</span><span class="sxs-lookup"><span data-stu-id="1e13d-185">PNG</span></span>               |
| <span data-ttu-id="1e13d-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="1e13d-186">FilterOption</span></span>            | <span data-ttu-id="1e13d-187">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="1e13d-187">VT\_UI1</span></span>           | [<span data-ttu-id="1e13d-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="1e13d-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="1e13d-189">PNG</span><span class="sxs-lookup"><span data-stu-id="1e13d-189">PNG</span></span>               |
| <span data-ttu-id="1e13d-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="1e13d-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="1e13d-191">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="1e13d-191">VT\_UI1</span></span>           | [<span data-ttu-id="1e13d-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="1e13d-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="1e13d-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="1e13d-193">TIFF</span></span>              |
| <span data-ttu-id="1e13d-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="1e13d-194">Luminance</span></span>               | <span data-ttu-id="1e13d-195">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="1e13d-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="1e13d-196">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="1e13d-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="1e13d-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="1e13d-197">JPEG</span></span>              |
| <span data-ttu-id="1e13d-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="1e13d-198">Chrominance</span></span>             | <span data-ttu-id="1e13d-199">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="1e13d-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="1e13d-200">64 voci (DCT)</span><span class="sxs-lookup"><span data-stu-id="1e13d-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="1e13d-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="1e13d-201">JPEG</span></span>              |
| <span data-ttu-id="1e13d-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="1e13d-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="1e13d-203">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="1e13d-203">VT\_UI1</span></span>           | [<span data-ttu-id="1e13d-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="1e13d-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="1e13d-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="1e13d-205">JPEG</span></span>              |
| <span data-ttu-id="1e13d-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="1e13d-206">SuppressApp0</span></span>            | <span data-ttu-id="1e13d-207">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="1e13d-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="1e13d-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="1e13d-208">JPEG</span></span>              |
| <span data-ttu-id="1e13d-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="1e13d-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="1e13d-210">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="1e13d-210">VT\_BOOL</span></span>          | <span data-ttu-id="1e13d-211">Attivato/Disattivato</span><span class="sxs-lookup"><span data-stu-id="1e13d-211">On/Off</span></span>                                                                            | <span data-ttu-id="1e13d-212">BMP</span><span class="sxs-lookup"><span data-stu-id="1e13d-212">BMP</span></span>               |



 

<span data-ttu-id="1e13d-213">Usare **VT \_ EMPTY** per indicare **\* che non è impostato \*** come predefinito.</span><span class="sxs-lookup"><span data-stu-id="1e13d-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="1e13d-214">Se le proprietà aggiuntive vengono impostate ma non supportate, il codificatore deve ignorarle. Ciò consente alle applicazioni di codificare meno logica se desiderano una funzionalità che potrebbe essere presente o meno.</span><span class="sxs-lookup"><span data-stu-id="1e13d-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="1e13d-215">Esempi di opzioni del codificatore</span><span class="sxs-lookup"><span data-stu-id="1e13d-215">Encoder Options Examples</span></span>

<span data-ttu-id="1e13d-216">Nell'esempio [di codifica TIFF precedente](#tiff-encoding-example) viene impostata un'opzione del codificatore specifica.</span><span class="sxs-lookup"><span data-stu-id="1e13d-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="1e13d-217">Il *membro pstrName* della struttura PROPBAG2 viene impostato sul nome della proprietà appropriato e VARIANT viene impostato sul varTYPE corrispondente e sul valore desiderato, in questo caso un membro dell'enumerazione [**WICTiffCompressionOption.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)</span><span class="sxs-lookup"><span data-stu-id="1e13d-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


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



<span data-ttu-id="1e13d-218">Per usare le opzioni predefinite del codificatore, è sufficiente inizializzare il frame bitmap con il contenitore delle proprietà restituito al momento della creazione del frame.</span><span class="sxs-lookup"><span data-stu-id="1e13d-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


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



<span data-ttu-id="1e13d-219">È anche possibile eliminare il contenitore delle proprietà quando non viene considerata alcuna opzione del codificatore.</span><span class="sxs-lookup"><span data-stu-id="1e13d-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1e13d-220">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e13d-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1e13d-221">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1e13d-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1e13d-222">Windows Imaging Component panoramica</span><span class="sxs-lookup"><span data-stu-id="1e13d-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="1e13d-223">Cenni preliminari sulla decodifica</span><span class="sxs-lookup"><span data-stu-id="1e13d-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="1e13d-224">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="1e13d-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1e13d-225">Come scrivere un codec WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1e13d-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
