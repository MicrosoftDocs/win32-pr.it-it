---
title: Utilizzo dell'elemento TextBox
description: Utilizzo dell'elemento TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Web Workshop, elemento TextBox
- progettazione di pagine Web, elemento TextBox
- Vector Markup Language (la), elemento TextBox
- LA (Vector Markup Language), elemento TextBox
- Vector graphics, elemento TextBox
- elemento TextBox
- Elementi la, TextBox
- Forme la, elemento TextBox
- Vector Markup Language (la), associazione del testo
- LA (Vector Markup Language), associazione di testo
- grafica vettoriale, associazione di testo
- LA forme, associazione di testo
- Aggiunta di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474123"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="c8a95-116">Utilizzo dell'elemento TextBox</span><span class="sxs-lookup"><span data-stu-id="c8a95-116">Using the Textbox Element</span></span>

<span data-ttu-id="c8a95-117">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c8a95-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c8a95-118">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c8a95-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c8a95-119">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c8a95-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c8a95-120">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c8a95-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c8a95-121">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c8a95-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c8a95-122">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c8a95-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="c8a95-123">Esempi:</span><span class="sxs-lookup"><span data-stu-id="c8a95-123">Examples:</span></span>

<span data-ttu-id="c8a95-124">Per aggiungere testo a un rettangolo, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:</span><span class="sxs-lookup"><span data-stu-id="c8a95-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="c8a95-125">Per allineare un collegamento ipertestuale a un rettangolo arrotondato con riempimento sfumato, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:</span><span class="sxs-lookup"><span data-stu-id="c8a95-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![textbox2.gif (1147 byte)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





<span data-ttu-id="c8a95-127">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span><span class="sxs-lookup"><span data-stu-id="c8a95-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 