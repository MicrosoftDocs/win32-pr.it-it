---
title: Uso dell'URL e del rollover del server
description: Uso dell'URL e del rollover del server
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Playlist Windows Media Metafile, rollover URL
- playlist, rollover degli URL
- playlist di metafile, rollover degli URL
- Playlist Windows Media Metafile, rollover server
- playlist, rollover del server
- playlist di metafile, rollover del server
- Playlist Windows Media Metafile, rollover di protocollo
- playlist, rollover dei protocolli
- playlist di metafile, rollover di protocollo
- Media Player di Windows, rollover degli URL
- Windows Media Player, rollover del server
- Windows Media Player, rollover dei protocolli
- Rollover degli URL
- rollover del server
- rollover del protocollo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330255"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="fa157-118">Uso dell'URL e del rollover del server</span><span class="sxs-lookup"><span data-stu-id="fa157-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="fa157-119">È possibile usare le playlist di metafile per fornire un mezzo per il rollover automatico a origini di contenuto alternative quando non è possibile accedere o riprodurre un flusso.</span><span class="sxs-lookup"><span data-stu-id="fa157-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="fa157-120">È possibile utilizzare questo metodo di rollover per specificare le origini dello stesso contenuto in server diversi o in tipi diversi di server.</span><span class="sxs-lookup"><span data-stu-id="fa157-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="fa157-121">È possibile, ad esempio, specificare una prima alternativa in un server Windows Media diverso.</span><span class="sxs-lookup"><span data-stu-id="fa157-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="fa157-122">Se il contenuto non viene riprodotto, il client può eseguire il rollback a una seconda alternativa in un server Web.</span><span class="sxs-lookup"><span data-stu-id="fa157-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="fa157-123">Windows Media Player tenta automaticamente di eseguire il rollback a protocolli diversi in base alle impostazioni delle proprietà di Windows Media prima di provare gli URL di rollover nella playlist.</span><span class="sxs-lookup"><span data-stu-id="fa157-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="fa157-124">Impostare il rollover del server e del protocollo inserendo più elementi **ref** in successione all'interno di un elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="fa157-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="fa157-125">Ogni elemento **ref** specifica un percorso o un protocollo alternativo per un file multimediale o un flusso.</span><span class="sxs-lookup"><span data-stu-id="fa157-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="fa157-126">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="fa157-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="fa157-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa157-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa157-128">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="fa157-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="fa157-129">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="fa157-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




