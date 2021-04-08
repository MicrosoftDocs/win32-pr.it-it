---
title: Attributo Angle (Fill) (la)
description: Attributo Angle (Fill) (la)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047272"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="62c52-103">Attributo Angle (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="62c52-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="62c52-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="62c52-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="62c52-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="62c52-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="62c52-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="62c52-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="62c52-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="62c52-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="62c52-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="62c52-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="62c52-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="62c52-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="62c52-110">Definisce l'angolo di un riempimento sfumato.</span><span class="sxs-lookup"><span data-stu-id="62c52-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="62c52-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="62c52-111">Read/write.</span></span> <span data-ttu-id="62c52-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="62c52-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="62c52-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="62c52-113">**Applies To**</span></span>

[<span data-ttu-id="62c52-114">Fill</span><span class="sxs-lookup"><span data-stu-id="62c52-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="62c52-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="62c52-115">**Tag Syntax**</span></span>

<span data-ttu-id="62c52-116"><v: *element* Angle = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="62c52-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="62c52-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="62c52-117">**Script Syntax**</span></span>

<span data-ttu-id="62c52-118">*element* . Angle = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="62c52-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="62c52-119">*espressione* = *elemento*. angolo</span><span class="sxs-lookup"><span data-stu-id="62c52-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="62c52-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="62c52-120">**Remarks**</span></span>

<span data-ttu-id="62c52-121">Il vettore di una sfumatura è perpendicolare al vettore della direzione di Blend da un colore a un altro.</span><span class="sxs-lookup"><span data-stu-id="62c52-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="62c52-122">Il valore predefinito è 0 (zero) gradi, ovvero un vettore orizzontale da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="62c52-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="62c52-123">Gli angoli positivi ruotano la sfumatura in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="62c52-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="62c52-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="62c52-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="62c52-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="62c52-125">**Example**</span></span>

<span data-ttu-id="62c52-126">Il riempimento della forma è costituito da una sfumatura di due colori, in esecuzione da blu a rosso a un angolo di 45 gradi.</span><span class="sxs-lookup"><span data-stu-id="62c52-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="62c52-127">Il rosso sarà nell'angolo superiore sinistro e blu sarà nell'angolo inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="62c52-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 