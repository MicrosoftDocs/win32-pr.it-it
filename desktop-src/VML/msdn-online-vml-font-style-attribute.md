---
title: Attributo Font-Style la
description: Attributo Font-Style la
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046818"
---
# <a name="vml-font-style-attribute"></a><span data-ttu-id="8e954-103">Attributo Font-Style la</span><span class="sxs-lookup"><span data-stu-id="8e954-103">VML Font-Style Attribute</span></span>

<span data-ttu-id="8e954-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8e954-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e954-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="8e954-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e954-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="8e954-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e954-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="8e954-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e954-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e954-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e954-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e954-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e954-110">Definisce la quantità di inclinazione per un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8e954-110">Defines the amount of slant for a font.</span></span> <span data-ttu-id="8e954-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8e954-111">Read/write.</span></span> <span data-ttu-id="8e954-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="8e954-112">**String**.</span></span>

<span data-ttu-id="8e954-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="8e954-113">**Applies To**</span></span>

[<span data-ttu-id="8e954-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="8e954-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="8e954-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="8e954-115">**Tag Syntax**</span></span>

<span data-ttu-id="8e954-116"><v: *elemento* Style = "font-style: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8e954-116"><v: *element* style="font-style: *expression* "></span></span>

<span data-ttu-id="8e954-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="8e954-117">**Script Syntax**</span></span>

<span data-ttu-id="8e954-118">*element* . Style. FontStyle = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="8e954-118">*element* .style.fontstyle="*expression*"</span></span>

<span data-ttu-id="8e954-119">*espressione* = *element*. Style. FontStyle</span><span class="sxs-lookup"><span data-stu-id="8e954-119">*expression*=*element*.style.fontstyle</span></span>

<span data-ttu-id="8e954-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="8e954-120">**Remarks**</span></span>

<span data-ttu-id="8e954-121">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="8e954-121">The values are:</span></span>

-   <span data-ttu-id="8e954-122">normale (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e954-122">normal (default)</span></span>
-   <span data-ttu-id="8e954-123">obliquo</span><span class="sxs-lookup"><span data-stu-id="8e954-123">oblique</span></span>
-   <span data-ttu-id="8e954-124">Corsivo</span><span class="sxs-lookup"><span data-stu-id="8e954-124">italic</span></span>

<span data-ttu-id="8e954-125">Molti browser eseguono il rendering obliquo come corsivo.</span><span class="sxs-lookup"><span data-stu-id="8e954-125">Most browsers render oblique as italic.</span></span> <span data-ttu-id="8e954-126">I valori corrispondono agli attributi di stile HTML standard.</span><span class="sxs-lookup"><span data-stu-id="8e954-126">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="8e954-127">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="8e954-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="8e954-128">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="8e954-128">**Example**</span></span>

<span data-ttu-id="8e954-129">Il tipo di carattere è corsivo (inclinato).</span><span class="sxs-lookup"><span data-stu-id="8e954-129">The font is italic (slanted).</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 