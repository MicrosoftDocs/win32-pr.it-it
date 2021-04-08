---
title: Attributo BWNormal di la
description: Attributo BWNormal di la
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046952"
---
# <a name="vml-bwnormal-attribute"></a><span data-ttu-id="3800b-103">Attributo BWNormal di la</span><span class="sxs-lookup"><span data-stu-id="3800b-103">VML BWNormal Attribute</span></span>

<span data-ttu-id="3800b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3800b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3800b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3800b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3800b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3800b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3800b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3800b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3800b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3800b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3800b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3800b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3800b-110">Definisce la modalità in bianco e nero per i normali dispositivi di output in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="3800b-110">Defines the black-and-white mode for normal black-and-white output devices.</span></span> <span data-ttu-id="3800b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3800b-111">Read/write.</span></span> <span data-ttu-id="3800b-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="3800b-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="3800b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3800b-113">**Applies To**</span></span>

[<span data-ttu-id="3800b-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="3800b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3800b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3800b-115">**Tag Syntax**</span></span>

<span data-ttu-id="3800b-116"><v: *element* o:bwnormal = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3800b-116"><v: *element* o:bwnormal=" *expression* "></span></span>

<span data-ttu-id="3800b-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3800b-117">**Remarks**</span></span>

<span data-ttu-id="3800b-118">Quando [BWMode](msdn-online-vml-bwmode-attribute.md) è impostato su **auto**, questo attributo viene usato per determinare come eseguire il rendering della forma in bianco e nero normale.</span><span class="sxs-lookup"><span data-stu-id="3800b-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in normal black and white.</span></span>

<span data-ttu-id="3800b-119">Per ulteriori informazioni sui valori di questo attributo, vedere l'argomento [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="3800b-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="3800b-120">Il valore predefinito è **auto**.</span><span class="sxs-lookup"><span data-stu-id="3800b-120">The default value is **auto**.</span></span>

<span data-ttu-id="3800b-121">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="3800b-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3800b-122">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3800b-122">**Example**</span></span>

<span data-ttu-id="3800b-123">La forma viene elaborata come immagine in scala di grigi per l'output normale in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="3800b-123">The shape is processed as a grayscale image for normal black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 