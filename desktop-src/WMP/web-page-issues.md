---
title: Problemi di pagina Web
description: Problemi di pagina Web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Playlist Windows Media Metafile, pagine Web
- playlist, pagine Web
- playlist di metafile, pagine Web
- Playlist Windows Media Metafile, personalizzazione di HTMLView
- playlist, personalizzazione di HTMLView
- playlist di metafile, personalizzazione di HTMLView
- Playlist Windows Media Metafile, personalizzazione HTMLView
- playlist, personalizzazione di HTMLView
- playlist di metafile, personalizzazione di HTMLView
- personalizzazione di HTMLView
- Windows Media Player, pagine Web
- Windows Media Player, personalizzazione di HTMLView
- Media Player di Windows, personalizzazione di HTMLView
- HTMLView, personalizzazione
- HTMLView, pagine Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713402"
---
# <a name="web-page-issues"></a><span data-ttu-id="30d1f-118">Problemi di pagina Web</span><span class="sxs-lookup"><span data-stu-id="30d1f-118">Web Page Issues</span></span>

<span data-ttu-id="30d1f-119">Quando si crea una pagina Web da visualizzare nella funzionalità Windows Media Player **Now Playing** , è necessario prendere in considerazione alcuni aspetti.</span><span class="sxs-lookup"><span data-stu-id="30d1f-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="30d1f-120">In questa sezione vengono illustrati alcuni dei problemi che possono verificarsi durante la creazione del contenuto basato sul Web.</span><span class="sxs-lookup"><span data-stu-id="30d1f-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="30d1f-121">Personalizzazione di HTMLView</span><span class="sxs-lookup"><span data-stu-id="30d1f-121">Customizing HTMLView</span></span>

