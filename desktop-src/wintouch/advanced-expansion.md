---
title: Espansione avanzata
description: Espansione avanzata
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Tocco, espansione
- Windows Tocco, espansione avanzata
- Windows Tocco, manipolazioni
- manipolazioni, espansione
- manipolazioni, espansione avanzata
- espansione, avanzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e176d91c08bd0d39383e2aba269bbdb5629cfe6b7c2d20eb1ac955786bef2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881501"
---
# <a name="advanced-expansion"></a>Espansione avanzata

La figura seguente illustra due modi in cui un oggetto può essere espanso.

![illustrazione che mostra una semplice espansione intorno al punto centrale di un oggetto e l'espansione avanzata intorno al punto centrale della manipolazione](images/expansion.png)

Nell'esempio A, il semplice esempio di espansione, l'oggetto viene espanso intorno al punto centrale. Nell'esempio B, l'oggetto viene espanso intorno al punto centrale della manipolazione. Per abilitare questa funzionalità, è necessario convertire l'oggetto durante l'espansione. La quantità di traslazione dell'oggetto è uguale alla distanza dal centro dell'oggetto al punto centrale del movimento. Intuitivamente, è come se si espandesse l'oggetto dal punto centrale del movimento di espansione e quindi lo si spostasse in modo che sia ancora nello stesso centro della posizione iniziale. Il codice seguente illustra un modo in cui questo concetto può essere applicato per abilitare l'espansione intorno a un punto centrale.


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

 

 




