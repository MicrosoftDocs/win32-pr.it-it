---
title: Rotazione Single-Finger
description: In questa sezione viene illustrato come ruotare un oggetto utilizzando un punto pivot.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Touch, rotazione
- Windows Touch, modifiche
- Windows Touch, rotazione a dito singolo
- Windows Touch, rotazione del punto pivot
- manipolazioni, rotazione
- rotazione, punti pivot
- rotazione, a dito singolo
- movimenti, rotazione a dito singolo
- rotazione di un singolo dito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855738"
---
# <a name="single-finger-rotation"></a><span data-ttu-id="b5f09-112">Rotazione Single-Finger</span><span class="sxs-lookup"><span data-stu-id="b5f09-112">Single-Finger Rotation</span></span>

<span data-ttu-id="b5f09-113">In questa sezione viene illustrato come ruotare un oggetto utilizzando un punto pivot.</span><span class="sxs-lookup"><span data-stu-id="b5f09-113">This section explains how to rotate an object using a pivot point.</span></span>

<span data-ttu-id="b5f09-114">Nell'immagine seguente viene illustrata la rotazione di un singolo dito.</span><span class="sxs-lookup"><span data-stu-id="b5f09-114">The following image illustrates single-finger rotation.</span></span>

![illustrazione che mostra due tipi di rotazione a dito singolo: intorno al centro o intorno al bordo](images/sfrotation.png)

<span data-ttu-id="b5f09-116">Nell'esempio A, l'oggetto viene ruotato intorno al punto centrale dell'oggetto utilizzando il movimento di rotazione.</span><span class="sxs-lookup"><span data-stu-id="b5f09-116">In example A, the object is rotated around the center point of the object by using the rotation gesture.</span></span> <span data-ttu-id="b5f09-117">Nell'esempio B l'oggetto viene ruotato spostando un singolo dito intorno al bordo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b5f09-117">In example B, the object is rotated by moving a single finger around the edge of the object.</span></span> <span data-ttu-id="b5f09-118">Il processore di manipolazione Abilita questa rotazione usando i valori del punto pivot e del raggio pivot.</span><span class="sxs-lookup"><span data-stu-id="b5f09-118">The manipulation processor enables this rotation by using pivot point and pivot radius values.</span></span> <span data-ttu-id="b5f09-119">Nell'immagine seguente vengono illustrati i componenti della rotazione di un singolo dito.</span><span class="sxs-lookup"><span data-stu-id="b5f09-119">The following image illustrates the components of single-finger rotation.</span></span>

![illustrazione che mostra i componenti della rotazione con un solo dito: pivotpointx, pivotpointy e pivotRadius](images/sfrotation-components.png)

<span data-ttu-id="b5f09-121">Dopo aver impostato i valori [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)e [**pivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , i messaggi di traduzione successivi includeranno la rotazione.</span><span class="sxs-lookup"><span data-stu-id="b5f09-121">After you set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy), and [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) values, subsequent translation messages will incorporate rotation.</span></span> <span data-ttu-id="b5f09-122">Maggiore è il raggio perno, maggiore è la modifica in x e y deve essere per ruotare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b5f09-122">The larger the pivot radius, the greater the change in x and y must be to rotate the object.</span></span> <span data-ttu-id="b5f09-123">Nel codice seguente viene illustrato come impostare questi valori nel processore di manipolazione.</span><span class="sxs-lookup"><span data-stu-id="b5f09-123">The following code shows how these values could be set in the manipulation processor.</span></span>


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



<span data-ttu-id="b5f09-124">Nell'esempio precedente, la distanza al bordo dell'oggetto, ridimensionato al 40%, viene utilizzata come raggio pivot.</span><span class="sxs-lookup"><span data-stu-id="b5f09-124">In the previous example, the distance to the edge of the object (scaled to 40 percent) is used as the pivot radius.</span></span> <span data-ttu-id="b5f09-125">Poiché le dimensioni dell'oggetto vengono prese in considerazione, questo calcolo è valido per ogni Delta di oggetti.</span><span class="sxs-lookup"><span data-stu-id="b5f09-125">Because the object size is taken into consideration, this calculation is valid for every object delta.</span></span> <span data-ttu-id="b5f09-126">Quando l'oggetto viene ridimensionato, il raggio pivot aumenta.</span><span class="sxs-lookup"><span data-stu-id="b5f09-126">As the object scales, the pivot radius grows.</span></span> <span data-ttu-id="b5f09-127">Questo valore e i valori x e y del centro dell'oggetto vengono passati al processore di manipolazione per ruotare l'oggetto intorno al punto di perno.</span><span class="sxs-lookup"><span data-stu-id="b5f09-127">This value and the object's center x and y values are passed to the manipulation processor to rotate the object around the pivot point.</span></span>

> [!Note]  
> <span data-ttu-id="b5f09-128">Il valore [**pivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) non deve essere mai compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b5f09-128">The [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) value should never be between 0.0 and 1.0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5f09-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5f09-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f09-130">Modifiche</span><span class="sxs-lookup"><span data-stu-id="b5f09-130">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> <dt>

[<span data-ttu-id="b5f09-131">**PivotRadius**</span><span class="sxs-lookup"><span data-stu-id="b5f09-131">**PivotRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[<span data-ttu-id="b5f09-132">**PivotPointX**</span><span class="sxs-lookup"><span data-stu-id="b5f09-132">**PivotPointX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[<span data-ttu-id="b5f09-133">**PivotPointY**</span><span class="sxs-lookup"><span data-stu-id="b5f09-133">**PivotPointY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




