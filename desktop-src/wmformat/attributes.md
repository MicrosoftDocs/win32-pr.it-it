---
title: Attributi (Windows Media Format 11 SDK)
description: Attributi
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400138"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="66fa8-107">Attributi (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="66fa8-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="66fa8-108">Un attributo è un singolo elemento di metadati.</span><span class="sxs-lookup"><span data-stu-id="66fa8-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="66fa8-109">La maggior parte degli attributi può essere impostata dall'applicazione e viene scritta nell'intestazione di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="66fa8-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="66fa8-110">Alcuni degli attributi predefiniti sono attributi codificati.</span><span class="sxs-lookup"><span data-stu-id="66fa8-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="66fa8-111">Questi attributi non vengono archiviati nell'intestazione di un file ASF, ma vengono calcolati dagli oggetti di Windows Media Format SDK quando il file viene caricato.</span><span class="sxs-lookup"><span data-stu-id="66fa8-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="66fa8-112">Poiché gli attributi codificati vengono sempre calcolati, sono intrinsecamente di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="66fa8-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="66fa8-113">Questo SDK include molte definizioni degli attributi che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="66fa8-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="66fa8-114">È anche possibile creare attributi personalizzati per descrivere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="66fa8-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="66fa8-115">Le sezioni seguenti descrivono gli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="66fa8-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="66fa8-116">Sezione</span><span class="sxs-lookup"><span data-stu-id="66fa8-116">Section</span></span>                                                                | <span data-ttu-id="66fa8-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66fa8-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66fa8-118">Elenco degli attributi</span><span class="sxs-lookup"><span data-stu-id="66fa8-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="66fa8-119">Fornisce un elenco alfabetico di tutti gli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="66fa8-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="66fa8-120">Dopo l'elenco, ogni attributo viene descritto singolarmente.</span><span class="sxs-lookup"><span data-stu-id="66fa8-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="66fa8-121">Attributi con più valori</span><span class="sxs-lookup"><span data-stu-id="66fa8-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="66fa8-122">Elenca gli attributi che possono essere aggiunti a un file più di una volta.</span><span class="sxs-lookup"><span data-stu-id="66fa8-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="66fa8-123">Attributi per tipo</span><span class="sxs-lookup"><span data-stu-id="66fa8-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="66fa8-124">Contiene elenchi di attributi ordinati per tipo.</span><span class="sxs-lookup"><span data-stu-id="66fa8-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="66fa8-125">Sono inclusi gli elenchi di attributi specifici, ad esempio quelli che gestiscono Digital Rights Management, ed elenchi di attributi suggeriti in base al tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="66fa8-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="66fa8-126">Supporto tag ID3</span><span class="sxs-lookup"><span data-stu-id="66fa8-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="66fa8-127">Elenca gli attributi compatibili con i tag ID3.</span><span class="sxs-lookup"><span data-stu-id="66fa8-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="66fa8-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66fa8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66fa8-129">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="66fa8-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="66fa8-130">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="66fa8-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="66fa8-131">**IWMHeaderInfo:: SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="66fa8-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="66fa8-132">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="66fa8-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




