---
title: Attributo INSERT la
description: Attributo INSERT la
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117906"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="b9813-103">Attributo INSERT la</span><span class="sxs-lookup"><span data-stu-id="b9813-103">VML Inset Attribute</span></span>

<span data-ttu-id="b9813-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b9813-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b9813-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b9813-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b9813-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b9813-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b9813-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b9813-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b9813-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b9813-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b9813-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b9813-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b9813-110">Specifica i valori del margine interno per il testo della casella di testo.</span><span class="sxs-lookup"><span data-stu-id="b9813-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="b9813-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b9813-111">Read/write.</span></span> <span data-ttu-id="b9813-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="b9813-112">**String**.</span></span>

<span data-ttu-id="b9813-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="b9813-113">**Applies To**</span></span>

[<span data-ttu-id="b9813-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="b9813-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="b9813-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="b9813-115">**Tag Syntax**</span></span>

<span data-ttu-id="b9813-116"><v: *elemento* Insert = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b9813-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="b9813-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="b9813-117">**Script Syntax**</span></span>

<span data-ttu-id="b9813-118">*element* . Insert = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="b9813-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="b9813-119">*espressione* = *elemento*. Insert</span><span class="sxs-lookup"><span data-stu-id="b9813-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="b9813-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="b9813-120">**Remarks**</span></span>

<span data-ttu-id="b9813-121">Il valore del margine interno del testo viene specificato come stringa contenente quattro valori, separati da virgole o spazi.</span><span class="sxs-lookup"><span data-stu-id="b9813-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="b9813-122">I valori misurano l'incasso dai bordi sinistro, superiore, destro e inferiore della casella specificata dall'attributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) di **path**.</span><span class="sxs-lookup"><span data-stu-id="b9813-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="b9813-123">I valori mancanti vengono impostati sul valore predefinito, ovvero "0.1 in, 0,05 in, 0.1 in, 0,05 in".</span><span class="sxs-lookup"><span data-stu-id="b9813-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="b9813-124">Per le forme ruotate nei browser che non supportano la rotazione, il rettangolo di delimitazione viene agganciato al multiplo più vicino di 90 gradi.</span><span class="sxs-lookup"><span data-stu-id="b9813-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="b9813-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="b9813-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="b9813-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="b9813-126">**Example**</span></span>

<span data-ttu-id="b9813-127">La casella di testo avrà un margine interno di 10 pixel.</span><span class="sxs-lookup"><span data-stu-id="b9813-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 