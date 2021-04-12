---
title: Attributo FitPath di la
description: Attributo FitPath di la
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224022"
---
# <a name="vml-fitpath-attribute"></a><span data-ttu-id="ad498-103">Attributo FitPath di la</span><span class="sxs-lookup"><span data-stu-id="ad498-103">VML FitPath Attribute</span></span>

<span data-ttu-id="ad498-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ad498-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ad498-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ad498-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ad498-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ad498-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ad498-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ad498-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ad498-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ad498-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ad498-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ad498-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ad498-110">Definisce se il testo corrisponde al percorso di una forma.</span><span class="sxs-lookup"><span data-stu-id="ad498-110">Defines whether the text fits the path of a shape.</span></span> <span data-ttu-id="ad498-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ad498-111">Read/write.</span></span> <span data-ttu-id="ad498-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="ad498-112">**VgTriState**.</span></span>

<span data-ttu-id="ad498-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ad498-113">**Applies To**</span></span>

[<span data-ttu-id="ad498-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="ad498-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="ad498-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ad498-115">**Tag Syntax**</span></span>

<span data-ttu-id="ad498-116"><v: *element* fitpath = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ad498-116"><v: *element* fitpath=" *expression* "></span></span>

<span data-ttu-id="ad498-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ad498-117">**Script Syntax**</span></span>

<span data-ttu-id="ad498-118">*element* . fitpath = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ad498-118">*element* .fitpath="*expression*"</span></span>

<span data-ttu-id="ad498-119">*espressione* = *elemento*. fitpath</span><span class="sxs-lookup"><span data-stu-id="ad498-119">*expression*=*element*.fitpath</span></span>

<span data-ttu-id="ad498-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ad498-120">**Remarks**</span></span>

<span data-ttu-id="ad498-121">Se **true**, ridimensiona il testo per riempire il percorso su cui si trova.</span><span class="sxs-lookup"><span data-stu-id="ad498-121">If **True**, sizes the text to fill the path it lies out on.</span></span> <span data-ttu-id="ad498-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="ad498-122">The default is **False**.</span></span>

<span data-ttu-id="ad498-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ad498-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ad498-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ad498-124">**Example**</span></span>

<span data-ttu-id="ad498-125">Il testo si adatterà al percorso.</span><span class="sxs-lookup"><span data-stu-id="ad498-125">The text will fit the path.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 