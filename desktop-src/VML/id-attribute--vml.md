---
title: Attributo ID (la)
description: Attributo ID (la)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473478"
---
# <a name="id-attribute-vml"></a><span data-ttu-id="311a4-103">Attributo ID (la)</span><span class="sxs-lookup"><span data-stu-id="311a4-103">ID Attribute (VML)</span></span>

<span data-ttu-id="311a4-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="311a4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="311a4-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="311a4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="311a4-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="311a4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="311a4-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="311a4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="311a4-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="311a4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="311a4-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="311a4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="311a4-110">Fornisce un identificatore univoco per un elemento.</span><span class="sxs-lookup"><span data-stu-id="311a4-110">Provides a unique identifier for an element.</span></span> <span data-ttu-id="311a4-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="311a4-111">Read/write.</span></span> <span data-ttu-id="311a4-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="311a4-112">**String**.</span></span>

<span data-ttu-id="311a4-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="311a4-113">**Applies To**</span></span>

<span data-ttu-id="311a4-114">Tutti gli elementi la.</span><span class="sxs-lookup"><span data-stu-id="311a4-114">All VML elements.</span></span>

<span data-ttu-id="311a4-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="311a4-115">**Tag Syntax**</span></span>

<span data-ttu-id="311a4-116"><v: *ElementName* ID = " *IDname* " ></span><span class="sxs-lookup"><span data-stu-id="311a4-116"><v: *elementname* id=" *idname* "></span></span>

<span data-ttu-id="311a4-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="311a4-117">**Script Syntax**</span></span>

<span data-ttu-id="311a4-118">*ElementName* . ID = " *IDname* "</span><span class="sxs-lookup"><span data-stu-id="311a4-118">*elementname* .id =" *idname* "</span></span>

<span data-ttu-id="311a4-119">*espressione* = *ElementName*. ID</span><span class="sxs-lookup"><span data-stu-id="311a4-119">*expression*=*elementname*.id</span></span>

<span data-ttu-id="311a4-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="311a4-120">**Remarks**</span></span>

<span data-ttu-id="311a4-121">Usare **ID** per fare riferimento a un elemento specifico.</span><span class="sxs-lookup"><span data-stu-id="311a4-121">Use **ID** to refer to a specific element.</span></span> <span data-ttu-id="311a4-122">Dopo aver creato una forma e dato un ID, è possibile utilizzare il nome ID quando si desidera modificare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="311a4-122">Once you have created a shape and given it an ID, you can use the ID name when you want to manipulate the element.</span></span>

<span data-ttu-id="311a4-123">L' **ID** è necessario per usare l'elemento [TipoForma](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="311a4-123">**ID** is required to use the [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span>

<span data-ttu-id="311a4-124">Quando la viene generato da Microsoft Office, se il nome di un modello a oggetti viene assegnato alla forma, l' **ID** viene impostato su questo nome.</span><span class="sxs-lookup"><span data-stu-id="311a4-124">When VML is generated by Microsoft Office, if an object model name is assigned to the shape, then **ID** is set to this name.</span></span> <span data-ttu-id="311a4-125">Se il nome del modello a oggetti non è impostato, il nome viene generato utilizzando *SPID* (Internal Shape ID) più un prefisso (S per Shape, M per la forma master, T per TipoForma).</span><span class="sxs-lookup"><span data-stu-id="311a4-125">If the object model name is not set, then the name is generated using the *Spid* (internal shape ID) plus a prefix (S for shape, M for master shape, T for shapetype).</span></span>

<span data-ttu-id="311a4-126">*Attributo standard la*.</span><span class="sxs-lookup"><span data-stu-id="311a4-126">*VML Standard Attribute*.</span></span>

<span data-ttu-id="311a4-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="311a4-127">**Example**</span></span>

<span data-ttu-id="311a4-128">Per modificare gli attributi di una forma, è necessario innanzitutto assegnare un ID alla forma. ad esempio, "rect".</span><span class="sxs-lookup"><span data-stu-id="311a4-128">To change the attributes of a shape, you must first give the shape an ID; for example, "myrect".</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



<span data-ttu-id="311a4-129">[Esempio di attributo ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span><span class="sxs-lookup"><span data-stu-id="311a4-129">[ID Attribute Example](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span></span> <span data-ttu-id="311a4-130">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="311a4-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 