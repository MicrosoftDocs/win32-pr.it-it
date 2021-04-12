---
title: Creazione di playlist di metafile
description: Creazione di playlist di metafile
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Playlist Windows Media Metafile, creazione
- playlist, creazione
- playlist di metafile, creazione
- creazione di playlist Windows Media Metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221782"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="85c2d-107">Creazione di playlist di metafile</span><span class="sxs-lookup"><span data-stu-id="85c2d-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="85c2d-108">È possibile creare una playlist utilizzando qualsiasi editor di testo, ad esempio Blocco note di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85c2d-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="85c2d-109">Aprire l'editor di testo.</span><span class="sxs-lookup"><span data-stu-id="85c2d-109">Open your text editor.</span></span> <span data-ttu-id="85c2d-110">Digitare le voci di script che si desidera implementare.</span><span class="sxs-lookup"><span data-stu-id="85c2d-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="85c2d-111">Al termine della digitazione nel blocco note, salvare il file con un nome file e un'estensione di file appropriati.</span><span class="sxs-lookup"><span data-stu-id="85c2d-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="85c2d-112">Per altre informazioni sulle estensioni, vedere [linee guida sull'estensione metafile](metafile-extension-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="85c2d-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="85c2d-113">Il nome file è in genere il nome del file o del flusso di Windows Media seguito da un'estensione di. Wax,. wvx o. asx.</span><span class="sxs-lookup"><span data-stu-id="85c2d-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="85c2d-114">Se, ad esempio, il contenuto multimediale è un file audio Windows Media con estensione WMA, utilizzare l'estensione cera quando si assegna un nome alla playlist.</span><span class="sxs-lookup"><span data-stu-id="85c2d-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="85c2d-115">Le playlist non devono includere codici di formattazione da un elaboratore di testo, ad esempio Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="85c2d-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="85c2d-116">Per assicurarsi che nella playlist non siano inclusi codici di formattazione, salvare il file come file di testo normale o ASCII.</span><span class="sxs-lookup"><span data-stu-id="85c2d-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="85c2d-117">Elementi e attributi non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="85c2d-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="85c2d-118">Il testo usato nella playlist per definire un elemento o un attributo può essere maiuscolo o minuscolo o una combinazione di entrambi.</span><span class="sxs-lookup"><span data-stu-id="85c2d-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="85c2d-119">Se un elemento non dispone di elementi figlio (quelli che modificano o sono contenuti all'interno di un altro elemento), è possibile usare una singola barra (/) alla fine del tag di apertura, immediatamente prima di ">", al posto di un tag di chiusura.</span><span class="sxs-lookup"><span data-stu-id="85c2d-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="85c2d-120">Gli elementi figlio di un elemento devono essere visualizzati tra il tag di apertura e di chiusura per l'elemento. in caso contrario, non si tratta di elementi figlio per l'elemento e vengono ignorati o generano un errore nella sintassi della playlist.</span><span class="sxs-lookup"><span data-stu-id="85c2d-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="85c2d-121">I primi quattro caratteri di una playlist devono essere " &lt; ASX".</span><span class="sxs-lookup"><span data-stu-id="85c2d-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="85c2d-122">L'elemento **ASX** viene usato in tutte le playlist se la relativa estensione è. Wax,. wvx o. asx.</span><span class="sxs-lookup"><span data-stu-id="85c2d-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="85c2d-123">Deve essere presente un solo elemento **ASX** per playlist.</span><span class="sxs-lookup"><span data-stu-id="85c2d-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="85c2d-124">Questo elemento identifica il file come playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="85c2d-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="85c2d-125">Non specifica il tipo di playlist.</span><span class="sxs-lookup"><span data-stu-id="85c2d-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="85c2d-126">L'elemento **ASX** ha tre attributi possibili:</span><span class="sxs-lookup"><span data-stu-id="85c2d-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="85c2d-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="85c2d-127">**VERSION**</span></span>

<span data-ttu-id="85c2d-128">L'attributo **Version** è obbligatorio e deve essere seguito immediatamente dopo l'elemento **ASX** , ad esempio "<ASX Version =" 3,0 " &gt; ".</span><span class="sxs-lookup"><span data-stu-id="85c2d-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="85c2d-129">Il numero di versione corrente è 3,0.</span><span class="sxs-lookup"><span data-stu-id="85c2d-129">The current version number is 3.0.</span></span> <span data-ttu-id="85c2d-130">Windows Media Player supporta tutte le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="85c2d-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="85c2d-131">I valori accettabili per l'attributo **Version** includono sia 3,0 che 3 (senza virgola decimale).</span><span class="sxs-lookup"><span data-stu-id="85c2d-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="85c2d-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="85c2d-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="85c2d-133">L'attributo **PREVIEWMODE** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="85c2d-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="85c2d-134">Fornisce un altro meccanismo per specificare per quanto tempo eseguire il rendering di un clip.</span><span class="sxs-lookup"><span data-stu-id="85c2d-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="85c2d-135">Se il valore dell'attributo **PREVIEWMODE** è sì, Windows Media Player eseguirà il rendering di ogni clip per la durata specificata dall'elemento **PREVIEWDURATION**.</span><span class="sxs-lookup"><span data-stu-id="85c2d-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="85c2d-136">Ogni clip può avere un **PREVIEWDURATION** specificato.</span><span class="sxs-lookup"><span data-stu-id="85c2d-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="85c2d-137">**BANNERBAR**</span><span class="sxs-lookup"><span data-stu-id="85c2d-137">**BANNERBAR**</span></span>

