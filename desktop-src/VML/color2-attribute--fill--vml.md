---
title: Attributo color2 (Fill) (la)
description: Attributo color2 (Fill) (la)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300222"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="c9c55-103">Attributo color2 (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="c9c55-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="c9c55-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c9c55-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c9c55-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c9c55-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c9c55-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c9c55-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c9c55-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c9c55-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c9c55-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c9c55-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c9c55-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c9c55-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c9c55-110">Definisce un secondo colore per le compilazioni.</span><span class="sxs-lookup"><span data-stu-id="c9c55-110">Defines a second color for fills.</span></span> <span data-ttu-id="c9c55-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c9c55-111">Read/write.</span></span> <span data-ttu-id="c9c55-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c55-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="c9c55-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c9c55-113">**Applies To**</span></span>

[<span data-ttu-id="c9c55-114">Fill</span><span class="sxs-lookup"><span data-stu-id="c9c55-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c9c55-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c9c55-115">**Tag Syntax**</span></span>

<span data-ttu-id="c9c55-116"><v: *element* color2 = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c9c55-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="c9c55-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="c9c55-117">**Script Syntax**</span></span>

<span data-ttu-id="c9c55-118">*element* . color2 = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="c9c55-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="c9c55-119">*espressione* = *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="c9c55-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="c9c55-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c9c55-120">**Remarks**</span></span>

<span data-ttu-id="c9c55-121">Viene usato un secondo colore quando un tipo di riempimento è un modello o una sfumatura.</span><span class="sxs-lookup"><span data-stu-id="c9c55-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="c9c55-122">Il valore predefinito è **bianco**.</span><span class="sxs-lookup"><span data-stu-id="c9c55-122">The default value is **White**.</span></span>

<span data-ttu-id="c9c55-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="c9c55-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c9c55-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c9c55-124">**Example**</span></span>

<span data-ttu-id="c9c55-125">Il tipo di riempimento della forma è un modello in cui il riempimento in primo piano viene definito dall'immagine di origine, ma lo sfondo trasparente viene definito dal secondo colore.</span><span class="sxs-lookup"><span data-stu-id="c9c55-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 