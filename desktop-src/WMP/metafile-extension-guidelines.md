---
title: Linee guida sull'estensione metafile
description: Linee guida sull'estensione metafile
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Metafile di Windows Media, estensioni
- Metafile di Windows Media, estensioni di file
- Metafile, estensioni
- Metafile, estensioni di file
- Windows Media, metafile
- estensioni dei nomi di file per i file multimediali di Windows
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045288"
---
# <a name="metafile-extension-guidelines"></a><span data-ttu-id="fd2ea-109">Linee guida sull'estensione metafile</span><span class="sxs-lookup"><span data-stu-id="fd2ea-109">Metafile Extension Guidelines</span></span>

<span data-ttu-id="fd2ea-110">Un'estensione di file fornisce un fornitore di software indipendente (ISV) con informazioni sui requisiti di rendering di un'applicazione che usa l'estensione e consente agli autori di contenuti di specificare come destinazione i tipi di giocatori generali.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-110">A file name extension provides an independent software vendor (ISV) with information about the rendering requirements of an application that uses the extension, and enables content authors to target general types of players.</span></span>

<span data-ttu-id="fd2ea-111">Le estensioni del nome Metafile di Windows Media vengono usate per identificare il formato dei file di Windows Media a cui fa riferimento un metafile.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-111">Windows Media metafile name extensions are used to identify the format of the Windows Media files that a metafile references.</span></span> <span data-ttu-id="fd2ea-112">I metafile di Windows Media con estensione Wax, wvx o ASX fanno riferimento rispettivamente ai file con estensione WMA, WMV e ASF.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-112">Windows Media metafiles with .wax, .wvx, or .asx extensions reference files with .wma, .wmv, and .asf extensions, respectively.</span></span> <span data-ttu-id="fd2ea-113">Tutti i metafile, indipendentemente dall'estensione del nome di file usato, hanno il tag dell'elemento **ASX** all'inizio del file con l'attributo **Version** specificato.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-113">All metafiles, regardless of the file name extension used, have the **ASX** element tag at the beginning of the file with the **version** attribute specified.</span></span>

<span data-ttu-id="fd2ea-114">La tabella seguente illustra i tipi di file multimediali a cui fa riferimento ogni tipo di estensione del nome di file del metafile.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-114">The following table shows the media file types referenced by each type of metafile file name extension.</span></span> <span data-ttu-id="fd2ea-115">Le colonne elencano le estensioni dei file multimediali, ovvero le estensioni dell'elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-115">The columns list media file name extensions, the rows list metafile name extensions.</span></span> <span data-ttu-id="fd2ea-116">Una X in una colonna indica un tipo di file multimediale a cui è possibile fare riferimento da una particolare estensione del nome di file Metafile.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-116">An X in a column indicates a media file type that can be referenced by a particular metafile file name extension.</span></span>



| <span data-ttu-id="fd2ea-117">Estensione</span><span class="sxs-lookup"><span data-stu-id="fd2ea-117">Extension</span></span> | <span data-ttu-id="fd2ea-118">.asf</span><span class="sxs-lookup"><span data-stu-id="fd2ea-118">.asf</span></span> | <span data-ttu-id="fd2ea-119">wma</span><span class="sxs-lookup"><span data-stu-id="fd2ea-119">.wma</span></span> | <span data-ttu-id="fd2ea-120">wmv</span><span class="sxs-lookup"><span data-stu-id="fd2ea-120">.wmv</span></span> |
|-----------|------|------|------|
| <span data-ttu-id="fd2ea-121">. wvx</span><span class="sxs-lookup"><span data-stu-id="fd2ea-121">.wvx</span></span>      | <span data-ttu-id="fd2ea-122">X</span><span class="sxs-lookup"><span data-stu-id="fd2ea-122">X</span></span>    | <span data-ttu-id="fd2ea-123">X</span><span class="sxs-lookup"><span data-stu-id="fd2ea-123">X</span></span>    | <span data-ttu-id="fd2ea-124">X</span><span class="sxs-lookup"><span data-stu-id="fd2ea-124">X</span></span>    |
| <span data-ttu-id="fd2ea-125">. Wax</span><span class="sxs-lookup"><span data-stu-id="fd2ea-125">.wax</span></span>      | <span data-ttu-id="fd2ea-126">X</span><span class="sxs-lookup"><span data-stu-id="fd2ea-126">X</span></span>    | <span data-ttu-id="fd2ea-127">X</span><span class="sxs-lookup"><span data-stu-id="fd2ea-127">X</span></span>    |      |
| <span data-ttu-id="fd2ea-128">.asx</span><span class="sxs-lookup"><span data-stu-id="fd2ea-128">.asx</span></span>      | <span data-ttu-id="fd2ea-129">X</span><span class="sxs-lookup"><span data-stu-id="fd2ea-129">X</span></span>    |      |      |



 

## <a name="related-topics"></a><span data-ttu-id="fd2ea-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd2ea-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd2ea-131">**Estensioni di file**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-131">**File Name Extensions**</span></span>](file-name-extensions.md)
</dt> <dt>

[<span data-ttu-id="fd2ea-132">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="fd2ea-133">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-133">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




