---
title: LA V-text-Reverse-attributo
description: LA V-text-Reverse-attributo
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047049"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="6f198-103">LA V-text-Reverse-attributo</span><span class="sxs-lookup"><span data-stu-id="6f198-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="6f198-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f198-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6f198-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="6f198-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6f198-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="6f198-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6f198-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="6f198-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6f198-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6f198-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6f198-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6f198-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6f198-110">Determina se l'ordine di layout delle righe è invertito.</span><span class="sxs-lookup"><span data-stu-id="6f198-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="6f198-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f198-111">Read/write.</span></span> <span data-ttu-id="6f198-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="6f198-112">**VgTriState**.</span></span>

<span data-ttu-id="6f198-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="6f198-113">**Applies To**</span></span>

[<span data-ttu-id="6f198-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="6f198-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="6f198-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="6f198-115">**Tag Syntax**</span></span>

<span data-ttu-id="6f198-116"><v: *elemento* Style = "v-text-Reverse: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6f198-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="6f198-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="6f198-117">**Script Syntax**</span></span>

<span data-ttu-id="6f198-118">*element* . Style. v-text-Reverse = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="6f198-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="6f198-119">*espressione* = *element*. Style. v-text-Reverse</span><span class="sxs-lookup"><span data-stu-id="6f198-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="6f198-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="6f198-120">**Remarks**</span></span>

<span data-ttu-id="6f198-121">Se **true**, l'ordine di layout delle righe viene invertito.</span><span class="sxs-lookup"><span data-stu-id="6f198-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="6f198-122">Questo attributo viene utilizzato per il layout di testo verticale.</span><span class="sxs-lookup"><span data-stu-id="6f198-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="6f198-123">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="6f198-123">The default value is **False**.</span></span>

<span data-ttu-id="6f198-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="6f198-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="6f198-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="6f198-125">**Example**</span></span>

<span data-ttu-id="6f198-126">L'ordine di layout è invertito.</span><span class="sxs-lookup"><span data-stu-id="6f198-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 