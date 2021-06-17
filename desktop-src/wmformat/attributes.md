---
title: Attributi (Windows Media Format 11 SDK)
description: Informazioni sugli attributi in Windows Media Format 11 SDK. Un attributo è un singolo elemento di metadati.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK,attributi
- Advanced Systems Format (ASF), attributi
- ASF (Advanced Systems Format), attributi
- attributi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262193"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="dac02-108">Attributi (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="dac02-108">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="dac02-109">Un attributo è un singolo elemento di metadati.</span><span class="sxs-lookup"><span data-stu-id="dac02-109">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="dac02-110">La maggior parte degli attributi può essere impostata dall'applicazione e viene scritta nell'intestazione di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="dac02-110">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="dac02-111">Alcuni degli attributi predefiniti sono attributi codificati.</span><span class="sxs-lookup"><span data-stu-id="dac02-111">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="dac02-112">Questi attributi non vengono archiviati nell'intestazione di un file ASF, ma vengono calcolati dagli oggetti di Windows Media Format SDK quando il file viene caricato.</span><span class="sxs-lookup"><span data-stu-id="dac02-112">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="dac02-113">Poiché gli attributi codificati vengono sempre calcolati, sono intrinsecamente di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dac02-113">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="dac02-114">Questo SDK include molte definizioni di attributo che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="dac02-114">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="dac02-115">È anche possibile creare attributi personalizzati per descrivere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="dac02-115">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="dac02-116">Le sezioni seguenti descrivono gli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="dac02-116">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="dac02-117">Sezione</span><span class="sxs-lookup"><span data-stu-id="dac02-117">Section</span></span>                                                                | <span data-ttu-id="dac02-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dac02-118">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dac02-119">Elenco degli attributi</span><span class="sxs-lookup"><span data-stu-id="dac02-119">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="dac02-120">Fornisce un elenco alfabetico di tutti gli attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="dac02-120">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="dac02-121">Dopo l'elenco, ogni attributo viene descritto singolarmente.</span><span class="sxs-lookup"><span data-stu-id="dac02-121">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="dac02-122">Attributi con più valori</span><span class="sxs-lookup"><span data-stu-id="dac02-122">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="dac02-123">Elenca gli attributi che possono essere aggiunti a un file più di una volta.</span><span class="sxs-lookup"><span data-stu-id="dac02-123">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="dac02-124">Attributi per tipo</span><span class="sxs-lookup"><span data-stu-id="dac02-124">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="dac02-125">Contiene elenchi di attributi ordinati in base al tipo.</span><span class="sxs-lookup"><span data-stu-id="dac02-125">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="dac02-126">Tra questi sono inclusi elenchi di attributi di utilizzo speciale (ad esempio quelli che gestiscono digital rights management) e gli elenchi di attributi suggeriti in base al tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="dac02-126">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="dac02-127">Supporto tag ID3</span><span class="sxs-lookup"><span data-stu-id="dac02-127">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="dac02-128">Elenca gli attributi compatibili con i tag ID3.</span><span class="sxs-lookup"><span data-stu-id="dac02-128">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="dac02-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dac02-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac02-130">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="dac02-130">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="dac02-131">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="dac02-131">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="dac02-132">**IWMHeaderInfo::SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="dac02-132">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="dac02-133">**Uso dei metadati**</span><span class="sxs-lookup"><span data-stu-id="dac02-133">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




