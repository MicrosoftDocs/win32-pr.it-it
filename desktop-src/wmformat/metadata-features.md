---
title: Funzionalità dei metadati
description: I metadati vengono utilizzati nei file ASF per descrivere il contenuto e le proprietà del file.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK, funzionalità dei metadati
- Windows Media Format SDK, funzionalità
- ASF (Advanced Systems Format), funzionalità dei metadati
- ASF (Advanced Systems Format), funzionalità dei metadati
- ASF (Advanced Systems Format), funzionalità
- ASF (Advanced Systems Format), funzionalità
- metadati, funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398762"
---
# <a name="metadata-features"></a><span data-ttu-id="d1d5d-110">Funzionalità dei metadati</span><span class="sxs-lookup"><span data-stu-id="d1d5d-110">Metadata Features</span></span>

<span data-ttu-id="d1d5d-111">I metadati vengono utilizzati nei file ASF per descrivere il contenuto e le proprietà del file.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="d1d5d-112">Tutti i file ASF creati devono includere i metadati appropriati.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="d1d5d-113">Per una panoramica, vedere [metadati](metadata.md). Windows Media Format SDK include il supporto per la modifica dei metadati tramite l'oggetto writer, l'oggetto editor dei metadati e gli oggetti Reader e Reader sincroni.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="d1d5d-114">È incluso il supporto nativo per un'ampia gamma di attributi di metadati.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="d1d5d-115">Vedere [attributi](attributes.md) per un elenco degli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="d1d5d-116">Il supporto dei metadati fornito dai vari oggetti di Windows Media Format SDK è flessibile e potente.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="d1d5d-117">Le funzionalità principali dei metadati sono riepilogate nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="d1d5d-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="d1d5d-118">Dimensioni degli attributi flessibili.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-118">Flexible attribute size.</span></span> <span data-ttu-id="d1d5d-119">Le dimensioni degli attributi dei metadati non sono limitate.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="d1d5d-120">Attributi a livello di flusso.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-120">Stream-level attributes.</span></span> <span data-ttu-id="d1d5d-121">I metadati nei file ASF possono essere assegnati al file nel suo complesso o a un determinato flusso.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="d1d5d-122">Attributi duplicati.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-122">Duplicated attributes.</span></span> <span data-ttu-id="d1d5d-123">Un attributo denominato può essere utilizzato più volte nello stesso file.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="d1d5d-124">Questa funzionalità viene usata in particolare quando si assegnano attributi descrittivi del contenuto.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="d1d5d-125">Ad esempio, un brano può avere più autori, ognuno dei quali richiede un attributo **Author** separato nel file.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="d1d5d-126">Più lingue.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-126">Multiple languages.</span></span> <span data-ttu-id="d1d5d-127">A ogni attributo è associata una lingua.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="d1d5d-128">È possibile impostare le lingue supportate e assegnarne una a ogni attributo che si scrive.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="d1d5d-129">Poiché è possibile duplicare gli attributi, è possibile fornire gli attributi più importanti in diversi linguaggi per raggiungere un numero maggiore di destinatari.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="d1d5d-130">Se non si specifica una lingua, verrà usata la lingua predefinita, ottenuta dal sistema operativo del computer che esegue l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="d1d5d-131">Attributi complessi.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-131">Complex attributes.</span></span> <span data-ttu-id="d1d5d-132">Alcuni degli attributi predefiniti supportano i dati strutturati.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="d1d5d-133">Per questi attributi, il tipo di dati è binario, ma il valore è una struttura definita in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="d1d5d-134">Negli argomenti seguenti vengono illustrate le altre funzionalità di metadati supportate.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="d1d5d-135">Argomento</span><span class="sxs-lookup"><span data-stu-id="d1d5d-135">Topic</span></span>                                  | <span data-ttu-id="d1d5d-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1d5d-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1d5d-137">Supporto ID3</span><span class="sxs-lookup"><span data-stu-id="d1d5d-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="d1d5d-138">Viene illustrato il supporto per i frame ID3 utilizzando gli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="d1d5d-139">Metadati personalizzati</span><span class="sxs-lookup"><span data-stu-id="d1d5d-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="d1d5d-140">Vengono illustrate le implicazioni dell'utilizzo di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d1d5d-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="d1d5d-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1d5d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d5d-142">**Funzionalità**</span><span class="sxs-lookup"><span data-stu-id="d1d5d-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="d1d5d-143">**Interfaccia IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="d1d5d-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="d1d5d-144">**Interfaccia IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="d1d5d-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="d1d5d-145">**Interfaccia IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="d1d5d-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="d1d5d-146">**Metadati**</span><span class="sxs-lookup"><span data-stu-id="d1d5d-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




