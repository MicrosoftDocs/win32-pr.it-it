---
title: Attributo di destinazione la
description: Attributo di destinazione la
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299847"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="102b0-103">Attributo di destinazione la</span><span class="sxs-lookup"><span data-stu-id="102b0-103">VML Target Attribute</span></span>

<span data-ttu-id="102b0-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="102b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="102b0-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="102b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="102b0-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="102b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="102b0-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="102b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="102b0-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="102b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="102b0-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="102b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="102b0-110">Definisce un frame o una finestra in cui viene visualizzato un URL.</span><span class="sxs-lookup"><span data-stu-id="102b0-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="102b0-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="102b0-111">Read/write.</span></span> <span data-ttu-id="102b0-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="102b0-112">**String**.</span></span>

<span data-ttu-id="102b0-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="102b0-113">**Applies To**</span></span>

[<span data-ttu-id="102b0-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="102b0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="102b0-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="102b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="102b0-116"><v: *elemento* target = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="102b0-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="102b0-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="102b0-117">**Remarks**</span></span>

<span data-ttu-id="102b0-118">L'attributo di **destinazione** è simile all'attributo di **destinazione** HTML standard degli ancoraggi.</span><span class="sxs-lookup"><span data-stu-id="102b0-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="102b0-119">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="102b0-119">Values include:</span></span>



| <span data-ttu-id="102b0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="102b0-120">Value</span></span>      | <span data-ttu-id="102b0-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102b0-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102b0-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="102b0-122">TargetName</span></span> | <span data-ttu-id="102b0-123">Stringa contenente il nome del frame o della finestra in cui caricare il documento.</span><span class="sxs-lookup"><span data-stu-id="102b0-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="102b0-124">\_vuoto</span><span class="sxs-lookup"><span data-stu-id="102b0-124">\_blank</span></span>    | <span data-ttu-id="102b0-125">Specifica che il documento collegato viene caricato in una nuova finestra vuota.</span><span class="sxs-lookup"><span data-stu-id="102b0-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="102b0-126">Questa finestra non è denominata.</span><span class="sxs-lookup"><span data-stu-id="102b0-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="102b0-127">\_media</span><span class="sxs-lookup"><span data-stu-id="102b0-127">\_media</span></span>    | <span data-ttu-id="102b0-128">A partire da Internet Explorer 6 per Windows XP Service Pack 2, l' \_ attributo supporto è obsoleto e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="102b0-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="102b0-129">Disponibile per la prima volta in Internet Explorer 6, questo valore specifica che il documento collegato deve essere caricato sulla barra multimediale.</span><span class="sxs-lookup"><span data-stu-id="102b0-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="102b0-130">\_padre</span><span class="sxs-lookup"><span data-stu-id="102b0-130">\_parent</span></span>   | <span data-ttu-id="102b0-131">Specifica che il documento collegato viene caricato nell'elemento padre diretto del documento contenente il collegamento.</span><span class="sxs-lookup"><span data-stu-id="102b0-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="102b0-132">\_ricerca</span><span class="sxs-lookup"><span data-stu-id="102b0-132">\_search</span></span>   | <span data-ttu-id="102b0-133">A partire da Internet Explorer 7 per Windows XP Service Pack 2,: l' \_ attributo di ricerca è obsoleto e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="102b0-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="102b0-134">Disponibile per la prima volta in Internet Explorer 6, questo valore specifica che il documento collegato deve essere caricato nel riquadro di ricerca del browser.</span><span class="sxs-lookup"><span data-stu-id="102b0-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="102b0-135">\_auto</span><span class="sxs-lookup"><span data-stu-id="102b0-135">\_self</span></span>     | <span data-ttu-id="102b0-136">Specifica che il documento collegato viene caricato nella finestra in cui è stato fatto clic sul collegamento (la finestra attiva).</span><span class="sxs-lookup"><span data-stu-id="102b0-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="102b0-137">\_In alto</span><span class="sxs-lookup"><span data-stu-id="102b0-137">\_top</span></span>      | <span data-ttu-id="102b0-138">Specifica che il documento collegato viene caricato nella finestra in primo piano.</span><span class="sxs-lookup"><span data-stu-id="102b0-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="102b0-139">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="102b0-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="102b0-140">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="102b0-140">**Example**</span></span>

<span data-ttu-id="102b0-141">Quando si fa clic sul rettangolo, il browser carica il home page Microsoft Corporation nella stessa finestra.</span><span class="sxs-lookup"><span data-stu-id="102b0-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="102b0-142">[Esempio di attributo di destinazione](/previous-versions/bb264096(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="102b0-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="102b0-143">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="102b0-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 