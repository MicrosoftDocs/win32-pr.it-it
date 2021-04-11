---
title: Attributo HRef (Shape) (la)
description: Attributo HRef (Shape) (la)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047270"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="0956e-103">Attributo HRef (Shape) (la)</span><span class="sxs-lookup"><span data-stu-id="0956e-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="0956e-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0956e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0956e-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="0956e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0956e-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="0956e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0956e-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="0956e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0956e-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0956e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0956e-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0956e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0956e-110">Definisce un URL per una forma.</span><span class="sxs-lookup"><span data-stu-id="0956e-110">Defines a URL for a shape.</span></span> <span data-ttu-id="0956e-111">Quando si fa clic sulla forma, il browser caricherà l'URL.</span><span class="sxs-lookup"><span data-stu-id="0956e-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="0956e-112">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0956e-112">Read/write.</span></span> <span data-ttu-id="0956e-113">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="0956e-113">**String**.</span></span>

<span data-ttu-id="0956e-114">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="0956e-114">**Applies To**</span></span>

[<span data-ttu-id="0956e-115">Con forme</span><span class="sxs-lookup"><span data-stu-id="0956e-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0956e-116">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="0956e-116">**Tag Syntax**</span></span>

<span data-ttu-id="0956e-117"><v: *element* href = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0956e-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="0956e-118">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="0956e-118">**Script Syntax**</span></span>

<span data-ttu-id="0956e-119">*element* . href = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="0956e-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="0956e-120">*espressione* = *elemento*. href</span><span class="sxs-lookup"><span data-stu-id="0956e-120">*expression*=*element*.href</span></span>

<span data-ttu-id="0956e-121">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="0956e-121">**Remarks**</span></span>

<span data-ttu-id="0956e-122">L'attributo **href** è simile all'attributo HTML **href** standard degli ancoraggi.</span><span class="sxs-lookup"><span data-stu-id="0956e-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="0956e-123">L'uso di **href** consente di creare facilmente pulsanti interessanti in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="0956e-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="0956e-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="0956e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="0956e-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0956e-125">**Example**</span></span>

<span data-ttu-id="0956e-126">Quando si fa clic sul rettangolo, il browser caricherà il home page Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="0956e-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="0956e-127">[Esempio di attributo href](/previous-versions/bb229672(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0956e-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="0956e-128">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="0956e-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 