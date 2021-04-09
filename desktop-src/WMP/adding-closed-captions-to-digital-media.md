---
title: Aggiunta di didascalie chiuse a file multimediali digitali
description: Aggiunta di didascalie chiuse a file multimediali digitali
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- SAMI (Synchronized Accessible Media Interchange), informazioni
- SAMI (interscambio multimediale accessibile sincronizzato), informazioni
- Windows Media Player, aggiunta di didascalie chiuse
- Modello a oggetti di Windows Media Player, aggiunta di didascalie chiuse
- modello a oggetti, aggiunta di didascalie chiuse
- Windows Media Player Mobile, aggiunta di didascalie chiuse
- Controllo ActiveX di Windows Media Player, aggiunta di didascalie chiuse
- Controllo ActiveX Windows Media Player Mobile, aggiunta di didascalie chiuse
- Controllo ActiveX, aggiunta di didascalie chiuse
- SAMI (Synchronized Accessible Media Interchange), aggiunta di didascalie chiuse
- SAMI (interscambio multimediale accessibile sincronizzato), aggiunta di didascalie chiuse
- Aggiunta di didascalie chiuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044386"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="4a9df-122">Aggiunta di didascalie chiuse a file multimediali digitali</span><span class="sxs-lookup"><span data-stu-id="4a9df-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="4a9df-123">Il formato di file SAMI (Synchronized Accessible Media Interchange) è un formato di file progettato per fornire testo sincronizzato, ad esempio didascalie, sottotitoli o descrizioni audio con contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="4a9df-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="4a9df-124">Integrato in un Web browser usando il modello a oggetti di Windows Media Player, SAMI promuove l'accessibilità.</span><span class="sxs-lookup"><span data-stu-id="4a9df-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="4a9df-125">Con SAMI è possibile creare contenuti multimediali avanzati che raggiungono un pubblico più ampio e diversificato.</span><span class="sxs-lookup"><span data-stu-id="4a9df-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="4a9df-126">Oltre ai tipi di carattere standard, SAMI può supportare altri stili di testo, ad esempio colori, dimensioni o linguaggi diversi per aiutare un'ampia gamma di utenti.</span><span class="sxs-lookup"><span data-stu-id="4a9df-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="4a9df-127">SAMI può essere particolarmente utile per gli utenti con ipovisione o con problemi di udito.</span><span class="sxs-lookup"><span data-stu-id="4a9df-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="4a9df-128">Il formato SAMI può essere utile anche per scopi didattici, ad esempio per insegnare gli studenti a un secondo linguaggio.</span><span class="sxs-lookup"><span data-stu-id="4a9df-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="4a9df-129">Questo argomento è incentrato sull'integrazione di SAMI con il modello a oggetti del controllo ActiveX di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4a9df-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="4a9df-130">I file SAMI esistono indipendentemente dai file multimediali digitali e non si basano su un formato video o audio specifico per funzionare.</span><span class="sxs-lookup"><span data-stu-id="4a9df-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="4a9df-131">Poiché i file sono separati, il controllo Windows Media Player individua, analizza, sincronizza ed esegue il rendering di ogni file nel computer del client.</span><span class="sxs-lookup"><span data-stu-id="4a9df-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="4a9df-132">In questo modo vengono fornite flessibilità e funzionalità aggiuntive, in quanto consentono di modificare i singoli file SAMI, l'incorporazione del file SAMI con formati multimediali digitali diversi e l'archiviazione di file SAMI in percorsi server diversi.</span><span class="sxs-lookup"><span data-stu-id="4a9df-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="4a9df-133">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="4a9df-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="4a9df-134">Sezione</span><span class="sxs-lookup"><span data-stu-id="4a9df-134">Section</span></span>                                                                                                                            | <span data-ttu-id="4a9df-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a9df-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a9df-136">Informazioni sui file SAMI</span><span class="sxs-lookup"><span data-stu-id="4a9df-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="4a9df-137">Viene descritta la struttura di base dei file SAMI.</span><span class="sxs-lookup"><span data-stu-id="4a9df-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="4a9df-138">Esempio di file SAMI</span><span class="sxs-lookup"><span data-stu-id="4a9df-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="4a9df-139">Descrive la struttura di un file SAMI di esempio.</span><span class="sxs-lookup"><span data-stu-id="4a9df-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="4a9df-140">Uso di SAMI con il controllo Media Player Windows in un browser</span><span class="sxs-lookup"><span data-stu-id="4a9df-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="4a9df-141">Viene descritto come usare SAMI in una pagina Web con il controllo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4a9df-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="4a9df-142">Informazioni sugli URL SAMI</span><span class="sxs-lookup"><span data-stu-id="4a9df-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="4a9df-143">Descrive in che modo è possibile associare i file multimediali digitali ai file SAMI usando un singolo URL.</span><span class="sxs-lookup"><span data-stu-id="4a9df-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4a9df-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a9df-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a9df-145">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="4a9df-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




