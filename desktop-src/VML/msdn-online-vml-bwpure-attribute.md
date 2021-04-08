---
title: Attributo BWPure di la
description: Attributo BWPure di la
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872673"
---
# <a name="vml-bwpure-attribute"></a><span data-ttu-id="6bb15-103">Attributo BWPure di la</span><span class="sxs-lookup"><span data-stu-id="6bb15-103">VML BWPure Attribute</span></span>

<span data-ttu-id="6bb15-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6bb15-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6bb15-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="6bb15-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6bb15-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="6bb15-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6bb15-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="6bb15-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6bb15-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6bb15-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6bb15-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6bb15-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6bb15-110">Definisce la modalità in bianco e nero per i dispositivi di output puri in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="6bb15-110">Defines the black-and-white mode for pure black-and-white output devices.</span></span> <span data-ttu-id="6bb15-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6bb15-111">Read/write.</span></span> <span data-ttu-id="6bb15-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="6bb15-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="6bb15-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="6bb15-113">**Applies To**</span></span>

[<span data-ttu-id="6bb15-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="6bb15-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6bb15-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="6bb15-115">**Tag Syntax**</span></span>

<span data-ttu-id="6bb15-116"><v: *element* o:bwpure = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6bb15-116"><v: *element* o:bwpure=" *expression* "></span></span>

<span data-ttu-id="6bb15-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="6bb15-117">**Remarks**</span></span>

<span data-ttu-id="6bb15-118">Quando [BWMode](msdn-online-vml-bwmode-attribute.md) è impostato su **auto**, questo attributo viene usato per determinare come eseguire il rendering della forma in bianco e nero puro.</span><span class="sxs-lookup"><span data-stu-id="6bb15-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in pure black and white.</span></span>

<span data-ttu-id="6bb15-119">Per ulteriori informazioni sui valori di questo attributo, vedere l'argomento [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb15-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="6bb15-120">Il valore predefinito è **auto**.</span><span class="sxs-lookup"><span data-stu-id="6bb15-120">The default is **auto**.</span></span>

<span data-ttu-id="6bb15-121">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="6bb15-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="6bb15-122">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="6bb15-122">**Example**</span></span>

<span data-ttu-id="6bb15-123">La forma viene elaborata come immagine a contrasto elevato per l'output puro nero e bianco.</span><span class="sxs-lookup"><span data-stu-id="6bb15-123">The shape is processed as a high contrast image for pure black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 