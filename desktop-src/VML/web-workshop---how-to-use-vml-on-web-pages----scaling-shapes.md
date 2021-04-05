---
title: Ridimensionamento di forme
description: Ridimensionamento di forme
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Web Workshop, ridimensionamento delle forme
- progettazione di pagine Web, ridimensionamento delle forme
- Vector Markup Language (la), ridimensionamento delle forme
- LA (Vector Markup Language), ridimensionamento delle forme
- grafica vettoriale, forme di ridimensionamento
- LA forme, ridimensionamento
- ridimensionamento di forme
- Vector Markup Language (la), forme di ridimensionamento
- LA (Vector Markup Language), forme di ridimensionamento
- grafica vettoriale, forme di ridimensionamento
- Forme la, ridimensionamento
- ridimensionamento di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727938"
---
# <a name="scaling-shapes"></a><span data-ttu-id="9ffc6-115">Ridimensionamento di forme</span><span class="sxs-lookup"><span data-stu-id="9ffc6-115">Scaling Shapes</span></span>

<span data-ttu-id="9ffc6-116">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9ffc6-117">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9ffc6-118">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9ffc6-119">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9ffc6-120">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9ffc6-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9ffc6-121">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9ffc6-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9ffc6-122">Si è appreso come creare e colorare forme in una pagina Web usando la.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="9ffc6-123">In questo argomento verrà illustrato come ridimensionare le forme con le dimensioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="9ffc6-124">LA utilizza la stessa sintassi definita nella sezione [Dettagli del modello di rendering visivo](https://www.w3.org/TR/PR-CSS2/visudet.mdl) della [specifica CSS2](https://www.w3.org/TR/PR-CSS2/) per specificare le dimensioni della casella contenitore in modo che il contenuto di una forma venga sottoposto a rendering (tracciato) all'interno della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="9ffc6-125">È possibile utilizzare gli attributi di stile **larghezza** e **altezza** per definire le dimensioni della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="9ffc6-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="9ffc6-126">Se ad esempio si disegna un ovale e si specifica **Style**=' width: 75pt; Height: 100PT ', l'ovale verrà disegnato all'interno di una casella contenitore con una dimensione di 75 punti (larghezza) di 100 punti (altezza), come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="9ffc6-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 byte)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="9ffc6-128">Se si modifica la dimensione in **Style**=' width: 120pt; Height: 140pt ', l'ovale diventa più grande perché viene ridimensionato all'interno della nuova casella contenitore con una dimensione di 120 punti (larghezza) per 140 punti (altezza), come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="9ffc6-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 byte)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="9ffc6-130">Se si modifica la dimensione in **Style**=' width: 60pt; Height: 40pt ', l'ovale diventa più piccolo perché viene ridimensionato all'interno della nuova casella contenitore con una dimensione di 60 punti (larghezza) per 40 punti (altezza), come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="9ffc6-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 byte)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 