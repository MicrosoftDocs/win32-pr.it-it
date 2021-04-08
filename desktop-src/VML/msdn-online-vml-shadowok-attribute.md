---
title: Attributo ShadowOK di la
description: Attributo ShadowOK di la
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046777"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="f9527-103">Attributo ShadowOK di la</span><span class="sxs-lookup"><span data-stu-id="f9527-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="f9527-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f9527-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f9527-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f9527-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f9527-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f9527-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f9527-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f9527-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f9527-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f9527-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f9527-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f9527-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f9527-110">Determina se verrà visualizzata un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="f9527-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="f9527-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f9527-111">Read/write.</span></span> <span data-ttu-id="f9527-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f9527-112">**VgTriState**.</span></span>

<span data-ttu-id="f9527-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f9527-113">**Applies To**</span></span>

[<span data-ttu-id="f9527-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="f9527-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="f9527-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f9527-115">**Tag Syntax**</span></span>

<span data-ttu-id="f9527-116"><v: *element* shadowok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f9527-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="f9527-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f9527-117">**Script Syntax**</span></span>

<span data-ttu-id="f9527-118">*element* . shadowok = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="f9527-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="f9527-119">*espressione* = *elemento*. shadowok</span><span class="sxs-lookup"><span data-stu-id="f9527-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="f9527-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f9527-120">**Remarks**</span></span>

<span data-ttu-id="f9527-121">Se **false**, il percorso non può contenere un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="f9527-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="f9527-122">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="f9527-122">The default is **True**.</span></span> <span data-ttu-id="f9527-123">Questo attributo esegue l'override di tutti gli altri attributi shadow nell'elemento padre o **shadow** .</span><span class="sxs-lookup"><span data-stu-id="f9527-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="f9527-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="f9527-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f9527-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f9527-125">**Example**</span></span>

<span data-ttu-id="f9527-126">La forma non avrà un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="f9527-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 