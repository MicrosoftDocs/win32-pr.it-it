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
# <a name="advanced-expansion"></a>Espansione avanzata

Nella figura seguente vengono illustrati due modi in cui un oggetto può essere espanso.

![illustrazione che mostra un'espansione semplice intorno al punto centrale di un oggetto ed espansione avanzata intorno al punto centrale della manipolazione](images/expansion.png)

Nell'esempio A, l'esempio di espansione semplice, l'oggetto viene espanso intorno al punto centrale. Nell'esempio B l'oggetto viene espanso intorno al punto centrale della manipolazione. Per abilitare questa operazione, è necessario convertire l'oggetto mentre è in corso l'espansione. La quantità che verrà convertita dall'oggetto corrisponde alla distanza dal centro dell'oggetto al punto centrale del movimento. Intuitivamente, è come se l'oggetto venisse espanso dal punto centrale del movimento di espansione e quindi spostato in modo che sia sempre nello stesso centro della posizione iniziale. Il codice seguente illustra un modo in cui questo concetto può essere applicato per consentire l'espansione in un punto centrale.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche](getting-started-with-manipulations.md)
</dt> </dl>

 

 




