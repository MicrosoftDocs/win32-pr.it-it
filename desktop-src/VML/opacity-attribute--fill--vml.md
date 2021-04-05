---
title: Attributo Opacity (Fill) (la)
description: Attributo Opacity (Fill) (la)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730135"
---
# <a name="opacity-attribute-fillvml"></a><span data-ttu-id="c3dd5-103">Attributo Opacity (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="c3dd5-103">Opacity Attribute (Fill)(VML)</span></span>

<span data-ttu-id="c3dd5-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c3dd5-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c3dd5-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c3dd5-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c3dd5-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c3dd5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c3dd5-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c3dd5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c3dd5-110">Definisce la trasparenza di un riempimento.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-110">Defines the transparency of a fill.</span></span> <span data-ttu-id="c3dd5-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-111">Read/write.</span></span> <span data-ttu-id="c3dd5-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="c3dd5-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span>

<span data-ttu-id="c3dd5-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c3dd5-113">**Applies To**</span></span>

[<span data-ttu-id="c3dd5-114">Fill</span><span class="sxs-lookup"><span data-stu-id="c3dd5-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c3dd5-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c3dd5-115">**Tag Syntax**</span></span>

<span data-ttu-id="c3dd5-116"><v: *elemento* Opacity = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c3dd5-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="c3dd5-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="c3dd5-117">**Script Syntax**</span></span>

<span data-ttu-id="c3dd5-118">*element* . Opacity = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="c3dd5-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="c3dd5-119">*espressione* = *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="c3dd5-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="c3dd5-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c3dd5-120">**Remarks**</span></span>

<span data-ttu-id="c3dd5-121">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-121">The default value is 1.0.</span></span>

<span data-ttu-id="c3dd5-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="c3dd5-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="c3dd5-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c3dd5-123">**Example**</span></span>

<span data-ttu-id="c3dd5-124">Il riempimento della forma sarà trasparente al 50%.</span><span class="sxs-lookup"><span data-stu-id="c3dd5-124">The fill of the shape will be 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 