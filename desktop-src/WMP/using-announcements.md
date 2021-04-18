---
title: Uso degli annunci
description: Uso degli annunci
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Playlist Windows Media Metafile, annunci
- playlist, annunci
- playlist di metafile, annunci
- Windows Media Player, annunci
- annunci
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298085"
---
# <a name="using-announcements"></a><span data-ttu-id="431ef-108">Uso degli annunci</span><span class="sxs-lookup"><span data-stu-id="431ef-108">Using Announcements</span></span>

<span data-ttu-id="431ef-109">Un annuncio è un file che contiene informazioni sull'URL per un flusso multimediale, tra cui l'indirizzo IP multicast, la porta, il formato del flusso e altre impostazioni della stazione.</span><span class="sxs-lookup"><span data-stu-id="431ef-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="431ef-110">Gli annunci vengono creati da amministratore di Windows Media quando viene creato un flusso di pubblicazione unicast o multicast.</span><span class="sxs-lookup"><span data-stu-id="431ef-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="431ef-111">Il client può caricare rapidamente il file di annuncio, quindi procedere con l'accesso al file multimediale di streaming.</span><span class="sxs-lookup"><span data-stu-id="431ef-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="431ef-112">Per un punto di pubblicazione unicast, viene aperto il flusso multimediale del punto di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="431ef-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="431ef-113">Per un punto di pubblicazione multicast, l'URL viene Estratto da un file della stazione di trasmissione con estensione NSC e viene eseguito l'accesso al supporto di streaming.</span><span class="sxs-lookup"><span data-stu-id="431ef-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="431ef-114">A differenza di un flusso unicast, nessuna informazione di intestazione è contenuta in un flusso multicast.</span><span class="sxs-lookup"><span data-stu-id="431ef-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="431ef-115">Tali informazioni provengono dal file della stazione di trasmissione con estensione NSC.</span><span class="sxs-lookup"><span data-stu-id="431ef-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="431ef-116">Windows Media Player in genere apre prima di tutto un file di annuncio, ovvero un uso per le playlist di metafile, che punta al percorso del file della stazione di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="431ef-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="431ef-117">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="431ef-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="431ef-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="431ef-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431ef-119">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="431ef-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="431ef-120">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="431ef-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




