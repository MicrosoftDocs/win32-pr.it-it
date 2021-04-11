---
description: In questo argomento vengono fornite informazioni sulla creazione dell'oggetto indicizzatore predefinito fornito da Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Creazione e configurazione dell'indicizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232539"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="02ebd-103">Creazione e configurazione dell'indicizzatore</span><span class="sxs-lookup"><span data-stu-id="02ebd-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="02ebd-104">L' *indicizzatore* ASF è un componente di livello WMContainer che viene usato per leggere o scrivere oggetti index in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="02ebd-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="02ebd-105">In questo argomento vengono fornite informazioni sulla creazione dell'oggetto indicizzatore predefinito fornito da Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="02ebd-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="02ebd-106">Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="02ebd-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="02ebd-107">**Per creare e inizializzare l'indicizzatore ASF**</span><span class="sxs-lookup"><span data-stu-id="02ebd-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="02ebd-108">Chiamare la funzione [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) per ricevere un puntatore [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) all'oggetto indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="02ebd-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="02ebd-109">Chiamare [**IMFASFIndexer:: Flags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) per specificare la modalità di lettura o scrittura per l'oggetto indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="02ebd-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="02ebd-110">Per impostazione predefinita, l'indicizzatore è configurato per la ricerca in futuro.</span><span class="sxs-lookup"><span data-stu-id="02ebd-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="02ebd-111">Uso</span><span class="sxs-lookup"><span data-stu-id="02ebd-111">Use</span></span>                       | <span data-ttu-id="02ebd-112">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="02ebd-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="02ebd-113">Lettura (ricerca in diretta)</span><span class="sxs-lookup"><span data-stu-id="02ebd-113">Reading (forward seeking)</span></span> | <span data-ttu-id="02ebd-114">Zero (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="02ebd-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="02ebd-115">Lettura (ricerca inversa)</span><span class="sxs-lookup"><span data-stu-id="02ebd-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="02ebd-116">**MFASF \_ indicizzatore \_ Read \_ per \_ REVERSEPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="02ebd-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="02ebd-117">Scrittura</span><span class="sxs-lookup"><span data-stu-id="02ebd-117">Writing</span></span>                   | <span data-ttu-id="02ebd-118">MFASF \_ indicizzatore \_ scrive un \_ nuovo \_ Indice</span><span class="sxs-lookup"><span data-stu-id="02ebd-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="02ebd-119">Non è possibile usare la stessa istanza dell'indicizzatore sia per la lettura che per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="02ebd-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="02ebd-120">È necessario configurare l'indicizzatore per uno o l'altro.</span><span class="sxs-lookup"><span data-stu-id="02ebd-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="02ebd-121">Chiamare [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) per inizializzare l'indicizzatore specificando il puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) dell'oggetto ContentInfo che descrive il file da scrivere o leggere.</span><span class="sxs-lookup"><span data-stu-id="02ebd-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="02ebd-122">L'oggetto ContentInfo contiene informazioni che costituiscono l' [oggetto intestazione ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="02ebd-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="02ebd-123">L'oggetto indicizzatore richiede un oggetto ContentInfo valido prima di generare o leggere voci di indice di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="02ebd-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="02ebd-124">Nell'esempio di codice seguente viene illustrato come un'applicazione può creare e inizializzare l'oggetto indicizzatore per l'utilizzo di contenuto ASF specifico.</span><span class="sxs-lookup"><span data-stu-id="02ebd-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="02ebd-125">L'oggetto ContentInfo rappresenta l'oggetto intestazione ASF; il contenuto viene passato come flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="02ebd-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="02ebd-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02ebd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ebd-127">Indicizzatore ASF</span><span class="sxs-lookup"><span data-stu-id="02ebd-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="02ebd-128">Utilizzo dell'indicizzatore per la ricerca all'interno di un file ASF</span><span class="sxs-lookup"><span data-stu-id="02ebd-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="02ebd-129">Uso dell'indicizzatore per scrivere un nuovo indice</span><span class="sxs-lookup"><span data-stu-id="02ebd-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



