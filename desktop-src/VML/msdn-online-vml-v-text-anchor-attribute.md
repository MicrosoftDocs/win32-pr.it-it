---
title: LA V-text-anchor-attributo
description: LA V-text-anchor-attributo
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399376"
---
# <a name="vml-v-text-anchor-attribute"></a><span data-ttu-id="33628-103">LA V-text-anchor-attributo</span><span class="sxs-lookup"><span data-stu-id="33628-103">VML V-Text-Anchor Attribute</span></span>

<span data-ttu-id="33628-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="33628-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="33628-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="33628-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="33628-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="33628-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="33628-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="33628-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="33628-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="33628-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="33628-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="33628-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="33628-110">Definisce l'ancoraggio verticale del testo in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="33628-110">Defines the vertical anchoring of text in a textbox.</span></span> <span data-ttu-id="33628-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="33628-111">Read/write.</span></span> <span data-ttu-id="33628-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="33628-112">**String**.</span></span>

<span data-ttu-id="33628-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="33628-113">**Applies To**</span></span>

[<span data-ttu-id="33628-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="33628-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="33628-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="33628-115">**Tag Syntax**</span></span>

<span data-ttu-id="33628-116"><v: *element* v-text-anchor = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="33628-116"><v: *element* v-text-anchor=" *expression* "></span></span>

<span data-ttu-id="33628-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="33628-117">**Remarks**</span></span>

<span data-ttu-id="33628-118">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="33628-118">Values include:</span></span>

-   <span data-ttu-id="33628-119">**Top** (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33628-119">**top** (default)</span></span>
-   <span data-ttu-id="33628-120">**intermedio**</span><span class="sxs-lookup"><span data-stu-id="33628-120">**middle**</span></span>
-   <span data-ttu-id="33628-121">**parte inferiore**</span><span class="sxs-lookup"><span data-stu-id="33628-121">**bottom**</span></span>
-   <span data-ttu-id="33628-122">**in alto al centro**</span><span class="sxs-lookup"><span data-stu-id="33628-122">**top-center**</span></span>
-   <span data-ttu-id="33628-123">**Centro centrale**</span><span class="sxs-lookup"><span data-stu-id="33628-123">**middle-center**</span></span>
-   <span data-ttu-id="33628-124">**in basso al centro**</span><span class="sxs-lookup"><span data-stu-id="33628-124">**bottom-center**</span></span>
-   <span data-ttu-id="33628-125">**Top-Baseline**</span><span class="sxs-lookup"><span data-stu-id="33628-125">**top-baseline**</span></span>
-   <span data-ttu-id="33628-126">**linea di base inferiore**</span><span class="sxs-lookup"><span data-stu-id="33628-126">**bottom-baseline**</span></span>
-   <span data-ttu-id="33628-127">**Top-Center-Baseline**</span><span class="sxs-lookup"><span data-stu-id="33628-127">**top-center-baseline**</span></span>
-   <span data-ttu-id="33628-128">**Bottom-Center-Baseline**</span><span class="sxs-lookup"><span data-stu-id="33628-128">**bottom-center-baseline**</span></span>

<span data-ttu-id="33628-129">Il testo verrà ancorato a una posizione verticale nella casella di testo come indicato dal valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="33628-129">The text will be anchored to a vertical position in the textbox as indicated by the attribute value.</span></span> <span data-ttu-id="33628-130">L'allineamento di un ancoraggio del testo diventa evidente solo se [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) è **false**.</span><span class="sxs-lookup"><span data-stu-id="33628-130">The alignment of a text anchor only becomes evident if [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) is **False**.</span></span> <span data-ttu-id="33628-131">Questo attributo è diverso dall'attributo di stile **allineamento verticale** , che viene usato per i linguaggi ideogrammi.</span><span class="sxs-lookup"><span data-stu-id="33628-131">This attribute is different from the **Vertical-Align** Style attribute, which is used for ideographic languages.</span></span>

<span data-ttu-id="33628-132">Questo attributo viene utilizzato da Microsoft Office per archiviare i dati nei documenti Web, ma non viene eseguito il rendering in Microsoft Internet Explorer 5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="33628-132">This attribute is used by Microsoft Office to store data in Web documents but does not render in Microsoft Internet Explorer 5 or greater.</span></span>

<span data-ttu-id="33628-133">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="33628-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="33628-134">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="33628-134">**Example**</span></span>

<span data-ttu-id="33628-135">Il testo è allineato alla parte inferiore della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="33628-135">The text is aligned to the bottom of the textbox.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 