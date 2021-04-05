---
title: Uso delle playlist di metafile
description: Uso delle playlist di metafile
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
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
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855674"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="d5cb3-106">Uso delle playlist di metafile</span><span class="sxs-lookup"><span data-stu-id="d5cb3-106">Using Metafile Playlists</span></span>

<span data-ttu-id="d5cb3-107">Le playlist specificano il modo in cui verranno riprodotti i supporti di streaming o i file multimediali e i metadati che verranno visualizzati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="d5cb3-108">In questa sezione vengono illustrati i diversi modi in cui è possibile utilizzare le playlist.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="d5cb3-109">La sezione è divisa negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="d5cb3-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="d5cb3-110">Topic</span></span>                                                                                              | <span data-ttu-id="d5cb3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5cb3-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5cb3-112">Modifica della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="d5cb3-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="d5cb3-113">Aggiunta di testo, collegamenti e immagini.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="d5cb3-114">Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="d5cb3-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="d5cb3-115">Uso delle playlist per reindirizzare il browser a Windows Media Player e specificare l'URL di un flusso o di un file multimediale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="d5cb3-116">Accesso ai supporti</span><span class="sxs-lookup"><span data-stu-id="d5cb3-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="d5cb3-117">Uso di elementi metafile e dei rispettivi elementi figlio per specificare il contenuto a cui accedere e l'ordine e la durata della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="d5cb3-118">Uso del cambio di flusso di eventi Live</span><span class="sxs-lookup"><span data-stu-id="d5cb3-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="d5cb3-119">Uso dell'elemento **Event** per specificare un flusso multimediale a cui accedere e quindi riprendere la riproduzione del flusso originale.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="d5cb3-120">Utilizzato per l'inserimento di annunci.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="d5cb3-121">Uso dei metafile per un cambio di flusso trasparente</span><span class="sxs-lookup"><span data-stu-id="d5cb3-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="d5cb3-122">Uso dell'elemento **Event** per precaricare il successivo flusso multimediale a cui accedere per evitare gap nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="d5cb3-123">Uso degli annunci</span><span class="sxs-lookup"><span data-stu-id="d5cb3-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="d5cb3-124">Utilizzo di un metafile per fornire informazioni sull'URL per un flusso multimediale, inclusi l'indirizzo IP multicast, la porta, il formato del flusso e altre impostazioni della stazione.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="d5cb3-125">Uso dell'URL e del rollover del server</span><span class="sxs-lookup"><span data-stu-id="d5cb3-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="d5cb3-126">Uso delle playlist di metafile per fornire un metodo per il rollover automatico a origini di contenuto alternative quando non è possibile accedere o riprodurre un flusso.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="d5cb3-127">Uso di parametri e comandi personalizzati</span><span class="sxs-lookup"><span data-stu-id="d5cb3-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="d5cb3-128">Utilizzo dell'elemento **param** per definire elementi personalizzati per fornire metadati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="d5cb3-129">Personalizzazione del recapito multimediale</span><span class="sxs-lookup"><span data-stu-id="d5cb3-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="d5cb3-130">Uso delle preferenze utente per determinare il contenuto broadcast.</span><span class="sxs-lookup"><span data-stu-id="d5cb3-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="d5cb3-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5cb3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5cb3-132">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="d5cb3-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="d5cb3-133">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d5cb3-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d5cb3-134">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d5cb3-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




