---
title: Attributo Font-Size la
description: Attributo Font-Size la
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474179"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="95388-103">Attributo Font-Size la</span><span class="sxs-lookup"><span data-stu-id="95388-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="95388-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="95388-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="95388-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="95388-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="95388-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="95388-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="95388-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="95388-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="95388-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="95388-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="95388-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="95388-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="95388-110">Definisce la dimensione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="95388-110">Defines the size of the font.</span></span> <span data-ttu-id="95388-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="95388-111">Read/write.</span></span> <span data-ttu-id="95388-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="95388-112">**String**.</span></span>

<span data-ttu-id="95388-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="95388-113">**Applies To**</span></span>

[<span data-ttu-id="95388-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="95388-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="95388-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="95388-115">**Tag Syntax**</span></span>

<span data-ttu-id="95388-116"><v: *elemento* Style = "font-size: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="95388-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="95388-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="95388-117">**Script Syntax**</span></span>

<span data-ttu-id="95388-118">*element* . Style. FontSize = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="95388-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="95388-119">*espressione* = *element*. Style. FontSize</span><span class="sxs-lookup"><span data-stu-id="95388-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="95388-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="95388-120">**Remarks**</span></span>

<span data-ttu-id="95388-121">Le dimensioni del carattere sono definite in punti.</span><span class="sxs-lookup"><span data-stu-id="95388-121">The font size is defined in points.</span></span> <span data-ttu-id="95388-122">I valori corrispondono agli attributi di stile HTML standard.</span><span class="sxs-lookup"><span data-stu-id="95388-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="95388-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="95388-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="95388-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="95388-124">**Example**</span></span>

<span data-ttu-id="95388-125">La dimensione del carattere è 36 punti.</span><span class="sxs-lookup"><span data-stu-id="95388-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 