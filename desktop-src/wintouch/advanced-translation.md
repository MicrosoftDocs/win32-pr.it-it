---
title: Traduzione avanzata
description: Traduzione avanzata
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Touch, traduzione
- Windows Touch, traduzione avanzata
- Windows Touch, modifiche
- manipolazioni, traduzione
- manipolazioni, traduzione avanzata
- conversione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855502"
---
# <a name="advanced-translation"></a><span data-ttu-id="66dfa-109">Traduzione avanzata</span><span class="sxs-lookup"><span data-stu-id="66dfa-109">Advanced Translation</span></span>

<span data-ttu-id="66dfa-110">Nella figura seguente sono illustrate due interpretazioni della traduzione.</span><span class="sxs-lookup"><span data-stu-id="66dfa-110">The following illustration shows two interpretations of translation.</span></span>

![illustrazione che mostra per prima cosa una semplice traduzione, in cui un oggetto viene spostato senza rotazione, quindi Mostra la traduzione avanzata, che implica lo spostamento con la rotazione](images/translation.png)

<span data-ttu-id="66dfa-112">Nell'esempio A, l'esempio di conversione semplice, l'oggetto viene spostato senza rotazione.</span><span class="sxs-lookup"><span data-stu-id="66dfa-112">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="66dfa-113">Nell'esempio B l'oggetto viene ruotato durante la conversione, a seconda del punto di contatto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66dfa-113">In example B, the object is rotated during the translation, depending on where the object contact point is.</span></span> <span data-ttu-id="66dfa-114">Se si Abilita la rotazione a dito singolo come descritto in [rotazione a dito singolo](single-finger-rotation.md), è possibile abilitare la traduzione complessa.</span><span class="sxs-lookup"><span data-stu-id="66dfa-114">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span> <span data-ttu-id="66dfa-115">Il diagramma seguente mostra i vari componenti della rotazione di un singolo dito durante l'esecuzione della conversione.</span><span class="sxs-lookup"><span data-stu-id="66dfa-115">The following diagram shows the various components of single-finger rotation when you are performing translation.</span></span>

![illustrazione che mostra i componenti della rotazione con un solo dito: pivotpointx, pivotpointy e pivotRadius](images/translation-complex-components.png)

<span data-ttu-id="66dfa-117">Quando l'oggetto viene spostato, il raggio viene ricalcolato e il punto di perno viene spostato.</span><span class="sxs-lookup"><span data-stu-id="66dfa-117">As the object is moved, the radius is recalculated and the pivot point is moved.</span></span>

<span data-ttu-id="66dfa-118">Il codice seguente illustra un modo in cui è possibile eseguire questa operazione in un'implementazione di [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) che consente una traduzione complessa.</span><span class="sxs-lookup"><span data-stu-id="66dfa-118">The following code shows one way that you can do this in an implementation of [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) that enables complex translation.</span></span>


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> <span data-ttu-id="66dfa-119">Le trasformazioni di oggetti vengono eseguite prima del calcolo dei punti pivot e del raggio.</span><span class="sxs-lookup"><span data-stu-id="66dfa-119">Object transformations occur before the pivot points and radius are calculated.</span></span> <span data-ttu-id="66dfa-120">In questo modo l'oggetto verrà spostato correttamente se l'utente esegue l'espansione dell'oggetto durante lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="66dfa-120">In this manner the object will move correctly if the user performs expansion on the object while it is moving.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="66dfa-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66dfa-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66dfa-122">Modifiche</span><span class="sxs-lookup"><span data-stu-id="66dfa-122">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




