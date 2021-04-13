---
title: Attributo Bullet la
description: Attributo Bullet la
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399247"
---
# <a name="vml-bullet-attribute"></a><span data-ttu-id="45295-103">Attributo Bullet la</span><span class="sxs-lookup"><span data-stu-id="45295-103">VML Bullet Attribute</span></span>

<span data-ttu-id="45295-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="45295-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="45295-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="45295-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="45295-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="45295-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="45295-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="45295-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="45295-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="45295-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="45295-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="45295-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="45295-110">Determina se una forma è un punto elenco grafico.</span><span class="sxs-lookup"><span data-stu-id="45295-110">Determines whether a shape is a graphical bullet.</span></span> <span data-ttu-id="45295-111">**VgTriState** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="45295-111">Read/write **VgTriState**.</span></span>

<span data-ttu-id="45295-112">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="45295-112">**Applies To**</span></span>

[<span data-ttu-id="45295-113">Con forme</span><span class="sxs-lookup"><span data-stu-id="45295-113">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="45295-114">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="45295-114">**Tag Syntax**</span></span>

<span data-ttu-id="45295-115"><v: *element* o:Bullet = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="45295-115"><v: *element* o:bullet=" *expression* "></span></span>

<span data-ttu-id="45295-116">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="45295-116">**Remarks**</span></span>

<span data-ttu-id="45295-117">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="45295-117">The default is **False**.</span></span> <span data-ttu-id="45295-118">Se **true**, la forma è un punto elenco grafico.</span><span class="sxs-lookup"><span data-stu-id="45295-118">If **True**, the shape is a graphical bullet.</span></span>

<span data-ttu-id="45295-119">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="45295-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="45295-120">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="45295-120">**Example**</span></span>

<span data-ttu-id="45295-121">La forma è un punto elenco.</span><span class="sxs-lookup"><span data-stu-id="45295-121">The shape is a bullet.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 