---
title: Metodo InkDraw
description: CGuiPaper mantiene anche un flag m \_ bInking. InkStart imposta su TRUE per segnalare che è in corso una sequenza di disegno. Ad esempio, il metodo InkDraw usa questo flag per determinare se deve disegnare e salvare i dati dell'input penna.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e146093d23fd16d122da1ea81d1c99bdf06ed926d5cb4dba2f1d77b747b2058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662761"
---
# <a name="inkdraw-method"></a>Metodo InkDraw

CGuiPaper mantiene anche un flag m \_ bInking. [InkStart](inkstart-method.md) imposta su **TRUE** per segnalare che è in corso una sequenza di disegno. Ad esempio, il metodo InkDraw usa questo flag per determinare se deve disegnare e salvare i dati dell'input penna.

Di seguito è riportato il metodo InkDraw di GUIPAPER. CPP.


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



Questo metodo non esegue alcuna operazione se m \_ bInking è **FALSE.** Questa è la condizione quando l'utente sposta semplicemente il mouse sulla finestra client senza premere il pulsante sinistro del mouse.

InkDraw ha chiaramente una doppia responsabilità. Le chiamate Win32 MoveToEx e LineTo vengono effettuate per disegnare immagini linea sullo schermo dell'interfaccia utente grafica (usando l'handle del contesto di dispositivo mantenuto in m \_ hDC). I dati dell'input penna vengono passati anche all'oggetto COPaper per la registrazione usando il metodo InkDraw dell'interfaccia [IPaper.](ipaper-methods.md) Quando m \_ bInkSaving **è FALSE,** InkDraw disegna l'immagine della linea ma non archivia i dati in COPaper. Questa condizione viene usata durante il ridisegno.

 

 




