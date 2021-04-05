---
title: Rotazione avanzata
description: In questa sezione viene illustrato come ruotare un oggetto in base alla posizione in cui l'utente esegue la manipolazione della rotazione.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Touch, rotazione
- Windows Touch, rotazione avanzata
- Windows Touch, modifiche
- manipolazioni, rotazione
- manipolazioni, rotazione avanzata
- rotazione, avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955187"
---
# <a name="advanced-rotation"></a><span data-ttu-id="cc312-109">Rotazione avanzata</span><span class="sxs-lookup"><span data-stu-id="cc312-109">Advanced Rotation</span></span>

<span data-ttu-id="cc312-110">In questa sezione viene illustrato come ruotare un oggetto in base alla posizione in cui l'utente esegue la manipolazione della rotazione.</span><span class="sxs-lookup"><span data-stu-id="cc312-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="cc312-111">Nell'immagine seguente vengono illustrati due diversi modi in cui un oggetto può essere ruotato.</span><span class="sxs-lookup"><span data-stu-id="cc312-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![illustrazione che mostra due tipi di rotazione a dito singolo: intorno al centro o intorno al bordo, con il bordo che interessa sia la rotazione che la traduzione](images/rotation.png)

<span data-ttu-id="cc312-113">Nell'esempio A, l'oggetto viene modificato intorno al punto centrale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc312-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="cc312-114">Nell'esempio B l'oggetto viene ruotato intorno al punto centrale della manipolazione.</span><span class="sxs-lookup"><span data-stu-id="cc312-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="cc312-115">Per supportare la manipolazione in un punto diverso dal punto centrale dell'oggetto, è necessario eseguire una manipolazione composta che esegue sia la rotazione che la traslazione.</span><span class="sxs-lookup"><span data-stu-id="cc312-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="cc312-116">Il codice seguente illustra il modo in cui questa manipolazione viene eseguita e calcolata.</span><span class="sxs-lookup"><span data-stu-id="cc312-116">The following code shows how this manipulation is performed and calculated.</span></span>


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a><span data-ttu-id="cc312-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc312-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc312-118">Manipolazioni avanzate</span><span class="sxs-lookup"><span data-stu-id="cc312-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="cc312-119">Modifiche</span><span class="sxs-lookup"><span data-stu-id="cc312-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




