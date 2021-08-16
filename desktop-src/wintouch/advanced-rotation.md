---
title: Rotazione avanzata
description: Questa sezione illustra come ruotare un oggetto in base alla posizione in cui l'utente sta eseguendo la manipolazione della rotazione.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Tocco, rotazione
- Windows Tocco, rotazione avanzata
- Windows Tocco, manipolazioni
- manipolazioni, rotazione
- manipolazioni, rotazione avanzata
- rotazione, avanzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dda17ae8076061f7b5b7b935afb2b7f8e5fb10cb270280f7edbb8c23aa896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199517"
---
# <a name="advanced-rotation"></a>Rotazione avanzata

Questa sezione illustra come ruotare un oggetto in base alla posizione in cui l'utente sta eseguendo la manipolazione della rotazione.

L'immagine seguente illustra due diversi modi in cui un oggetto può essere ruotato.

![Figura che mostra due tipi di rotazione con un dito singolo: intorno al centro o intorno al bordo, con il bordo che coinvolge sia la rotazione che la traslazione](images/rotation.png)

Nell'esempio A, l'oggetto viene modificato intorno al punto centrale dell'oggetto. Nell'esempio B, l'oggetto viene ruotato intorno al punto centrale della manipolazione. Per supportare la manipolazione intorno a un punto diverso dal punto centrale dell'oggetto, è necessario eseguire una manipolazione composta che esegua sia la rotazione che la traslazione. Il codice seguente illustra come viene eseguita e calcolata questa manipolazione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche avanzate](advanced-manipulations.md)
</dt> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> </dl>

 

 




