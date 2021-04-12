---
title: Attributo Chromakey di la
description: Attributo Chromakey di la
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338142"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="ea229-103">Attributo Chromakey di la</span><span class="sxs-lookup"><span data-stu-id="ea229-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="ea229-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ea229-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ea229-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ea229-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ea229-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ea229-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ea229-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ea229-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ea229-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ea229-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ea229-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ea229-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ea229-110">Definisce il valore del colore dell'immagine che verrà considerato trasparente.</span><span class="sxs-lookup"><span data-stu-id="ea229-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="ea229-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ea229-111">Read/write.</span></span> <span data-ttu-id="ea229-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="ea229-112">**VgColor**.</span></span>

<span data-ttu-id="ea229-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ea229-113">**Applies To**</span></span>

[<span data-ttu-id="ea229-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="ea229-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="ea229-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ea229-115">**Tag Syntax**</span></span>

<span data-ttu-id="ea229-116"><v: *element* Chromakey = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ea229-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="ea229-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ea229-117">**Script Syntax**</span></span>

<span data-ttu-id="ea229-118">*element* . Chromakey = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ea229-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="ea229-119">*espressione* = *elemento*. Chromakey</span><span class="sxs-lookup"><span data-stu-id="ea229-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="ea229-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ea229-120">**Remarks**</span></span>

<span data-ttu-id="ea229-121">Utilizzare questo attributo per rendere trasparente le parti di un'immagine mediante l'impostazione della trasparenza su un colore specifico.</span><span class="sxs-lookup"><span data-stu-id="ea229-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="ea229-122">Se, ad esempio, il valore **Chromakey** è **nero**, qualsiasi parte dell'immagine che è nera sarà trasparente e il colore di riempimento verrà visualizzato nella parte dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="ea229-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="ea229-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ea229-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ea229-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ea229-124">**Example**</span></span>

<span data-ttu-id="ea229-125">Le aree dell'immagine che sono nere a tinta unita diventeranno trasparenti, consentendo di visualizzare il colore di riempimento verde attraverso tali aree.</span><span class="sxs-lookup"><span data-stu-id="ea229-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 