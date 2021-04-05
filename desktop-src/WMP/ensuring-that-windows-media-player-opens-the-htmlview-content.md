---
title: Verifica che Windows Media Player Apra il contenuto di HTMLView
description: Verifica che Windows Media Player Apra il contenuto di HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Playlist Windows Media Metafile, Windows Media Player apertura di contenuto HTMLView
- playlist, Windows Media Player apertura di contenuto HTMLView
- playlist di metafile, Windows Media Player apertura di contenuto HTMLView
- Playlist Windows Media Metafile, apertura del contenuto di HTMLView
- playlist, apertura del contenuto di HTMLView
- playlist di metafile, apertura del contenuto di HTMLView
- apertura del contenuto di HTMLView
- Windows Media Player, apertura del contenuto di HTMLView
- Windows Media Player, contenuto HTMLView
- HTMLView, apertura del contenuto
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710975"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="85935-113">Verifica che Windows Media Player Apra il contenuto di HTMLView</span><span class="sxs-lookup"><span data-stu-id="85935-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="85935-114">Attualmente, le serie Windows Media Player 9 e Windows Media Player 10 sono gli unici lettori che supportano il parametro *HtmlView* nei file con estensione asx.</span><span class="sxs-lookup"><span data-stu-id="85935-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="85935-115">Ciò significa che è necessario eseguire i passaggi per assicurarsi che il contenuto di HTMLView riproduca in queste versioni di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="85935-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="85935-116">È necessario innanzitutto determinare se Windows Media Player 9 o Windows Media Player 10 è installato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="85935-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="85935-117">Windows Media Player SDK include un esempio completo in cui viene illustrato come rilevare versioni diverse di Windows Media Player in Web browser diversi.</span><span class="sxs-lookup"><span data-stu-id="85935-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="85935-118">Sebbene un'analisi completa dell'esempio di rilevamento esula dall'ambito di questa sezione, è possibile eseguire alcuni passaggi di base per determinare quale versione di Windows Media Player computer dell'utente è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="85935-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="85935-119">Nella sua forma più semplice, il rilevamento di Windows Media Player comporta l'incorporamento del controllo lettore nella pagina Web che si collega al contenuto di HTMLView e quindi controlla il valore recuperato dal *lettore*. proprietà **VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="85935-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="85935-120">Dopo aver verificato che l'utente dispone di Windows Media Player 9 serie o Windows Media Player 10 installato, è possibile usare il metodo [Player. openPlayer](player-openplayer.md) per aprire il contenuto nel lettore in modalità piena.</span><span class="sxs-lookup"><span data-stu-id="85935-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="85935-121">Il metodo **openPlayer** garantisce che il contenuto venga inizialmente visualizzato nella funzionalità di **riproduzione** del lettore in modalità completa, anziché in un'interfaccia, in modalità Mini Player o in un altro lettore registrato come programma predefinito per i file con estensione asx, ma non supporta htmlview.</span><span class="sxs-lookup"><span data-stu-id="85935-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="85935-122">Una volta visualizzato il contenuto, tuttavia, l'utente ha il controllo completo di Windows Media Player, vale a dire che può scegliere di visualizzare una funzionalità diversa da **Now**, passare alla modalità Skin o addirittura uscire dal lettore.</span><span class="sxs-lookup"><span data-stu-id="85935-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="85935-123">Il codice di esempio seguente consente di creare una pagina Web per Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="85935-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="85935-124">Questa pagina apre un file con estensione asx, che specifica una pagina Web HTMLView che viene visualizzata nel lettore in modalità completa quando è installato Windows Media Player 9 Series o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="85935-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="85935-125">Il codice nell'esempio precedente incorpora il controllo Windows Media Player con la proprietà **uiMode** impostata su "invisibile" e gli attributi Height e Width del lettore impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="85935-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="85935-126">Ciò è dovuto al fatto che la pagina Web non richiede la visualizzazione iniziale dell'interfaccia utente del controllo del lettore, ma richiede solo l'accesso al modello a oggetti del lettore.</span><span class="sxs-lookup"><span data-stu-id="85935-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="85935-127">La pagina Visualizza anche un pulsante di input che consente all'utente di riprodurre il file con estensione asx.</span><span class="sxs-lookup"><span data-stu-id="85935-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="85935-128">Quando l'utente fa clic sul pulsante Riproduci ASX, viene eseguita la funzione PlayASX di Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="85935-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="85935-129">Questa funzione recupera innanzitutto il valore per la proprietà Player **VERSIONINFO** , usando il metodo JScript **parseInt** per esaminare il valore numerico della stringa recuperata.</span><span class="sxs-lookup"><span data-stu-id="85935-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="85935-130">Se il valore numerico è maggiore o uguale a 9 (vale a dire che l'utente ha installato Windows Media Player 9 Series), il codice di script chiama il metodo **openPlayer** , passando l'URL del file con estensione asx contenente il parametro htmlview.</span><span class="sxs-lookup"><span data-stu-id="85935-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="85935-131">Questo metodo apre il file con estensione asx usando Windows Media Player in modalità completa, riproduce il contenuto multimediale digitale nella playlist. asx e visualizza il contenuto basato sul Web HTMLView nella funzionalità **Now Playing** .</span><span class="sxs-lookup"><span data-stu-id="85935-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="85935-132">Se il valore numerico della stringa di versione non è maggiore o uguale a 9 (ovvero se per l'utente non è installato Windows Media Player 9 o versione successiva nel computer in uso), il codice di script modifica **uiMode** del controllo Player in "full", imposta una nuova larghezza e altezza per il controllo e quindi apre il file con estensione asx nel lettore incorporato specificando un valore per la proprietà **URL** .</span><span class="sxs-lookup"><span data-stu-id="85935-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="85935-133">In questo caso, il contenuto multimediale digitale viene riprodotto nella pagina Web, ma tutti i valori di HTMLView specificati nel file con estensione ASX vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="85935-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="85935-134">Il modo in cui il contenuto viene riprodotto quando l'utente non dispone di Windows Media Player 9 serie o Windows Media Player 10 installato dipende dall'utente.</span><span class="sxs-lookup"><span data-stu-id="85935-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="85935-135">Nell'esempio precedente viene illustrato come specificare che il contenuto viene riprodotto nella pagina Web invece che nel lettore in modalità completa, ignorando qualsiasi contenuto HTMLView nel processo.</span><span class="sxs-lookup"><span data-stu-id="85935-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="85935-136">È possibile adottare altri approcci.</span><span class="sxs-lookup"><span data-stu-id="85935-136">There are other approaches you might take.</span></span> <span data-ttu-id="85935-137">Ad esempio, è possibile richiedere all'utente di installare una versione più recente di Windows Media Player, rendendo tale versione del lettore un requisito per la riproduzione del contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="85935-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85935-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85935-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85935-139">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="85935-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="85935-140">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="85935-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="85935-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="85935-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




