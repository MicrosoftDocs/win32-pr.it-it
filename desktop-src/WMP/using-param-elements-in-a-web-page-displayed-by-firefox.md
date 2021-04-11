---
title: Uso di elementi PARAM in una pagina Web visualizzata da Firefox
description: Uso di elementi PARAM in una pagina Web visualizzata da Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Media Player di Windows, elementi PARAM nell'elemento OBJECT
- Modello a oggetti di Windows Media Player, elementi PARAM nell'elemento OBJECT
- modello a oggetti, elementi PARAM nell'elemento OBJECT
- Windows Media Player Mobile, elementi PARAM nell'elemento oggetto
- Controllo ActiveX Windows Media Player, elementi PARAM nell'elemento OBJECT
- Controllo ActiveX Windows Media Player Mobile, elementi PARAM nell'elemento oggetto
- Controllo ActiveX, elementi PARAM nell'elemento OBJECT
- incorporamento, pagine Web
- Incorporamento di pagine Web, elementi PARAM nell'elemento OBJECT
- Elementi PARAM nell'elemento OBJECT
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, elementi PARAM nell'elemento OBJECT
- Incorporamento di pagine Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332868"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="d8676-122">Uso di elementi PARAM in una pagina Web visualizzata da Firefox</span><span class="sxs-lookup"><span data-stu-id="d8676-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="d8676-123">È possibile usare gli elementi PARAM all'interno di un elemento oggetto per impostare lo stato iniziale del controllo Player.</span><span class="sxs-lookup"><span data-stu-id="d8676-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="d8676-124">Ad esempio, gli elementi PARAM nell'esempio seguente specificano che il controllo deve riprodurre automaticamente Seattle. wmv.</span><span class="sxs-lookup"><span data-stu-id="d8676-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="d8676-125">La maggior parte degli elementi PARAM può essere interpretata da Internet Explorer e da Firefox.</span><span class="sxs-lookup"><span data-stu-id="d8676-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="d8676-126">Tuttavia, esistono alcuni elementi PARAM che il plug-in di Firefox non supporta.</span><span class="sxs-lookup"><span data-stu-id="d8676-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="d8676-127">Per informazioni sugli elementi PARAM supportati dal plug-in di Firefox, vedere [elementi param in un elemento Object](param-elements-in-an-object-element.md).</span><span class="sxs-lookup"><span data-stu-id="d8676-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8676-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8676-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8676-129">**Uso del controllo Media Player Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="d8676-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




