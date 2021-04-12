---
title: Attributo color2 (Stroke) (la)
description: Attributo color2 (Stroke) (la)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473763"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="2fa8c-103">Attributo color2 (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="2fa8c-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="2fa8c-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2fa8c-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2fa8c-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2fa8c-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2fa8c-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2fa8c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2fa8c-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2fa8c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2fa8c-110">Definisce un secondo colore per i tratti.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-110">Defines a second color for strokes.</span></span> <span data-ttu-id="2fa8c-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-111">Read/write.</span></span> <span data-ttu-id="2fa8c-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-112">**String**.</span></span>

<span data-ttu-id="2fa8c-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="2fa8c-113">**Applies To**</span></span>

[<span data-ttu-id="2fa8c-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="2fa8c-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="2fa8c-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="2fa8c-115">**Tag Syntax**</span></span>

<span data-ttu-id="2fa8c-116"><v: *element* color2 = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2fa8c-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="2fa8c-117">Sintassi dello script</span><span class="sxs-lookup"><span data-stu-id="2fa8c-117">Script Syntax</span></span>

<span data-ttu-id="2fa8c-118">*element* . color2 = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="2fa8c-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="2fa8c-119">*espressione* = *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="2fa8c-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="2fa8c-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="2fa8c-120">**Remarks**</span></span>

<span data-ttu-id="2fa8c-121">Un secondo colore viene usato quando il tipo di riempimento di un tratto è un modello.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="2fa8c-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="2fa8c-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="2fa8c-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="2fa8c-123">**Example**</span></span>

<span data-ttu-id="2fa8c-124">Il tratto della forma è un riempimento di pattern in cui il riempimento viene definito dall'immagine di origine, ma lo sfondo trasparente viene definito dal secondo colore.</span><span class="sxs-lookup"><span data-stu-id="2fa8c-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 