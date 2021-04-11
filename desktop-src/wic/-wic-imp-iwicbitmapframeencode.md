---
description: Implementazione di IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementazione di IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232888"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="e1747-103">Implementazione di IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="e1747-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="e1747-104">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="e1747-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="e1747-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) è la controparte del codificatore dell'interfaccia [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="e1747-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="e1747-106">È possibile implementare questa interfaccia nella classe di codifica a livello di frame, ovvero la classe che esegue la codifica effettiva dei bit dell'immagine per ogni frame.</span><span class="sxs-lookup"><span data-stu-id="e1747-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="e1747-107">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="e1747-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="e1747-108">Ridimensionamento e risoluzione</span><span class="sxs-lookup"><span data-stu-id="e1747-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="e1747-109">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="e1747-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="e1747-110">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="e1747-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="e1747-111">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="e1747-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="e1747-112">Anteprima</span><span class="sxs-lookup"><span data-stu-id="e1747-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="e1747-113">WritePixels</span><span class="sxs-lookup"><span data-stu-id="e1747-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="e1747-114">WriteSource</span><span class="sxs-lookup"><span data-stu-id="e1747-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="e1747-115">Eseguire il commit</span><span class="sxs-lookup"><span data-stu-id="e1747-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="e1747-116">SetPalette</span><span class="sxs-lookup"><span data-stu-id="e1747-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="e1747-117">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="e1747-117">Initialize</span></span>

<span data-ttu-id="e1747-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) è il primo metodo richiamato su un oggetto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) dopo che ne è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="e1747-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="e1747-119">Questo metodo ha un parametro, che può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e1747-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="e1747-120">Questo parametro rappresenta le opzioni del codificatore ed è la stessa istanza di [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) creata nel metodo [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) sul decodificatore a livello di contenitore e passata di nuovo al chiamante nel parametro pIEncoderOptions di tale metodo.</span><span class="sxs-lookup"><span data-stu-id="e1747-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="e1747-121">In quel momento è stato popolato lo struct IPropertyBag2 con proprietà che rappresentano le opzioni di codifica supportate dal codificatore a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="e1747-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="e1747-122">Il chiamante ha ora fornito i valori per tali proprietà per indicare determinati parametri dell'opzione di codifica e passa di nuovo lo stesso oggetto per inizializzare l'oggetto **IWICBitmapFrameEncode** .</span><span class="sxs-lookup"><span data-stu-id="e1747-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="e1747-123">Quando si codificano i bit dell'immagine, è necessario applicare le opzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="e1747-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="e1747-124">Ridimensionamento e risoluzione</span><span class="sxs-lookup"><span data-stu-id="e1747-124">SetSize and SetResolution</span></span>

<span data-ttu-id="e1747-125">Le [**dimensioni**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) e la [**risoluzione**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) dei problemi sono di chiara interpretazione.</span><span class="sxs-lookup"><span data-stu-id="e1747-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="e1747-126">Il chiamante utilizza questi metodi per specificare le dimensioni e la risoluzione per l'immagine codificata.</span><span class="sxs-lookup"><span data-stu-id="e1747-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="e1747-127">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="e1747-127">SetPixelFormat</span></span>

<span data-ttu-id="e1747-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) viene usato per richiedere un formato pixel in cui codificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="e1747-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="e1747-129">Se il formato pixel richiesto non è supportato, è necessario restituire il GUID del formato pixel più vicino supportato in *pPixelFormat*, che è un parametro in/out.</span><span class="sxs-lookup"><span data-stu-id="e1747-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="e1747-130">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="e1747-130">SetColorContexts</span></span>

<span data-ttu-id="e1747-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) viene usato per specificare uno o più contesti di colore validi (noti anche come profili colori) per questa immagine.</span><span class="sxs-lookup"><span data-stu-id="e1747-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="e1747-132">È importante specificare i contesti di colore, in modo che un'applicazione che decodifica l'immagine in un secondo momento possa eseguire la conversione dal profilo dei colori di origine al profilo di destinazione del dispositivo usato per visualizzare o stampare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="e1747-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="e1747-133">Senza un profilo colori, non è possibile ottenere colori coerenti tra dispositivi diversi.</span><span class="sxs-lookup"><span data-stu-id="e1747-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="e1747-134">Questo può essere frustrante per gli utenti finali quando le foto hanno un aspetto diverso su monitoraggi diversi e non possono ottenere le stampe corrispondenti a quanto visualizzato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="e1747-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="e1747-135">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="e1747-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="e1747-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) restituisce un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) che un'applicazione può usare per inserire o modificare proprietà di metadati specifiche in un blocco di metadati nel frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e1747-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="e1747-137">È possibile creare un'istanza di un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) da [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="e1747-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="e1747-138">È possibile crearlo dalla [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), nello stesso modo in cui [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) è stato creato da un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nel metodo [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) sull'interfaccia [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="e1747-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="e1747-139">È anche possibile crearlo da un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)esistente, ad esempio quello ottenuto usando il metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="e1747-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="e1747-140">Il parametro *pguidVendor* consente di specificare un particolare fornitore per il writer di query da utilizzare quando si crea un'istanza di un writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="e1747-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="e1747-141">Se, ad esempio, si forniscono i propri writer di metadati, è consigliabile specificare il proprio GUID fornitore.</span><span class="sxs-lookup"><span data-stu-id="e1747-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="e1747-142">È possibile passare **null** a questo parametro se non si ha una preferenza.</span><span class="sxs-lookup"><span data-stu-id="e1747-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="e1747-143">Anteprima</span><span class="sxs-lookup"><span data-stu-id="e1747-143">SetThumbnail</span></span>

