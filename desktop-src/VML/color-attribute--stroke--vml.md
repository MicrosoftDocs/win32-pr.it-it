---
title: Attributo Color (Stroke) (la)
description: Attributo Color (Stroke) (la)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300223"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="7772a-103">Attributo Color (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="7772a-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="7772a-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7772a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7772a-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="7772a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7772a-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="7772a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7772a-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="7772a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7772a-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7772a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7772a-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7772a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7772a-110">Definisce il colore di un tratto.</span><span class="sxs-lookup"><span data-stu-id="7772a-110">Defines the color of a stroke.</span></span> <span data-ttu-id="7772a-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7772a-111">Read/write.</span></span> <span data-ttu-id="7772a-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="7772a-112">**VgColor**.</span></span>

<span data-ttu-id="7772a-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="7772a-113">**Applies To**</span></span>

[<span data-ttu-id="7772a-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="7772a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7772a-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="7772a-115">**Tag Syntax**</span></span>

<span data-ttu-id="7772a-116"><v: *elemento* color = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7772a-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="7772a-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="7772a-117">**Script Syntax**</span></span>

<span data-ttu-id="7772a-118">*element* . Color = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="7772a-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="7772a-119">*espressione* = *elemento*. Color</span><span class="sxs-lookup"><span data-stu-id="7772a-119">*expression*=*element*.color</span></span>

<span data-ttu-id="7772a-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="7772a-120">**Remarks**</span></span>

<span data-ttu-id="7772a-121">Esegue l'override dell'attributo **StrokeColor** di una forma.</span><span class="sxs-lookup"><span data-stu-id="7772a-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="7772a-122">Il valore predefinito è **nero**.</span><span class="sxs-lookup"><span data-stu-id="7772a-122">The default value is **black**.</span></span>

<span data-ttu-id="7772a-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="7772a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7772a-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="7772a-124">**Example**</span></span>

<span data-ttu-id="7772a-125">Il colore del tratto della forma è **verde**, non **rosso**.</span><span class="sxs-lookup"><span data-stu-id="7772a-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 