<span data-ttu-id="30d1f-122">La pagina Web di HTMLView può essere semplice o complessa.</span><span class="sxs-lookup"><span data-stu-id="30d1f-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="30d1f-123">È possibile includere gli elementi utilizzati in genere nel contenuto basato sul Web.</span><span class="sxs-lookup"><span data-stu-id="30d1f-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="30d1f-124">Se si incorpora il controllo Media Player di Windows, è possibile visualizzare una delle interfacce utente fornite dal controllo, creare una propria interfaccia utente utilizzando codice HTML e script o non fornire alcuna interfaccia utente (il che significa che l'utente può utilizzare i controlli di trasporto del lettore in modalità completa).</span><span class="sxs-lookup"><span data-stu-id="30d1f-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="30d1f-125">Le dimensioni consigliate per le pagine Web visualizzate con la funzionalità HTMLView sono 575 x 345 pixel.</span><span class="sxs-lookup"><span data-stu-id="30d1f-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="30d1f-126">L'utente, tuttavia, ha la possibilità di ridimensionare Media Player di Windows e scegliere la risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="30d1f-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="30d1f-127">Se la pagina Web HTMLView è più grande delle dimensioni configurate dalla funzionalità **Now Playing** , il lettore Visualizza barre di scorrimento orizzontali e verticali che consentono all'utente di visualizzare l'intera pagina.</span><span class="sxs-lookup"><span data-stu-id="30d1f-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="30d1f-128">È necessario testare il contenuto di HTMLView usando un'ampia gamma di risoluzioni dello schermo e dimensioni dei lettori per determinare le dimensioni migliori per la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="30d1f-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="30d1f-129">Windows Media Player non fornisce un metodo che consente di specificare una dimensione per il lettore in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="30d1f-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="30d1f-130">Navigazione di pagine Web</span><span class="sxs-lookup"><span data-stu-id="30d1f-130">Web page navigation</span></span>

<span data-ttu-id="30d1f-131">Windows Media Player non fornisce una barra degli strumenti di navigazione per le pagine Web visualizzate nella funzionalità **Now Playing** .</span><span class="sxs-lookup"><span data-stu-id="30d1f-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="30d1f-132">Ciò significa che è possibile controllare completamente se gli utenti possono uscire dalla pagina Web di HTMLView.</span><span class="sxs-lookup"><span data-stu-id="30d1f-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="30d1f-133">Se si desidera consentire agli utenti di passare ad altre pagine Web, è necessario includere elementi nel codice HTML per fornire tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="30d1f-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="30d1f-134">Recupero della finestra padre</span><span class="sxs-lookup"><span data-stu-id="30d1f-134">Retrieving the parent window</span></span>

<span data-ttu-id="30d1f-135">Se il codice di script esistente usa **Window. Parent** per recuperare l'oggetto finestra padre, il codice non funzionerà nella pagina Web htmlview.</span><span class="sxs-lookup"><span data-stu-id="30d1f-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="30d1f-136">Quando si usa HTMLView, non è presente alcun oggetto finestra padre; Pertanto, questa funzionalità di scripting non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="30d1f-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="30d1f-137">Informazioni sul browser incorporato</span><span class="sxs-lookup"><span data-stu-id="30d1f-137">About the embedded browser</span></span>

<span data-ttu-id="30d1f-138">Poiché Windows Media Player utilizza un'istanza incorporata di Internet Explorer per visualizzare il contenuto di HTMLView, le impostazioni utente e i criteri per Internet Explorer si applicano a tutte le pagine Web visualizzate nel lettore.</span><span class="sxs-lookup"><span data-stu-id="30d1f-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="30d1f-139">Se, ad esempio, l'utente ha configurato Internet Explorer per impedire che le pagine Web scarichino i cookie nel computer, non è possibile eseguire questa operazione nella pagina Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="30d1f-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="30d1f-140">Le pagine Web aperte con la funzionalità HTMLView vengono sempre eseguite nell'area di sicurezza **Internet** di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="30d1f-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="30d1f-141">Il controllo Web browser incorporato usa le stesse regole per memorizzare nella cache le pagine Web come la versione autonoma di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="30d1f-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="30d1f-142">È consigliabile usare Active Server Pages (ASP) quando si crea il contenuto per garantire che il contenuto venga distribuito dal server Web ogni volta che Windows Media Player accede alla pagina Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="30d1f-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="30d1f-143">L'utilizzo di pagine ASP può essere semplice quanto la ridenominazione della pagina Web per l'utilizzo di un'estensione del nome di file ASP.</span><span class="sxs-lookup"><span data-stu-id="30d1f-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="30d1f-144">Informazioni sul contenuto Web locale</span><span class="sxs-lookup"><span data-stu-id="30d1f-144">About local Web content</span></span>

<span data-ttu-id="30d1f-145">La funzionalità HTMLView non consente di aprire le pagine Web archiviate nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="30d1f-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="30d1f-146">Invio di una richiesta all'utente</span><span class="sxs-lookup"><span data-stu-id="30d1f-146">Prompting the user</span></span>

<span data-ttu-id="30d1f-147">È possibile utilizzare **Window. prompt** per richiedere informazioni all'utente.</span><span class="sxs-lookup"><span data-stu-id="30d1f-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="30d1f-148">Tuttavia, **Window. Alert** e **Window. Confirm** non sono disponibili quando si usa htmlview.</span><span class="sxs-lookup"><span data-stu-id="30d1f-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="30d1f-149">Problemi di temporizzazione</span><span class="sxs-lookup"><span data-stu-id="30d1f-149">Timing issues</span></span>

<span data-ttu-id="30d1f-150">È possibile che si verifichino problemi temporali quando si usa un controllo di Windows Media Player incorporato nella pagina Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="30d1f-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="30d1f-151">In HTMLView, un controllo lettore incorporato condivide il motore di riproduzione con le Media Player Windows autonome.</span><span class="sxs-lookup"><span data-stu-id="30d1f-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="30d1f-152">È possibile che il lettore autonomo possa aprire e iniziare a riprodurre la prima voce della playlist prima che la pagina Web (e, pertanto, il controllo Player) finisca il caricamento.</span><span class="sxs-lookup"><span data-stu-id="30d1f-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="30d1f-153">Ciò significa che se si gestiscono gli eventi **OpenStateChange** o **PlayStateChange** , il codice di script non riceverà le notifiche degli eventi per questi eventi fino a quando non verrà caricato il controllo del lettore e gli oggetti associati.</span><span class="sxs-lookup"><span data-stu-id="30d1f-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="30d1f-154">È possibile eseguire le operazioni nel codice per ritardare la riproduzione fino a quando non viene creata un'istanza del controllo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="30d1f-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="30d1f-155">A questo scopo, è possibile fare in modo che la prima voce nella playlist del metafile punti a un file di immagine e impostare la durata del file su un periodo di tempo che consenta il caricamento del controllo lettore.</span><span class="sxs-lookup"><span data-stu-id="30d1f-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="30d1f-156">Nell'esempio di codice seguente viene illustrata questa opzione:</span><span class="sxs-lookup"><span data-stu-id="30d1f-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="30d1f-157">Quando si apre la playlist precedente, Windows Media Player attende la prima voce nella playlist per un massimo di un minuto mentre il giocatore carica la pagina Web HTMLView.</span><span class="sxs-lookup"><span data-stu-id="30d1f-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="30d1f-158">Quindi, nella pagina Web di HTMLView, scrivere codice script per gestire l'evento **OnLoad** per l'elemento **Body** .</span><span class="sxs-lookup"><span data-stu-id="30d1f-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="30d1f-159">Nella funzione del gestore eventi chiamare il metodo Player **Controls. Next** per iniziare la riproduzione della seconda voce nella playlist.</span><span class="sxs-lookup"><span data-stu-id="30d1f-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="30d1f-160">Quando la pagina Web nell'esempio precedente termina il caricamento, Windows Media Player avanza immediatamente alla seconda voce della playlist.</span><span class="sxs-lookup"><span data-stu-id="30d1f-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="30d1f-161">Questa operazione sostituisce la durata specificata per il primo elemento nella playlist, ovvero l'utente non deve attendere il completamento di un minuto prima di visualizzare il contenuto desiderato; deve attendere il completamento del caricamento della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="30d1f-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="30d1f-162">Poiché a questo punto viene creata completamente un'istanza del controllo Player, gli eventi **OpenStateChange** e **PlayStateChange** possono essere gestiti nel modo consueto.</span><span class="sxs-lookup"><span data-stu-id="30d1f-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30d1f-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30d1f-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30d1f-164">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="30d1f-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="30d1f-165">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="30d1f-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="30d1f-166">**Evento Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="30d1f-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




