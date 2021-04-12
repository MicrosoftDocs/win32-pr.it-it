---
title: Espansione avanzata
description: Espansione avanzata
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Touch, espansione
- Windows Touch, espansione avanzata
- Windows Touch, modifiche
- manipolazioni, espansione
- manipolazioni, espansione avanzata
- espansione, avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220996"
---
# <a name="advanced-expansion"></a><span data-ttu-id="df4b8-109">Espansione avanzata</span><span class="sxs-lookup"><span data-stu-id="df4b8-109">Advanced Expansion</span></span>

<span data-ttu-id="df4b8-110">Nella figura seguente vengono illustrati due modi in cui un oggetto può essere espanso.</span><span class="sxs-lookup"><span data-stu-id="df4b8-110">The following illustration shows two ways that an object can be expanded.</span></span>

![illustrazione che mostra un'espansione semplice intorno al punto centrale di un oggetto ed espansione avanzata intorno al punto centrale della manipolazione](images/expansion.png)

<span data-ttu-id="df4b8-112">Nell'esempio A, l'esempio di espansione semplice, l'oggetto viene espanso intorno al punto centrale.</span><span class="sxs-lookup"><span data-stu-id="df4b8-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="df4b8-113">Nell'esempio B l'oggetto viene espanso intorno al punto centrale della manipolazione.</span><span class="sxs-lookup"><span data-stu-id="df4b8-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="df4b8-114">Per abilitare questa operazione, è necessario convertire l'oggetto mentre è in corso l'espansione.</span><span class="sxs-lookup"><span data-stu-id="df4b8-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="df4b8-115">La quantità che verrà convertita dall'oggetto corrisponde alla distanza dal centro dell'oggetto al punto centrale del movimento.</span><span class="sxs-lookup"><span data-stu-id="df4b8-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="df4b8-116">Intuitivamente, è come se l'oggetto venisse espanso dal punto centrale del movimento di espansione e quindi spostato in modo che sia sempre nello stesso centro della posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="df4b8-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="df4b8-117">Il codice seguente illustra un modo in cui questo concetto può essere applicato per consentire l'espansione in un punto centrale.</span><span class="sxs-lookup"><span data-stu-id="df4b8-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="df4b8-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df4b8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df4b8-119">Modifiche</span><span class="sxs-lookup"><span data-stu-id="df4b8-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




