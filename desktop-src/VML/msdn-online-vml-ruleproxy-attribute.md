---
title: Attributo RuleProxy di la
description: Attributo RuleProxy di la
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300362"
---
# <a name="vml-ruleproxy-attribute"></a><span data-ttu-id="e9f34-103">Attributo RuleProxy di la</span><span class="sxs-lookup"><span data-stu-id="e9f34-103">VML RuleProxy Attribute</span></span>

<span data-ttu-id="e9f34-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e9f34-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e9f34-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e9f34-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e9f34-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e9f34-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e9f34-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e9f34-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e9f34-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e9f34-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e9f34-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e9f34-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e9f34-110">Determina se verrà utilizzato un proxy per il motore regole.</span><span class="sxs-lookup"><span data-stu-id="e9f34-110">Determines whether a proxy for the rules engine will be used.</span></span> <span data-ttu-id="e9f34-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e9f34-111">Read/write.</span></span> <span data-ttu-id="e9f34-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e9f34-112">**VgTriState**.</span></span>

<span data-ttu-id="e9f34-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e9f34-113">**Applies To**</span></span>

[<span data-ttu-id="e9f34-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="e9f34-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e9f34-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e9f34-115">**Tag Syntax**</span></span>

<span data-ttu-id="e9f34-116"><v: *element* ruleproxy = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e9f34-116"><v: *element* ruleproxy=" *expression* "></span></span>

<span data-ttu-id="e9f34-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e9f34-117">**Remarks**</span></span>

<span data-ttu-id="e9f34-118">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="e9f34-118">The default value is **False**.</span></span> <span data-ttu-id="e9f34-119">Se **true**, viene utilizzato un proxy.</span><span class="sxs-lookup"><span data-stu-id="e9f34-119">If **True**, a proxy is used.</span></span>

<span data-ttu-id="e9f34-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="e9f34-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="e9f34-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e9f34-121">**Example**</span></span>

<span data-ttu-id="e9f34-122">Viene utilizzato un proxy per elaborare la forma.</span><span class="sxs-lookup"><span data-stu-id="e9f34-122">A proxy is used to process the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 