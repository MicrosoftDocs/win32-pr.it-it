---
title: Uso di una playlist metafile
description: Uso di una playlist metafile
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Playlist Windows Media Metafile, uso
- playlist di metafile, uso
- playlist, uso
- Playlist Windows Media Metafile, informazioni
- playlist di metafile, informazioni
- playlist, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709850"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="90ad7-109">Uso di una playlist metafile</span><span class="sxs-lookup"><span data-stu-id="90ad7-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="90ad7-110">Dal momento che non è possibile collegarsi direttamente da una pagina Web a un server di flussi multimediali, si usano le playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="90ad7-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="90ad7-111">Le playlist di metafile contengono le informazioni necessarie per Windows Media Player e vengono archiviate in un server Web.</span><span class="sxs-lookup"><span data-stu-id="90ad7-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="90ad7-112">È quindi possibile eseguire il collegamento dal documento Web a una playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="90ad7-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="90ad7-113">Quando viene aperta una playlist di metafile, il controllo viene trasferito a Windows Media Player, che elabora il file, si connette al server multimediale di streaming e riproduce il contenuto specificato.</span><span class="sxs-lookup"><span data-stu-id="90ad7-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="90ad7-114">Il browser scarica prima di tutto la playlist metafile nella directory della cache dell'utente.</span><span class="sxs-lookup"><span data-stu-id="90ad7-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="90ad7-115">Poiché la playlist del metafile è piccola, si tratta di un passaggio molto rapido.</span><span class="sxs-lookup"><span data-stu-id="90ad7-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="90ad7-116">Il computer dell'utente trova quindi nella tabella delle associazioni di file l'associazione della playlist del metafile con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="90ad7-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="90ad7-117">Windows Media Player apre e interpreta lo scripting nella playlist del metafile, che contiene, tra le altre cose, l'URL del contenuto di streaming.</span><span class="sxs-lookup"><span data-stu-id="90ad7-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="90ad7-118">Windows Media Player usa l'URL per individuare il contenuto e avviare il flusso.</span><span class="sxs-lookup"><span data-stu-id="90ad7-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="90ad7-119">Lo script di playlist di metafile controlla quindi l'esperienza di streaming.</span><span class="sxs-lookup"><span data-stu-id="90ad7-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="90ad7-120">Poiché le playlist di metafile funzionano tramite un'applicazione helper associata al tipo ASXMIME (Application/Mplayer2 o video/x-ms-asf), sono compatibili con qualsiasi browser che supporta le applicazioni helper.</span><span class="sxs-lookup"><span data-stu-id="90ad7-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="90ad7-121">Gli esempi illustrati in questo documento funzioneranno con Microsoft Internet Explorer 4,0 e versioni successive e con Netscape Navigator 4,0 e versioni successive in Microsoft Win32® e le piattaforme Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="90ad7-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="90ad7-122">In tutti gli esempi, sarà necessario assicurarsi che i file multimediali digitali a cui si fa riferimento abbiano percorsi e nomi file validi per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="90ad7-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90ad7-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90ad7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ad7-124">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="90ad7-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="90ad7-125">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="90ad7-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="90ad7-126">**Cenni preliminari sui file di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="90ad7-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




