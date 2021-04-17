---
description: Implementazione di IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementazione di IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530270"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="06f6c-103">Implementazione di IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="06f6c-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="06f6c-104">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="06f6c-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="06f6c-105">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="06f6c-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="06f6c-106">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="06f6c-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="06f6c-107">AddWriter</span><span class="sxs-lookup"><span data-stu-id="06f6c-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="06f6c-108">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="06f6c-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="06f6c-109">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="06f6c-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="06f6c-110">La classe di codifica a livello di frame implementa questa interfaccia per esporre tutti i blocchi di metadati e richiedere il writer di metadati appropriato per ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="06f6c-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="06f6c-111">Se il formato dell'immagine supporta i metadati globali, al di fuori di qualsiasi singolo frame, è necessario implementare anche questa interfaccia sulla classe del codificatore a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="06f6c-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="06f6c-112">Per una descrizione più dettagliata dei gestori di metadati, vedere la sezione in [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nella sezione relativa all'implementazione di un decodificatore WIC-Enabled.</span><span class="sxs-lookup"><span data-stu-id="06f6c-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="06f6c-113">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="06f6c-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="06f6c-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) usa un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) per inizializzare il writer del blocco.</span><span class="sxs-lookup"><span data-stu-id="06f6c-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="06f6c-115">È possibile ottenere il **IWICMetadataBlockReader** dal decodificatore per decodificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="06f6c-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="06f6c-116">Poiché l'inizializzazione di [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) con un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) crea un'istanza di un writer di metadati per ogni lettore di metadati esposto dall'oggetto **IWICMetadataBlockReader** , l'applicazione non deve richiedere esplicitamente un writer per ogni blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="06f6c-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="06f6c-117">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="06f6c-117">GetWriterByIndex</span></span>

<span data-ttu-id="06f6c-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) restituisce l'oggetto [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) per il blocco di metadati nth, dove n è il valore passato nel parametro *nIndex* .</span><span class="sxs-lookup"><span data-stu-id="06f6c-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="06f6c-119">Se non è presente alcun writer di metadati registrato in grado di gestire il tipo di metadati nel blocco ennesimo, la factory del componente restituisce il gestore di metadati sconosciuto, che considererà il blocco dei metadati come oggetto binario di grandi dimensioni (BLOB).</span><span class="sxs-lookup"><span data-stu-id="06f6c-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="06f6c-120">Verrà serializzato come flusso di bit senza provare ad analizzarlo.</span><span class="sxs-lookup"><span data-stu-id="06f6c-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="06f6c-121">AddWriter</span><span class="sxs-lookup"><span data-stu-id="06f6c-121">AddWriter</span></span>

<span data-ttu-id="06f6c-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) consente a un chiamante di aggiungere un nuovo writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="06f6c-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="06f6c-123">Questa operazione è necessaria se un'applicazione desidera aggiungere metadati di un formato diverso rispetto a qualsiasi blocco di metadati esistente.</span><span class="sxs-lookup"><span data-stu-id="06f6c-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="06f6c-124">Ad esempio, un'applicazione potrebbe voler aggiungere alcuni metadati XMP.</span><span class="sxs-lookup"><span data-stu-id="06f6c-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="06f6c-125">Se non è presente alcun blocco di metadati XMP, l'applicazione deve creare un'istanza di un writer di metadati XMP e usare il metodo **AddWriter** per includerlo nella raccolta di writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="06f6c-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="06f6c-126">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="06f6c-126">SetWriterByIndex</span></span>

<span data-ttu-id="06f6c-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) viene utilizzato per aggiungere un writer di metadati in corrispondenza di un indice specifico nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="06f6c-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="06f6c-128">Se un writer di metadati è attualmente presente in tale indice, il nuovo deve sostituirlo.</span><span class="sxs-lookup"><span data-stu-id="06f6c-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="06f6c-129">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="06f6c-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="06f6c-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) viene utilizzato per rimuovere un writer di metadati dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="06f6c-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f6c-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06f6c-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06f6c-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="06f6c-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06f6c-133">Implementazione di IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="06f6c-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="06f6c-134">Installazione e registrazione di CODEC</span><span class="sxs-lookup"><span data-stu-id="06f6c-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="06f6c-135">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="06f6c-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="06f6c-136">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="06f6c-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



