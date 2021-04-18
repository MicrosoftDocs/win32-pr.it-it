---
description: Voci del registro di sistema Encoder-Specific
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Voci del registro di sistema Encoder-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314474"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="00bad-103">Voci del registro di sistema Encoder-Specific</span><span class="sxs-lookup"><span data-stu-id="00bad-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="00bad-104">Oltre alle voci elencate in precedenza per il codificatore, è inoltre necessario registrare il codificatore nella categoria dei codificatori Windows Imaging Component (WIC), in modo che il motore di individuazione possa trovarlo.</span><span class="sxs-lookup"><span data-stu-id="00bad-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="00bad-105">A tale scopo, effettuare le seguenti voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="00bad-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="00bad-106">Il primo GUID nelle voci seguenti è l'identificatore di categoria (CATId) per WICBitmapEncoders.</span><span class="sxs-lookup"><span data-stu-id="00bad-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="00bad-107">Registrazione di un formato contenitore con writer di metadati</span><span class="sxs-lookup"><span data-stu-id="00bad-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="00bad-108">Se si crea un nuovo formato del contenitore per il codec, è necessario creare anche le voci del registro di sistema per supportare i writer di metadati per i blocchi di metadati nelle immagini.</span><span class="sxs-lookup"><span data-stu-id="00bad-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="00bad-109">È necessario creare le voci seguenti nell'identificatore di classe (CLSID) del writer di metadati per ogni formato di metadati supportato nel formato del contenitore.</span><span class="sxs-lookup"><span data-stu-id="00bad-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="00bad-110">Se il codec usa un contenitore Tagged Image File Format (TIFF), queste informazioni sono già presenti nel registro di sistema e non è necessario creare queste voci.</span><span class="sxs-lookup"><span data-stu-id="00bad-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="00bad-111">Se si usa un formato di contenitore di tipo TIFF o JPEG, è necessario registrare un'associazione tra il contenitore e il formato del contenitore.</span><span class="sxs-lookup"><span data-stu-id="00bad-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="00bad-112">Per ulteriori informazioni, vedere l'introduzione all' [integrazione con la raccolta foto di Windows e Esplora risorse](-wic-integrationregentries.md).</span><span class="sxs-lookup"><span data-stu-id="00bad-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00bad-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00bad-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="00bad-114">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="00bad-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00bad-115">Voci generali del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="00bad-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="00bad-116">Voci del registro di sistema specifiche del codificatore</span><span class="sxs-lookup"><span data-stu-id="00bad-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="00bad-117">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="00bad-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="00bad-118">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="00bad-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



