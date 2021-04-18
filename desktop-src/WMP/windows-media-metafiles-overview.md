---
title: Cenni preliminari sui file di Windows Media
description: Cenni preliminari sui file di Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Metafile di Windows Media, informazioni
- Windows Media Player, metafile
- Windows Media Player, metafile di Windows Media
- Metafile, informazioni
- Windows Media, metafile
- Playlist Windows Media Metafile, informazioni
- playlist, informazioni
- Metafile di Windows Media, sintassi
- Metafile, sintassi
- playlist di metafile, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298211"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="f8305-113">Cenni preliminari sui file di Windows Media</span><span class="sxs-lookup"><span data-stu-id="f8305-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="f8305-114">La parte più importante della corretta utilizzo di metafile Windows Media consiste nell'utilizzare la sintassi corretta per gli elementi del metafile.</span><span class="sxs-lookup"><span data-stu-id="f8305-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="f8305-115">Gli errori di sintassi in un metafile di Windows Media possono causare qualsiasi operazione da un singolo attributo che viene trascurato, in modo che il metafile non venga riconosciuto come valido e non riesca a funzionare.</span><span class="sxs-lookup"><span data-stu-id="f8305-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="f8305-116">È altrettanto importante l'ordine in cui gli elementi vengono visualizzati in un metafile di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f8305-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="f8305-117">Gli attributi di alcuni elementi eseguono temporaneamente l'override degli attributi di elementi simili in sezioni diverse del metafile.</span><span class="sxs-lookup"><span data-stu-id="f8305-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="f8305-118">Esiste un [ordine di precedenza](order-of-precedence.md)definito.</span><span class="sxs-lookup"><span data-stu-id="f8305-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="f8305-119">Le playlist Windows Media metafile sono metafile di Windows Media che forniscono informazioni utilizzate da Windows Media Player per ricevere flussi unicast, flussi multicast e altri supporti supportati da una rete Intranet o Internet.</span><span class="sxs-lookup"><span data-stu-id="f8305-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="f8305-120">Una playlist di metafile è fondamentalmente un collegamento al contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="f8305-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="f8305-121">Una playlist di metafile può essere inviata come messaggio di posta elettronica, usata come riferimento al collegamento in una pagina Web, creata dinamicamente tramite Active Server Pages (ASP) o esistere come file autonomo in un'unità disco locale.</span><span class="sxs-lookup"><span data-stu-id="f8305-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="f8305-122">Una playlist di metafile può fare riferimento a un'altra playlist di metafile, a una pagina ASP o a un file di Windows Media Station (con estensione di file NSC).</span><span class="sxs-lookup"><span data-stu-id="f8305-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="f8305-123">Un file con estensione NSC viene usato per definire un Windows Media Station per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f8305-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="f8305-124">Il processo di gestione di base è lo stesso per ogni caso.</span><span class="sxs-lookup"><span data-stu-id="f8305-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8305-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8305-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8305-126">**Informazioni sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f8305-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




