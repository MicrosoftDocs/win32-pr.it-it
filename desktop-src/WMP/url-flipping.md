---
title: Capovolgimento URL
description: Capovolgimento URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "103714722"
---
# <a name="url-flipping"></a><span data-ttu-id="deb40-120">Capovolgimento URL</span><span class="sxs-lookup"><span data-stu-id="deb40-120">URL Flipping</span></span>

<span data-ttu-id="deb40-121">L'uso di pagine Web per le presentazioni è denominato capovolgimento dell'URL e viene gestito automaticamente da Windows Media Player quando rileva i comandi di script URL incorporati nel flusso multimediale digitale che sta riproducendo.</span><span class="sxs-lookup"><span data-stu-id="deb40-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="deb40-122">È possibile specificare un frame di destinazione per le pagine in ogni comando di script oppure è possibile specificarlo impostando la proprietà **Settings. defaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="deb40-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="deb40-123">È possibile impostare questa proprietà nel codice script o usando un elemento PARAM all'interno dell'elemento OBJECT che incorpora il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="deb40-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="deb40-124">È possibile gestire i comandi script URL nel codice JScript esattamente come si gestiscono i comandi di script personalizzati.</span><span class="sxs-lookup"><span data-stu-id="deb40-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="deb40-125">Se si desidera che il controllo Windows Media Player ignori i comandi di script URL, in modo che sia possibile gestirli interamente autonomamente, impostare le *Impostazioni*. proprietà **invokeURLs** su false nel codice script o utilizzando un elemento param come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="deb40-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="deb40-126">Nell'esempio seguente viene illustrato un frame tipico per l'capovolgimento degli URL.</span><span class="sxs-lookup"><span data-stu-id="deb40-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="deb40-127">Per prima cosa, creare una pagina che descrive il frame:</span><span class="sxs-lookup"><span data-stu-id="deb40-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="deb40-128">Successivamente, creare il file player.html a cui viene fatto riferimento nel frame con frame usando il codice seguente (si presuppone che il file video. wmv esista nella stessa directory dei file HTML):</span><span class="sxs-lookup"><span data-stu-id="deb40-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



<span data-ttu-id="deb40-129">Se le pagine Web sono sufficientemente piccole da caricare rapidamente, questa configurazione può essere sufficiente per le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="deb40-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="deb40-130">Se, d'altra parte, le pagine Web sono complesse, i flussi multimediali avanzati possono risultare più efficaci a seconda della velocità di connessione dei destinatari.</span><span class="sxs-lookup"><span data-stu-id="deb40-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="deb40-131">Il capovolgimento degli URL non funziona correttamente con le pagine visualizzate in Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="deb40-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="deb40-132">Anziché apparire nel frame specificato da **DefaultFrame**, ogni comando script URL ricevuto in Navigator Visualizza l'URL in una nuova finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="deb40-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="deb40-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="deb40-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb40-134">**Creazione di presentazioni Web-Based**</span><span class="sxs-lookup"><span data-stu-id="deb40-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="deb40-135">**Uso dello script per controllare il capovolgimento degli URL**</span><span class="sxs-lookup"><span data-stu-id="deb40-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




