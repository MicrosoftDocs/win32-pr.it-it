---
title: Attributo FillOK di la
description: Attributo FillOK di la
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339175"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="adeb2-103">Attributo FillOK di la</span><span class="sxs-lookup"><span data-stu-id="adeb2-103">VML FillOK Attribute</span></span>

<span data-ttu-id="adeb2-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="adeb2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="adeb2-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="adeb2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="adeb2-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="adeb2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="adeb2-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="adeb2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="adeb2-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="adeb2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="adeb2-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="adeb2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="adeb2-110">Determina se verrà visualizzato un riempimento.</span><span class="sxs-lookup"><span data-stu-id="adeb2-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="adeb2-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="adeb2-111">Read/write.</span></span> <span data-ttu-id="adeb2-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="adeb2-112">**VgTriState**.</span></span>

<span data-ttu-id="adeb2-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="adeb2-113">**Applies To**</span></span>

[<span data-ttu-id="adeb2-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="adeb2-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="adeb2-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="adeb2-115">**Tag Syntax**</span></span>

<span data-ttu-id="adeb2-116"><v: *element* fillok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="adeb2-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="adeb2-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="adeb2-117">**Script Syntax**</span></span>

<span data-ttu-id="adeb2-118">*element* . fillok = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="adeb2-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="adeb2-119">*espressione* = *elemento*. fillok</span><span class="sxs-lookup"><span data-stu-id="adeb2-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="adeb2-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="adeb2-120">**Remarks**</span></span>

<span data-ttu-id="adeb2-121">Se **false**, il percorso non può essere compilato.</span><span class="sxs-lookup"><span data-stu-id="adeb2-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="adeb2-122">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="adeb2-122">The default is **True**.</span></span> <span data-ttu-id="adeb2-123">Questo attributo esegue l'override di tutti gli altri attributi Fill nell'elemento padre o **Fill** .</span><span class="sxs-lookup"><span data-stu-id="adeb2-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="adeb2-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="adeb2-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="adeb2-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="adeb2-125">**Example**</span></span>

<span data-ttu-id="adeb2-126">Il percorso non verrà compilato.</span><span class="sxs-lookup"><span data-stu-id="adeb2-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 