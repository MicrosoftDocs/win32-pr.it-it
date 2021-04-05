---
title: Attributo Path la
description: Attributo Path la
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872922"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="40130-103">Attributo Path la</span><span class="sxs-lookup"><span data-stu-id="40130-103">VML Path Attribute</span></span>

<span data-ttu-id="40130-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="40130-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="40130-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="40130-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="40130-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="40130-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="40130-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="40130-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="40130-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="40130-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="40130-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="40130-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="40130-110">Specifica la linea che costituisce i bordi di una forma.</span><span class="sxs-lookup"><span data-stu-id="40130-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="40130-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="40130-111">Read/write.</span></span> <span data-ttu-id="40130-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="40130-112">**String**.</span></span>

<span data-ttu-id="40130-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="40130-113">**Applies To**</span></span>

[<span data-ttu-id="40130-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="40130-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="40130-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="40130-115">**Tag Syntax**</span></span>

<span data-ttu-id="40130-116"><v: *elemento* path = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="40130-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="40130-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="40130-117">**Script Syntax**</span></span>

<span data-ttu-id="40130-118">*element* . Path = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="40130-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="40130-119">*espressione* = *elemento*. Path</span><span class="sxs-lookup"><span data-stu-id="40130-119">*expression*=*element*.path</span></span>

<span data-ttu-id="40130-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="40130-120">**Remarks**</span></span>

<span data-ttu-id="40130-121">Se una forma contiene l'elemento [path](msdn-online-vml-path-element.md) , i comandi Path dell'elemento Path hanno la precedenza sul valore dell'attributo Shape.</span><span class="sxs-lookup"><span data-stu-id="40130-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="40130-122">Per informazioni dettagliate sul set di comandi usato per i percorsi, vedere l'argomento relativo all'elemento **path** .</span><span class="sxs-lookup"><span data-stu-id="40130-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="40130-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="40130-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="40130-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="40130-124">**Example**</span></span>

<span data-ttu-id="40130-125">Un percorso quadrato chiuso viene definito nella stringa dell'attributo path.</span><span class="sxs-lookup"><span data-stu-id="40130-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="40130-126">Un punto iniziale viene definito con `m` (usato per il comando **MoveTo** ) a 1, 1 e viene disegnata una riga con la `l` lettera "L" usata per il comando **LineTo** dalla posizione iniziale (1,1) agli altri tre punti (in ordine): 1.200; 200.200; 200, 1.</span><span class="sxs-lookup"><span data-stu-id="40130-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="40130-127">La riga viene chiusa con `x` (**Close**) e terminata con `e` (**end**).</span><span class="sxs-lookup"><span data-stu-id="40130-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="40130-128">Si noti che le coordinate sono specificate nello spazio delle coordinate relative e che la dimensione reale è determinata dalla **larghezza** e dall' **altezza**.</span><span class="sxs-lookup"><span data-stu-id="40130-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="40130-129">[Esempio di attributo path](/previous-versions/bb264089(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="40130-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="40130-130">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="40130-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 