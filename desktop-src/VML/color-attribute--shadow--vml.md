---
title: Attributo Color (Shadow) (la)
description: Attributo Color (Shadow) (la)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299861"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="9efef-103">Attributo Color (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="9efef-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="9efef-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9efef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9efef-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9efef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9efef-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9efef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9efef-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9efef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9efef-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9efef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9efef-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9efef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9efef-110">Definisce il colore dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="9efef-110">Defines the color of the shadow.</span></span> <span data-ttu-id="9efef-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9efef-111">Read/write.</span></span> <span data-ttu-id="9efef-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="9efef-112">**VgColor**.</span></span>

<span data-ttu-id="9efef-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="9efef-113">**Applies To**</span></span>

[<span data-ttu-id="9efef-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="9efef-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="9efef-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="9efef-115">**Tag Syntax**</span></span>

<span data-ttu-id="9efef-116"><v: *elemento* color = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9efef-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="9efef-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="9efef-117">**Script Syntax**</span></span>

<span data-ttu-id="9efef-118">*element* . Color = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="9efef-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="9efef-119">*espressione* = *elemento*. Color</span><span class="sxs-lookup"><span data-stu-id="9efef-119">*expression*=*element*.color</span></span>

<span data-ttu-id="9efef-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="9efef-120">**Remarks**</span></span>

<span data-ttu-id="9efef-121">Usare l'attributo color per impostare o ottenere il colore di un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="9efef-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="9efef-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="9efef-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="9efef-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="9efef-123">**Example**</span></span>

<span data-ttu-id="9efef-124">L'ombreggiatura è verde.</span><span class="sxs-lookup"><span data-stu-id="9efef-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 