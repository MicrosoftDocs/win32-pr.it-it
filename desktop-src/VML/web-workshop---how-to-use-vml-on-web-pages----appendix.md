---
title: Appendice (la)
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Workshop Web, spazi dei nomi
- Workshop Web, stili di comportamento
- progettazione di pagine Web, spazi dei nomi
- progettazione di pagine Web, stili di comportamento
- Vector Markup Language (la), spazi dei nomi
- LA (Vector Markup Language), spazi dei nomi
- grafica vettoriale, spazi dei nomi
- Vector Markup Language (la), stili di comportamento
- LA (Vector Markup Language), stili di comportamento
- grafica vettoriale, stili di comportamento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400135"
---
# <a name="appendix-vml"></a><span data-ttu-id="014d3-114">Appendice (la)</span><span class="sxs-lookup"><span data-stu-id="014d3-114">Appendix (VML)</span></span>

<span data-ttu-id="014d3-115">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="014d3-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="014d3-116">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="014d3-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="014d3-117">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="014d3-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="014d3-118">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="014d3-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="014d3-119">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="014d3-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="014d3-120">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="014d3-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="014d3-121">Per fare in modo che i browser sappiano come passare i dati a un processore specifico di la, è necessario digitare alcune informazioni, ad esempio gli spazi dei nomi e gli stili di comportamento.</span><span class="sxs-lookup"><span data-stu-id="014d3-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="014d3-122">È quindi possibile usare la per digitare elementi grafici nell' `<BODY>` area.</span><span class="sxs-lookup"><span data-stu-id="014d3-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="014d3-123">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="014d3-123">In this topic:</span></span>

-   <span data-ttu-id="014d3-124">[Namespaces](#namespaces) (Spazi dei nomi)</span><span class="sxs-lookup"><span data-stu-id="014d3-124">[Namespaces](#namespaces)</span></span>
-   [<span data-ttu-id="014d3-125">Stili di comportamento</span><span class="sxs-lookup"><span data-stu-id="014d3-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="014d3-126">Spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="014d3-126">Namespaces</span></span>

<span data-ttu-id="014d3-127">Un meccanismo XML indica lo spazio dei nomi da cui deriva un elemento.</span><span class="sxs-lookup"><span data-stu-id="014d3-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="014d3-128">Se si passa dall'analisi in HTML all'analisi in XML, questo meccanismo indica l'opzione all'interno del linguaggio HTML.</span><span class="sxs-lookup"><span data-stu-id="014d3-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="014d3-129">Chiedere al fornitore del processore la quali informazioni sono necessarie per lo spazio dei nomi XML.</span><span class="sxs-lookup"><span data-stu-id="014d3-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="014d3-130">Se si utilizza Microsoft Internet Explorer per eseguire il rendering di la, digitare sempre la riga seguente nel `<HTML>` Tag:</span><span class="sxs-lookup"><span data-stu-id="014d3-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="014d3-131">Queste informazioni indicano a Internet Explorer di passare allo spazio dei nomi "urn: schemas-microsoft-com: la" durante l'analisi di un tag XML con un prefisso `v:` e di passare i dati risultanti al processore la.</span><span class="sxs-lookup"><span data-stu-id="014d3-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="014d3-132">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="014d3-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="014d3-133">Stili di comportamento</span><span class="sxs-lookup"><span data-stu-id="014d3-133">Behavior Styles</span></span>

<span data-ttu-id="014d3-134">LA è definito in Microsoft Internet Explorer come comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="014d3-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="014d3-135">Per eseguire il rendering di la, digitare sempre le righe seguenti nell' `<HEAD>` area:</span><span class="sxs-lookup"><span data-stu-id="014d3-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="014d3-136">LA viene implementato in Internet Explorer tramite VGX.DLL.</span><span class="sxs-lookup"><span data-stu-id="014d3-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="014d3-137">Se l'installazione iniziale del browser non include il comportamento di la, potrebbe essere necessario aggiungerlo come opzione.</span><span class="sxs-lookup"><span data-stu-id="014d3-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="014d3-138">Non è necessario aggiungere un `<object>` tag.</span><span class="sxs-lookup"><span data-stu-id="014d3-138">You do not need to add an `<object>` tag.</span></span>

 

 
