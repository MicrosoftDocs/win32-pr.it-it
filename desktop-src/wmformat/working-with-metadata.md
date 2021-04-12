---
title: Utilizzo dei metadati
description: Utilizzo dei metadati
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK, panoramica dei metadati
- Advanced Systems Format (ASF), panoramica dei metadati
- ASF (Advanced Systems Format), panoramica dei metadati
- metadati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398770"
---
# <a name="working-with-metadata"></a><span data-ttu-id="e4bcf-107">Utilizzo dei metadati</span><span class="sxs-lookup"><span data-stu-id="e4bcf-107">Working with Metadata</span></span>

<span data-ttu-id="e4bcf-108">Il supporto dei metadati è fornito dall'oggetto writer, dagli oggetti Reader e Reader sincroni e dall'oggetto editor dei metadati.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="e4bcf-109">Per informazioni generali sui metadati, vedere [metadati](metadata.md).</span><span class="sxs-lookup"><span data-stu-id="e4bcf-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="e4bcf-110">Per informazioni sulle funzionalità che supportano i metadati in Windows Media Format SDK, vedere [funzionalità dei metadati](metadata-features.md).</span><span class="sxs-lookup"><span data-stu-id="e4bcf-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="e4bcf-111">L'interfaccia per la modifica dei metadati è [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), che è possibile ottenere chiamando il metodo **QueryInterface** di qualsiasi interfaccia in uno degli oggetti elencati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="e4bcf-112">**IWMHeaderInfo3** eredita i metodi di [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span><span class="sxs-lookup"><span data-stu-id="e4bcf-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="e4bcf-113">I metodi di **IWMHeaderInfo3** che gestiscono gli attributi di metadati rappresentano un approccio diverso per accedere ai metadati rispetto a quello usato dai metodi di **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="e4bcf-114">Usare sempre i metodi più recenti.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-114">You should always use the newer methods.</span></span>

<span data-ttu-id="e4bcf-115">I metadati in un file ASF sono identificati da un indice e da un numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="e4bcf-116">Agli attributi a livello di file viene assegnato un numero di flusso pari a 0.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="e4bcf-117">Nelle versioni precedenti di Windows Media Format SDK, gli attributi possono essere identificati in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="e4bcf-118">Tuttavia, poiché è ora possibile duplicare i nomi di attributo all'interno di un flusso, questa operazione non è più possibile.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="e4bcf-119">È invece possibile recuperare tutti gli indici che corrispondono a un nome.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="e4bcf-120">Per altre informazioni, vedere [recupero di attributi di metadati](retrieving-metadata-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e4bcf-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="e4bcf-121">Per semplificare la ricerca rapida degli attributi, è possibile usare un numero di flusso speciale, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="e4bcf-122">Usare questo numero di flusso per identificare il file nel suo complesso, anziché uno specifico flusso o gli attributi a livello di file.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="e4bcf-123">Gli oggetti di Windows Media Format SDK mantengono indici distinti per ogni flusso e per gli attributi a livello di file.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="e4bcf-124">Quando si usa Stream 0xFFFF, gli indici sono diversi da quelli usati quando si specifica un flusso specifico.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="e4bcf-125">Ad esempio, l'attributo che è index 0 per stream 0 non corrisponderà all'attributo index 0 per Stream 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="e4bcf-126">Le sezioni seguenti descrivono in modo più dettagliato l'uso dei metadati.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="e4bcf-127">Sezione</span><span class="sxs-lookup"><span data-stu-id="e4bcf-127">Section</span></span>                                                                    | <span data-ttu-id="e4bcf-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4bcf-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e4bcf-129">Recupero degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="e4bcf-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="e4bcf-130">Viene descritto come leggere gli attributi dei metadati da un'intestazione di file.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="e4bcf-131">Impostazione degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="e4bcf-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="e4bcf-132">Viene descritto come aggiungere nuovi attributi di metadati a un'intestazione di file.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="e4bcf-133">Modifica degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="e4bcf-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="e4bcf-134">Viene descritto come modificare gli attributi di metadati esistenti.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="e4bcf-135">Rimozione degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="e4bcf-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="e4bcf-136">Viene descritto come rimuovere gli attributi di metadati esistenti.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="e4bcf-137">Uso di attributi di metadati complessi</span><span class="sxs-lookup"><span data-stu-id="e4bcf-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="e4bcf-138">Viene descritto come utilizzare gli attributi i cui valori sono rappresentati da strutture.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="e4bcf-139">Diverse applicazioni di esempio illustrano come recuperare e modificare i metadati.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="e4bcf-140">In particolare, vedere l'esempio MetadataEdit, disponibile in entrambe le versioni di C++ e C#.</span><span class="sxs-lookup"><span data-stu-id="e4bcf-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4bcf-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4bcf-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4bcf-142">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="e4bcf-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="e4bcf-143">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="e4bcf-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="e4bcf-144">**Applicazioni di esempio**</span><span class="sxs-lookup"><span data-stu-id="e4bcf-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




