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
# <a name="advanced-translation"></a>Traduzione avanzata

Nella figura seguente sono illustrate due interpretazioni della traduzione.

![illustrazione che mostra per prima cosa una semplice traduzione, in cui un oggetto viene spostato senza rotazione, quindi Mostra la traduzione avanzata, che implica lo spostamento con la rotazione](images/translation.png)

Nell'esempio A, l'esempio di conversione semplice, l'oggetto viene spostato senza rotazione. Nell'esempio B l'oggetto viene ruotato durante la conversione, a seconda del punto di contatto dell'oggetto. Se si Abilita la rotazione a dito singolo come descritto in [rotazione a dito singolo](single-finger-rotation.md), è possibile abilitare la traduzione complessa. Il diagramma seguente mostra i vari componenti della rotazione di un singolo dito durante l'esecuzione della conversione.

![illustrazione che mostra i componenti della rotazione con un solo dito: pivotpointx, pivotpointy e pivotRadius](images/translation-complex-components.png)

Quando l'oggetto viene spostato, il raggio viene ricalcolato e il punto di perno viene spostato.

Il codice seguente illustra un modo in cui è possibile eseguire questa operazione in un'implementazione di [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) che consente una traduzione complessa.


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
> Le trasformazioni di oggetti vengono eseguite prima del calcolo dei punti pivot e del raggio. In questo modo l'oggetto verrà spostato correttamente se l'utente esegue l'espansione dell'oggetto durante lo spostamento.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> </dl>

 

 




