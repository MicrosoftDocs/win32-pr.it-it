---
description: Implementazione di IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementazione di IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050087"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="2186b-103">Implementazione di IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="2186b-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="2186b-104">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="2186b-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="2186b-105">Quando un'applicazione richiede un decodificatore, il primo punto di interazione con il codec è tramite l'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="2186b-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="2186b-106">Si tratta dell'interfaccia a livello di contenitore che fornisce l'accesso alle proprietà di primo livello del contenitore e, soprattutto, dei frame in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="2186b-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="2186b-107">Si tratta dell'interfaccia principale della classe decodificatore a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="2186b-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="2186b-108">Alcuni formati di immagine hanno anteprime globali, contesti di colore o metadati, mentre molti formati di immagine li forniscono solo per singolo frame.</span><span class="sxs-lookup"><span data-stu-id="2186b-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="2186b-109">I metodi per l'accesso a questi elementi sono facoltativi in [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), ma sono necessari in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="2186b-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="2186b-110">Analogamente, alcuni codec non utilizzano formati pixel indicizzati e pertanto non è necessario implementare i metodi [CopyPalette](-wic-imp-iwicbitmapframedecode.md) su una delle due interfacce.</span><span class="sxs-lookup"><span data-stu-id="2186b-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="2186b-111">Per altre informazioni sui metodi facoltativi **IWICBitmapDecoder** , vedere [implementazione di IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), dove sono implementate più di frequente.</span><span class="sxs-lookup"><span data-stu-id="2186b-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="2186b-112">QueryCapability</span><span class="sxs-lookup"><span data-stu-id="2186b-112">QueryCapability</span></span>

