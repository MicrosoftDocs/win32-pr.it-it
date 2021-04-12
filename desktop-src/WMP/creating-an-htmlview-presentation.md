---
title: Creazione di una presentazione HTMLView
description: Creazione di una presentazione HTMLView
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Playlist Windows Media Metafile, presentazioni HTMLView
- playlist, presentazioni HTMLView
- playlist di metafile, presentazioni HTMLView
- Playlist Windows Media Metafile, creazione di presentazioni HTMLView
- playlist, creazione di presentazioni HTMLView
- playlist di metafile, creazione di presentazioni HTMLView
- creazione di presentazioni HTMLView
- Windows Media Player, creazione di presentazioni HTMLView
- Windows Media Player, presentazioni HTMLView
- HTMLView, creazione di presentazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396294"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="99a06-113">Creazione di una presentazione HTMLView</span><span class="sxs-lookup"><span data-stu-id="99a06-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="99a06-114">Per creare una presentazione HTMLView di base, sono necessari almeno tre elementi:</span><span class="sxs-lookup"><span data-stu-id="99a06-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="99a06-115">**Contenuto multimediale digitale.**</span><span class="sxs-lookup"><span data-stu-id="99a06-115">**Digital media content.**</span></span> <span data-ttu-id="99a06-116">Si tratta di uno o più file audio o video riprodotti da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="99a06-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="99a06-117">**Una pagina Web.**</span><span class="sxs-lookup"><span data-stu-id="99a06-117">**A webpage.**</span></span> <span data-ttu-id="99a06-118">Si tratta del contenuto basato sul Web che viene visualizzato nella funzionalità **Now Play** dell'interfaccia utente del lettore.</span><span class="sxs-lookup"><span data-stu-id="99a06-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="99a06-119">**Metafile di Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="99a06-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="99a06-120">Si tratta della playlist di metafile che indica a Windows Media Player di combinare il contenuto multimediale digitale con la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="99a06-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="99a06-121">Un file con estensione asx è un file di testo che fornisce informazioni su un flusso di file e la relativa presentazione.</span><span class="sxs-lookup"><span data-stu-id="99a06-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="99a06-122">In base alla sintassi Extensible Markup Language (XML), i file con estensione ASX possono contenere diversi elementi, ciascuno identificato da un tag con attributi associati.</span><span class="sxs-lookup"><span data-stu-id="99a06-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="99a06-123">L'elemento **param** fornisce un modo per associare un parametro personalizzato a una voce specifica in una playlist di metafile o all'intero metafile.</span><span class="sxs-lookup"><span data-stu-id="99a06-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="99a06-124">Uno dei nomi di parametro predefiniti disponibili per l'utilizzo è "HTMLView".</span><span class="sxs-lookup"><span data-stu-id="99a06-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="99a06-125">Si tratta del parametro che determina la visualizzazione della pagina Web specificata dal valore URL in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="99a06-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="99a06-126">Il codice di esempio seguente mostra un file con estensione asx che combina un singolo file multimediale digitale con una singola pagina Web:</span><span class="sxs-lookup"><span data-stu-id="99a06-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="99a06-127">Quando in Windows Media Player viene aperto il file con estensione asx nell'esempio precedente, l'audio viene riprodotto dal file denominato Content1. WMA e viene visualizzata la pagina Web denominata htmlview.htm nella funzionalità **ora di riproduzione** del lettore in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="99a06-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="99a06-128">L'utente può sospendere, cercare e arrestare il contenuto audio usando i controlli Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="99a06-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="99a06-129">È possibile modificare facilmente la pagina Web visualizzata per ogni parte del contenuto associando un elemento **param** a ogni voce, come illustrato nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="99a06-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="99a06-130">Nell'esempio precedente, Windows Media Player Visualizza prima di tutto la pagina Web htmlview1.htm durante la riproduzione del file audio digitale Content1. WMA.</span><span class="sxs-lookup"><span data-stu-id="99a06-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="99a06-131">Quando il giocatore apre la voce successiva nella playlist, Content2. WMA, la pagina Web visualizzata in **Now Playing** changes to htmlview2.htm.</span><span class="sxs-lookup"><span data-stu-id="99a06-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="99a06-132">In questo modo, è possibile specificare la pagina Web visualizzata dall'utente per ogni contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="99a06-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99a06-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99a06-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a06-134">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="99a06-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="99a06-135">**PARAM (elemento)**</span><span class="sxs-lookup"><span data-stu-id="99a06-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




