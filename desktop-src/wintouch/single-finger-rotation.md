---
title: Single-Finger rotazione
description: Questa sezione illustra come ruotare un oggetto usando un punto pivot.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Tocco, rotazione
- Windows Tocco, manipolazioni
- Windows Tocco, rotazione con un solo dito
- Windows Tocco, rotazione del punto pivot
- manipolazioni, rotazione
- rotazione, punti pivot
- rotazione, dito singolo
- movimenti, rotazione con un solo dito
- rotazione con un solo dito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110653"
---
# <a name="single-finger-rotation"></a>Single-Finger rotazione

Questa sezione illustra come ruotare un oggetto usando un punto pivot.

L'immagine seguente illustra la rotazione con un solo dito.

![Figura che mostra due tipi di rotazione con un dito singolo: intorno al centro o intorno al bordo](images/sfrotation.png)

Nell'esempio A, l'oggetto viene ruotato intorno al punto centrale dell'oggetto usando il movimento di rotazione. Nell'esempio B, l'oggetto viene ruotato spostando un singolo dito intorno al bordo dell'oggetto. Il processore di manipolazione abilita questa rotazione usando i valori del punto pivot e del raggio del pivot. L'immagine seguente illustra i componenti della rotazione con un solo dito.

![Illustrazione che mostra i componenti della rotazione con un dito singolo: pivotpointx, pivotpointy e pivotradius](images/sfrotation-components.png)

Dopo aver impostato i [**valori PivotPointX,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)e [**PivotRadius,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) i messaggi di traduzione successivi incorporano la rotazione. Maggiore è il raggio del pivot, maggiore sarà la modifica in x e y per ruotare l'oggetto. Il codice seguente illustra come impostare questi valori nel processore di manipolazione.


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



Nell'esempio precedente viene usata la distanza dal bordo dell'oggetto (ridimensionata al 40%) come raggio pivot. Poiché le dimensioni dell'oggetto vengono prese in considerazione, questo calcolo è valido per ogni delta dell'oggetto. Man mano che l'oggetto viene ridimensionato, il raggio del pivot aumenta. Questo valore e i valori x e y al centro dell'oggetto vengono passati al processore di manipolazione per ruotare l'oggetto intorno al punto pivot.

> [!Note]  
> Il [**valore di PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) non deve mai essere compreso tra 0,0 e 1,0.

 

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

 

 




