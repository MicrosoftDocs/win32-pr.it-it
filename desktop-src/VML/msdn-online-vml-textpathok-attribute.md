---
title: Attributo TextPathOK di la
description: Attributo TextPathOK di la
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872569"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="6fcbd-103">Attributo TextPathOK di la</span><span class="sxs-lookup"><span data-stu-id="6fcbd-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="6fcbd-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6fcbd-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6fcbd-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6fcbd-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6fcbd-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6fcbd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6fcbd-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6fcbd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6fcbd-110">Determina se verrà visualizzato un percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="6fcbd-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-111">Read/write.</span></span> <span data-ttu-id="6fcbd-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-112">**VgTriState**.</span></span>

<span data-ttu-id="6fcbd-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="6fcbd-113">**Applies To**</span></span>

[<span data-ttu-id="6fcbd-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fcbd-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="6fcbd-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="6fcbd-115">**Tag Syntax**</span></span>

<span data-ttu-id="6fcbd-116"><v: *element* textpathok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6fcbd-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="6fcbd-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="6fcbd-117">**Script Syntax**</span></span>

<span data-ttu-id="6fcbd-118">*elemento* .</span><span class="sxs-lookup"><span data-stu-id="6fcbd-118">*element* .</span></span> <span data-ttu-id="6fcbd-119">textpathok = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="6fcbd-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="6fcbd-120">*espressione* = *elemento*.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-120">*expression*=*element*.</span></span> <span data-ttu-id="6fcbd-121">textpathok</span><span class="sxs-lookup"><span data-stu-id="6fcbd-121">textpathok</span></span>

<span data-ttu-id="6fcbd-122">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="6fcbd-122">**Remarks**</span></span>

<span data-ttu-id="6fcbd-123">Se **false**, il percorso non può contenere un percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="6fcbd-124">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-124">The default is **False**.</span></span> <span data-ttu-id="6fcbd-125">Questo attributo deve essere impostato su **true** per visualizzare il testo in un percorso.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="6fcbd-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="6fcbd-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="6fcbd-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="6fcbd-127">**Example**</span></span>

<span data-ttu-id="6fcbd-128">La forma ha un percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-128">The shape has a text path.</span></span> <span data-ttu-id="6fcbd-129">Viene visualizzato il testo "Hello la" lungo una curva a forma di Smile.</span><span class="sxs-lookup"><span data-stu-id="6fcbd-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 