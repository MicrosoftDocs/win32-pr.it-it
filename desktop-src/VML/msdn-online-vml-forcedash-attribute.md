---
title: Attributo ForceDash di la
description: Attributo ForceDash di la
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047054"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="94cb8-103">Attributo ForceDash di la</span><span class="sxs-lookup"><span data-stu-id="94cb8-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="94cb8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="94cb8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="94cb8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="94cb8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="94cb8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="94cb8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="94cb8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="94cb8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="94cb8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="94cb8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="94cb8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="94cb8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="94cb8-110">Determina se un contorno tratteggiato viene utilizzato per disegnare una forma quando una forma non ha linea o riempimento.</span><span class="sxs-lookup"><span data-stu-id="94cb8-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="94cb8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="94cb8-111">Read/write.</span></span> <span data-ttu-id="94cb8-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="94cb8-112">**VgTriState**.</span></span>

<span data-ttu-id="94cb8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="94cb8-113">**Applies To**</span></span>

[<span data-ttu-id="94cb8-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="94cb8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="94cb8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="94cb8-115">**Tag Syntax**</span></span>

<span data-ttu-id="94cb8-116"><v: *element* o:forcedash = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="94cb8-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="94cb8-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="94cb8-117">**Remarks**</span></span>

<span data-ttu-id="94cb8-118">Utilizzato dai segnaposto di Microsoft PowerPoint per disegnare un contorno tratteggiato quando non è presente alcuna riga e nessun riempimento per una forma.</span><span class="sxs-lookup"><span data-stu-id="94cb8-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="94cb8-119">L'impostazione predefinita è **False**.</span><span class="sxs-lookup"><span data-stu-id="94cb8-119">Default is **False**.</span></span> <span data-ttu-id="94cb8-120">Se **true**, viene usato un contorno tratteggiato per indicare un segnaposto.</span><span class="sxs-lookup"><span data-stu-id="94cb8-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="94cb8-121">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="94cb8-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="94cb8-122">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="94cb8-122">**Example**</span></span>

<span data-ttu-id="94cb8-123">Una linea tratteggiata verrà utilizzata per eseguire il rendering della forma se non è presente alcuna linea o riempimento.</span><span class="sxs-lookup"><span data-stu-id="94cb8-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 