---
title: Attributo FitShape di la
description: Attributo FitShape di la
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300400"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="38fde-103">Attributo FitShape di la</span><span class="sxs-lookup"><span data-stu-id="38fde-103">VML FitShape Attribute</span></span>

<span data-ttu-id="38fde-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="38fde-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="38fde-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="38fde-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="38fde-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="38fde-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="38fde-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="38fde-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="38fde-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="38fde-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="38fde-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="38fde-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="38fde-110">Definisce se il testo corrisponde al rettangolo di delimitazione di una forma.</span><span class="sxs-lookup"><span data-stu-id="38fde-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="38fde-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="38fde-111">Read/write.</span></span> <span data-ttu-id="38fde-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="38fde-112">**VgTriState**.</span></span>

<span data-ttu-id="38fde-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="38fde-113">**Applies To**</span></span>

[<span data-ttu-id="38fde-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="38fde-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="38fde-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="38fde-115">**Tag Syntax**</span></span>

<span data-ttu-id="38fde-116"><v: *element* fitshape = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="38fde-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="38fde-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="38fde-117">**Script Syntax**</span></span>

<span data-ttu-id="38fde-118">*element* . fitshape = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="38fde-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="38fde-119">*espressione* = *elemento*. fitshape</span><span class="sxs-lookup"><span data-stu-id="38fde-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="38fde-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="38fde-120">**Remarks**</span></span>

<span data-ttu-id="38fde-121">Se è **true**, il testo viene allungato ai bordi della casella che definisce l'intera forma.</span><span class="sxs-lookup"><span data-stu-id="38fde-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="38fde-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="38fde-122">The default is **False**.</span></span>

<span data-ttu-id="38fde-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="38fde-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="38fde-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="38fde-124">**Example**</span></span>

<span data-ttu-id="38fde-125">Il testo si estenderà per adattarsi alla forma.</span><span class="sxs-lookup"><span data-stu-id="38fde-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 