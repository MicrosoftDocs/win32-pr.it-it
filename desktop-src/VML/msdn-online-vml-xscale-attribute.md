---
title: Attributo la XScale
description: Attributo la XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337702"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="929e3-103">Attributo la XScale</span><span class="sxs-lookup"><span data-stu-id="929e3-103">VML XScale Attribute</span></span>

<span data-ttu-id="929e3-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="929e3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="929e3-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="929e3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="929e3-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="929e3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="929e3-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="929e3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="929e3-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="929e3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="929e3-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="929e3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="929e3-110">Determina se verrà utilizzato un TextPath diretto al posto del percorso della forma.</span><span class="sxs-lookup"><span data-stu-id="929e3-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="929e3-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="929e3-111">Read/write.</span></span> <span data-ttu-id="929e3-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="929e3-112">**VgTriState**.</span></span>

<span data-ttu-id="929e3-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="929e3-113">**Applies To**</span></span>

[<span data-ttu-id="929e3-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="929e3-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="929e3-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="929e3-115">**Tag Syntax**</span></span>

<span data-ttu-id="929e3-116"><v: *elemento* Style = "XScale: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="929e3-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="929e3-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="929e3-117">**Script Syntax**</span></span>

<span data-ttu-id="929e3-118">*element* . Style. XScale = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="929e3-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="929e3-119">*espressione* = *element*. Style. XScale</span><span class="sxs-lookup"><span data-stu-id="929e3-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="929e3-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="929e3-120">**Remarks**</span></span>

<span data-ttu-id="929e3-121">Se **true**, il testo viene eseguito lungo aPath da sinistra verso destra lungo il valore x del limite inferiore della forma.</span><span class="sxs-lookup"><span data-stu-id="929e3-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="929e3-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="929e3-122">The default value is **False**.</span></span>

<span data-ttu-id="929e3-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="929e3-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="929e3-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="929e3-124">**Example**</span></span>

<span data-ttu-id="929e3-125">Il testo verrà visualizzato come se fosse stato disegnato su una linea orizzontale, anche se il percorso della forma è una diagonale.</span><span class="sxs-lookup"><span data-stu-id="929e3-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 