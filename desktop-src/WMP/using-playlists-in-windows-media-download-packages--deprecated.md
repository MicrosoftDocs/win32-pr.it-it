---
title: Uso delle playlist nei pacchetti di download di Windows Media (deprecato)
description: Uso delle playlist nei pacchetti di download di Windows Media (deprecato)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- playlist, pacchetti di download di Windows Media
- playlist di metafile, pacchetti di download di Windows Media
- Playlist Windows Media Metafile, pacchetti di download di Windows Media
- Pacchetti di download di Windows Media, playlist
- Pacchetti di download di Windows Media, playlist di metafile
- Pacchetti di download di Windows Media, playlist metafile di Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396499"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="fe3a3-113">Uso delle playlist nei pacchetti di download di Windows Media (deprecato)</span><span class="sxs-lookup"><span data-stu-id="fe3a3-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="fe3a3-114">Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="fe3a3-115">Le playlist sono metafile Windows Media con estensione asx che forniscono informazioni che indicano a Windows Media Player come riprodurre il contenuto in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="fe3a3-116">Combinando più file di contenuto in un singolo pacchetto di download di Windows Media, è possibile controllare e personalizzare il pacchetto di download di Windows Media usando la playlist.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="fe3a3-117">In generale, le playlist di metafile vengono usate dai pacchetti di download di Windows Media per fare riferimento al contenuto multimediale nel pacchetto piuttosto che a un flusso da un server in una rete Intranet o Internet.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="fe3a3-118">Tuttavia, i riferimenti URL all'interno del file con estensione asx sono supportati.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="fe3a3-119">Utilizzando XML, il metafile fornisce le informazioni utilizzate da Windows Media Player per riprodurre e visualizzare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="fe3a3-120">Le playlist sono costituite da vari elementi di codice XML con i tag e gli attributi associati.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="fe3a3-121">Ogni elemento in una playlist Windows Media Metafile definisce una particolare impostazione o azione in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="fe3a3-122">Il computer dell'utente associa un metafile di Windows Media con estensione di file ASX con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="fe3a3-123">Windows Media Player apre e analizza il codice XML nel metafile, che contiene il percorso per individuare i file audio o video in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="fe3a3-124">Lo script di metafile controlla quindi l'esperienza audio, video e grafica.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="fe3a3-125">Il metafile contiene anche informazioni elaborate e visualizzate da Windows Media Player nella casella di riepilogo a discesa della playlist.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="fe3a3-126">Immediatamente dopo la visualizzazione dell'elenco, viene riprodotto il primo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="fe3a3-127">Una playlist di metafile è un collegamento ai file che contengono il contenuto incluso nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="fe3a3-128">Il codice seguente è un esempio di un metafile che specifica il bordo da visualizzare usando l'elemento **Skin** , due canzoni da riprodurre e le informazioni della playlist per ogni brano.</span><span class="sxs-lookup"><span data-stu-id="fe3a3-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="fe3a3-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe3a3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe3a3-130">**Bordi per Windows Media Player (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="fe3a3-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="fe3a3-131">**Pacchetti di download di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="fe3a3-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="fe3a3-132">**Metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fe3a3-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




