---
title: Attributo Color (Fill) (la)
description: Attributo Color (Fill) (la)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473222"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="41f61-103">Attributo Color (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="41f61-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="41f61-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="41f61-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="41f61-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="41f61-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="41f61-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="41f61-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="41f61-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="41f61-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="41f61-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="41f61-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="41f61-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="41f61-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="41f61-110">Definisce il colore di un riempimento.</span><span class="sxs-lookup"><span data-stu-id="41f61-110">Defines the color of a fill.</span></span> <span data-ttu-id="41f61-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="41f61-111">Read/write.</span></span> <span data-ttu-id="41f61-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="41f61-112">**VgColor**.</span></span>

<span data-ttu-id="41f61-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="41f61-113">**Applies To**</span></span>

[<span data-ttu-id="41f61-114">Fill</span><span class="sxs-lookup"><span data-stu-id="41f61-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="41f61-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="41f61-115">**Tag Syntax**</span></span>

<span data-ttu-id="41f61-116"><v: *elemento* color = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="41f61-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="41f61-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="41f61-117">**Script Syntax**</span></span>

<span data-ttu-id="41f61-118">*element* . Color = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="41f61-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="41f61-119">*espressione* = *elemento*. Color</span><span class="sxs-lookup"><span data-stu-id="41f61-119">*expression*=*element*.color</span></span>

<span data-ttu-id="41f61-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="41f61-120">**Remarks**</span></span>

<span data-ttu-id="41f61-121">Esegue l'override dell'attributo **FillColor** di una forma.</span><span class="sxs-lookup"><span data-stu-id="41f61-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="41f61-122">Il valore predefinito è **bianco**.</span><span class="sxs-lookup"><span data-stu-id="41f61-122">The default value is **White**.</span></span>

<span data-ttu-id="41f61-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="41f61-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="41f61-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="41f61-124">**Example**</span></span>

<span data-ttu-id="41f61-125">Il colore di riempimento della forma è verde.</span><span class="sxs-lookup"><span data-stu-id="41f61-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 