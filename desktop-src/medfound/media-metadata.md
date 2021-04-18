---
description: Metadati del supporto
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadati del supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320703"
---
# <a name="media-metadata"></a><span data-ttu-id="54e68-103">Metadati del supporto</span><span class="sxs-lookup"><span data-stu-id="54e68-103">Media Metadata</span></span>

<span data-ttu-id="54e68-104">I file multimediali contengono proprietà che descrivono il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="54e68-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="54e68-105">In Microsoft Media Foundation, queste proprietà possono essere categorizzate come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="54e68-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="54e68-106">**Gli attributi di tipo supporto** specificano i parametri di codifica, ad esempio l'algoritmo di codifica (sottotipo di supporto), le dimensioni del fotogramma video, la frequenza dei fotogrammi video, la velocità in bit audio e la frequenza di campionamento audio.</span><span class="sxs-lookup"><span data-stu-id="54e68-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="54e68-107">Per ulteriori informazioni sugli attributi di tipo media, vedere [tipi di supporto](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="54e68-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="54e68-108">I **metadati** contengono informazioni descrittive per il contenuto multimediale, ad esempio titolo, artista, compositore e genere.</span><span class="sxs-lookup"><span data-stu-id="54e68-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="54e68-109">I metadati possono anche descrivere i parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="54e68-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="54e68-110">Può essere più veloce accedere a queste informazioni tramite metadati rispetto agli attributi di tipo supporto.</span><span class="sxs-lookup"><span data-stu-id="54e68-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="54e68-111">Le **Proprietà DRM** contengono informazioni sulle restrizioni di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="54e68-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="54e68-112">Attualmente Media Foundation non supporta le proprietà DRM tramite i metadati, ad eccezione della proprietà **\_ \_ protetta da pkey DRM** .</span><span class="sxs-lookup"><span data-stu-id="54e68-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="54e68-113">Esistono due modi per leggere i metadati in Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="54e68-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="54e68-114">Interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (metadati Media Foundation versione 1).</span><span class="sxs-lookup"><span data-stu-id="54e68-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="54e68-115">L'interfaccia di Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (metadati della Shell).</span><span class="sxs-lookup"><span data-stu-id="54e68-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="54e68-116">I metadati della shell sono relativi non solo ai file multimediali ma a una gamma molto più ampia di file nel sistema.</span><span class="sxs-lookup"><span data-stu-id="54e68-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="54e68-117">Nella tabella seguente vengono confrontate le caratteristiche e le limitazioni di ogni API dei metadati.</span><span class="sxs-lookup"><span data-stu-id="54e68-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54e68-118">Metadati di Media Foundation V1</span><span class="sxs-lookup"><span data-stu-id="54e68-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="54e68-119">Metadati della shell</span><span class="sxs-lookup"><span data-stu-id="54e68-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54e68-120">Richiede Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="54e68-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="54e68-121">Richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54e68-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="54e68-122">I metadati della shell in generale non richiedono Windows 7, ma Media Foundation non supportava i metadati della shell prima di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54e68-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e68-123">Le proprietà non sono compatibili con il sistema di proprietà della shell.</span><span class="sxs-lookup"><span data-stu-id="54e68-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="54e68-124">Le proprietà sono compatibili con il sistema di proprietà della shell.</span><span class="sxs-lookup"><span data-stu-id="54e68-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e68-125">Le proprietà possono essere valide per l'intero file o a livello di flusso.</span><span class="sxs-lookup"><span data-stu-id="54e68-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="54e68-126">Sono supportate solo le proprietà a livello di file.</span><span class="sxs-lookup"><span data-stu-id="54e68-126">Only file-level properties are supported.</span></span> <span data-ttu-id="54e68-127">Le proprietà a livello di flusso non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="54e68-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e68-128">Le proprietà possono avere valori in più lingue.</span><span class="sxs-lookup"><span data-stu-id="54e68-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="54e68-129">I valori in più lingue non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="54e68-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e68-130">Le chiavi delle proprietà sono stringhe a caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="54e68-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="54e68-131">Le chiavi delle proprietà sono valori <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="54e68-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e68-132">I valori delle proprietà sono valori <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="54e68-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="54e68-133">I valori delle proprietà sono valori <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="54e68-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="54e68-134">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="54e68-134">In this section</span></span>



| <span data-ttu-id="54e68-135">Argomento</span><span class="sxs-lookup"><span data-stu-id="54e68-135">Topic</span></span>                                                                                     | <span data-ttu-id="54e68-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54e68-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54e68-137">Provider di metadati della shell</span><span class="sxs-lookup"><span data-stu-id="54e68-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="54e68-138">A partire da Windows 7, Media Foundation espone i metadati tramite l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="54e68-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="54e68-139">Proprietà dei metadati dei file multimediali</span><span class="sxs-lookup"><span data-stu-id="54e68-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="54e68-140">Questo argomento elenca le proprietà dei metadati più comuni per i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="54e68-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="54e68-141">Provider di metadati in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54e68-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="54e68-142">In Windows Vista Media Foundation espone i metadati tramite l'interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="54e68-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="54e68-143">Se si implementa un'origine multimediale personalizzata e si vuole esporre i metadati della shell, vedere [provider di metadati personalizzati per i file multimediali](custom-metadata-providers-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="54e68-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54e68-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54e68-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e68-145">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54e68-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