<span data-ttu-id="2186b-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) è il metodo utilizzato per l'arbitraggio di codec.</span><span class="sxs-lookup"><span data-stu-id="2186b-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="2186b-114">(Vedere [individuazione e arbitraggio](-wic-howwicworks.md) nell'argomento [come funziona il componente Windows Imaging](-wic-howwicworks.md) ).</span><span class="sxs-lookup"><span data-stu-id="2186b-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="2186b-115">Se due codec sono in grado di decodificare lo stesso formato di immagine o se si verifica una collisione del modello in cui due codec usano lo stesso modello di identificazione, questo metodo consente di selezionare il codec che può gestire meglio qualsiasi immagine specifica.</span><span class="sxs-lookup"><span data-stu-id="2186b-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="2186b-116">Quando si richiama questo metodo, Windows Imaging Component (WIC) passa il flusso effettivo che contiene l'immagine.</span><span class="sxs-lookup"><span data-stu-id="2186b-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="2186b-117">È necessario verificare se è possibile decodificare ogni fotogramma all'interno dell'immagine ed enumerare i blocchi di metadati per dichiarare accuratamente le funzionalità di questo decodificatore rispetto al flusso di file specifico passato.</span><span class="sxs-lookup"><span data-stu-id="2186b-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="2186b-118">Questa operazione è importante per tutti i decodificatori, ma è particolarmente importante per i formati di immagine basati sui contenitori Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="2186b-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="2186b-119">Il processo di individuazione funziona mediante la corrispondenza dei modelli associati ai decodificatori nel registro di sistema con i modelli nel file di immagine effettivo.</span><span class="sxs-lookup"><span data-stu-id="2186b-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="2186b-120">Dichiarare il modello di identificazione nel registro di sistema garantisce che il decodificatore venga sempre rilevato per le immagini nel formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="2186b-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="2186b-121">Tuttavia, il decodificatore potrebbe essere ancora rilevato per le immagini in altri formati.</span><span class="sxs-lookup"><span data-stu-id="2186b-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="2186b-122">Ad esempio, tutti i contenitori TIFF includono il modello TIFF, che è un modello di identificazione valido per il formato di immagine TIFF.</span><span class="sxs-lookup"><span data-stu-id="2186b-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="2186b-123">Ciò significa che, durante l'individuazione, verranno trovati almeno due modelli di identificazione nei file di immagine per qualsiasi formato di immagine basato su un contenitore di tipo TIFF.</span><span class="sxs-lookup"><span data-stu-id="2186b-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="2186b-124">Uno sarà il modello TIFF e l'altro sarà il modello di formato immagine effettivo.</span><span class="sxs-lookup"><span data-stu-id="2186b-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="2186b-125">Sebbene sia meno probabile, è possibile che si verifichino conflitti di modelli tra altri formati di immagine non correlati.</span><span class="sxs-lookup"><span data-stu-id="2186b-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="2186b-126">Questo è il motivo per cui l'individuazione e l'arbitraggio sono un processo in due fasi.</span><span class="sxs-lookup"><span data-stu-id="2186b-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="2186b-127">Verificare sempre che il flusso di immagini passato a [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) sia in realtà un'istanza valida del proprio formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="2186b-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="2186b-128">Inoltre, se il codec decodifica un formato di immagine per cui non si è proprietari della specifica, l'implementazione di **QueryCapability** deve verificare la presenza di qualsiasi funzionalità che può essere valida con la specifica del formato di immagine che il codec non implementa.</span><span class="sxs-lookup"><span data-stu-id="2186b-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="2186b-129">In questo modo gli utenti non possono riscontrare errori di decodifica non necessari o ottenere risultati imprevisti con il codec.</span><span class="sxs-lookup"><span data-stu-id="2186b-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="2186b-130">Prima di eseguire qualsiasi operazione sull'immagine, è necessario salvare la posizione corrente del flusso, in modo che sia possibile ripristinarla nella posizione originale prima di restituire il metodo.</span><span class="sxs-lookup"><span data-stu-id="2186b-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="2186b-131">L'enumerazione [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) che specifica le funzionalità viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="2186b-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="2186b-132">È necessario dichiarare **WICBitmapDecoderCapabilitySameEncoder** solo se il codificatore è quello che ha codificato l'immagine.</span><span class="sxs-lookup"><span data-stu-id="2186b-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="2186b-133">Dopo aver verificato se è possibile decodificare ogni frame nel contenitore, dichiarare **WICBitmapDecoderCapabilityCanDecodeSomeImages** se è possibile decodificare alcuni ma non tutti i frame, **WICBitmapDecoderCapabilityCanDecodeAllImages** se è possibile decodificare tutti i frame o nessuno dei due se non è possibile decodificarli.</span><span class="sxs-lookup"><span data-stu-id="2186b-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="2186b-134">Queste due enumerazioni si escludono a vicenda. Se si restituisce **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** verrà ignorato. Dichiarare **WICBitmapDecoderCapabilityCanEnumerateMetadata** dopo avere verificato che sia possibile enumerare i blocchi di metadati nel contenitore di immagini.</span><span class="sxs-lookup"><span data-stu-id="2186b-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="2186b-135">Non è necessario cercare un'anteprima in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="2186b-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="2186b-136">Se è presente un'anteprima globale ed è possibile decodificarla, è possibile dichiarare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span><span class="sxs-lookup"><span data-stu-id="2186b-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="2186b-137">Se non è presente un'anteprima globale, provare a decodificare l'anteprima per il frame 0.</span><span class="sxs-lookup"><span data-stu-id="2186b-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="2186b-138">Se non è presente alcuna anteprima in nessuna di queste posizioni, non dichiarare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2186b-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="2186b-139">Dopo aver determinato le funzionalità del decodificatore rispetto al flusso di immagini passato a questo metodo, eseguire un'operazione OR con il [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) verificato che questo decodificatore possa eseguire su questa immagine e restituire il risultato.</span><span class="sxs-lookup"><span data-stu-id="2186b-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="2186b-140">Ricordarsi di ripristinare il flusso nella posizione originale prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="2186b-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="2186b-141">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="2186b-141">Initialize</span></span>

<span data-ttu-id="2186b-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) viene richiamato da un'applicazione dopo che è stato selezionato un decodificatore per decodificare un'immagine specifica.</span><span class="sxs-lookup"><span data-stu-id="2186b-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="2186b-143">Il flusso di immagini viene passato al decodificatore e un chiamante può specificare facoltativamente l'opzione della cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) per gestire i metadati nel file.</span><span class="sxs-lookup"><span data-stu-id="2186b-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="2186b-144">Alcune applicazioni usano metadati più di altre.</span><span class="sxs-lookup"><span data-stu-id="2186b-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="2186b-145">Per la maggior parte delle applicazioni non è necessario accedere a tutti i metadati in un file di immagine e verranno richiesti metadati specifici in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2186b-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="2186b-146">In altre applicazioni, invece, i metadati vengono memorizzati nella cache prima che il flusso di file venga aperto ed eseguo l'I/O del disco ogni volta che è necessario accedere ai metadati.</span><span class="sxs-lookup"><span data-stu-id="2186b-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="2186b-147">Se il chiamante non specifica un'opzione della cache dei metadati, il comportamento predefinito di memorizzazione nella cache deve essere memorizzato nella cache su richiesta.</span><span class="sxs-lookup"><span data-stu-id="2186b-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="2186b-148">Ciò significa che non è necessario caricare i metadati in memoria fino a quando l'applicazione non esegue una richiesta specifica per i metadati.</span><span class="sxs-lookup"><span data-stu-id="2186b-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="2186b-149">Se l'applicazione specifica **WICDecodeMetadataCacheOnLoad**, i metadati devono essere caricati in memoria immediatamente e memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="2186b-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="2186b-150">Quando i metadati vengono memorizzati nella cache durante il caricamento, il flusso di file può essere rilasciato dopo che i metadati sono stati memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="2186b-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="2186b-151">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="2186b-151">GetContainerFormat</span></span>

<span data-ttu-id="2186b-152">Per implementare [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), restituire solo il GUID del formato di immagine dell'immagine per cui viene creata un'istanza del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2186b-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="2186b-153">Questo metodo viene inoltre implementato in [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="2186b-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="2186b-154">GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="2186b-154">GetDecoderInfo</span></span>

<span data-ttu-id="2186b-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) restituisce un oggetto [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="2186b-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="2186b-156">Per ottenere l'oggetto **IWICBitmapDecoderInfo** , è sufficiente passare il GUID del decodificatore al metodo [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), quindi richiedere l'interfaccia **IWICBitmapDecoderInfo** su di esso, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2186b-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="2186b-157">GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="2186b-157">GetFrameCount</span></span>

<span data-ttu-id="2186b-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) restituisce semplicemente il numero di frame nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="2186b-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="2186b-159">Alcuni formati di contenitore supportano più frame e altri supportano solo un frame per ogni contenitore.</span><span class="sxs-lookup"><span data-stu-id="2186b-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="2186b-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="2186b-160">GetFrame</span></span>

<span data-ttu-id="2186b-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) è un metodo importante sull'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) perché il frame contiene i bit dell'immagine effettivi e l'oggetto del decodificatore di frame restituito da questo metodo è l'oggetto che esegue la decodifica effettiva dell'immagine richiesta.</span><span class="sxs-lookup"><span data-stu-id="2186b-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="2186b-162">Ovvero l'altro oggetto che è necessario implementare durante la scrittura di un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2186b-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="2186b-163">Per ulteriori informazioni sui decodificatori di frame, vedere [implementazione di IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span><span class="sxs-lookup"><span data-stu-id="2186b-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="2186b-164">Getpreview</span><span class="sxs-lookup"><span data-stu-id="2186b-164">GetPreview</span></span>

<span data-ttu-id="2186b-165">[**Getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) restituisce un'anteprima dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2186b-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="2186b-166">Per una descrizione dettagliata delle anteprime, vedere Implementazione del metodo [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) sull'implementazione dell'interfaccia [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .</span><span class="sxs-lookup"><span data-stu-id="2186b-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="2186b-167">Se il formato dell'immagine contiene un'anteprima JPEG incorporata, è consigliabile, anziché scrivere un decodificatore JPEG per decodificarlo, delegare al decodificatore JPEG fornito con la piattaforma WIC per la decodifica di anteprime e anteprime.</span><span class="sxs-lookup"><span data-stu-id="2186b-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="2186b-168">A tale scopo, cercare all'inizio dei dati dell'immagine di anteprima nel flusso e richiamare il metodo [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="2186b-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="2186b-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2186b-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2186b-170">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2186b-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2186b-171">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="2186b-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="2186b-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="2186b-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="2186b-173">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2186b-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2186b-174">Interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="2186b-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="2186b-175">Implementazione di IWICBitmapCodecProgressNotification (decodificatore)</span><span class="sxs-lookup"><span data-stu-id="2186b-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="2186b-176">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="2186b-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="2186b-177">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="2186b-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



