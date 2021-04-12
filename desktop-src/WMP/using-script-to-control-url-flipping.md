---
title: Uso dello script per controllare il capovolgimento degli URL
description: Uso dello script per controllare il capovolgimento degli URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, presentazioni basate sul Web
- Modello a oggetti di Windows Media Player, presentazioni basate sul Web
- modello a oggetti, presentazioni basate sul Web
- Presentazioni Windows Media Player per dispositivi mobili, basate sul Web
- Windows Media Player ActiveX Control, presentazioni basate sul Web
- Controllo ActiveX Windows Media Player Mobile, presentazioni basate sul Web
- Controllo ActiveX, presentazioni basate sul Web
- Windows Media Player, capovolgimento URL
- Modello a oggetti di Windows Media Player, capovolgimento degli URL
- modello a oggetti, capovolgimento URL
- Windows Media Player Mobile, capovolgimento URL
- Controllo ActiveX Windows Media Player, capovolgimento URL
- Controllo ActiveX Windows Media Player Mobile, capovolgimento URL
- Controllo ActiveX, capovolgimento URL
- Presentazioni basate sul Web, capovolgimento degli URL
- creazione di presentazioni basate sul Web, capovolgimento degli URL
- Capovolgimento URL
- Windows Media Player, streaming multimediale avanzato
- Modello a oggetti di Windows Media Player, streaming multimediale avanzato
- modello a oggetti, flusso multimediale avanzato
- Windows Media Player Mobile, streaming multimediale avanzato
- Controllo ActiveX di Windows Media Player, streaming multimediale avanzato
- Controllo ActiveX Windows Media Player Mobile, streaming multimediale avanzato
- Controllo ActiveX, streaming multimediale avanzato
- Presentazioni basate sul Web, streaming multimediale avanzato
- creazione di presentazioni basate sul Web, streaming multimediale avanzato
- streaming multimediale avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104397043"
---
# <a name="using-script-to-control-url-flipping"></a><span data-ttu-id="03329-130">Uso dello script per controllare il capovolgimento degli URL</span><span class="sxs-lookup"><span data-stu-id="03329-130">Using Script to Control URL Flipping</span></span>

<span data-ttu-id="03329-131">Quando un utente si connette a un flusso multimediale avanzato mentre il flusso è già in corso, è possibile che la pagina Web trasmessa venga visualizzata prima che tutti gli elementi siano arrivati e siano stati memorizzati nella cache se Windows Media Player richiama automaticamente l'URL.</span><span class="sxs-lookup"><span data-stu-id="03329-131">When a user connects to a rich media stream while the stream is already in progress, it is possible for the streamed webpage to display before all the elements have arrived and been cached if Windows Media Player automatically invokes the URL.</span></span> <span data-ttu-id="03329-132">Quando si verifica questa situazione, l'utente visualizza una pagina Web vuota o incompleta finché non arriva il set di dati successivo nella cache.</span><span class="sxs-lookup"><span data-stu-id="03329-132">When this happens, the user sees a blank or incomplete webpage until the next set of data arrives in the cache.</span></span>

<span data-ttu-id="03329-133">È possibile evitare di visualizzare una pagina Web vuota o incompleta richiamando l'URL utilizzando lo script anziché consentire a Windows Media Player di eseguirlo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="03329-133">You can avoid displaying a blank or incomplete webpage by invoking the URL using script instead of letting Windows Media Player do it automatically.</span></span> <span data-ttu-id="03329-134">In questo modo, è possibile ignorare il primo capovolgimento dell'URL e quindi richiamare gli URL successivi usando il codice di script.</span><span class="sxs-lookup"><span data-stu-id="03329-134">That way, you can ignore the first URL flip and then invoke subsequent URLs by using script code.</span></span>

> [!Note]  
> <span data-ttu-id="03329-135">In questa sezione si presuppone che si stia eseguendo lo streaming HTML con Windows Media Encoder 9 Series SDK e che sia stato impostato il flusso HTML per la ripetizione.</span><span class="sxs-lookup"><span data-stu-id="03329-135">This section assumes that you are streaming HTML using the Windows Media Encoder 9 Series SDK and that you have set the HTML stream to repeat.</span></span>

 

