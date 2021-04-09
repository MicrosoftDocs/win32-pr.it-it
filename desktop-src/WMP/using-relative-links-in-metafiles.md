---
title: Uso di collegamenti relativi nei metafile
description: Uso di collegamenti relativi nei metafile
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Playlist Windows Media Metafile, collegamenti relativi
- playlist, collegamenti relativi
- playlist di metafile, collegamenti relativi
- Metafile, collegamenti relativi
- Metafile di Windows Media, collegamenti relativi
- collegamenti relativi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855842"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="a7ab0-109">Uso di collegamenti relativi nei metafile</span><span class="sxs-lookup"><span data-stu-id="a7ab0-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="a7ab0-110">I collegamenti relativi sono una funzionalità completamente supportata dei file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="a7ab0-111">È possibile usare collegamenti relativi nei metafile in modo analogo a come vengono usati nei documenti HTML.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="a7ab0-112">L'utilizzo di collegamenti relativi consente di creare metafile portabili, ovvero è possibile copiare o spostare un'intera struttura di directory in un altro server senza aggiornare i percorsi a file grafici utilizzati come banner o gli attributi **href** degli elementi **moreinfo** (se fanno riferimento a file nello stesso server Web del metafile archiviato).</span><span class="sxs-lookup"><span data-stu-id="a7ab0-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="a7ab0-113">I collegamenti relativi funzionano in qualsiasi applicazione che li supporta, perché le parti dell'URL non incluse nell'attributo **href** di un elemento sono incluse nell'URL inviato dall'applicazione al server quando viene richiesto l'URL.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="a7ab0-114">Ciò significa che il protocollo (ad esempio https://), il nome del server e la directory virtuale in cui si trova il file contenente il collegamento relativo sono tutti inclusi nell'URL inviato al server.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="a7ab0-115">Se il file multimediale o l'URL a cui si collega il collegamento utilizzando un collegamento relativo non si trova nello stesso server del metafile, il collegamento relativo non è valido.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="a7ab0-116">Queste informazioni sui collegamenti relativi sono corrette solo quando si usa un collegamento ai metafile aperti nel Media Player Windows autonomo.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="a7ab0-117">Quando si usa il controllo Media Player Windows incorporato, tutti i collegamenti sono relativi alla pagina in cui è ospitato il controllo, a meno che l'elemento figlio di **base** dell'elemento **ASX** non venga usato per reindirizzare il percorso relativo.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="a7ab0-118">Tutti i collegamenti relativi nel metafile devono essere completamente relativi, non relativi all'unità, per i flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="a7ab0-119">Quando un URL inizia con un \\ carattere "", il collegamento è relativo all'unità.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="a7ab0-120">Windows Media Player tenta di aprire il file collegato all'unità in cui è stato aperto il metafile, in genere un server Web.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="a7ab0-121">Poiché i server Web utilizzano le directory virtuali, Windows Media Player tenta di trovare il flusso o il file multimediale specificato in una sottodirectory di una directory virtuale nel server Web da cui è stato aperto il metafile.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="a7ab0-122">Un utente non può accedere a una directory del server.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="a7ab0-123">Nell'esempio riportato in questa sezione viene illustrato l'utilizzo di un collegamento completamente relativo.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="a7ab0-124">È possibile utilizzare i collegamenti relativi alle unità quando si utilizzano metafile in un singolo computer in cui sono presenti tutti i file multimediali collegati alla playlist del metafile in un dispositivo di archiviazione del computer.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="a7ab0-125">Tuttavia, non è possibile eseguire lo streaming di file multimediali in questo modo.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="a7ab0-126">Quando si usa un collegamento a un altro metafile per consentire i collegamenti relativi, il nome visualizzato come titolo di Windows Media Player è il titolo del metafile originale.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="a7ab0-127">Non è possibile usare collegamenti relativi per gli URL di un server dei flussi multimediali perché vengono usati protocolli diversi per accedere al contenuto dei flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="a7ab0-128">Nella playlist di esempio seguente, il primo **ENTRYREF** contiene un URL per un'altra playlist, relativa. Wax.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="a7ab0-129">L'esempio seguente è il file relativo. Wax, che contiene collegamenti relativi.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="a7ab0-130">L'URL che contiene il riferimento alla playlist, relativa. Wax, può esistere in una playlist di metafile ovunque sia accessibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="a7ab0-131">Affinché l'URL venga elaborato correttamente, deve essere presente un server Web denominato "example.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="a7ab0-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="a7ab0-132">Il server Web deve avere una directory virtuale definita come "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="a7ab0-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="a7ab0-133">La playlist a cui si fa riferimento, relativa. Wax, deve esistere nel server Web denominato "example.microsoft.com" nella directory virtuale "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="a7ab0-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="a7ab0-134">Per poter accedere e riprodurre correttamente i file multimediali a cui viene fatto riferimento nella playlist relativa. Wax, è necessario che sia presente una directory denominata "graphics", che è una sottodirectory della directory virtuale del server "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="a7ab0-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="a7ab0-135">Il file di grafica Logo1.jpg, a cui si fa riferimento nell'elemento **banner** , deve essere la sottodirectory denominata graphics.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="a7ab0-136">Analogamente, un documento denominato Category1.htm deve trovarsi in una sottodirectory denominata Categoria1.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="a7ab0-137">La directory denominata Categoria1 deve esistere come sottodirectory della directory virtuale "Metafiles" sul server Web example.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a7ab0-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7ab0-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7ab0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ab0-139">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="a7ab0-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a7ab0-140">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="a7ab0-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a7ab0-141">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a7ab0-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a7ab0-142">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a7ab0-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




