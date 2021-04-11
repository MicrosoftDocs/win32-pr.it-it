---
title: Attributo StrokeOK di la
description: Attributo StrokeOK di la
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963293"
---
# <a name="vml-strokeok-attribute"></a><span data-ttu-id="407ca-103">Attributo StrokeOK di la</span><span class="sxs-lookup"><span data-stu-id="407ca-103">VML StrokeOK Attribute</span></span>

<span data-ttu-id="407ca-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="407ca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="407ca-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="407ca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="407ca-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="407ca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="407ca-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="407ca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="407ca-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="407ca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="407ca-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="407ca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="407ca-110">Determina se un tratto verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="407ca-110">Determines whether a stroke will be displayed.</span></span> <span data-ttu-id="407ca-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="407ca-111">Read/write.</span></span> <span data-ttu-id="407ca-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="407ca-112">**VgTriState**.</span></span>

<span data-ttu-id="407ca-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="407ca-113">**Applies To**</span></span>

[<span data-ttu-id="407ca-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="407ca-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="407ca-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="407ca-115">**Tag Syntax**</span></span>

<span data-ttu-id="407ca-116"><v: *element* strokeok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="407ca-116"><v: *element* strokeok=" *expression* "></span></span>

<span data-ttu-id="407ca-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="407ca-117">**Script Syntax**</span></span>

<span data-ttu-id="407ca-118">*element* . strokeok = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="407ca-118">*element* .strokeok="*expression*"</span></span>

<span data-ttu-id="407ca-119">*espressione* = *elemento*. strokeok</span><span class="sxs-lookup"><span data-stu-id="407ca-119">*expression*=*element*.strokeok</span></span>

<span data-ttu-id="407ca-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="407ca-120">**Remarks**</span></span>

<span data-ttu-id="407ca-121">Se **false**, non è possibile tracciare il percorso.</span><span class="sxs-lookup"><span data-stu-id="407ca-121">If **False**, the path cannot be stroked.</span></span> <span data-ttu-id="407ca-122">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="407ca-122">The default is **True**.</span></span> <span data-ttu-id="407ca-123">Questo attributo esegue l'override di tutti gli altri attributi Stroke nell'elemento padre o **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="407ca-123">This attribute overrides all other stroke attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="407ca-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="407ca-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="407ca-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="407ca-125">**Example**</span></span>

<span data-ttu-id="407ca-126">Il percorso non verrà tracciato.</span><span class="sxs-lookup"><span data-stu-id="407ca-126">The path will not be stroked.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 