<span data-ttu-id="03329-136">Per prima cosa, è necessario creare una pagina Web con frame che contenga il frame con il lettore incorporato e il frame in cui viene visualizzato il codice HTML di streaming.</span><span class="sxs-lookup"><span data-stu-id="03329-136">First, you must create a frameset webpage to contain the frame with the embedded Player and the frame that displays the streaming HTML.</span></span> <span data-ttu-id="03329-137">Ognuno di questi due frame visualizzerà inizialmente una pagina Web separata, pertanto si creerà un totale di tre pagine Web.</span><span class="sxs-lookup"><span data-stu-id="03329-137">Each of these two frames will display a separate webpage initially, so you will create a total of three webpages.</span></span> <span data-ttu-id="03329-138">Nell'esempio di codice seguente viene illustrata la pagina Web Frameset:</span><span class="sxs-lookup"><span data-stu-id="03329-138">The following example code demonstrates the frameset webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



<span data-ttu-id="03329-139">Nell'esempio di pagina Web precedente sono incorporati due frame.</span><span class="sxs-lookup"><span data-stu-id="03329-139">The preceding webpage example incorporates two frames.</span></span> <span data-ttu-id="03329-140">Il primo frame viene visualizzato nella parte sinistra della finestra del browser e viene visualizzata la pagina Web denominata incorpora \_player.htm.</span><span class="sxs-lookup"><span data-stu-id="03329-140">The first frame displays in the left half of the browser window and displays the webpage named embed\_player.htm.</span></span> <span data-ttu-id="03329-141">Il codice di esempio seguente crea questa pagina Web:</span><span class="sxs-lookup"><span data-stu-id="03329-141">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="03329-142">Il secondo frame del frame viene visualizzato nella parte destra della finestra del browser e visualizza una pagina Web denominata "blank.htm".</span><span class="sxs-lookup"><span data-stu-id="03329-142">The second frame in the frameset displays in the right half of the browser window and displays a webpage named "blank.htm".</span></span> <span data-ttu-id="03329-143">Il codice di esempio seguente crea questa pagina Web:</span><span class="sxs-lookup"><span data-stu-id="03329-143">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



<span data-ttu-id="03329-144">Quando la pagina frameset viene caricata nel browser, il riquadro sinistro mostra il lettore incorporato e il frame destro Mostra il testo "caricamento..." informare l'utente che saranno più prossimi i dati.</span><span class="sxs-lookup"><span data-stu-id="03329-144">When the frameset page loads in the browser, the left frame shows the embedded Player and the right frame shows the text "Loading..." to inform the user that more data is forthcoming.</span></span> <span data-ttu-id="03329-145">Quando il primo comando script URL arriva dal flusso HTML, il gestore eventi modifica semplicemente il valore del flag **booleano** .</span><span class="sxs-lookup"><span data-stu-id="03329-145">When the first URL script command arrives from the HTML stream, the event handler simply changes the value of the **Boolean** flag.</span></span> <span data-ttu-id="03329-146">Quando ogni comando script URL successivo arriva dal flusso HTML, lo script nel gestore eventi carica il nuovo URL nel frame denominato "Content" e la pagina Web completa viene visualizzata nel frame che si trova nella metà destra della finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="03329-146">When each subsequent URL script command arrives from the HTML stream, the script in the event handler loads the new URL into the frame named "content", and the complete webpage displays in the frame located in the right half of the browser window.</span></span>

<span data-ttu-id="03329-147">Per ulteriori informazioni sul flusso di HTML utilizzando Windows Media, vedere Windows Media Encoder SDK.</span><span class="sxs-lookup"><span data-stu-id="03329-147">For more information about streaming HTML using Windows Media, see the Windows Media Encoder SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03329-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03329-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03329-149">**Streaming multimediale avanzato**</span><span class="sxs-lookup"><span data-stu-id="03329-149">**Rich Media Streaming**</span></span>](rich-media-streaming.md)
</dt> <dt>

[<span data-ttu-id="03329-150">**Capovolgimento URL**</span><span class="sxs-lookup"><span data-stu-id="03329-150">**URL Flipping**</span></span>](url-flipping.md)
</dt> </dl>

 

 