<span data-ttu-id="85c2d-138">L'attributo facoltativo **BANNERBAR** definisce se il controllo Media Player Windows riserva spazio per una rappresentazione grafica del banner.</span><span class="sxs-lookup"><span data-stu-id="85c2d-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="85c2d-139">(Usare l'elemento **banner** per specificare l'immagine da visualizzare). Se il valore di **BANNERBAR** è fixed, Windows Media Player riserva lo spazio del banner per la visualizzazione e per ogni clip, indipendentemente dal fatto che la playlist del metafile specifichi un banner per la visualizzazione o la clip.</span><span class="sxs-lookup"><span data-stu-id="85c2d-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="85c2d-140">In questo modo, le dimensioni della finestra di Media Player di Windows vengono mantenute uguali (tranne quando le dimensioni del video cambiano) indipendentemente dall'assenza o dalla presenza di un grafico del banner.</span><span class="sxs-lookup"><span data-stu-id="85c2d-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="85c2d-141">Se alla Mostra o alla clip non è associato alcun banner, lo spazio riservato per uno è nero.</span><span class="sxs-lookup"><span data-stu-id="85c2d-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="85c2d-142">Se il valore dell'attributo **BANNERBAR** è auto, Windows Media Player riserva spazio per il banner solo quando la visualizzazione o la clip ne include una.</span><span class="sxs-lookup"><span data-stu-id="85c2d-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="85c2d-143">Per ulteriori informazioni sui tre attributi dell'elemento **ASX** , vedere la voce di riferimento per l' [elemento ASX](asx-element.md).</span><span class="sxs-lookup"><span data-stu-id="85c2d-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="85c2d-144">Un elemento **ASX** contiene elementi figlio **entry** che definiscono informazioni sui file multimediali a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="85c2d-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="85c2d-145">Ogni elemento **entry** deve contenere un elemento **ref** che specifica il percorso del file multimediale da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="85c2d-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="85c2d-146">È necessario che sia presente almeno un elemento **entry** o **ENTRYREF** all'interno di un elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="85c2d-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="85c2d-147">Gli altri elementi definiti nell'ambito dell'elemento **ASX** , ad esempio **titolo** e **autore**, sono associati ai metadati visualizzati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="85c2d-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="85c2d-148">Le playlist più semplici vengono create aggiungendo più elementi **entry** con un singolo elemento **ref** a un metafile.</span><span class="sxs-lookup"><span data-stu-id="85c2d-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="85c2d-149">Ogni elemento **entry** in una playlist di metafile viene sottoposto a rendering nell'ordine in cui viene visualizzato nel file come se l'utente avesse aperto manualmente ogni clip.</span><span class="sxs-lookup"><span data-stu-id="85c2d-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="85c2d-150">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="85c2d-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="85c2d-151">Assicurarsi che la playlist funzioni facendo doppio clic su di essa in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="85c2d-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="85c2d-152">Windows Media Player dovrebbe aprire e avviare lo streaming del contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="85c2d-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="85c2d-153">Dopo aver verificato il corretto funzionamento della playlist, salvarla nel server Web insieme alle pagine Web e collegarla tramite un elemento **href** oppure incorporarla in una pagina Web usando l'elemento **oggetto** di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="85c2d-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="85c2d-154">Le sezioni seguenti contengono ulteriori informazioni:</span><span class="sxs-lookup"><span data-stu-id="85c2d-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="85c2d-155">Annidamento di metafile</span><span class="sxs-lookup"><span data-stu-id="85c2d-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="85c2d-156">Utilizzo di pagine ASP per la creazione dinamica di playlist di metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="85c2d-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="85c2d-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85c2d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85c2d-158">**Elemento BANNER**</span><span class="sxs-lookup"><span data-stu-id="85c2d-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="85c2d-159">**Playlist di esempio**</span><span class="sxs-lookup"><span data-stu-id="85c2d-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="85c2d-160">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="85c2d-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="85c2d-161">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="85c2d-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




