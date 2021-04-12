---
title: La MSO-wrap-Distance-Left-attributo
description: La MSO-wrap-Distance-Left-attributo
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337870"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a><span data-ttu-id="0bbe9-103">La MSO-wrap-Distance-Left-attributo</span><span class="sxs-lookup"><span data-stu-id="0bbe9-103">VML MSO-Wrap-Distance-Left Attribute</span></span>

<span data-ttu-id="0bbe9-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0bbe9-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0bbe9-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0bbe9-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0bbe9-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0bbe9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0bbe9-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0bbe9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0bbe9-110">Definisce la distanza tra il lato sinistro della forma e il testo che lo racchiude.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-110">Defines the distance from the left side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="0bbe9-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-111">Read/write.</span></span> <span data-ttu-id="0bbe9-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-112">**String**.</span></span>

<span data-ttu-id="0bbe9-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="0bbe9-113">**Applies To**</span></span>

[<span data-ttu-id="0bbe9-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="0bbe9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0bbe9-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="0bbe9-115">**Tag Syntax**</span></span>

<span data-ttu-id="0bbe9-116"><v: *element* Style = "MSO-wrap-Distance-Left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0bbe9-116"><v: *element* style="mso-wrap-distance-left: *expression* "></span></span>

<span data-ttu-id="0bbe9-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="0bbe9-117">**Remarks**</span></span>

<span data-ttu-id="0bbe9-118">Si noti che questo attributo è diverso dall'attributo del **margine** CSS.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="0bbe9-119">**Margin** modifica l'origine della forma in modo da includere le aree dei margini, ma la distanza dal ritorno a capo nell'Microsoft Office non modifica l'origine della forma.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="0bbe9-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="0bbe9-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0bbe9-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0bbe9-121">**Example**</span></span>

<span data-ttu-id="0bbe9-122">La forma ha una distanza a capo sinistro di 10 punti.</span><span class="sxs-lookup"><span data-stu-id="0bbe9-122">The shape has a left wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 