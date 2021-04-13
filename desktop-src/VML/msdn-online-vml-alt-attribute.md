---
title: LA alt-attributo
description: LA alt-attributo
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224008"
---
# <a name="vml-alt-attribute"></a><span data-ttu-id="1d669-103">LA alt-attributo</span><span class="sxs-lookup"><span data-stu-id="1d669-103">VML Alt Attribute</span></span>

<span data-ttu-id="1d669-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1d669-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1d669-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1d669-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1d669-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1d669-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1d669-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="1d669-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1d669-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1d669-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1d669-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1d669-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1d669-110">Definisce il testo alternativo da visualizzare anziché un elemento grafico.</span><span class="sxs-lookup"><span data-stu-id="1d669-110">Defines alternative text to be displayed instead of a graphic.</span></span> <span data-ttu-id="1d669-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1d669-111">Read/write.</span></span> <span data-ttu-id="1d669-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="1d669-112">**String**.</span></span>

<span data-ttu-id="1d669-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="1d669-113">**Applies To**</span></span>

[<span data-ttu-id="1d669-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="1d669-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1d669-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="1d669-115">**Tag Syntax**</span></span>

<span data-ttu-id="1d669-116"><v: *elemento* Alt = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1d669-116"><v: *element* alt=" *expression* "></span></span>

<span data-ttu-id="1d669-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="1d669-117">**Script Syntax**</span></span>

<span data-ttu-id="1d669-118">*element* . Alt = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="1d669-118">*element* .alt="*expression*"</span></span>

<span data-ttu-id="1d669-119">*espressione* = *elemento*. Alt</span><span class="sxs-lookup"><span data-stu-id="1d669-119">*expression*=*element*.alt</span></span>

<span data-ttu-id="1d669-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="1d669-120">**Remarks**</span></span>

<span data-ttu-id="1d669-121">L'attributo **ALT** è simile all'attributo **ALT** HTML standard.</span><span class="sxs-lookup"><span data-stu-id="1d669-121">The **Alt** attribute is similar to the standard HTML **Alt** attribute.</span></span> <span data-ttu-id="1d669-122">Questo attributo fornisce un modo per i browser che convertono il testo in sintesi vocale per descrivere elementi grafici in una pagina.</span><span class="sxs-lookup"><span data-stu-id="1d669-122">This attribute provides a way for browsers that convert text to speech to describe graphical elements on a page.</span></span>

<span data-ttu-id="1d669-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="1d669-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1d669-124">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="1d669-124">**See Also**</span></span>

[<span data-ttu-id="1d669-125">Con forme</span><span class="sxs-lookup"><span data-stu-id="1d669-125">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1d669-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="1d669-126">**Example**</span></span>

<span data-ttu-id="1d669-127">L'elemento **ALT** seguente visualizzerà la frase "Red Rectangle" nei browser che convertono le pagine Web in frasi vocali.</span><span class="sxs-lookup"><span data-stu-id="1d669-127">The **Alt** element below will display the phrase "Red rectangle" in browsers that convert Web pages to spoken phrases.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="1d669-128">[Esempio di attributo ALT](/previous-versions/bb229663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d669-128">[Alt Attribute Example](/previous-versions/bb229663(v=vs.85)).</span></span> <span data-ttu-id="1d669-129">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="1d669-129">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 