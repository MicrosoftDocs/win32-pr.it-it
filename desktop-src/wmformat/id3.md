---
title: Supporto ID3
description: ID3 è un'organizzazione che ha definito un set di standard per l'inclusione dei metadati nei file audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK, supporto ID3
- ASF (Advanced Systems Format), supporto ID3
- ASF (Advanced Systems Format), supporto ID3
- metadati, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713369"
---
# <a name="id3-support"></a><span data-ttu-id="00e97-108">Supporto ID3</span><span class="sxs-lookup"><span data-stu-id="00e97-108">ID3 Support</span></span>

<span data-ttu-id="00e97-109">ID3 è un'organizzazione che ha definito un set di standard per l'inclusione dei metadati nei file audio MPEG Layer-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="00e97-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="00e97-110">Gli oggetti di Windows Media Format SDK forniscono supporto per gli attributi compatibili con ID3.</span><span class="sxs-lookup"><span data-stu-id="00e97-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="00e97-111">Sono supportate tre diverse versioni ID3: ID3v1. x, ID3v 2.2 e ID3v 2.3/v2, 4.</span><span class="sxs-lookup"><span data-stu-id="00e97-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="00e97-112">Per un elenco degli attributi che corrispondono ai frame ID3, vedere Supporto di [tag ID3](id3-tag-support.md).</span><span class="sxs-lookup"><span data-stu-id="00e97-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="00e97-113">Se non specificato diversamente, non viene eseguita alcuna convalida dei dati del frame ID3 da parte degli oggetti di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="00e97-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="00e97-114">Ad esempio, l'attributo dei metadati [**WM/lyrics \_ sincronizzato**](wm-lyrics-synchronised.md) archivia i lyrics del brano con i timestamp corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="00e97-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="00e97-115">Quando si scrive un attributo di tipo **WM/lyrics \_ sincronizzato** , gli oggetti di questo SDK non verificheranno che i timestamp siano in ordine cronologico o eseguano la convalida di qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="00e97-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00e97-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00e97-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00e97-117">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="00e97-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="00e97-118">**Funzionalità dei metadati**</span><span class="sxs-lookup"><span data-stu-id="00e97-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="00e97-119">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="00e97-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




