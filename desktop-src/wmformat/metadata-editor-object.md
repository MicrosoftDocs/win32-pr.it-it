---
title: Oggetto Metadata Editor
description: Oggetto Metadata Editor
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media Format SDK, oggetti dell'editor di metadati
- ASF (Advanced Systems Format), oggetti dell'editor di metadati
- ASF (Advanced Systems Format), oggetti dell'editor di metadati
- oggetti, oggetti dell'editor di metadati
- oggetti dell'editor di metadati, informazioni
- metadati, oggetti Editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724100"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="69191-109">Oggetto Metadata Editor</span><span class="sxs-lookup"><span data-stu-id="69191-109">Metadata Editor Object</span></span>

<span data-ttu-id="69191-110">L'oggetto dell'editor di metadati viene utilizzato per modificare le informazioni archiviate nella sezione dell'intestazione dei file ASF.</span><span class="sxs-lookup"><span data-stu-id="69191-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="69191-111">Gli elementi più comuni modificati da questo oggetto sono gli attributi dei metadati.</span><span class="sxs-lookup"><span data-stu-id="69191-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="69191-112">Inoltre, l'editor di metadati gestisce i [*marcatori*](wmformat-glossary.md) e i comandi di script.</span><span class="sxs-lookup"><span data-stu-id="69191-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="69191-113">L'unico caso in cui è necessario utilizzare l'editor di metadati è quando si desidera modificare l'intestazione di un file esistente senza riprodurlo.</span><span class="sxs-lookup"><span data-stu-id="69191-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="69191-114">L'oggetto dell'editor di metadati viene creato dalla funzione [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), che imposta un puntatore a un'interfaccia **IWMMetadataEditor** .</span><span class="sxs-lookup"><span data-stu-id="69191-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="69191-115">Le altre interfacce dell'oggetto dell'editor di metadati possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="69191-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="69191-116">Le interfacce seguenti sono supportate dall'oggetto dell'editor di metadati.</span><span class="sxs-lookup"><span data-stu-id="69191-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="69191-117">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="69191-117">Interface</span></span>                                        | <span data-ttu-id="69191-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69191-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69191-119">**IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="69191-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="69191-120">Consente di modificare le applicazioni per esaminare le proprietà [*DRM*](wmformat-glossary.md) di un file ASF senza avere alcun diritto di riprodurre il contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="69191-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="69191-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="69191-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="69191-122">Modifica gli attributi, i marcatori e i comandi di script nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="69191-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="69191-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="69191-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="69191-124">Recupera le informazioni sul codec.</span><span class="sxs-lookup"><span data-stu-id="69191-124">Retrieves codec information.</span></span> <span data-ttu-id="69191-125">Eredita tutti i metodi di **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="69191-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="69191-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="69191-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="69191-127">Fornisce supporto avanzato per attributi, inclusi attributi di grandi dimensioni, più linguaggi e nomi di attributi duplicati.</span><span class="sxs-lookup"><span data-stu-id="69191-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="69191-128">Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="69191-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="69191-129">**IWMMetadataEditor**</span><span class="sxs-lookup"><span data-stu-id="69191-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="69191-130">Apre, chiude e salva le modifiche apportate all'intestazione di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="69191-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="69191-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="69191-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="69191-132">Apre un file ASF per la modifica dell'intestazione con più opzioni di accesso e condivisione file.</span><span class="sxs-lookup"><span data-stu-id="69191-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="69191-133">Eredita tutti i metodi di **IWMMetadataEditor**.</span><span class="sxs-lookup"><span data-stu-id="69191-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="69191-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69191-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69191-135">**Indicatori**</span><span class="sxs-lookup"><span data-stu-id="69191-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="69191-136">**Metadati**</span><span class="sxs-lookup"><span data-stu-id="69191-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="69191-137">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="69191-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="69191-138">**Comandi script**</span><span class="sxs-lookup"><span data-stu-id="69191-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="69191-139">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="69191-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




