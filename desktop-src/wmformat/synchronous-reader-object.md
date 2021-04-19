---
title: Oggetto lettore sincrono
description: Oggetto lettore sincrono
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK, oggetti Reader sincroni
- ASF (Advanced Systems Format), oggetti Reader sincroni
- ASF (Advanced Systems Format), oggetti Reader sincroni
- oggetti, oggetti Reader sincroni
- lettori sincroni, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299516"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="adc98-108">Oggetto lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="adc98-108">Synchronous Reader Object</span></span>

<span data-ttu-id="adc98-109">L'oggetto Reader sincrono viene usato per leggere i file multimediali digitali usando chiamate sincrone.</span><span class="sxs-lookup"><span data-stu-id="adc98-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="adc98-110">L'oggetto Reader sincrono viene creato dalla funzione [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), che imposta un puntatore a un'interfaccia **IWMSyncReader** .</span><span class="sxs-lookup"><span data-stu-id="adc98-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="adc98-111">Le altre interfacce supportate dall'interfaccia di lettura sincrona possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="adc98-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="adc98-112">Le interfacce seguenti sono supportate dall'oggetto Reader sincrono.</span><span class="sxs-lookup"><span data-stu-id="adc98-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="adc98-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="adc98-113">Interface</span></span>                                | <span data-ttu-id="adc98-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc98-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adc98-115">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="adc98-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="adc98-116">Imposta e recupera le informazioni di intestazione, ad esempio i metadati, i [*marcatori*](wmformat-glossary.md)e così via.</span><span class="sxs-lookup"><span data-stu-id="adc98-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="adc98-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="adc98-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="adc98-118">Enumera le informazioni sui codec disponibili.</span><span class="sxs-lookup"><span data-stu-id="adc98-118">Enumerates the available codec information.</span></span> <span data-ttu-id="adc98-119">Eredita tutti i metodi di **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="adc98-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="adc98-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="adc98-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="adc98-121">Supporta le dimensioni degli attributi grandi, i nomi di attributi duplicati e il supporto di più lingue.</span><span class="sxs-lookup"><span data-stu-id="adc98-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="adc98-122">Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="adc98-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="adc98-123">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="adc98-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="adc98-124">Consente di accedere alle informazioni sul profilo del file Windows Media caricato nel lettore.</span><span class="sxs-lookup"><span data-stu-id="adc98-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="adc98-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="adc98-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="adc98-126">Recupera l'identificatore univoco globale (GUID), se presente, associato al profilo.</span><span class="sxs-lookup"><span data-stu-id="adc98-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="adc98-127">Eredita tutti i metodi di **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="adc98-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="adc98-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="adc98-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="adc98-129">Supporta la condivisione della larghezza di banda e le informazioni relative alla priorità del flusso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="adc98-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="adc98-130">Eredita tutti i metodi di **IWMProfile** e **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="adc98-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="adc98-131">**IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="adc98-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="adc98-132">Fornisce funzionalità di lettura sincrona per i file multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="adc98-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="adc98-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="adc98-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="adc98-134">Fornisce supporto per la ricerca di codici temporali SMPTE e per l'allocazione manuale di campioni.</span><span class="sxs-lookup"><span data-stu-id="adc98-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="adc98-135">Eredita tutti i metodi di **IWMSyncReader**.</span><span class="sxs-lookup"><span data-stu-id="adc98-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="adc98-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="adc98-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adc98-137">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="adc98-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="adc98-138">**Oggetto Lettore**</span><span class="sxs-lookup"><span data-stu-id="adc98-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="adc98-139">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="adc98-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




