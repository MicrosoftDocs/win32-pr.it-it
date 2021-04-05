---
title: Attributo ID (Stroke) (la)
description: Attributo ID (Stroke) (la)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728338"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="d8dc1-103">Attributo ID (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="d8dc1-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="d8dc1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d8dc1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d8dc1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d8dc1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d8dc1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d8dc1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d8dc1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d8dc1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d8dc1-110">Nome che fornisce un identificatore univoco per un tratto.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="d8dc1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-111">Read/write.</span></span> <span data-ttu-id="d8dc1-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-112">**String**.</span></span>

<span data-ttu-id="d8dc1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d8dc1-113">**Applies To**</span></span>

[<span data-ttu-id="d8dc1-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="d8dc1-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="d8dc1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d8dc1-115">**Tag Syntax**</span></span>

<span data-ttu-id="d8dc1-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d8dc1-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="d8dc1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d8dc1-117">**Script Syntax**</span></span>

<span data-ttu-id="d8dc1-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d8dc1-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="d8dc1-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="d8dc1-119">*expression*=*element*.id</span></span>

<span data-ttu-id="d8dc1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d8dc1-120">**Remarks**</span></span>

<span data-ttu-id="d8dc1-121">Usare **ID** per fare riferimento a un tratto specifico.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="d8dc1-122">Una volta creato un tratto e dato un ID, è possibile utilizzare il nome ID quando si desidera modificare il tratto.</span><span class="sxs-lookup"><span data-stu-id="d8dc1-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="d8dc1-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d8dc1-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="d8dc1-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d8dc1-124">**Example**</span></span>

<span data-ttu-id="d8dc1-125">La forma ha un ID tratto denominato "stroke".</span><span class="sxs-lookup"><span data-stu-id="d8dc1-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 