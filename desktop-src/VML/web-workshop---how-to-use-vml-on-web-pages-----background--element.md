---
title: Utilizzo dell'elemento background
description: Utilizzo dell'elemento background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web Workshop, elemento background
- progettazione di pagine Web, elemento background
- Vector Markup Language (la), elemento background
- LA (Vector Markup Language), elemento background
- Vector graphics, elemento background
- elemento background
- Elementi la, background
- Forme la, elemento background
- Vector Markup Language (la), personalizzazione degli sfondi
- LA (Vector Markup Language), personalizzazione degli sfondi
- grafica vettoriale, personalizzazione degli sfondi
- LA forme, personalizzazione degli sfondi
- personalizzazione degli sfondi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872621"
---
# <a name="using-the-background-element"></a><span data-ttu-id="c15e3-116">Utilizzo dell'elemento background</span><span class="sxs-lookup"><span data-stu-id="c15e3-116">Using the Background Element</span></span>

<span data-ttu-id="c15e3-117">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c15e3-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c15e3-118">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c15e3-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c15e3-119">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c15e3-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c15e3-120">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c15e3-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c15e3-121">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c15e3-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c15e3-122">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c15e3-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c15e3-123">In questo argomento verrà illustrato come è possibile personalizzare lo sfondo di una pagina Web utilizzando l' `<background>` elemento fornito in la.</span><span class="sxs-lookup"><span data-stu-id="c15e3-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="c15e3-124">Come si è appreso dall' [argomento `<fill>` use](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , è possibile inserire il `<fill>` sottoelemento all'interno `<shape>` di, `<shapetype>` o qualsiasi elemento Shape predefinito per descrivere come riempire la forma.</span><span class="sxs-lookup"><span data-stu-id="c15e3-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="c15e3-125">Analogamente, è possibile inserire il `<fill>` sottoelemento all'interno dell' `<background>` elemento per descrivere come riempire lo sfondo di una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="c15e3-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="c15e3-126">È quindi possibile usare gli attributi di proprietà del `<fill>` sottoelemento per personalizzare l'effetto di riempimento, ad esempio [riempimento sfumato](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [riempimento pattern](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)o [riempimento immagine](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span><span class="sxs-lookup"><span data-stu-id="c15e3-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="c15e3-127">Ad esempio, per creare uno sfondo con riempimento sfumato, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:</span><span class="sxs-lookup"><span data-stu-id="c15e3-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="c15e3-128">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span><span class="sxs-lookup"><span data-stu-id="c15e3-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 