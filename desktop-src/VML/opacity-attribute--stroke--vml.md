---
title: Attributo Opacity (Stroke) (la)
description: Attributo Opacity (Stroke) (la)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474158"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="fcc35-103">Attributo Opacity (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="fcc35-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="fcc35-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fcc35-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fcc35-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="fcc35-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fcc35-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="fcc35-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fcc35-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="fcc35-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fcc35-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fcc35-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fcc35-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fcc35-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fcc35-110">Definisce la quantità di trasparenza di un tratto.</span><span class="sxs-lookup"><span data-stu-id="fcc35-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="fcc35-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fcc35-111">Read/write.</span></span> <span data-ttu-id="fcc35-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="fcc35-112">**VgFraction**.</span></span>

<span data-ttu-id="fcc35-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="fcc35-113">**Applies To**</span></span>

[<span data-ttu-id="fcc35-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="fcc35-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="fcc35-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="fcc35-115">**Tag Syntax**</span></span>

<span data-ttu-id="fcc35-116"><v: *elemento* Opacity = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="fcc35-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="fcc35-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="fcc35-117">**Script Syntax**</span></span>

<span data-ttu-id="fcc35-118">*element* . Opacity = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="fcc35-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="fcc35-119">*espressione* = *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="fcc35-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="fcc35-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="fcc35-120">**Remarks**</span></span>

<span data-ttu-id="fcc35-121">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="fcc35-121">The default value is 1.0.</span></span>

<span data-ttu-id="fcc35-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="fcc35-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="fcc35-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="fcc35-123">**Example**</span></span>

<span data-ttu-id="fcc35-124">Il tratto è trasparente al 50%.</span><span class="sxs-lookup"><span data-stu-id="fcc35-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 