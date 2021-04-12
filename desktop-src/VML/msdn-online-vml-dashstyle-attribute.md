---
title: Attributo DashStyle di la
description: Attributo DashStyle di la
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337718"
---
# <a name="vml-dashstyle-attribute"></a><span data-ttu-id="a1ae6-103">Attributo DashStyle di la</span><span class="sxs-lookup"><span data-stu-id="a1ae6-103">VML DashStyle Attribute</span></span>

<span data-ttu-id="a1ae6-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a1ae6-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a1ae6-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a1ae6-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a1ae6-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a1ae6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a1ae6-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a1ae6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a1ae6-110">Specifica il punto e il tratteggio per un tratto.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-110">Specifies the dot and dash pattern for a stroke.</span></span> <span data-ttu-id="a1ae6-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-111">Read/write.</span></span> <span data-ttu-id="a1ae6-112">**VgLineDashStyle**.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-112">**VgLineDashStyle**.</span></span>

<span data-ttu-id="a1ae6-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a1ae6-113">**Applies To**</span></span>

[<span data-ttu-id="a1ae6-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="a1ae6-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="a1ae6-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a1ae6-115">**Tag Syntax**</span></span>

<span data-ttu-id="a1ae6-116"><v: *element* DashStyle = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a1ae6-116"><v: *element* dashstyle=" *expression* "></span></span>

<span data-ttu-id="a1ae6-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="a1ae6-117">**Script Syntax**</span></span>

<span data-ttu-id="a1ae6-118">*element* . DashStyle = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-118">*element* .dashstyle="*expression*"</span></span>

<span data-ttu-id="a1ae6-119">*espressione* = *elemento*. DashStyle</span><span class="sxs-lookup"><span data-stu-id="a1ae6-119">*expression*=*element*.dashstyle</span></span>

<span data-ttu-id="a1ae6-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a1ae6-120">**Remarks**</span></span>

<span data-ttu-id="a1ae6-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="a1ae6-121">Values include:</span></span>

-   <span data-ttu-id="a1ae6-122">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="a1ae6-122">Solid (default)</span></span>
-   <span data-ttu-id="a1ae6-123">ShortDash</span><span class="sxs-lookup"><span data-stu-id="a1ae6-123">ShortDash</span></span>
-   <span data-ttu-id="a1ae6-124">ShortDot</span><span class="sxs-lookup"><span data-stu-id="a1ae6-124">ShortDot</span></span>
-   <span data-ttu-id="a1ae6-125">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="a1ae6-125">ShortDashDot</span></span>
-   <span data-ttu-id="a1ae6-126">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="a1ae6-126">ShortDashDotDot</span></span>
-   <span data-ttu-id="a1ae6-127">Punto</span><span class="sxs-lookup"><span data-stu-id="a1ae6-127">Dot</span></span>
-   <span data-ttu-id="a1ae6-128">Trattino</span><span class="sxs-lookup"><span data-stu-id="a1ae6-128">Dash</span></span>
-   <span data-ttu-id="a1ae6-129">LongDash</span><span class="sxs-lookup"><span data-stu-id="a1ae6-129">LongDash</span></span>
-   <span data-ttu-id="a1ae6-130">DashDot</span><span class="sxs-lookup"><span data-stu-id="a1ae6-130">DashDot</span></span>
-   <span data-ttu-id="a1ae6-131">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="a1ae6-131">LongDashDot</span></span>
-   <span data-ttu-id="a1ae6-132">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="a1ae6-132">LongDashDotDot</span></span>

<span data-ttu-id="a1ae6-133">L'attributo **DashStyle** consente all'utente di specificare un modello Dash definito in modo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-133">The **DashStyle** attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="a1ae6-134">Questa operazione viene eseguita usando una serie di numeri.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-134">This is done using a series of numbers.</span></span> <span data-ttu-id="a1ae6-135">Gli stili Dash sono definiti in termini di lunghezza del trattino (la parte disegnata del tratto) e della lunghezza dello spazio tra i trattini.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-135">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="a1ae6-136">Le lunghezze sono relative alla lunghezza riga: la lunghezza di "1" è uguale alla lunghezza riga.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-136">The lengths are relative to the line width: a length of "1" is equal to the line width.</span></span> <span data-ttu-id="a1ae6-137">Lo stile di **estremità** viene applicato a ogni trattino, lo stile della freccia non lo è.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-137">The **EndCap** style is applied to each dash, the arrow style is not.</span></span> <span data-ttu-id="a1ae6-138">La stringa definisce prima di tutto la lunghezza del trattino, quindi la lunghezza dello spazio.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-138">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="a1ae6-139">Questa operazione può essere ripetuta per formare stili trattini complessi.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-139">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="a1ae6-140">La stringa deve sempre contenere una coppia di numeri; Se contiene un numero dispari di numeri, l'ultimo può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-140">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span>

<span data-ttu-id="a1ae6-141">Nella tabella seguente sono elencati alcuni valori tipici e una descrizione dell'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-141">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="a1ae6-142">"0" implica un punto che dovrebbe essere quadruplo simmetrico (con i tappi di fine round deve essere un cerchio).</span><span class="sxs-lookup"><span data-stu-id="a1ae6-142">"0" implies a dot that should be fourfold symmetrical (with round end caps it should be a circle).</span></span> <span data-ttu-id="a1ae6-143">Se il limite finale della riga è "flat", un visualizzatore deve scegliere un trattino del sistema operativo predefinito, laddove possibile (in altre parole.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-143">If the line end cap is "flat," a viewer should choose a built-in operating system dash where possible (in other words.</span></span> <span data-ttu-id="a1ae6-144">un elemento che è veloce da creare.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-144">something that is fast to draw.).</span></span> <span data-ttu-id="a1ae6-145">La tabella seguente illustra alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-145">The following table shows some examples.</span></span>



| <span data-ttu-id="a1ae6-146">DashStyle</span><span class="sxs-lookup"><span data-stu-id="a1ae6-146">DashStyle</span></span>     | <span data-ttu-id="a1ae6-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1ae6-147">Description</span></span>                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ae6-148">"2 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-148">"2 2"</span></span>         | <span data-ttu-id="a1ae6-149">Trattini brevi.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-149">Short-dashes.</span></span> <span data-ttu-id="a1ae6-150">Ogni trattino e lo spazio tra corrispondono al doppio della larghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-150">Each dash and the space between is twice the width of the line.</span></span>                        |
| <span data-ttu-id="a1ae6-151">"0 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-151">"0 2"</span></span>         | <span data-ttu-id="a1ae6-152">Punti.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-152">Dots.</span></span> <span data-ttu-id="a1ae6-153">Lo spazio tra corrisponde al doppio della larghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-153">Space between is twice the width of the line.</span></span>                                                  |
| <span data-ttu-id="a1ae6-154">"2 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-154">"2 2 0 2"</span></span>     | <span data-ttu-id="a1ae6-155">Punto di trattino breve.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-155">Short dash dot.</span></span>                                                                                      |
| <span data-ttu-id="a1ae6-156">"2 2 0 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-156">"2 2 0 2 0 2"</span></span> | <span data-ttu-id="a1ae6-157">Punto di tratteggio breve.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-157">Short dash dot dot.</span></span>                                                                                  |
| <span data-ttu-id="a1ae6-158">"1 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-158">"1 2"</span></span>         | <span data-ttu-id="a1ae6-159">Punto.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-159">Dot.</span></span> <span data-ttu-id="a1ae6-160">Ogni trattino è la larghezza della linea, mentre ogni spazio corrisponde al doppio della larghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-160">Each dash is the width of the line, while each space is twice the width of the line.</span></span>            |
| <span data-ttu-id="a1ae6-161">"4 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-161">"4 2"</span></span>         | <span data-ttu-id="a1ae6-162">Dash.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-162">Dash.</span></span> <span data-ttu-id="a1ae6-163">Ogni trattino è quattro volte la larghezza della linea mentre ogni spazio corrisponde al doppio della larghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-163">Each dash is four times the width of the line while each space is twice the width of the line.</span></span> |
| <span data-ttu-id="a1ae6-164">"8 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-164">"8 2"</span></span>         | <span data-ttu-id="a1ae6-165">Trattino lungo.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-165">Long dash.</span></span>                                                                                           |
| <span data-ttu-id="a1ae6-166">"4 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-166">"4 2 1 2"</span></span>     | <span data-ttu-id="a1ae6-167">Punto tratteggiato.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-167">Dash dot.</span></span>                                                                                            |
| <span data-ttu-id="a1ae6-168">"8 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-168">"8 2 1 2"</span></span>     | <span data-ttu-id="a1ae6-169">Punto di tratteggio lungo.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-169">Long dash dot.</span></span>                                                                                       |
| <span data-ttu-id="a1ae6-170">"8 2 1 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="a1ae6-170">"8 2 1 2 1 2"</span></span> | <span data-ttu-id="a1ae6-171">Punto di tratteggio lungo.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-171">Long dash dot dot.</span></span>                                                                                   |



 

<span data-ttu-id="a1ae6-172">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="a1ae6-172">*VML Standard Attribute*</span></span>

<span data-ttu-id="a1ae6-173">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a1ae6-173">**Example**</span></span>

<span data-ttu-id="a1ae6-174">La forma presenta uno stile tratteggiato di trattini alternativi e punti.</span><span class="sxs-lookup"><span data-stu-id="a1ae6-174">The shape has a dash style of alternating dashes and dots.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 