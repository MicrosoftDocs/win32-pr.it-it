---
title: La MSO-attributo in modalità wrap
description: La MSO-attributo in modalità wrap
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338094"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="7015e-103">La MSO-attributo in modalità wrap</span><span class="sxs-lookup"><span data-stu-id="7015e-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="7015e-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7015e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7015e-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="7015e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7015e-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="7015e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7015e-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="7015e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7015e-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7015e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7015e-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7015e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7015e-110">Definisce la modalità di wrapping per il testo.</span><span class="sxs-lookup"><span data-stu-id="7015e-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="7015e-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7015e-111">Read/write.</span></span> <span data-ttu-id="7015e-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="7015e-112">**String**.</span></span>

<span data-ttu-id="7015e-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="7015e-113">**Applies To**</span></span>

[<span data-ttu-id="7015e-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="7015e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7015e-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="7015e-115">**Tag Syntax**</span></span>

<span data-ttu-id="7015e-116"><v: *elemento* Style = "MSO-Wrap-Mode: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7015e-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="7015e-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="7015e-117">**Remarks**</span></span>

<span data-ttu-id="7015e-118">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="7015e-118">Values include:</span></span>



| <span data-ttu-id="7015e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7015e-119">Value</span></span>          | <span data-ttu-id="7015e-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7015e-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="7015e-121">square</span><span class="sxs-lookup"><span data-stu-id="7015e-121">square</span></span>         | <span data-ttu-id="7015e-122">Esegue il wrapping del testo intorno alla forma in un quadrato.</span><span class="sxs-lookup"><span data-stu-id="7015e-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="7015e-123">una stretta</span><span class="sxs-lookup"><span data-stu-id="7015e-123">tight</span></span>          | <span data-ttu-id="7015e-124">Il testo viene incapsulato vicino alla forma.</span><span class="sxs-lookup"><span data-stu-id="7015e-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="7015e-125">in alto e in basso</span><span class="sxs-lookup"><span data-stu-id="7015e-125">top-and-bottom</span></span> | <span data-ttu-id="7015e-126">Il testo passa dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="7015e-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="7015e-127">-</span><span class="sxs-lookup"><span data-stu-id="7015e-127">through</span></span>        | <span data-ttu-id="7015e-128">Il testo viene visualizzato attraverso la forma.</span><span class="sxs-lookup"><span data-stu-id="7015e-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="7015e-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7015e-129">none</span></span>           | <span data-ttu-id="7015e-130">Il testo non viene incapsulato.</span><span class="sxs-lookup"><span data-stu-id="7015e-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="7015e-131">Usato da Microsoft PowerPoint per il salvataggio nel codice HTML per indicare se il ritorno a capo automatico all'interno di una forma è on (**Square**) o off (**nessuno**).</span><span class="sxs-lookup"><span data-stu-id="7015e-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="7015e-132">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="7015e-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="7015e-133">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="7015e-133">**Example**</span></span>

<span data-ttu-id="7015e-134">Il codice seguente indica che WordWrap all'interno di una forma AutoShape è attivato in PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="7015e-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 