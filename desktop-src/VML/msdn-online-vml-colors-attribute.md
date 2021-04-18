---
title: Attributo colori la
description: Attributo colori la
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516965"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="f43f3-103">Attributo colori la</span><span class="sxs-lookup"><span data-stu-id="f43f3-103">VML Colors Attribute</span></span>

<span data-ttu-id="f43f3-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f43f3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f43f3-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f43f3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f43f3-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f43f3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f43f3-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f43f3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f43f3-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f43f3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f43f3-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f43f3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f43f3-110">Definisce più colori per un riempimento sfumato.</span><span class="sxs-lookup"><span data-stu-id="f43f3-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="f43f3-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f43f3-111">Read/write.</span></span> <span data-ttu-id="f43f3-112">**IVgGradientColorArray**.</span><span class="sxs-lookup"><span data-stu-id="f43f3-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="f43f3-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f43f3-113">**Applies To**</span></span>

[<span data-ttu-id="f43f3-114">Fill</span><span class="sxs-lookup"><span data-stu-id="f43f3-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="f43f3-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f43f3-115">**Tag Syntax**</span></span>

<span data-ttu-id="f43f3-116"><v: *elemento* Colors = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f43f3-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="f43f3-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f43f3-117">**Script Syntax**</span></span>

<span data-ttu-id="f43f3-118">*element* . Colors = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="f43f3-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="f43f3-119">*espressione* = *elemento*. Colors</span><span class="sxs-lookup"><span data-stu-id="f43f3-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="f43f3-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f43f3-120">**Remarks**</span></span>

<span data-ttu-id="f43f3-121">Utilizzato per definire una matrice costituita da valori abbinati di percentuali ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) e color ([VgColor](msdn-online-vml-ivgcolor.md)).</span><span class="sxs-lookup"><span data-stu-id="f43f3-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="f43f3-122">La matrice crea un riempimento sfumato usando ogni punto della matrice, a partire dallo 0% (definito da **colore**) e terminando al 100% (definito da **color2**).</span><span class="sxs-lookup"><span data-stu-id="f43f3-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="f43f3-123">È possibile definire colori intermedi lungo il percorso assegnando un valore di colore a una percentuale.</span><span class="sxs-lookup"><span data-stu-id="f43f3-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="f43f3-124">La coppia percentuale e colore non è separata da una virgola, ma le coppie sono separate tra loro da virgole.</span><span class="sxs-lookup"><span data-stu-id="f43f3-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="f43f3-125">Attributo standard la</span><span class="sxs-lookup"><span data-stu-id="f43f3-125">VML Standard Attribute</span></span>

<span data-ttu-id="f43f3-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f43f3-126">**Example**</span></span>

<span data-ttu-id="f43f3-127">La forma presenta un riempimento sfumato costituito da quattro colori, a partire da rosso, da sfumatura a giallo, da verde a finallyblue.</span><span class="sxs-lookup"><span data-stu-id="f43f3-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 