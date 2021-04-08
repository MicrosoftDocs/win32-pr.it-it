---
title: Attributo color2 (Shadow) (la)
description: Attributo color2 (Shadow) (la)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729194"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="63715-103">Attributo color2 (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="63715-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="63715-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="63715-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63715-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="63715-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63715-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="63715-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63715-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="63715-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63715-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="63715-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63715-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="63715-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63715-110">Definisce il secondo colore di un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="63715-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="63715-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="63715-111">Read/write.</span></span> <span data-ttu-id="63715-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="63715-112">**VgColor**.</span></span>

<span data-ttu-id="63715-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="63715-113">**Applies To**</span></span>

[<span data-ttu-id="63715-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="63715-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="63715-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="63715-115">**Tag Syntax**</span></span>

<span data-ttu-id="63715-116"><v: *element* color2 = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="63715-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="63715-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="63715-117">**Script Syntax**</span></span>

<span data-ttu-id="63715-118">*element* . color2 = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="63715-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="63715-119">*espressione* = *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="63715-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="63715-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="63715-120">**Remarks**</span></span>

<span data-ttu-id="63715-121">Usare un secondo colore per creare effetti speciali di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="63715-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="63715-122">Per ulteriori informazioni sui secondi colori, vedere l'attributo [Type](type-attribute--shadow--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="63715-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="63715-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="63715-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="63715-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="63715-124">**Example**</span></span>

<span data-ttu-id="63715-125">L'ombreggiatura è blu per un secondo colore.</span><span class="sxs-lookup"><span data-stu-id="63715-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 