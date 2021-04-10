---
title: Attributo Text-Decoration la
description: Attributo Text-Decoration la
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963152"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="08333-103">Attributo Text-Decoration la</span><span class="sxs-lookup"><span data-stu-id="08333-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="08333-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="08333-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08333-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="08333-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08333-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="08333-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08333-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="08333-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08333-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="08333-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08333-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="08333-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08333-110">Definisce lo stile dell'effetto di testo.</span><span class="sxs-lookup"><span data-stu-id="08333-110">Defines the style of text decoration.</span></span> <span data-ttu-id="08333-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="08333-111">Read/write.</span></span> <span data-ttu-id="08333-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="08333-112">**String**.</span></span>

<span data-ttu-id="08333-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="08333-113">**Applies To**</span></span>

[<span data-ttu-id="08333-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="08333-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="08333-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="08333-115">**Tag Syntax**</span></span>

<span data-ttu-id="08333-116"><v: *elemento* Style = "text-decoration: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="08333-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="08333-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="08333-117">**Script Syntax**</span></span>

<span data-ttu-id="08333-118">*element* . Style. TextDecoration = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="08333-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="08333-119">*espressione* = *element*. Style. TextDecoration</span><span class="sxs-lookup"><span data-stu-id="08333-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="08333-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="08333-120">**Remarks**</span></span>

<span data-ttu-id="08333-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="08333-121">Values include:</span></span>

-   <span data-ttu-id="08333-122">Nessuno (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="08333-122">none (default)</span></span>
-   <span data-ttu-id="08333-123">sottolineato</span><span class="sxs-lookup"><span data-stu-id="08333-123">underline</span></span>
-   <span data-ttu-id="08333-124">linea sopra</span><span class="sxs-lookup"><span data-stu-id="08333-124">overline</span></span>
-   <span data-ttu-id="08333-125">line-through</span><span class="sxs-lookup"><span data-stu-id="08333-125">line-through</span></span>
-   <span data-ttu-id="08333-126">blink</span><span class="sxs-lookup"><span data-stu-id="08333-126">blink</span></span>

<span data-ttu-id="08333-127">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="08333-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="08333-128">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="08333-128">**Example**</span></span>

<span data-ttu-id="08333-129">Il testo sarà sottolineato.</span><span class="sxs-lookup"><span data-stu-id="08333-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 