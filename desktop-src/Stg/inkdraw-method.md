---
title: Metodo InkDraw
description: CGuiPaper mantiene anche un \_ flag m bInking. InkStart lo imposta su TRUE per segnalare che una sequenza di disegno è in corso. Ad esempio, il metodo InkDraw usa questo flag per determinare se deve disegnare e salvare i dati di input penna.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396535"
---
# <a name="inkdraw-method"></a>Metodo InkDraw

CGuiPaper mantiene anche un \_ flag m bInking. [InkStart](inkstart-method.md) lo imposta su **true** per segnalare che una sequenza di disegno è in corso. Ad esempio, il metodo InkDraw usa questo flag per determinare se deve disegnare e salvare i dati di input penna.

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



Questo metodo non esegue alcuna operazione se m \_ bInking è **false**. Questa condizione si verifica quando l'utente passa semplicemente il puntatore del mouse sulla finestra del client senza premere il pulsante sinistro del mouse.

InkDraw ha chiaramente una duplice responsabilità. Le chiamate Win32 MoveToEx e LineTo vengono effettuate per creare immagini linea sulla schermata GUI (usando l'handle del contesto di dispositivo mantenuto in m \_ HDC). I dati Ink vengono anche passati all'oggetto Copaper per la registrazione tramite il metodo InkDraw dell'interfaccia [iPaper](ipaper-methods.md) . Quando m \_ bInkSaving è **false**, InkDraw disegna l'immagine della linea, ma non archivia i dati in un documento. Questa condizione viene utilizzata durante il ridisegno.

 

 




