---
title: Attributo offset (Shadow) (la)
description: Attributo offset (Shadow) (la)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963147"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="03dd8-103">Attributo offset (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="03dd8-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="03dd8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="03dd8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="03dd8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="03dd8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="03dd8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="03dd8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="03dd8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="03dd8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="03dd8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="03dd8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="03dd8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="03dd8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="03dd8-110">Definisce la distanza con cui l'ombreggiatura si estende oltre la forma.</span><span class="sxs-lookup"><span data-stu-id="03dd8-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="03dd8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="03dd8-111">Read/write.</span></span> <span data-ttu-id="03dd8-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="03dd8-112">**VgVector2D**.</span></span>

<span data-ttu-id="03dd8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="03dd8-113">**Applies To**</span></span>

[<span data-ttu-id="03dd8-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="03dd8-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="03dd8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="03dd8-115">**Tag Syntax**</span></span>

<span data-ttu-id="03dd8-116"><v: *elemento* offset = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="03dd8-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="03dd8-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="03dd8-117">**Script Syntax**</span></span>

<span data-ttu-id="03dd8-118">*element* . offset = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="03dd8-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="03dd8-119">*espressione* = *elemento*. offset</span><span class="sxs-lookup"><span data-stu-id="03dd8-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="03dd8-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="03dd8-120">**Remarks**</span></span>

<span data-ttu-id="03dd8-121">L'offset predefinito per il valore x è 2PT e l'impostazione predefinita per il valore y è 2Pt.</span><span class="sxs-lookup"><span data-stu-id="03dd8-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="03dd8-122">I valori sono una misura assoluta o un valore frazionario di forma.</span><span class="sxs-lookup"><span data-stu-id="03dd8-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="03dd8-123">Se frazionarie, variano da 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="03dd8-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="03dd8-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="03dd8-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="03dd8-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="03dd8-125">**Example**</span></span>

<span data-ttu-id="03dd8-126">La forma presenta un'ombreggiatura con un offset di 5 punti verso il basso e 10 punta a destra.</span><span class="sxs-lookup"><span data-stu-id="03dd8-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 