---
title: Attributo Offset2 di la
description: Attributo Offset2 di la
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517050"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="d6506-103">Attributo Offset2 di la</span><span class="sxs-lookup"><span data-stu-id="d6506-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="d6506-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d6506-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6506-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d6506-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6506-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d6506-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6506-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d6506-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6506-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6506-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6506-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6506-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6506-110">Determina un secondo offset.</span><span class="sxs-lookup"><span data-stu-id="d6506-110">Determines a second offset.</span></span> <span data-ttu-id="d6506-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d6506-111">Read/write.</span></span> <span data-ttu-id="d6506-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d6506-112">**VgVector2D**.</span></span>

<span data-ttu-id="d6506-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d6506-113">**Applies To**</span></span>

[<span data-ttu-id="d6506-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="d6506-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="d6506-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d6506-115">**Tag Syntax**</span></span>

<span data-ttu-id="d6506-116"><v: *element* offset2 = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d6506-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="d6506-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d6506-117">**Script Syntax**</span></span>

<span data-ttu-id="d6506-118">*element* . offset2 = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d6506-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="d6506-119">*espressione* = *elemento*. offset2</span><span class="sxs-lookup"><span data-stu-id="d6506-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="d6506-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d6506-120">**Remarks**</span></span>

<span data-ttu-id="d6506-121">L'impostazione predefinita per un secondo offset per il valore x è 0 e l'impostazione predefinita per il valore y è 0.</span><span class="sxs-lookup"><span data-stu-id="d6506-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="d6506-122">I valori sono una misura assoluta o un valore frazionario di forma.</span><span class="sxs-lookup"><span data-stu-id="d6506-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="d6506-123">Se frazionari, i valori sono compresi tra 50% e-50%.</span><span class="sxs-lookup"><span data-stu-id="d6506-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="d6506-124">Usare un secondo offset per creare effetti speciali di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="d6506-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="d6506-125">Per ulteriori informazioni sugli offset secondo, vedere l'attributo [Type](type-attribute--shadow--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="d6506-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="d6506-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d6506-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="d6506-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d6506-127">**Example**</span></span>

<span data-ttu-id="d6506-128">Viene creata una doppia ombreggiatura per la forma.</span><span class="sxs-lookup"><span data-stu-id="d6506-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 