<span data-ttu-id="e1747-144">L' [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) viene utilizzata per fornire un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="e1747-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="e1747-145">Tutte le immagini devono fornire un'anteprima a livello globale, in ogni frame o in entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="e1747-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="e1747-146">I metodi **GetThumbnail** e **sethumbnail** sono facoltativi a livello di contenitore, ma se un codec restituisce WINCODEC \_ Err \_ CODECNOTHUMBNAIL dal metodo [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , Windows Imaging Component (WIC) richiamerà il metodo [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) per il frame 0.</span><span class="sxs-lookup"><span data-stu-id="e1747-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="e1747-147">Se non viene trovata alcuna anteprima in nessuna delle due località, WIC deve decodificare l'immagine completa e ridimensionarla in base alle dimensioni di anteprima, il che potrebbe comportare un notevole calo delle prestazioni per le immagini più grandi.</span><span class="sxs-lookup"><span data-stu-id="e1747-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="e1747-148">L'anteprima deve avere una dimensione e una risoluzione che consentono di decodificare e visualizzare rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e1747-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="e1747-149">Per questo motivo, le anteprime sono più comunemente immagini JPEG.</span><span class="sxs-lookup"><span data-stu-id="e1747-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="e1747-150">Si noti che, se si usa il formato JPEG per le anteprime, non è necessario scrivere un codificatore JPEG per codificarli o un decodificatore JPEG per decodificarli.</span><span class="sxs-lookup"><span data-stu-id="e1747-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="e1747-151">È sempre necessario delegare il codec JPEG fornito con la piattaforma WIC per la codifica e la decodifica delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="e1747-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="e1747-152">WritePixels</span><span class="sxs-lookup"><span data-stu-id="e1747-152">WritePixels</span></span>

