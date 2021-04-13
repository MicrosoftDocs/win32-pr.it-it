---
title: Introduzione a la
description: Introduzione a la
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Vector Markup Language (la), riferimento
- LA (Vector Markup Language), riferimento
- grafica vettoriale, riferimento la
- grafica vettoriale, Vector Markup Language (la)
- riferimento per Vector Markup Language (la)
- Riferimento a la
- Vector Markup Language (la), elemento Shape
- LA (Vector Markup Language), elemento Shape
- graphics vettoriale, elemento Shape
- Shape-elemento
- Elementi la, forma
- Vector Markup Language (la), VBScript
- LA (Vector Markup Language), VBScript
- Vector Markup Language (la), JavaScript
- LA (Vector Markup Language), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399182"
---
# <a name="vml-introduction"></a><span data-ttu-id="3e342-118">Introduzione a la</span><span class="sxs-lookup"><span data-stu-id="3e342-118">VML Introduction</span></span>

<span data-ttu-id="3e342-119">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3e342-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3e342-120">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3e342-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3e342-121">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3e342-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3e342-122">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3e342-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3e342-123">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3e342-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3e342-124">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3e342-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3e342-125">Questo documento fornisce un riferimento dettagliato completo all'implementazione della Vector Markup Language (la) fornita con Microsoft Office 2000.</span><span class="sxs-lookup"><span data-stu-id="3e342-125">This document gives a complete detailed reference to the implementation of the Vector Markup Language (VML) that is shipped with Microsoft Office 2000.</span></span> <span data-ttu-id="3e342-126">Altre implementazioni possono variare.</span><span class="sxs-lookup"><span data-stu-id="3e342-126">Other implementations may vary.</span></span> <span data-ttu-id="3e342-127">Per ulteriori informazioni su la come standard, vedere la [specifica la](https://www.w3.org/TR/NOTE-datetime.html) .</span><span class="sxs-lookup"><span data-stu-id="3e342-127">Consult the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) for more information about VML as a standard.</span></span>

<span data-ttu-id="3e342-128">LA è definito come un set di elementi XML e gli attributi corrispondenti per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="3e342-128">VML is defined as a set of XML elements and the corresponding attributes for each element.</span></span> <span data-ttu-id="3e342-129">Poiché l'elemento **Shape** è il blocco predefinito di base di la, fare clic [qui](shape-element--vml.md) per iniziare il riferimento.</span><span class="sxs-lookup"><span data-stu-id="3e342-129">Since the **Shape** element is the basic building block of VML, click [here](shape-element--vml.md) to begin the reference.</span></span>

<span data-ttu-id="3e342-130">Si noti che questo riferimento contiene diversi esempi e demo.</span><span class="sxs-lookup"><span data-stu-id="3e342-130">Note that this reference contains several examples and demos.</span></span> <span data-ttu-id="3e342-131">Per visualizzare il la Live, è necessario che Microsoft Internet Explorer 5,0 o versione successiva sia installato.</span><span class="sxs-lookup"><span data-stu-id="3e342-131">You must have Microsoft Internet Explorer 5.0 or greater installed to view the live VML.</span></span>

<span data-ttu-id="3e342-132">Oltre alle informazioni sull'utilizzo di elementi e attributi come tag XML che estendono HTML, questo riferimento contiene sintassi ed esempi che illustrano come utilizzare lo scripting e le funzionalità Document Object Model di Internet Explorer 5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3e342-132">In addition to the information about using elements and attributes as XML tags that extend HTML, this reference contains syntax and examples that show how to use the scripting and the Document Object Model features of Internet Explorer 5 or greater.</span></span> <span data-ttu-id="3e342-133">L'uso di script con la consente di creare elementi "immediatamente" e di modificare gli attributi in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="3e342-133">Using script with VML enables you to create elements "on the fly" and manipulate attributes in real time.</span></span>

<span data-ttu-id="3e342-134">Questo esempio di questo riferimento usa VBScript e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3e342-134">This examples in this reference uses VBScript and Javascript.</span></span> <span data-ttu-id="3e342-135">Se si utilizza un linguaggio di scripting diverso da quello illustrato in un esempio, è necessario trovare la corrispondenza tra maiuscole e minuscole per tutti i nomi di elementi e attributi.</span><span class="sxs-lookup"><span data-stu-id="3e342-135">If you use use a different scripting language than the one shown in an example, you must match the case of all element and attribute names.</span></span> <span data-ttu-id="3e342-136">Il riferimento fornisce la sintassi di scripting corretta per i linguaggi con distinzione tra maiuscole e minuscole, ad esempio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3e342-136">The reference gives scripting syntax that is correct for case-sensitive languages such as JavaScript.</span></span> <span data-ttu-id="3e342-137">In caso di dubbi sul caso di caratteri corretti, utilizzare un Visualizzatore oggetti (ad esempio OLEView) per esplorare l'VGX.DLL per determinare il caso esatto di un elemento o di un attributo.</span><span class="sxs-lookup"><span data-stu-id="3e342-137">If in doubt regarding the correct character case, use an object browser (such as OLEView) to explore the VGX.DLL to determine the exact case of an element or attribute.</span></span> <span data-ttu-id="3e342-138">Si noti che quando la viene usato come tag XML, la distinzione tra maiuscole e minuscole dipende dal tipo di documento del documento sottostante.</span><span class="sxs-lookup"><span data-stu-id="3e342-138">Note that when VML is used as XML tags, case sensitivity depends on the document type of you underlying document.</span></span> <span data-ttu-id="3e342-139">Se si usa una modalità Strict. Il DOCTYPE, gli elementi e gli attributi faranno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3e342-139">If you are using a strict mode !DOCTYPE, elements and attributes will be case sensitive.</span></span>

[<span data-ttu-id="3e342-140">Riferimento la</span><span class="sxs-lookup"><span data-stu-id="3e342-140">The VML Reference</span></span>](shape-element--vml.md)

 

 