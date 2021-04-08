---
title: Uso di HTML con Windows Media Player
description: Uso di HTML con Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Modello a oggetti di Windows Media Player, HTML
- modello a oggetti, HTML
- Controllo ActiveX di Windows Media Player, HTML per il modello a oggetti
- Controllo ActiveX, HTML per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, HTML per il modello a oggetti
- Windows Media Player Mobile, HTML per il modello a oggetti
- HTML con Windows Media Player
- Incorporamento di pagine Web, HTML
- incorporamento, pagine Web
- comandi script
- Capovolgimento URL
- streaming multimediale avanzato
- supporto browser
- visualizzazione di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856262"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="164c9-118">Uso di HTML con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="164c9-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="164c9-119">Panoramica</span><span class="sxs-lookup"><span data-stu-id="164c9-119">Overview</span></span>

<span data-ttu-id="164c9-120">Usare HTML con Windows Media Player è un ottimo modo per combinare audio e video con testo e grafica.</span><span class="sxs-lookup"><span data-stu-id="164c9-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="164c9-121">È possibile incorporare il controllo Windows Media Player in una pagina Web quando si desidera integrare il contenuto statico o creare applicazioni Web con supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="164c9-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="164c9-122">Quando si desidera integrare i supporti digitali con HTML, d'altra parte, è possibile visualizzare le pagine Web nella modalità completa del lettore facendovi riferimento nelle playlist di Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="164c9-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="164c9-123">Se si scrivono programmi personalizzati che incorporano il controllo Windows Media Player in modalità remota, è anche possibile controllare le pagine Web visualizzate nei vari riquadri della modalità completa del lettore quando gli utenti disancorano il controllo.</span><span class="sxs-lookup"><span data-stu-id="164c9-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="164c9-124">Ciò consente di mantenere la continuità tra gli stati ancorati e non ancorati.</span><span class="sxs-lookup"><span data-stu-id="164c9-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="164c9-125">Incorporamento Web</span><span class="sxs-lookup"><span data-stu-id="164c9-125">Web Embedding</span></span>

