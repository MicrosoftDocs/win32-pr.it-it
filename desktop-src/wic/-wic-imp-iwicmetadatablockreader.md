---
description: Implementazione di IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementazione di IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882193"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="65235-103">Implementazione di IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="65235-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="65235-104">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="65235-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="65235-105">All'interno di un'immagine sono spesso presenti più blocchi di metadati, ognuno dei quali espone tipi diversi di informazioni in formati diversi.</span><span class="sxs-lookup"><span data-stu-id="65235-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="65235-106">Nel modello di Windows Imaging Component (WIC), i gestori di metadati sono componenti distinti che, come i decodificatori, sono individuabili in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="65235-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="65235-107">Ogni formato di metadati dispone di un gestore separato e ognuno di questi gestori di metadati può essere utilizzato con qualsiasi formato di immagine che supporti il formato dei metadati gestito.</span><span class="sxs-lookup"><span data-stu-id="65235-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="65235-108">Se pertanto il formato dell'immagine supporta EXIF, XMP, IPTC o un altro formato, è possibile sfruttare i gestori di metadati standard per questi formati forniti con WIC e non è necessario scrivere i propri.</span><span class="sxs-lookup"><span data-stu-id="65235-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="65235-109">Naturalmente, se si crea un nuovo formato di metadati, è necessario scrivere un gestore di metadati per tale formato, che verrà individuato e richiamato in fase di esecuzione, esattamente come quelli standard.</span><span class="sxs-lookup"><span data-stu-id="65235-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="65235-110">Se il formato dell'immagine è basato su un contenitore Tagged Image File Format (TIFF) o JPEG, non sarà necessario scrivere alcun gestore di metadati (a meno che non si sviluppi un formato di metadati nuovo o proprietario).</span><span class="sxs-lookup"><span data-stu-id="65235-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="65235-111">Nei contenitori TIFF e JPEG i blocchi di metadati si trovano all'interno di IFDs e ogni contenitore ha una struttura IFD diversa.</span><span class="sxs-lookup"><span data-stu-id="65235-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="65235-112">WIC fornisce gestori IFD per entrambi i formati di contenitore che esplorano la struttura IFD e delegano ai gestori di metadati standard per accedere ai metadati al suo interno.</span><span class="sxs-lookup"><span data-stu-id="65235-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="65235-113">Quindi, se il formato dell'immagine è basato su uno di questi contenitori, è possibile sfruttare automaticamente i gestori IFD di WIC.</span><span class="sxs-lookup"><span data-stu-id="65235-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="65235-114">Tuttavia, se si dispone di un formato di contenitore proprietario con una struttura di metadati di primo livello univoca, è necessario scrivere un gestore in grado di esplorare la struttura di livello superiore e delegare ai gestori di metadati appropriati, esattamente come avviene per i gestori IFD.</span><span class="sxs-lookup"><span data-stu-id="65235-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="65235-115">In modo analogo a WIC fornisce un livello di astrazione per le applicazioni che consente loro di utilizzare tutti i formati di immagine nello stesso modo tramite un set coerente di interfacce, WIC fornisce un livello di astrazione per gli autori di codec in relazione ai formati di metadati.</span><span class="sxs-lookup"><span data-stu-id="65235-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="65235-116">Come indicato in precedenza, non è necessario che gli autori di codec funzionino direttamente con i vari formati di metadati che possono essere presenti in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="65235-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="65235-117">Tuttavia, ogni autore di codec è responsabile di fornire un modo per enumerare i blocchi di metadati, in modo che sia possibile individuare e creare un'istanza di un gestore di metadati appropriato per ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="65235-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="65235-118">È necessario implementare questa interfaccia nella classe di decodifica a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="65235-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="65235-119">Potrebbe anche essere necessario implementarlo nella classe decodificatore a livello di contenitore se il formato dell'immagine espone i metadati globali all'esterno dei singoli frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="65235-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="65235-120">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="65235-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="65235-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="65235-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="65235-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="65235-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="65235-123">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="65235-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="65235-124">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="65235-124">GetContainerFormat</span></span>

<span data-ttu-id="65235-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) è uguale al metodo [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) sull'implementazione di [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="65235-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="65235-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="65235-126">GetCount</span></span>

<span data-ttu-id="65235-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) restituisce il numero di blocchi di metadati di primo livello associati al frame.</span><span class="sxs-lookup"><span data-stu-id="65235-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="65235-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="65235-128">GetEnumerator</span></span>

