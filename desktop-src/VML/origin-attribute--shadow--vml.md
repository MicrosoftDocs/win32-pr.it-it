---
title: Attributo Origin (Shadow) (la)
description: Attributo Origin (Shadow) (la)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729994"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="9bd06-103">Attributo Origin (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="9bd06-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="9bd06-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9bd06-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9bd06-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9bd06-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9bd06-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9bd06-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9bd06-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9bd06-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9bd06-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9bd06-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9bd06-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9bd06-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9bd06-110">Definisce il centro dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="9bd06-110">Defines the center of the shadow.</span></span> <span data-ttu-id="9bd06-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9bd06-111">Read/write.</span></span> <span data-ttu-id="9bd06-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="9bd06-112">**VgVector2D**.</span></span>

<span data-ttu-id="9bd06-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="9bd06-113">**Applies To**</span></span>

[<span data-ttu-id="9bd06-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="9bd06-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="9bd06-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="9bd06-115">**Tag Syntax**</span></span>

<span data-ttu-id="9bd06-116"><v: *element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9bd06-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="9bd06-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="9bd06-117">**Script Syntax**</span></span>

<span data-ttu-id="9bd06-118">*element* . Origin = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="9bd06-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="9bd06-119">*espressione* = *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="9bd06-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="9bd06-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="9bd06-120">**Remarks**</span></span>

<span data-ttu-id="9bd06-121">Coppia di valori frazionari della forma, compresi tra 50% e-50%.</span><span class="sxs-lookup"><span data-stu-id="9bd06-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="9bd06-122">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="9bd06-122">The default value is 0,0.</span></span>

<span data-ttu-id="9bd06-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="9bd06-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9bd06-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="9bd06-124">**Example**</span></span>

<span data-ttu-id="9bd06-125">L'ombreggiatura ha un'origine che è il 20% verso il basso e il 20% a destra dell'origine della forma.</span><span class="sxs-lookup"><span data-stu-id="9bd06-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 