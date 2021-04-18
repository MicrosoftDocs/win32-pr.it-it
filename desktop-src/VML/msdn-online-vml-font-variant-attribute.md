---
title: Attributo Font-Variant la
description: Attributo Font-Variant la
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399092"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="2a4c5-103">Attributo Font-Variant la</span><span class="sxs-lookup"><span data-stu-id="2a4c5-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="2a4c5-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2a4c5-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2a4c5-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2a4c5-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2a4c5-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2a4c5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2a4c5-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2a4c5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2a4c5-110">Definisce lo stile Variant di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-110">Defines the variant style of a font.</span></span> <span data-ttu-id="2a4c5-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-111">Read/write.</span></span> <span data-ttu-id="2a4c5-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-112">**String**.</span></span>

<span data-ttu-id="2a4c5-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="2a4c5-113">**Applies To**</span></span>

[<span data-ttu-id="2a4c5-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="2a4c5-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="2a4c5-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="2a4c5-115">**Tag Syntax**</span></span>

<span data-ttu-id="2a4c5-116"><v: *element* Style = "font-variant: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2a4c5-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="2a4c5-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="2a4c5-117">**Script Syntax**</span></span>

<span data-ttu-id="2a4c5-118">*element* . Style. fontVariant = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="2a4c5-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="2a4c5-119">*espressione* = *element*. Style. fontVariant</span><span class="sxs-lookup"><span data-stu-id="2a4c5-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="2a4c5-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="2a4c5-120">**Remarks**</span></span>

<span data-ttu-id="2a4c5-121">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2a4c5-121">The values are:</span></span>

-   <span data-ttu-id="2a4c5-122">normale (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a4c5-122">normal (default)</span></span>
-   <span data-ttu-id="2a4c5-123">Small-Caps</span><span class="sxs-lookup"><span data-stu-id="2a4c5-123">small-caps</span></span>

<span data-ttu-id="2a4c5-124">I valori corrispondono agli attributi di stile HTML standard.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="2a4c5-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="2a4c5-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="2a4c5-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="2a4c5-126">**Example**</span></span>

<span data-ttu-id="2a4c5-127">Viene eseguito il rendering del tipo di carattere con lettere maiuscole minuscole.</span><span class="sxs-lookup"><span data-stu-id="2a4c5-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 