<span data-ttu-id="164c9-126">È possibile utilizzare il controllo Media Player Windows come parte di una pagina Web creata.</span><span class="sxs-lookup"><span data-stu-id="164c9-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="164c9-127">Vedere [incorporare il controllo Windows Media Player in una pagina Web](embedding-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="164c9-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="164c9-128">Comandi script e capovolgimento URL</span><span class="sxs-lookup"><span data-stu-id="164c9-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="164c9-129">I comandi script sono coppie di testo/valore che è possibile incorporare nei file multimediali digitali o nei flussi.</span><span class="sxs-lookup"><span data-stu-id="164c9-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="164c9-130">È possibile utilizzare i comandi di script personalizzati esclusivamente per attivare il codice dello script, consentendo a Windows Media Player di gestire automaticamente altri comandi di script.</span><span class="sxs-lookup"><span data-stu-id="164c9-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="164c9-131">Quando sono presenti diverse pagine Web che accompagnano una presentazione multimediale digitale, i comandi script URL possono modificare automaticamente la pagina in un frame mentre il controllo Media Player Windows continua a riprodurre file multimediali digitali in un altro frame.</span><span class="sxs-lookup"><span data-stu-id="164c9-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="164c9-132">Questa operazione è denominata capovolgimento degli URL ed è un ottimo modo per creare una presentazione multimediale.</span><span class="sxs-lookup"><span data-stu-id="164c9-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="164c9-133">Altri comandi script gestiti automaticamente consentono di passare dalla riproduzione a un altro file multimediale o flusso, visualizzare il testo della didascalia o generare eventi, ad esempio inserimenti ad, definiti in una playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="164c9-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="164c9-134">Per ulteriori informazioni sul capovolgimento degli URL, vedere la pagina relativa alla [creazione di presentazioni Web-Based](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="164c9-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="164c9-135">Streaming multimediale avanzato</span><span class="sxs-lookup"><span data-stu-id="164c9-135">Rich Media Streaming</span></span>

<span data-ttu-id="164c9-136">Il capovolgimento degli URL funziona meglio con pagine semplici che si caricano rapidamente.</span><span class="sxs-lookup"><span data-stu-id="164c9-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="164c9-137">Con pagine più complesse, più componenti vengono trasferiti singolarmente, rendendo difficile la sincronizzazione della visualizzazione delle pagine con supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="164c9-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="164c9-138">Per consentire presentazioni multimediali complesse complesse, le pagine Web possono essere aggiunte a un flusso multimediale e distribuite al lettore in modo analogo a audio e video.</span><span class="sxs-lookup"><span data-stu-id="164c9-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="164c9-139">In questo modo è possibile sincronizzare i componenti della presentazione in modo molto più semplice, soprattutto su connessioni a bassa velocità.</span><span class="sxs-lookup"><span data-stu-id="164c9-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="164c9-140">Per ulteriori informazioni sui flussi multimediali avanzati, vedere la pagina relativa alla [creazione di presentazioni Web-Based](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="164c9-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="164c9-141">Supporto browser</span><span class="sxs-lookup"><span data-stu-id="164c9-141">Browser Support</span></span>

<span data-ttu-id="164c9-142">È possibile incorporare il controllo Windows Media Player in Microsoft Internet Explorer, Firefox e Netscape Navigator, sebbene il processo sia leggermente diverso per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="164c9-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="164c9-143">È anche possibile creare pagine Web progettate per funzionare con tutti e tre i browser.</span><span class="sxs-lookup"><span data-stu-id="164c9-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="164c9-144">Con Internet Explorer e Firefox, il controllo viene incorporato usando l'elemento oggetto HTML.</span><span class="sxs-lookup"><span data-stu-id="164c9-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="164c9-145">Il navigatore richiede un approccio diverso, tuttavia, perché non supporta direttamente i controlli ActiveX.</span><span class="sxs-lookup"><span data-stu-id="164c9-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="164c9-146">Con Navigator si usa l'elemento APPLET per incorporare una speciale applet Java nella pagina.</span><span class="sxs-lookup"><span data-stu-id="164c9-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="164c9-147">Questa applet gestisce la comunicazione con il controllo ActiveX del lettore.</span><span class="sxs-lookup"><span data-stu-id="164c9-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="164c9-148">Per ulteriori informazioni sul supporto di Firefox, vedere [utilizzo del controllo Windows Media Player con Firefox](using-the-windows-media-player-control-with-firefox.md).</span><span class="sxs-lookup"><span data-stu-id="164c9-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="164c9-149">Per altre informazioni sul supporto di Netscape Navigator, vedere [uso di Windows Media Player con netscape 7,1](using-windows-media-player-with-netscape-7-1.md).</span><span class="sxs-lookup"><span data-stu-id="164c9-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="164c9-150">Visualizzazione di pagine Web in modalità completa del lettore</span><span class="sxs-lookup"><span data-stu-id="164c9-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="164c9-151">È possibile estendere le funzionalità di Windows Media Player o fornire una visualizzazione personalizzata delle informazioni che accompagnano i supporti digitali visualizzando le pagine Web in modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="164c9-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="164c9-152">Si tratta della funzionalità HTMLView di metafile di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="164c9-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="164c9-153">I metafile offrono un ottimo controllo sul contenuto della playlist, consentendo di eseguire facilmente la transizione tra clip, inserire annunci e visualizzare immagini ancora in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="164c9-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="164c9-154">Per visualizzare le pagine Web nella modalità completa del lettore, usare l'elemento PARAM per aggiungere riferimenti URL alle voci della playlist o a intere playlist.</span><span class="sxs-lookup"><span data-stu-id="164c9-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="164c9-155">Per ulteriori informazioni sull'utilizzo di pagine Web in metafile, vedere [visualizzazione di pagine Web in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="164c9-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="164c9-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="164c9-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="164c9-157">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="164c9-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




