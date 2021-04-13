---
title: Attributo Gain la
description: Attributo Gain la
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399379"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="608d8-103">Attributo Gain la</span><span class="sxs-lookup"><span data-stu-id="608d8-103">VML Gain Attribute</span></span>

<span data-ttu-id="608d8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="608d8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="608d8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="608d8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="608d8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="608d8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="608d8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="608d8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="608d8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="608d8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="608d8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="608d8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="608d8-110">Definisce l'intensità di tutti i colori in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="608d8-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="608d8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="608d8-111">Read/write.</span></span> <span data-ttu-id="608d8-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="608d8-112">**VgNumber**.</span></span>

<span data-ttu-id="608d8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="608d8-113">**Applies To**</span></span>

[<span data-ttu-id="608d8-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="608d8-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="608d8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="608d8-115">**Tag Syntax**</span></span>

<span data-ttu-id="608d8-116"><v: *element* Gain = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="608d8-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="608d8-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="608d8-117">**Script Syntax**</span></span>

<span data-ttu-id="608d8-118">*element* . Gain = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="608d8-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="608d8-119">*espressione* = *elemento*. Gain</span><span class="sxs-lookup"><span data-stu-id="608d8-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="608d8-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="608d8-120">**Remarks**</span></span>

<span data-ttu-id="608d8-121">Questo attributo definisce la luminosità del colore bianco, che influisce su tutti gli altri colori.</span><span class="sxs-lookup"><span data-stu-id="608d8-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="608d8-122">I valori variano da 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="608d8-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="608d8-123">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="608d8-123">The default value is 1.0.</span></span> <span data-ttu-id="608d8-124">Il valore 0 non visualizza alcuna immagine.</span><span class="sxs-lookup"><span data-stu-id="608d8-124">A value of 0 displays no image.</span></span> <span data-ttu-id="608d8-125">I valori maggiori di 1 alleggeriscono l'immagine e i valori minori di 1 fanno sembrare il grigio.</span><span class="sxs-lookup"><span data-stu-id="608d8-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="608d8-126">Questo attributo può essere utilizzato per creare effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="608d8-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="608d8-127">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="608d8-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="608d8-128">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="608d8-128">**Example**</span></span>

<span data-ttu-id="608d8-129">L'immagine verrà visualizzata con tutti i colori tendenti verso il grigio.</span><span class="sxs-lookup"><span data-stu-id="608d8-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 