---
title: Attributo font la
description: Attributo font la
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300398"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="5150b-103">Attributo font la</span><span class="sxs-lookup"><span data-stu-id="5150b-103">VML Font Attribute</span></span>

<span data-ttu-id="5150b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5150b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5150b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5150b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5150b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5150b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5150b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="5150b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5150b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5150b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5150b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5150b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5150b-110">Specifica un valore composto di attributi del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5150b-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="5150b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5150b-111">Read/write.</span></span> <span data-ttu-id="5150b-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="5150b-112">**String**.</span></span>

<span data-ttu-id="5150b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="5150b-113">**Applies To**</span></span>

[<span data-ttu-id="5150b-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="5150b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5150b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="5150b-115">**Tag Syntax**</span></span>

<span data-ttu-id="5150b-116"><v: *elemento* Style = "font: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5150b-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="5150b-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="5150b-117">**Script Syntax**</span></span>

<span data-ttu-id="5150b-118">*element* . Style. font = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="5150b-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="5150b-119">*espressione* = *element*. Style. font</span><span class="sxs-lookup"><span data-stu-id="5150b-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="5150b-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="5150b-120">**Remarks**</span></span>

<span data-ttu-id="5150b-121">Definisce gli attributi di un tipo di carattere, inclusi famiglia, stile, peso, dimensioni e Variant.</span><span class="sxs-lookup"><span data-stu-id="5150b-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="5150b-122">L'ordine delle definizioni nella stringa è: tipo di **carattere**, **variante del tipo** di carattere, **spessore** del carattere, dimensioni del **carattere**, **altezza della riga** e **famiglia di caratteri**.</span><span class="sxs-lookup"><span data-stu-id="5150b-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="5150b-123">I valori corrispondono agli attributi di stile HTML standard.</span><span class="sxs-lookup"><span data-stu-id="5150b-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="5150b-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="5150b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5150b-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="5150b-125">**Example**</span></span>

<span data-ttu-id="5150b-126">Il tipo di carattere del testo TextPath è Italic, Small Caps, Bold, 36 Point Arial.</span><span class="sxs-lookup"><span data-stu-id="5150b-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 