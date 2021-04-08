---
title: Attributo BWMode di la
description: Attributo BWMode di la
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728295"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="22514-103">Attributo BWMode di la</span><span class="sxs-lookup"><span data-stu-id="22514-103">VML BWMode Attribute</span></span>

<span data-ttu-id="22514-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="22514-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="22514-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="22514-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="22514-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="22514-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="22514-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="22514-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="22514-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="22514-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="22514-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="22514-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="22514-110">Determina come viene eseguito il rendering di una forma per i dispositivi di output neri e bianchi.</span><span class="sxs-lookup"><span data-stu-id="22514-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="22514-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="22514-111">Read/write.</span></span> <span data-ttu-id="22514-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="22514-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="22514-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="22514-113">**Applies To**</span></span>

[<span data-ttu-id="22514-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="22514-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="22514-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="22514-115">**Tag Syntax**</span></span>

<span data-ttu-id="22514-116"><v: *element* o:bwmode = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="22514-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="22514-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="22514-117">**Remarks**</span></span>

<span data-ttu-id="22514-118">Quando una forma viene stampata su una stampante nera e bianca o visualizzata in una visualizzazione in bianco e nero in un'applicazione, sono possibili diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="22514-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="22514-119">Per ulteriori informazioni sui valori di questo attributo, vedere l'argomento [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="22514-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="22514-120">Il valore predefinito è **auto**.</span><span class="sxs-lookup"><span data-stu-id="22514-120">The default value is **auto**.</span></span>

<span data-ttu-id="22514-121">Se viene specificato **auto** , viene usato [BWNormal](msdn-online-vml-bwnormal-attribute.md) per determinare il comportamento per l'output normale nero e bianco e [BWPure](msdn-online-vml-bwpure-attribute.md) viene usato per determinare il comportamento per l'output puro nero e bianco.</span><span class="sxs-lookup"><span data-stu-id="22514-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="22514-122">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="22514-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="22514-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="22514-123">**Example**</span></span>

<span data-ttu-id="22514-124">La modalità nero e bianco della forma è **auto**.</span><span class="sxs-lookup"><span data-stu-id="22514-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 