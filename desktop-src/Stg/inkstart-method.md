---
title: Metodo InkStart
description: I metodi InkStart, InkDraw e InkStop usano tutti costrutti GUI Win32, ad esempio contesti di dispositivo e oggetti penna.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955707"
---
# <a name="inkstart-method"></a>Metodo InkStart

I metodi **InkStart**, [**InkDraw**](inkdraw-method.md)e [**INKSTOP**](cguipaper-methods.md) usano tutti costrutti GUI Win32, ad esempio contesti di dispositivo e oggetti penna. Viene illustrato il motivo per cui CGuiPaper è necessario come livello separato di incapsulamento. Gli aspetti dell'interfaccia utente grafica del paper di disegno vengono gestiti in CGuiPaper. L'oggetto Copaper viene inviato solo ai dati di input penna.

Un altro motivo di progettazione per il livello di incapsulamento CGuiPaper è la doppia natura dei metodi **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) . Non solo la chiamata a un documento per registrare i dati di input penna come si verificano, disegnano anche un'immagine visiva del disegno quando si verifica. CGuiPaper mantiene un \_ flag m bInkSaving per gestire questa duplice natura. Quando m \_ bInkSaving è false, l'immagine viene disegnata sullo schermo, ma i dati non vengono inviati al documento per la registrazione.

Questo schema viene utilizzato per il ridisegno quando l'utente non sta muovendo il mouse ma i dati di input penna del documento vengono inviati a CGuiPaper per il ridisegno automatico. CGuiPaper può essere indicato per impostare il flag m bInkSaving chiamando il \_ relativo metodo [**InkSaving**](cguipaper-methods.md) .

I frammenti di codice di esempio seguenti illustrano i metodi **InkStart** di GUIPAPER. CPP E SINK. CPP.

## <a name="inkstart-method-guipapercpp"></a>Metodo InkStart (GUIPAPER. CPP


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a>Metodo InkStart (SINK. CPP

**StoClien** riceve i dati di disegno sotto forma di chiamate all'interfaccia **IPaperSink** connessa nell'oggetto COPaperSink. Questi metodi corrispondono ai metodi **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) simili in CGuiPaper.


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



Quando **InkStart** viene chiamato nel sink, chiama CGuiPaper per disattivare il salvataggio dell'input penna in un documento. Non è necessario che il documento riceva una copia con echi dei dati inviati. Quando [**InkDraw**](inkdraw-method.md) viene chiamato nel sink, passa semplicemente la chiamata a **CGuiPaper:: InkDraw**. Quando [**InkStop**](cguipaper-methods.md) viene chiamato nel sink, viene chiamato CGuiPaper per riattivare l'input penna. Il risultato è la riproduzione dei dati dell'input penna di un documento in CGuiPaper solo per la visualizzazione.

È possibile testare il comportamento di **StoClien** quando il relativo **IPaperSink** è disconnesso scegliendo l'opzione Disconnetti dal menu sink. Come esperimento, dopo la disconnessione del sink scegliere About dal menu?. Verrà visualizzata la finestra di dialogo informazioni su, che coprirà parte del disegno di **StoClien**. Fare clic su OK nella finestra di dialogo informazioni su. Si noti che la parte del disegno che è stata analizzata è ora finita. I dati di disegno non vengono persi, ma parte dell'immagine è. Il client ha ricevuto il \_ messaggio di disegno WM ed ha emesso il metodo [**iPaper:: redisegna**](ipaper--redraw.md) . Tuttavia, poiché il sink non era connesso, non ha ricevuto le chiamate **IPaperSink** per ridisegnare il disegno.

È anche possibile testare questo comportamento riducendo al minimo **StoClien** e quindi ripristinarlo. In questo caso, l'intera immagine del disegno viene persa e deve essere ridisegnata. Per ridisegnare l'immagine del disegno dopo uno di questi test, utilizzare il menu sink per riconnettersi, quindi scegliere [**ridisegna**](ipaper--redraw.md) dal menu Disegna.

 

 




