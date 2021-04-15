---
title: Nascondere il controllo Media Player Windows
description: Nascondere il controllo Media Player Windows
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- incorporamento, pagine Web
- Windows Media Player, nascondere il controllo ActiveX
- Modello a oggetti di Windows Media Player, nascondere il controllo ActiveX
- modello a oggetti, che nasconde il controllo ActiveX
- Windows Media Player Mobile, controllo hidingActiveX
- Controllo ActiveX di Windows Media Player, nascondere
- Controllo ActiveX Windows Media Player Mobile, nascondere
- Controllo ActiveX, nascondere
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Incorporamento di pagine Web, controllo ActiveX nascosto
- nascondere il controllo ActiveX di Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331455"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="6eb96-126">Nascondere il controllo Media Player Windows</span><span class="sxs-lookup"><span data-stu-id="6eb96-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="6eb96-127">L'oggetto ActiveX di Windows Media Player viene incorporato in una pagina Web utilizzando l'elemento oggetto.</span><span class="sxs-lookup"><span data-stu-id="6eb96-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="6eb96-128">Diversamente dalle versioni precedenti, l'elemento oggetto che definisce Media Player di Windows deve essere inserito nella sezione del corpo di una pagina Web, tra i tag <BODY> e </BODY> .</span><span class="sxs-lookup"><span data-stu-id="6eb96-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="6eb96-129">L'inserimento dell'oggetto ActiveX Media Player Windows nella sezione HEAD di una pagina Web per nascondere l'interfaccia utente può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="6eb96-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="6eb96-130">Se si inserisce il controllo ActiveX di Windows Media Player nella sezione del corpo di una pagina Web, verrà visualizzata l'interfaccia utente del controllo.</span><span class="sxs-lookup"><span data-stu-id="6eb96-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="6eb96-131">Se non si desidera che venga visualizzata e si desidera creare un'interfaccia utente personalizzata, impostare gli attributi Height e Width dell'elemento OBJECT su zero.</span><span class="sxs-lookup"><span data-stu-id="6eb96-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="6eb96-132">Il controllo può essere reso invisibile anche impostando il *lettore*. proprietà **uiMode** su "invisibile".</span><span class="sxs-lookup"><span data-stu-id="6eb96-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="6eb96-133">Questa operazione può essere eseguita usando un tag PARAM, come illustrato nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="6eb96-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="6eb96-134">In questo caso, lo spazio è riservato per il controllo con altezza e larghezza, ma non viene visualizzato nulla nello spazio riservato fino a quando **uiMode** non viene modificato in un valore diverso da "invisibile".</span><span class="sxs-lookup"><span data-stu-id="6eb96-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="6eb96-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6eb96-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eb96-136">**Uso del controllo Media Player di Windows in una pagina Web**</span><span class="sxs-lookup"><span data-stu-id="6eb96-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




