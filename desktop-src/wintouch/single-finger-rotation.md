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
# <a name="single-finger-rotation"></a>Rotazione Single-Finger

In questa sezione viene illustrato come ruotare un oggetto utilizzando un punto pivot.

Nell'immagine seguente viene illustrata la rotazione di un singolo dito.

![illustrazione che mostra due tipi di rotazione a dito singolo: intorno al centro o intorno al bordo](images/sfrotation.png)

Nell'esempio A, l'oggetto viene ruotato intorno al punto centrale dell'oggetto utilizzando il movimento di rotazione. Nell'esempio B l'oggetto viene ruotato spostando un singolo dito intorno al bordo dell'oggetto. Il processore di manipolazione Abilita questa rotazione usando i valori del punto pivot e del raggio pivot. Nell'immagine seguente vengono illustrati i componenti della rotazione di un singolo dito.

![illustrazione che mostra i componenti della rotazione con un solo dito: pivotpointx, pivotpointy e pivotRadius](images/sfrotation-components.png)

Dopo aver impostato i valori [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)e [**pivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , i messaggi di traduzione successivi includeranno la rotazione. Maggiore è il raggio perno, maggiore è la modifica in x e y deve essere per ruotare l'oggetto. Nel codice seguente viene illustrato come impostare questi valori nel processore di manipolazione.


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



Nell'esempio precedente, la distanza al bordo dell'oggetto, ridimensionato al 40%, viene utilizzata come raggio pivot. Poiché le dimensioni dell'oggetto vengono prese in considerazione, questo calcolo è valido per ogni Delta di oggetti. Quando l'oggetto viene ridimensionato, il raggio pivot aumenta. Questo valore e i valori x e y del centro dell'oggetto vengono passati al processore di manipolazione per ruotare l'oggetto intorno al punto di perno.

> [!Note]  
> Il valore [**pivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) non deve essere mai compreso tra 0,0 e 1,0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> <dt>

[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




