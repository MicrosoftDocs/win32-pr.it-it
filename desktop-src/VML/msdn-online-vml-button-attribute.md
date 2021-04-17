---
title: Attributo Button la
description: Attributo Button la
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300020"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="e01f1-103">Attributo Button la</span><span class="sxs-lookup"><span data-stu-id="e01f1-103">VML Button Attribute</span></span>

<span data-ttu-id="e01f1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e01f1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e01f1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e01f1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e01f1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e01f1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e01f1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e01f1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e01f1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e01f1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e01f1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e01f1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e01f1-110">Determina se una forma verrà elaborata come pulsante.</span><span class="sxs-lookup"><span data-stu-id="e01f1-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="e01f1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e01f1-111">Read/write.</span></span> <span data-ttu-id="e01f1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e01f1-112">**VgTriState**.</span></span>

<span data-ttu-id="e01f1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e01f1-113">**Applies To**</span></span>

[<span data-ttu-id="e01f1-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="e01f1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e01f1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e01f1-115">**Tag Syntax**</span></span>

<span data-ttu-id="e01f1-116"><v: *element* o:Button = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e01f1-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="e01f1-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e01f1-117">**Remarks**</span></span>

<span data-ttu-id="e01f1-118">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="e01f1-118">The default is **False**.</span></span> <span data-ttu-id="e01f1-119">Se **true**, la forma viene elaborata come pulsante.</span><span class="sxs-lookup"><span data-stu-id="e01f1-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="e01f1-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="e01f1-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="e01f1-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e01f1-121">**Example**</span></span>

<span data-ttu-id="e01f1-122">La forma è un pulsante.</span><span class="sxs-lookup"><span data-stu-id="e01f1-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 