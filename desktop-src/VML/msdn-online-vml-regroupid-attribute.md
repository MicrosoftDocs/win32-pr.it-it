---
title: Attributo ReGroupID di la
description: Attributo ReGroupID di la
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399140"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="e4f3b-103">Attributo ReGroupID di la</span><span class="sxs-lookup"><span data-stu-id="e4f3b-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="e4f3b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e4f3b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e4f3b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e4f3b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e4f3b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e4f3b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e4f3b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e4f3b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e4f3b-110">Definisce un gruppo precedente per una forma.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="e4f3b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-111">Read/write.</span></span> <span data-ttu-id="e4f3b-112">**VgInteger**.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-112">**VgInteger**.</span></span>

<span data-ttu-id="e4f3b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e4f3b-113">**Applies To**</span></span>

[<span data-ttu-id="e4f3b-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="e4f3b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e4f3b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e4f3b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e4f3b-116"><v: *element* o:regroupid = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e4f3b-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="e4f3b-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e4f3b-117">**Remarks**</span></span>

<span data-ttu-id="e4f3b-118">Un numero ID viene utilizzato per identificare i gruppi di forme che non sono più raggruppati.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="e4f3b-119">Consente di raggruppare le forme a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="e4f3b-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="e4f3b-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="e4f3b-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e4f3b-121">**Example**</span></span>

<span data-ttu-id="e4f3b-122">La forma faceva parte di un gruppo indicato dall'ID gruppo 040754.</span><span class="sxs-lookup"><span data-stu-id="e4f3b-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 