<span data-ttu-id="e1747-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) è il metodo utilizzato per passare le righe di analisi da una bitmap in memoria per la codifica.</span><span class="sxs-lookup"><span data-stu-id="e1747-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="e1747-154">Il metodo verrà chiamato ripetutamente fino a quando tutte le righe di analisi non sono state passate.</span><span class="sxs-lookup"><span data-stu-id="e1747-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="e1747-155">Il parametro *LineCount* indica il numero di righe di analisi da scrivere in questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="e1747-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="e1747-156">Il parametro *cbStride* indica il numero di byte per riga di analisi.</span><span class="sxs-lookup"><span data-stu-id="e1747-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="e1747-157">*cbBufferSize* indica le dimensioni del buffer passato nel parametro pbPixels, che contiene i bit di immagine effettivi da codificare.</span><span class="sxs-lookup"><span data-stu-id="e1747-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="e1747-158">Se l'altezza combinata delle righe di analisi dalle chiamate cumulative è maggiore dell'altezza specificata nel metodo [**sesize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , restituire WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="e1747-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="e1747-159">Quando [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) è **WICBitmapEncoderCacheInMemory**, le righe di analisi devono essere memorizzate nella cache fino a quando non sono state passate tutte le righe di analisi.</span><span class="sxs-lookup"><span data-stu-id="e1747-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="e1747-160">Se l'opzione cache del codificatore è **WICBitmapEncoderCacheTempFile**, le righe di analisi devono essere memorizzate nella cache in un file temporaneo, creato durante l'inizializzazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e1747-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="e1747-161">In entrambi i casi, l'immagine non deve essere codificata finché il chiamante chiama [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span><span class="sxs-lookup"><span data-stu-id="e1747-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="e1747-162">Nel caso in cui l'opzione cache sia **WICBitmapEncoderNoCache**, il codificatore deve codificare le righe di analisi man mano che vengono ricevute, se possibile.</span><span class="sxs-lookup"><span data-stu-id="e1747-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="e1747-163">(In alcuni formati, questo non è possibile e le righe di analisi devono essere memorizzate nella cache fino a quando non viene chiamato il commit).</span><span class="sxs-lookup"><span data-stu-id="e1747-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="e1747-164">La maggior parte dei codec non elaborati non implementerà [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), perché non supportano la modifica dei bit dell'immagine nel file non elaborato.</span><span class="sxs-lookup"><span data-stu-id="e1747-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="e1747-165">I codec non elaborati devono comunque implementare **WritePixels**, tuttavia, poiché quando vengono aggiunti metadati, può aumentare la dimensione del file, richiedendo la riscrittura del file sul disco.</span><span class="sxs-lookup"><span data-stu-id="e1747-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="e1747-166">In tal caso, è necessario essere in grado di copiare i bit dell'immagine esistente, che è il metodo **WritePixels** .</span><span class="sxs-lookup"><span data-stu-id="e1747-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="e1747-167">WriteSource</span><span class="sxs-lookup"><span data-stu-id="e1747-167">WriteSource</span></span>

<span data-ttu-id="e1747-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) viene usato per codificare un oggetto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="e1747-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="e1747-169">Il primo parametro è un puntatore a un oggetto **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="e1747-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="e1747-170">Il secondo parametro è un WICRect che specifica l'area di interesse da codificare.</span><span class="sxs-lookup"><span data-stu-id="e1747-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="e1747-171">Questo metodo può essere chiamato più volte in successione, a condizione che la larghezza di ogni rettangolo corrisponda alla larghezza dell'immagine finale da codificare.</span><span class="sxs-lookup"><span data-stu-id="e1747-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="e1747-172">Se la larghezza del rettangolo passato nel parametro PRC è diversa dalla larghezza specificata nel metodo sesize, restituire WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS.</span><span class="sxs-lookup"><span data-stu-id="e1747-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="e1747-173">Se l'altezza combinata delle righe di analisi dalle chiamate cumulative è maggiore dell'altezza specificata nel metodo sesize, restituire WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="e1747-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="e1747-174">Le opzioni della cache funzionano allo stesso modo con questo metodo, come per il metodo [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e1747-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="e1747-175">Commit</span><span class="sxs-lookup"><span data-stu-id="e1747-175">Commit</span></span>

<span data-ttu-id="e1747-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) è il metodo che serializza i bit dell'immagine codificata nel flusso di file e scorre tutti i writer di metadati per il frame richiedendo loro di serializzare i metadati nel flusso.</span><span class="sxs-lookup"><span data-stu-id="e1747-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="e1747-177">Nel caso in cui l'opzione cache del codificatore sia WICBitmapEncoderCacheInMemory o WICBitmapEncoderCacheTempFile, questo metodo è anche responsabile della codifica dell'immagine e quando l'opzione cache è WICBitmapEncoderCacheTempFile, il metodo **commit** deve eliminare anche il file temporaneo usato per memorizzare nella cache i dati dell'immagine prima della codifica.</span><span class="sxs-lookup"><span data-stu-id="e1747-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="e1747-178">Questo metodo viene sempre richiamato dopo che tutte le righe o i rettangoli di analisi che costituiscono l'immagine sono stati passati utilizzando il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) o [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="e1747-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="e1747-179">Le dimensioni del rettangolo finale composto tramite le chiamate accumulate a WritePixels o WriteSource devono essere uguali a quelle specificate nel metodo sesize.</span><span class="sxs-lookup"><span data-stu-id="e1747-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="e1747-180">Se la dimensione non corrisponde alla dimensione prevista, questo metodo deve restituire WINCODECERROR \_ UNEXPECTEDSIZE.</span><span class="sxs-lookup"><span data-stu-id="e1747-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="e1747-181">Per scorrere i writer dei metadati e indicare a ogni writer di metadati di serializzare i metadati, passare al flusso, richiamare GetWriterByIndex per scorrere i writer per ogni blocco e richiamare IWICPersistStream. Save su ogni writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="e1747-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="e1747-182">SetPalette</span><span class="sxs-lookup"><span data-stu-id="e1747-182">SetPalette</span></span>

<span data-ttu-id="e1747-183">Solo i codec con formati indicizzati devono implementare il metodo [**sepalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="e1747-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="e1747-184">Se un'immagine usa un formato indicizzato, usare questo metodo per specificare la tavolozza dei colori usati nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e1747-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="e1747-185">Se il codec non ha un formato indicizzato, restituire WINCODEC \_ Err \_ PALETTEUNAVAILABLE da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e1747-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1747-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1747-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e1747-187">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e1747-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1747-188">Implementazione di IWICBitmapCodecProgressNotification (encoder)</span><span class="sxs-lookup"><span data-stu-id="e1747-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="e1747-189">Implementazione di IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="e1747-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="e1747-190">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e1747-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="e1747-191">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="e1747-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