<span data-ttu-id="65235-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) restituisce un enumeratore che il chiamante può usare per enumerare i blocchi di metadati nel frame e leggerne i metadati.</span><span class="sxs-lookup"><span data-stu-id="65235-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="65235-130">Per implementare questo metodo, è necessario creare un lettore di metadati per ogni blocco di metadati e implementare un oggetto di enumerazione che enumera la raccolta di Reader dei metadati.</span><span class="sxs-lookup"><span data-stu-id="65235-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="65235-131">L'oggetto di enumerazione deve implementare [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) in modo che sia possibile eseguirne il cast in IEnumUnknown quando viene restituito nel parametro *ppIEnumMetadata* .</span><span class="sxs-lookup"><span data-stu-id="65235-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="65235-132">Quando si implementa l'oggetto di enumerazione, è possibile creare tutti i lettori di metadati quando si crea per la prima volta l'oggetto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) o quando si crea l'oggetto di enumerazione per la prima volta oppure è possibile crearli in modo differito all'interno dell'implementazione del metodo [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) .</span><span class="sxs-lookup"><span data-stu-id="65235-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="65235-133">In molti casi, è più efficiente crearli in modalità differita, ma nell'esempio seguente i reader di blocco vengono tutti creati nel costruttore per risparmiare spazio.</span><span class="sxs-lookup"><span data-stu-id="65235-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="65235-134">Per creare i lettori di metadati, utilizzare il metodo [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) .</span><span class="sxs-lookup"><span data-stu-id="65235-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="65235-135">Quando si richiama questo metodo, si passa il GUID del formato del contenitore nel parametro *guidContainerFormat* .</span><span class="sxs-lookup"><span data-stu-id="65235-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="65235-136">Se si ha la preferenza di fornitore per un lettore di metadati, è possibile passare il GUID del fornitore preferito nel parametro *pGuidVendor* .</span><span class="sxs-lookup"><span data-stu-id="65235-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="65235-137">Se, ad esempio, l'azienda scrive gestori di metadati e si vuole usare il proprio, se presente, è possibile passare il GUID del fornitore.</span><span class="sxs-lookup"><span data-stu-id="65235-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="65235-138">Nella maggior parte dei casi, è sufficiente passare **null** e consentire al sistema di selezionare il lettore di metadati appropriato.</span><span class="sxs-lookup"><span data-stu-id="65235-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="65235-139">Se si richiede un fornitore specifico e tale fornitore dispone di un lettore di metadati installato nel computer, WIC restituirà il lettore del fornitore.</span><span class="sxs-lookup"><span data-stu-id="65235-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="65235-140">Tuttavia, se il fornitore richiesto non dispone di un lettore di metadati installato nel computer e se è disponibile un lettore di metadati appropriato, il lettore verrà restituito anche se non è del fornitore preferito.</span><span class="sxs-lookup"><span data-stu-id="65235-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="65235-141">Se nel computer non è presente alcun lettore di metadati per il tipo di metadati nel blocco, la factory del componente restituisce il gestore di metadati sconosciuto, che considererà il blocco di metadati come oggetto binario di grandi dimensioni (BLOB) e deserializza il blocco di metadati dal file senza alcun tentativo di analisi.</span><span class="sxs-lookup"><span data-stu-id="65235-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="65235-142">Per il parametro *dwOptions* , eseguire un'operazione OR tra il [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) appropriato e il [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)appropriato.</span><span class="sxs-lookup"><span data-stu-id="65235-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="65235-143">Il **WICPersistOptions** descrive come il contenitore è disposto. Il valore predefinito è Little-endian.</span><span class="sxs-lookup"><span data-stu-id="65235-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="65235-144">[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specificare se si desidera ottenere UnknownMetadataHandler se nel computer non è presente alcun lettore di metadati in grado di leggere il formato dei metadati di un blocco specifico.</span><span class="sxs-lookup"><span data-stu-id="65235-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="65235-145">**WICMetadataCreationAllowUnknown** è l'impostazione predefinita ed è necessario consentire sempre la creazione di UnknownMetadtataHandler.</span><span class="sxs-lookup"><span data-stu-id="65235-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="65235-146">Il UnknownMetadataHandler considera i metadati non riconosciuti come un BLOB.</span><span class="sxs-lookup"><span data-stu-id="65235-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="65235-147">Non può analizzarlo, ma lo scrive nel flusso come un BLOB e lo rende intatto quando viene scritto nel flusso durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="65235-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="65235-148">In questo modo è possibile creare gestori di metadati per i metadati proprietari o i formati di metadati che non vengono forniti con il sistema.</span><span class="sxs-lookup"><span data-stu-id="65235-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="65235-149">Poiché i metadati vengono conservati intatti, anche se non è presente alcun gestore nel computer che lo riconosce, quando un gestore di metadati appropriato viene installato in un secondo momento, i metadati saranno ancora presenti e potranno essere letti.</span><span class="sxs-lookup"><span data-stu-id="65235-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="65235-150">Se non si consente la creazione di UnknownMetadataHandler, l'alternativa è l'eliminazione o la sovrascrittura dei metadati non riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="65235-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="65235-151">Si tratta di una forma di perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="65235-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="65235-152">Se si scrive un gestore di metadati personalizzato per i metadati proprietari, è consigliabile non includere mai riferimenti a qualsiasi elemento all'esterno del blocco di metadati stesso.</span><span class="sxs-lookup"><span data-stu-id="65235-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="65235-153">Sebbene il UnknownMetadataHandler manterrà i metadati intatti, i metadati vengono spostati quando i file vengono modificati e tutti i riferimenti a qualsiasi elemento all'esterno del proprio blocco non saranno più validi in questo caso.</span><span class="sxs-lookup"><span data-stu-id="65235-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="65235-154">Il parametro *pIStream* è il flusso effettivo che si sta decodificando.</span><span class="sxs-lookup"><span data-stu-id="65235-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="65235-155">Prima di passare al flusso, è necessario cercare all'inizio del blocco di metadati per il quale si richiede un lettore.</span><span class="sxs-lookup"><span data-stu-id="65235-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="65235-156">Il lettore di metadati appropriato per il blocco di metadati in corrispondenza della posizione corrente in [IStream](/windows/desktop/api/objidl/nn-objidl-istream) verrà restituito nel parametro *ppiReader* .</span><span class="sxs-lookup"><span data-stu-id="65235-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="65235-157">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="65235-157">GetReaderByIndex</span></span>

<span data-ttu-id="65235-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) restituisce il lettore di metadati in corrispondenza dell'indice richiesto nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="65235-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65235-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65235-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="65235-160">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="65235-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="65235-161">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="65235-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="65235-162">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="65235-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="65235-163">Implementazione di IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="65235-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="65235-164">Implementazione di IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="65235-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="65235-165">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="65235-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="65235-166">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="65235-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
