---
title: Didascalie chiuse
description: Didascalie chiuse
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- Media Player di Windows, migrazione di didascalie chiuse
- Modello a oggetti di Windows Media Player, sottotitoli Smigrating
- modello a oggetti, migrazione di didascalie chiuse
- Windows Media Player Mobile, migrazione di didascalie chiuse
- Controllo ActiveX di Windows Media Player, migrazione di didascalie chiuse
- Controllo ActiveX di Windows Media Player Mobile, migrazione di didascalie chiuse
- Controllo ActiveX, migrazione di didascalie chiuse
- SAMI (Synchronized Accessible Media Interchange), migrazione di didascalie chiuse
- SAMI (interscambio multimediale accessibile sincronizzato), migrazione di didascalie chiuse
- Guida alla migrazione, l'interscambio multimediale accessibile sincronizzato (SAMI)
- Guida alla migrazione, sottotitoli codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117415"
---
# <a name="closed-captioning"></a><span data-ttu-id="3d371-121">Didascalie chiuse</span><span class="sxs-lookup"><span data-stu-id="3d371-121">Closed Captioning</span></span>

<span data-ttu-id="3d371-122">Il controllo ActiveX di Windows Media Player 6,4 include un pannello di visualizzazione didascalia chiuso integrato che, quando reso visibile, Abilita i sottotitoli codificati accessibili da Media Interchange (SAMI) sincronizzati e visualizza il testo del titolo chiuso.</span><span class="sxs-lookup"><span data-stu-id="3d371-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="3d371-123">Il controllo Windows Media Player 7 o versioni successive Abilita la visualizzazione della didascalia chiusa di SAMI usando un **<DIV>** elemento HTML.</span><span class="sxs-lookup"><span data-stu-id="3d371-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="3d371-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="3d371-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="3d371-125">Questa tecnica offre una flessibilità completa, dal momento che è possibile progettare la pagina Web per visualizzare le didascalie chiuse in modo personalizzato; non è più necessario che la visualizzazione didascalia chiusa si trovi in una posizione fissa adiacente all'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3d371-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="3d371-126">Dopo aver creato un'area per la visualizzazione di didascalie chiuse, usare *ClosedCaption*. proprietà **captioningID** per specificare il percorso in cui Windows Media Player esegue il rendering del testo della didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="3d371-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="3d371-127">Windows Media Player Software Development Kit (SDK) contiene un esempio funzionante di un lettore incorporato che Visualizza il testo del titolo chiuso.</span><span class="sxs-lookup"><span data-stu-id="3d371-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="3d371-128">Per ottenere gli esempi di SDK, scaricare e installare l'SDK completo di Windows Media Player dal sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d371-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="3d371-129">Per ulteriori informazioni sui sottotitoli codificati e SAMI, vedere il [sito Web di accessibilità Microsoft](https://www.microsoft.com/enable/).</span><span class="sxs-lookup"><span data-stu-id="3d371-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d371-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d371-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d371-131">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="3d371-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="3d371-132">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="3d371-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="3d371-133">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="3d371-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




