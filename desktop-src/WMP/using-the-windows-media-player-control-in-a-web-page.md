---
title: Uso del controllo Media Player di Windows in una pagina Web
description: Uso del controllo Media Player di Windows in una pagina Web
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
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
- Incorporamento di pagine Web, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221728"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="ce943-115">Uso del controllo Media Player di Windows in una pagina Web</span><span class="sxs-lookup"><span data-stu-id="ce943-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="ce943-116">Incorporando il controllo Windows Media Player in una pagina Web è possibile personalizzare completamente il modo in cui l'utente interagisce con il controllo.</span><span class="sxs-lookup"><span data-stu-id="ce943-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="ce943-117">È possibile usare l'interfaccia fornita dal controllo oppure è possibile nasconderla e visualizzare un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ce943-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="ce943-118">È possibile specificare più proprietà di controllo Media Player Windows nel punto in cui si incorpora il controllo oppure è possibile impostare le proprietà del lettore e chiamare i metodi del lettore nel codice di script.</span><span class="sxs-lookup"><span data-stu-id="ce943-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="ce943-119">Le sezioni seguenti descrivono le nozioni di base per incorporare il controllo in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="ce943-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="ce943-120">Sezione</span><span class="sxs-lookup"><span data-stu-id="ce943-120">Section</span></span>                                                                                                        | <span data-ttu-id="ce943-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce943-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce943-122">Nascondere il controllo Media Player Windows</span><span class="sxs-lookup"><span data-stu-id="ce943-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="ce943-123">Vengono descritte le opzioni per nascondere il controllo Media Player di Windows quando si desidera fornire un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ce943-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="ce943-124">Elementi PARAM in un elemento OBJECT</span><span class="sxs-lookup"><span data-stu-id="ce943-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="ce943-125">Viene descritto come inizializzare il controllo Media Player Windows durante l'incorporamento.</span><span class="sxs-lookup"><span data-stu-id="ce943-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="ce943-126">Esempio semplice di scripting in una pagina Web</span><span class="sxs-lookup"><span data-stu-id="ce943-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="ce943-127">Viene descritto un esempio semplice, ma completo, di un controllo Player incorporato con un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ce943-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="ce943-128">Uso del controllo Media Player Windows con Firefox</span><span class="sxs-lookup"><span data-stu-id="ce943-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="ce943-129">Viene descritto come incorporare il controllo Windows Media Player in una pagina Web in modo che venga visualizzato correttamente da un browser Firefox.</span><span class="sxs-lookup"><span data-stu-id="ce943-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="ce943-130">Uso di Windows Media Player con Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="ce943-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="ce943-131">Viene descritto come usare il controllo Windows Media Player con Netscape 7,1 e altri Web browser basati su Gecko.</span><span class="sxs-lookup"><span data-stu-id="ce943-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="ce943-132">Il controllo Windows Media Player 10 Mobile contiene funzionalità basate su un subset delle funzionalità disponibili nella versione desktop del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="ce943-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="ce943-133">Pertanto, può essere incorporato in una pagina Web di Pocket Internet Explorer nello stesso modo in cui il controllo desktop è incorporato in una pagina Web di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ce943-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="ce943-134">Per sapere se un metodo, una proprietà o un evento specifico è supportato per il controllo Windows Media Player 10 Mobile, vedere [riferimento del modello a oggetti per lo scripting](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="ce943-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ce943-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce943-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce943-136">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="ce943-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




