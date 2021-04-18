---
description: Questo argomento si applica a Windows Vista e versioni successive.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integrazione con raccolta foto di Windows e Esplora risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314885"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="24964-103">Integrazione con raccolta foto di Windows e Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="24964-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="24964-104">Questo argomento si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="24964-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="24964-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="24964-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="24964-106">Introduzione</span><span class="sxs-lookup"><span data-stu-id="24964-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="24964-107">Integrazione con l'archivio di proprietà di Windows</span><span class="sxs-lookup"><span data-stu-id="24964-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="24964-108">Integrazione con la raccolta foto di Windows</span><span class="sxs-lookup"><span data-stu-id="24964-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="24964-109">Integrazione con la cache delle anteprime di Windows</span><span class="sxs-lookup"><span data-stu-id="24964-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="24964-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24964-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="24964-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="24964-111">Introduction</span></span>

<span data-ttu-id="24964-112">Per abilitare la raccolta foto di Windows e Esplora risorse per visualizzare le anteprime e cercare e aggiornare i metadati delle immagini standard, un codec deve disporre di un'implementazione delle interfacce [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associate.</span><span class="sxs-lookup"><span data-stu-id="24964-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="24964-113">L'interfaccia IThumbnailProvider viene utilizzata per recuperare le anteprime e popolare la cache delle anteprime e l'interfaccia IPropertyStore viene utilizzata per la ricerca e l'aggiornamento dei metadati associati a un file.</span><span class="sxs-lookup"><span data-stu-id="24964-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="24964-114">A partire da Windows Vista, tutti i tipi di file hanno anteprime e metadati, ma tipi di file diversi richiedono implementazioni diverse di queste interfacce per recuperare o generare le anteprime e i metadati.</span><span class="sxs-lookup"><span data-stu-id="24964-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="24964-115">Il sistema fornisce le implementazioni predefinite di queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="24964-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="24964-116">L'implementazione predefinita di IThumbnailProvider può essere utilizzata per qualsiasi formato di immagine abilitato per Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="24964-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="24964-117">L'implementazione predefinita di IPropertyStore può essere utilizzata con qualsiasi formato di immagine abilitato per WIC basato su un contenitore Tagged Image File Format (TIFF) o JPEG.</span><span class="sxs-lookup"><span data-stu-id="24964-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="24964-118">Per associare il formato di immagine alle implementazioni predefinite di entrambe le interfacce, è necessario aggiungere solo alcune voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="24964-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="24964-119">Le voci seguenti indicano alla raccolta foto di Windows e a Esplora risorse che un'estensione di file (. ext) e il tipo MIME associato sono associati a un formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="24964-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="24964-120">La voce seguente indica a Windows e alle applicazioni che usano il tipo di contenuto (noto anche come tipo MIME) che un file con un'estensione specifica (. ext) è un formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="24964-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="24964-121">Il proprietario del tipo di file deve scegliere un `<image sub type value>` che identifichi in modo univoco il formato di file e il valore del tipo di contenuto deve essere registrato con IANA.</span><span class="sxs-lookup"><span data-stu-id="24964-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="24964-122">La voce seguente indica a Windows, Windows Search e alle applicazioni che usano [System. Kind](../properties/props-system-kind.md) che un'estensione di file (. ext) deve essere considerata come un'immagine.</span><span class="sxs-lookup"><span data-stu-id="24964-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="24964-123">In particolare, indica che la proprietà System. Kind dell'estensione del file deve essere impostata su Picture.</span><span class="sxs-lookup"><span data-stu-id="24964-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="24964-124">Integrazione con l'archivio di proprietà di Windows</span><span class="sxs-lookup"><span data-stu-id="24964-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="24964-125">Talvolta le stesse proprietà dei metadati sono esposte in schemi di metadati diversi, spesso con nomi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="24964-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="24964-126">Quando una di queste proprietà viene aggiornata, ma le altre non lo sono, i metadati all'interno del file possono non essere sincronizzati. Il gestore delle proprietà Photo fornisce l'implementazione predefinita di **IPropertyStore** per le immagini e viene usato dalle applicazioni, nonché dalla raccolta foto di Windows e da Esplora risorse, per garantire che tutti i metadati in un'immagine rimangano sincronizzati e che le proprietà visualizzate dalle applicazioni siano coerenti con quelle visualizzate dalla raccolta foto di Windows e da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="24964-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="24964-127">Quando il gestore delle proprietà Photo aggiorna i metadati, verifica che queste proprietà vengano aggiornate in modo coerente in tutti i formati di metadati comuni presenti nel file.</span><span class="sxs-lookup"><span data-stu-id="24964-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="24964-128">Il gestore delle proprietà Photo deve comprendere il formato del contenitore e come individuare le varie proprietà al suo interno.</span><span class="sxs-lookup"><span data-stu-id="24964-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="24964-129">In generale, il gestore delle proprietà Photo non è in grado di capire come i diversi blocchi di metadati sono disposti in un formato contenitore proprietario.</span><span class="sxs-lookup"><span data-stu-id="24964-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="24964-130">Tuttavia, se i metadati nel formato del contenitore sono disposti allo stesso modo dei metadati in un formato contenitore TIFF o in un formato contenitore JPEG, il gestore delle proprietà Photo può sfruttare tali informazioni per aggiornare i metadati in modo coerente anche nel formato del contenitore.</span><span class="sxs-lookup"><span data-stu-id="24964-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="24964-131">È possibile registrare questa associazione creando la seguente voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="24964-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="24964-132">Questa voce notifica al gestore della proprietà Photo che il formato del contenitore identificato da questo GUID riconosce gli stessi percorsi del linguaggio di query dei metadati del formato del contenitore con il GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span><span class="sxs-lookup"><span data-stu-id="24964-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="24964-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 è il GUID del formato del contenitore TIFF).</span><span class="sxs-lookup"><span data-stu-id="24964-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="24964-134">La voce seguente associa l'implementazione predefinita del gestore delle proprietà Photo di **IPropertyStore** con i file con estensione ". ext".</span><span class="sxs-lookup"><span data-stu-id="24964-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="24964-135">Il primo GUID è l'IID dell'interfaccia **IPropertyStore** e il secondo è il GUID dell'implementazione del gestore delle proprietà Photo.</span><span class="sxs-lookup"><span data-stu-id="24964-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="24964-136">I codec che usano un formato proprietario non compatibile con il formato di contenitore TIFF o JPEG devono scrivere la propria implementazione di **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="24964-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="24964-137">Integrazione con la raccolta foto di Windows</span><span class="sxs-lookup"><span data-stu-id="24964-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="24964-138">Raccolta foto di Windows si basa su WIC e può visualizzare qualsiasi formato di immagine abilitato per WIC per cui è installato il codec.</span><span class="sxs-lookup"><span data-stu-id="24964-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="24964-139">Per notificare al sistema che il formato dell'immagine può essere aperto nella raccolta foto di Windows, è necessario creare un'associazione di file creando le voci del registro di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="24964-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="24964-140">ProgID è in genere l'estensione del nome file aggiunta con la parola "file".</span><span class="sxs-lookup"><span data-stu-id="24964-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="24964-141">Se, ad esempio, l'estensione del nome file è. txt, ProgID sarà in genere "txtFile".</span><span class="sxs-lookup"><span data-stu-id="24964-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="24964-142">Per supportare le associazioni di file, potrebbe essere necessario creare altre voci del registro di sistema standard. Tuttavia, poiché the'y non sono specifici di WIC, esulano dall'ambito di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="24964-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="24964-143">Integrazione con la cache delle anteprime di Windows</span><span class="sxs-lookup"><span data-stu-id="24964-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="24964-144">Le due voci seguenti indicano che è possibile usare l'implementazione del provider di anteprime WIC standard per recuperare le anteprime dei file con questa estensione.</span><span class="sxs-lookup"><span data-stu-id="24964-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="24964-145">Il primo GUID è l'IID dell'interfaccia [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , mentre il secondo è il GUID dell'implementazione di sistema standard di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="24964-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="24964-146">(Tutte le voci in HLCR \\ . ext \\ ShellEx \\ vengono ripetute in HKCR \\ SystemFileAssociations \\ . ext \\ ShellEx \\ .)</span><span class="sxs-lookup"><span data-stu-id="24964-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="24964-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24964-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24964-148">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="24964-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24964-149">Voci del registro di sistema specifiche del codificatore</span><span class="sxs-lookup"><span data-stu-id="24964-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="24964-150">Installazione e registrazione di CODEC</span><span class="sxs-lookup"><span data-stu-id="24964-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="24964-151">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="24964-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="24964-152">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="24964-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
