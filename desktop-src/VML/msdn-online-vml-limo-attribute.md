---
title: Attributo limo la
description: Attributo limo la
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399088"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="a3fc4-103">Attributo limo la</span><span class="sxs-lookup"><span data-stu-id="a3fc4-103">VML Limo Attribute</span></span>

<span data-ttu-id="a3fc4-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a3fc4-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a3fc4-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a3fc4-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a3fc4-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a3fc4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a3fc4-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a3fc4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a3fc4-110">Definisce un punto di estensione nel percorso.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="a3fc4-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-111">Read/write.</span></span> <span data-ttu-id="a3fc4-112">**Vector2D**.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-112">**Vector2D**.</span></span>

<span data-ttu-id="a3fc4-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-113">**Applies To**</span></span>

[<span data-ttu-id="a3fc4-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="a3fc4-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="a3fc4-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-115">**Tag Syntax**</span></span>

<span data-ttu-id="a3fc4-116"><v: *element* limo = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a3fc4-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="a3fc4-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-117">**Script Syntax**</span></span>

<span data-ttu-id="a3fc4-118">*element* . Limo = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="a3fc4-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="a3fc4-119">*espressione* = *element*. limo</span><span class="sxs-lookup"><span data-stu-id="a3fc4-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="a3fc4-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-120">**Remarks**</span></span>

<span data-ttu-id="a3fc4-121">Il valore predefinito è "0 0".</span><span class="sxs-lookup"><span data-stu-id="a3fc4-121">The default value is "0 0".</span></span> <span data-ttu-id="a3fc4-122">Le Stretch Limo sono punti sul bordo di una forma che definiscono dove e come una forma può essere allungata da un utente in un editor grafico.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="a3fc4-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="a3fc4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a3fc4-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-124">**Example**</span></span>

<span data-ttu-id="a3fc4-125">Un punto di estensione limo viene definito A metà lungo la linea orizzontale.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 