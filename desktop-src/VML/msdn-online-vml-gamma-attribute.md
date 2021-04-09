---
title: Attributo gamma la
description: Attributo gamma la
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b74c80739d694038601588eee4c8ad7ed90923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118086"
---
# <a name="vml-gamma-attribute"></a><span data-ttu-id="c74b5-103">Attributo gamma la</span><span class="sxs-lookup"><span data-stu-id="c74b5-103">VML Gamma Attribute</span></span>

<span data-ttu-id="c74b5-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c74b5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c74b5-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c74b5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c74b5-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c74b5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c74b5-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c74b5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c74b5-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c74b5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c74b5-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c74b5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c74b5-110">Definisce la quantità di contrasto per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="c74b5-110">Defines the amount of contrast for an image.</span></span> <span data-ttu-id="c74b5-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c74b5-111">Read/write.</span></span> <span data-ttu-id="c74b5-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="c74b5-112">**VgNumber**.</span></span>

<span data-ttu-id="c74b5-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c74b5-113">**Applies To**</span></span>

[<span data-ttu-id="c74b5-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="c74b5-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="c74b5-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c74b5-115">**Tag Syntax**</span></span>

<span data-ttu-id="c74b5-116"><v: *element* gamma = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c74b5-116"><v: *element* gamma=" *expression* "></span></span>

<span data-ttu-id="c74b5-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="c74b5-117">**Script Syntax**</span></span>

<span data-ttu-id="c74b5-118">*element* . gamma = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="c74b5-118">*element* .gamma="*expression*"</span></span>

<span data-ttu-id="c74b5-119">*espressione* = *element*. gamma</span><span class="sxs-lookup"><span data-stu-id="c74b5-119">*expression*=*element*.gamma</span></span>

<span data-ttu-id="c74b5-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c74b5-120">**Remarks**</span></span>

<span data-ttu-id="c74b5-121">Diminuendo la gamma sotto 1 si modifica un'immagine per renderla più a contrasto, mentre i valori maggiori di 1 riducono il contrasto.</span><span class="sxs-lookup"><span data-stu-id="c74b5-121">Decreasing the gamma below 1 modifies an image to make it more contrasty, while values greater than 1 decrease the contrast.</span></span> <span data-ttu-id="c74b5-122">I valori utili sono compresi tra 0,3 e 3.</span><span class="sxs-lookup"><span data-stu-id="c74b5-122">Useful values are from 0.3 to about 3.</span></span> <span data-ttu-id="c74b5-123">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="c74b5-123">The default value is 0.</span></span>

<span data-ttu-id="c74b5-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="c74b5-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c74b5-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c74b5-125">**Example**</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 