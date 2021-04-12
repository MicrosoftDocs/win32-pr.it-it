---
title: Metadati
description: Ai fini di questo SDK, i metadati sono informazioni che descrivono un file ASF o il contenuto del file.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK, panoramica dei metadati
- Advanced Systems Format (ASF), panoramica dei metadati
- ASF (Advanced Systems Format), panoramica dei metadati
- metadati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332295"
---
# <a name="metadata"></a><span data-ttu-id="b51b2-107">Metadati</span><span class="sxs-lookup"><span data-stu-id="b51b2-107">Metadata</span></span>

<span data-ttu-id="b51b2-108">Ai fini di questo SDK, i metadati sono informazioni che descrivono un file ASF o il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="b51b2-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="b51b2-109">La sezione di intestazione di un file ASF contiene tutti i metadati associati a tale file.</span><span class="sxs-lookup"><span data-stu-id="b51b2-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="b51b2-110">Singoli elementi di metadati in un file ASF sono denominati attributi.</span><span class="sxs-lookup"><span data-stu-id="b51b2-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="b51b2-111">Ogni attributo ha un nome e un valore.</span><span class="sxs-lookup"><span data-stu-id="b51b2-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="b51b2-112">In questa documentazione vengono usate le costanti globali per identificare gli attributi.</span><span class="sxs-lookup"><span data-stu-id="b51b2-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="b51b2-113">Ad esempio, il titolo di un file ASF viene archiviato nell'attributo **g \_ wszWMTitle** .</span><span class="sxs-lookup"><span data-stu-id="b51b2-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="b51b2-114">In Windows Media Format SDK sono definiti diversi attributi che consentono di gestire le esigenze più comuni dei metadati.</span><span class="sxs-lookup"><span data-stu-id="b51b2-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="b51b2-115">Inoltre, è possibile creare attributi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b51b2-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="b51b2-116">È necessario prestare attenzione quando si denominano gli attributi personalizzati, tuttavia, poiché altri sviluppatori di applicazioni possono utilizzare gli stessi nomi e possono verificarsi conflitti.</span><span class="sxs-lookup"><span data-stu-id="b51b2-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="b51b2-117">Alcuni attributi vengono impostati dall'SDK e non possono essere modificati manualmente.</span><span class="sxs-lookup"><span data-stu-id="b51b2-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="b51b2-118">Ad esempio, quando si indicizza un file ASF, l'SDK imposta l'attributo **g \_ wszWMSeekable** per indicare che è ora possibile leggere il file da un punto specificato.</span><span class="sxs-lookup"><span data-stu-id="b51b2-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="b51b2-119">Gli altri attributi sono puramente informativi e devono essere impostati manualmente.</span><span class="sxs-lookup"><span data-stu-id="b51b2-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="b51b2-120">Ad esempio, se si vuole tenere traccia dell'autore di un file, è necessario impostare **g \_ wszWMAuthor**.</span><span class="sxs-lookup"><span data-stu-id="b51b2-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="b51b2-121">Windows Media Format SDK fornisce il supporto per gli attributi applicabili all'intero file e gli attributi che si applicano ai singoli flussi.</span><span class="sxs-lookup"><span data-stu-id="b51b2-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="b51b2-122">È possibile utilizzare Windows Media Format SDK per modificare i metadati nei file MP3, anche se è consigliabile utilizzare sempre gli attributi conformi a ID3 nei file MP3 per mantenere la compatibilità con altri programmi di manipolazione MP3.</span><span class="sxs-lookup"><span data-stu-id="b51b2-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b51b2-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b51b2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b51b2-124">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="b51b2-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="b51b2-125">**Oggetto Metadata Editor**</span><span class="sxs-lookup"><span data-stu-id="b51b2-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="b51b2-126">**Funzionalità dei metadati**</span><span class="sxs-lookup"><span data-stu-id="b51b2-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="b51b2-127">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="b51b2-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




