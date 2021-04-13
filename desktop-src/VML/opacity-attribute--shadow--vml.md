---
title: Attributo Opacity (Shadow) (la)
description: Attributo Opacity (Shadow) (la)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399157"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="9265c-103">Attributo Opacity (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="9265c-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="9265c-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9265c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9265c-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9265c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9265c-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9265c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9265c-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9265c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9265c-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9265c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9265c-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9265c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9265c-110">Determina la trasparenza di un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="9265c-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="9265c-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9265c-111">Read/write.</span></span> <span data-ttu-id="9265c-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9265c-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="9265c-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="9265c-113">**Applies To**</span></span>

[<span data-ttu-id="9265c-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="9265c-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="9265c-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="9265c-115">**Tag Syntax**</span></span>

<span data-ttu-id="9265c-116"><v: *elemento* Opacity = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9265c-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="9265c-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="9265c-117">**Script Syntax**</span></span>

<span data-ttu-id="9265c-118">*element* . Opacity = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="9265c-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="9265c-119">*espressione* = *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="9265c-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="9265c-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="9265c-120">**Remarks**</span></span>

<span data-ttu-id="9265c-121">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="9265c-121">The default value is 1.</span></span> <span data-ttu-id="9265c-122">Il valore 0 renderà un'ombreggiatura completamente trasparente.</span><span class="sxs-lookup"><span data-stu-id="9265c-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="9265c-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="9265c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9265c-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="9265c-124">**Example**</span></span>

<span data-ttu-id="9265c-125">La forma presenta un'ombreggiatura trasparente al 50%.</span><span class="sxs-lookup"><span data-stu-id="9265c-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 