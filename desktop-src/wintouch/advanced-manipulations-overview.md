---
title: Cenni preliminari sulle manipolazioni avanzate
description: In questa sezione vengono illustrate le modifiche avanzate per le applicazioni.
ms.assetid: a0c3fecb-d3c7-4f12-90be-5f77f4f5883e
keywords:
- Windows Touch, modifiche
- Windows Touch, modifiche avanzate
- Windows Touch, modifiche complesse
- Windows Touch, espansione
- Windows Touch, espansione avanzata
- Windows Touch, rotazione
- Windows Touch, rotazione avanzata
- Windows Touch, traduzione
- Windows Touch, traduzione avanzata
- manipolazioni, avanzate
- manipolazioni, complesse
- manipolazioni, espansione
- manipolazioni, espansione avanzata
- manipolazioni, rotazione
- manipolazioni, rotazione avanzata
- manipolazioni, traduzione
- manipolazioni, traduzione avanzata
- espansione, avanzata
- rotazione, avanzata
- traduzione, avanzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f58a5dffb3c2d11e07a8c6495ec777579916481
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044202"
---
# <a name="advanced-manipulations-overview"></a><span data-ttu-id="5b0ea-123">Cenni preliminari sulle manipolazioni avanzate</span><span class="sxs-lookup"><span data-stu-id="5b0ea-123">Advanced Manipulations Overview</span></span>

<span data-ttu-id="5b0ea-124">In questa sezione vengono illustrate le modifiche avanzate per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-124">This section explains advanced manipulations for applications.</span></span>

<span data-ttu-id="5b0ea-125">Ai fini dell'usabilità, potrebbe essere necessario aggiungere modifiche complesse all'applicazione in modo che gli oggetti possano essere manipolati con un grado di granularità preciso.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-125">For usability purposes, you may want to add complex manipulations to your application so that objects can be manipulated with a fine degree of granularity.</span></span> <span data-ttu-id="5b0ea-126">Nelle sezioni seguenti vengono descritte le manipolazioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-126">The following sections describe advanced manipulations.</span></span>

### <a name="advanced-expansion"></a><span data-ttu-id="5b0ea-127">Espansione avanzata</span><span class="sxs-lookup"><span data-stu-id="5b0ea-127">Advanced Expansion</span></span>

<span data-ttu-id="5b0ea-128">Nella figura seguente sono illustrate due interpretazioni dell'espansione.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-128">The following illustration shows two interpretations of expansion.</span></span>

![illustrazione che mostra un'espansione semplice intorno al punto centrale di un oggetto ed espansione avanzata intorno al punto centrale della manipolazione](images/expansion.png)

<span data-ttu-id="5b0ea-130">Nell'esempio A, l'esempio di espansione semplice, l'oggetto viene espanso intorno al punto centrale.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-130">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="5b0ea-131">Nell'esempio B l'oggetto viene espanso intorno al punto centrale della manipolazione.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-131">In example B, the object is expanded around the center point of the manipulation.</span></span>

### <a name="advanced-rotation"></a><span data-ttu-id="5b0ea-132">Rotazione avanzata</span><span class="sxs-lookup"><span data-stu-id="5b0ea-132">Advanced Rotation</span></span>

<span data-ttu-id="5b0ea-133">Nella figura seguente sono illustrate due interpretazioni della rotazione.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-133">The following illustration shows two interpretations of rotation.</span></span>

![illustrazione che mostra due tipi di rotazione a dito singolo: intorno al centro o intorno al bordo, con il bordo che interessa sia la rotazione che la traduzione](images/rotation.png)

<span data-ttu-id="5b0ea-135">Nell'esempio A, l'esempio di rotazione semplice, l'oggetto viene ruotato intorno al punto centrale.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-135">In example A, the simple rotation example, the object is rotated around its center point.</span></span> <span data-ttu-id="5b0ea-136">Nell'esempio B l'oggetto viene ruotato intorno al punto centrale della manipolazione.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-136">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="5b0ea-137">Per ulteriori informazioni sulla rotazione complessa, vedere la sezione [rotazione avanzata](advanced-rotation.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0ea-137">For more information on complex rotation, see the [Advanced Rotation](advanced-rotation.md) section.</span></span>

## <a name="advanced-translation"></a><span data-ttu-id="5b0ea-138">Traduzione avanzata</span><span class="sxs-lookup"><span data-stu-id="5b0ea-138">Advanced Translation</span></span>

<span data-ttu-id="5b0ea-139">Nella figura seguente sono illustrate due interpretazioni della traduzione.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-139">The following illustration shows two interpretations of translation.</span></span>

![illustrazione che mostra la traduzione semplice, in cui un oggetto viene spostato senza rotazione e la traduzione avanzata, che implica lo spostamento e la rotazione](images/translation.png)

<span data-ttu-id="5b0ea-141">Nell'esempio A, l'esempio di conversione semplice, l'oggetto viene spostato senza rotazione.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-141">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="5b0ea-142">Nell'esempio B l'oggetto viene ruotato durante la conversione a seconda della posizione in cui si trova il punto di contatto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-142">In example B, the object is rotated during the translation depending on where the object contact point is.</span></span> <span data-ttu-id="5b0ea-143">Se si Abilita la rotazione a dito singolo come descritto in [rotazione a dito singolo](single-finger-rotation.md), è possibile abilitare la traduzione complessa.</span><span class="sxs-lookup"><span data-stu-id="5b0ea-143">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b0ea-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b0ea-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b0ea-145">Modifiche</span><span class="sxs-lookup"><span data-stu-id="5b0ea-145">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




