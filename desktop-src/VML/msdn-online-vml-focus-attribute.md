---
title: LA-attributo attivo
description: LA-attributo attivo
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047339"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="f8cfa-103">LA-attributo attivo</span><span class="sxs-lookup"><span data-stu-id="f8cfa-103">VML Focus Attribute</span></span>

<span data-ttu-id="f8cfa-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f8cfa-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f8cfa-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f8cfa-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f8cfa-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f8cfa-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f8cfa-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f8cfa-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f8cfa-110">Definisce il centro di un riempimento sfumato lineare.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="f8cfa-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-111">Read/write.</span></span> <span data-ttu-id="f8cfa-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-112">**VgFraction**.</span></span>

<span data-ttu-id="f8cfa-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f8cfa-113">**Applies To**</span></span>

[<span data-ttu-id="f8cfa-114">Fill</span><span class="sxs-lookup"><span data-stu-id="f8cfa-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="f8cfa-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f8cfa-115">**Tag Syntax**</span></span>

<span data-ttu-id="f8cfa-116"><v: *elemento* Focus = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f8cfa-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="f8cfa-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f8cfa-117">**Script Syntax**</span></span>

<span data-ttu-id="f8cfa-118">*element* . Focus = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="f8cfa-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="f8cfa-119">*espressione* = *elemento*. Focus</span><span class="sxs-lookup"><span data-stu-id="f8cfa-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="f8cfa-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f8cfa-120">**Remarks**</span></span>

<span data-ttu-id="f8cfa-121">Definisce la posizione iniziale del centro della Blend.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="f8cfa-122">I valori sono compresi tra 100% e-100%.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="f8cfa-123">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-123">The default value is 0.</span></span> <span data-ttu-id="f8cfa-124">Un valore 100% (o-100%) Sposta lo stato attivo in modo da invertire la direzione della sfumatura (influisce sul **colore** e **color2**).</span><span class="sxs-lookup"><span data-stu-id="f8cfa-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="f8cfa-125">Il valore 50% modificherà la Blend in modo che il **colore** sia a entrambe le estremità e **color2** al centro.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="f8cfa-126">Il valore-50% modificherà la Blend in modo che **color2** sia a entrambe le estremità e il **colore** sia al centro.</span><span class="sxs-lookup"><span data-stu-id="f8cfa-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="f8cfa-127">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="f8cfa-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="f8cfa-128">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f8cfa-128">**Example**</span></span>

<span data-ttu-id="f8cfa-129">Lo stato attivo sfumato del riempimento viene spostato in modo che il rosso (**colore**) sarà una banda al centro della forma e che la parte superiore e inferiore sarà blu (**color2**).</span><span class="sxs-lookup"><span data-stu-id="f8cfa-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 