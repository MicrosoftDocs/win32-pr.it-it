---
title: Guida ai metafile di Windows Media
description: Guida ai metafile di Windows Media
ms.assetid: d2360a63-f073-44b0-8637-1f22b577f51a
keywords:
- Metafile di Windows Media, informazioni
- Windows Media Player, metafile
- Windows Media Player, metafile di Windows Media
- Metafile, informazioni
- Windows Media, metafile
- Playlist Windows Media Metafile, informazioni
- playlist, informazioni
- playlist di metafile, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcf0a4c98ae49d1cdf3b7e36e8a278f184cd4632
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955780"
---
# <a name="windows-media-metafile-guide"></a><span data-ttu-id="ee9d7-111">Guida ai metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="ee9d7-111">Windows Media Metafile Guide</span></span>

<span data-ttu-id="ee9d7-112">Un metafile di Windows Media può essere semplice o complesso quanto necessario.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-112">A Windows Media metafile can be as simple or complex as you need it to be.</span></span> <span data-ttu-id="ee9d7-113">Il metafile Windows Media più semplice contiene solo il Uniform Resource Locator (URL) di alcuni contenuti multimediali in un server.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-113">The most basic Windows Media metafile contains only the Uniform Resource Locator (URL) of some multimedia content on a server.</span></span> <span data-ttu-id="ee9d7-114">Il client, Windows Media Player, analizza queste informazioni e quindi apre il file multimediale o il flusso definito in Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-114">The client, Windows Media Player, parses this information and then opens the media file or stream defined in the Windows Media metafile.</span></span> <span data-ttu-id="ee9d7-115">Un metafile complesso può contenere più file o flussi disposti in una playlist, istruzioni su come riprodurre file o flussi, testo e elementi grafici come titolo, autore e testo del copyright, inserimento di annunci personalizzati in un flusso Live, collegamenti ipertestuali associati a elementi nell'interfaccia Media Player di Windows e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-115">A complex metafile can contain multiple files or streams arranged in a playlist, instructions on how to play the files or streams, text and graphic elements such as title, author, and copyright text, personalized ad insertion into a live stream, hyperlinks associated with elements on the Windows Media Player interface, and more.</span></span>

<span data-ttu-id="ee9d7-116">Nelle sezioni seguenti vengono fornite informazioni dettagliate su come creare e utilizzare le playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-116">The following sections provide detailed information on how to create and use Windows Media metafile playlists.</span></span>



| <span data-ttu-id="ee9d7-117">Sezione</span><span class="sxs-lookup"><span data-stu-id="ee9d7-117">Section</span></span>                                                            | <span data-ttu-id="ee9d7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee9d7-118">Description</span></span>                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee9d7-119">Tipi di playlist</span><span class="sxs-lookup"><span data-stu-id="ee9d7-119">Types of Playlists</span></span>](types-of-playlists.md)                       | <span data-ttu-id="ee9d7-120">Elenca le estensioni di file disponibili.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-120">Lists available file name extensions.</span></span>                                               |
| [<span data-ttu-id="ee9d7-121">Creazione di playlist di metafile</span><span class="sxs-lookup"><span data-stu-id="ee9d7-121">Creating Metafile Playlists</span></span>](creating-metafile-playlists.md)     | <span data-ttu-id="ee9d7-122">Viene descritto come creare playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-122">Describes how to create Windows Media metafile playlists.</span></span>                           |
| [<span data-ttu-id="ee9d7-123">Playlist di metafile</span><span class="sxs-lookup"><span data-stu-id="ee9d7-123">Metafile Playlists</span></span>](metafile-playlists.md)                       | <span data-ttu-id="ee9d7-124">Descrive l'utilizzo, la creazione di script, i metadati e l'elaborazione della playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-124">Describes metafile playlist usage, scripting, metadata, and processing.</span></span>             |
| [<span data-ttu-id="ee9d7-125">Linee guida sull'estensione metafile</span><span class="sxs-lookup"><span data-stu-id="ee9d7-125">Metafile Extension Guidelines</span></span>](metafile-extension-guidelines.md) | <span data-ttu-id="ee9d7-126">Descrive l'uso preferito delle estensioni di file per i file multimediali di streaming.</span><span class="sxs-lookup"><span data-stu-id="ee9d7-126">Describes the preferred use of file name extensions for streaming media files.</span></span>      |
| [<span data-ttu-id="ee9d7-127">Ordine di precedenza</span><span class="sxs-lookup"><span data-stu-id="ee9d7-127">Order of Precedence</span></span>](order-of-precedence.md)                     | <span data-ttu-id="ee9d7-128">Descrive in che modo gli elementi della playlist di metafile eseguono l'override di altri elementi della playlist</span><span class="sxs-lookup"><span data-stu-id="ee9d7-128">Describes how metafile playlist elements override other metafile playlist elements.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ee9d7-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee9d7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee9d7-130">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ee9d7-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ee9d7-131">**Metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ee9d7-131">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




