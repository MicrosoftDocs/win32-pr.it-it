---
title: Attributo ID (percorso) (la)
description: Attributo ID (percorso) (la)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117775"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="a00fe-103">Attributo ID (percorso) (la)</span><span class="sxs-lookup"><span data-stu-id="a00fe-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="a00fe-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a00fe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a00fe-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a00fe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a00fe-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a00fe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a00fe-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a00fe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a00fe-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a00fe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a00fe-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a00fe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a00fe-110">Nome che fornisce un identificatore univoco per un percorso.</span><span class="sxs-lookup"><span data-stu-id="a00fe-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="a00fe-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a00fe-111">Read/write.</span></span> <span data-ttu-id="a00fe-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="a00fe-112">**String**.</span></span>

<span data-ttu-id="a00fe-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a00fe-113">**Applies To**</span></span>

[<span data-ttu-id="a00fe-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="a00fe-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="a00fe-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a00fe-115">**Tag Syntax**</span></span>

<span data-ttu-id="a00fe-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a00fe-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="a00fe-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="a00fe-117">**Script Syntax**</span></span>

<span data-ttu-id="a00fe-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="a00fe-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="a00fe-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="a00fe-119">*expression*=*element*.id</span></span>

<span data-ttu-id="a00fe-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a00fe-120">**Remarks**</span></span>

<span data-ttu-id="a00fe-121">Usare **ID** per fare riferimento a un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="a00fe-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="a00fe-122">Una volta creato un percorso e dato un ID, è possibile utilizzare il nome dell'ID quando si desidera modificare il percorso.</span><span class="sxs-lookup"><span data-stu-id="a00fe-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="a00fe-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="a00fe-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a00fe-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a00fe-124">**Example**</span></span>

<span data-ttu-id="a00fe-125">La forma ha un ID di percorso denominato "percorso".</span><span class="sxs-lookup"><span data-stu-id="a00fe-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 