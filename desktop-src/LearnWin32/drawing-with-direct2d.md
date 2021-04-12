---
title: Disegno con Direct2D
description: Dopo aver creato le risorse grafiche, si è pronti per il progetto.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472899"
---
# <a name="drawing-with-direct2d"></a>Disegno con Direct2D

Dopo aver creato le risorse grafiche, si è pronti per il progetto.

## <a name="drawing-an-ellipse"></a>Disegno di un'ellisse

Il programma [Circle](your-first-direct2d-program.md) esegue una logica di disegno molto semplice:

1.  Riempire lo sfondo con un colore a tinta unita.
2.  Viene disegnato un cerchio pieno.

![screenshot del programma Circle.](images/graphics08.png)

Poiché la destinazione di rendering è una finestra (in contrapposizione a una bitmap o ad altra superficie Offscreen), il disegno viene eseguito in risposta ai messaggi di disegno [**WM \_**](/windows/desktop/gdi/wm-paint) . Il codice seguente illustra la procedura della finestra per il programma Circle.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

Ecco il codice che disegna il cerchio.

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



L'interfaccia [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) viene utilizzata per tutte le operazioni di disegno. Il metodo del programma `OnPaint` esegue le operazioni seguenti:

1.  Il metodo [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) segnala l'inizio del disegno.
2.  Il metodo [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) riempie l'intera destinazione di rendering con un colore a tinta unita. Il colore viene specificato come una struttura [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) . È possibile usare la classe [**D2D1:: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) per inizializzare la struttura. Per ulteriori informazioni, vedere [utilizzo del colore in Direct2D](using-color-in-direct2d.md).
3.  Il metodo [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) disegna un'ellisse piena, usando il pennello specificato per il riempimento. Un'ellisse è specificata da un punto centrale e dai raggi x e y. Se i raggi x e y sono uguali, il risultato è un cerchio.
4.  Il metodo [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) segnala il completamento del disegno per questo frame. Tutte le operazioni di disegno devono essere inserite tra le chiamate a [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw**.

I metodi [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)e [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) hanno tutti un tipo restituito **void** . Se si verifica un errore durante l'esecuzione di uno di questi metodi, l'errore viene segnalato tramite il valore restituito del metodo [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Il `CreateGraphicsResources` metodo viene illustrato nell'argomento [creazione di risorse Direct2D](render-targets--devices--and-resources.md). Questo metodo crea la destinazione di rendering e il pennello a tinta unita.

Il dispositivo potrebbe memorizzare nel buffer i comandi di disegno e rinviarne l'esecuzione fino a quando non viene chiamato [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . È possibile forzare il dispositivo a eseguire tutti i comandi di disegno in sospeso chiamando [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). Lo scaricamento può tuttavia ridurre le prestazioni.

## <a name="handling-device-loss"></a>Gestione della perdita di dispositivi

Mentre il programma è in esecuzione, il dispositivo grafico in uso potrebbe non essere più disponibile. Ad esempio, il dispositivo può andare perduto se viene modificata la risoluzione dello schermo o se l'utente rimuove la scheda di visualizzazione. Se il dispositivo viene perso, anche la destinazione di rendering diventa non valida, insieme alle risorse dipendenti dal dispositivo associate al dispositivo. Direct2D segnala un dispositivo perso restituendo il codice di errore **D2DERR \_ ricrea \_ destinazione** dal metodo [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Se viene visualizzato questo codice di errore, è necessario ricreare la destinazione di rendering e tutte le risorse dipendenti dal dispositivo.

Per eliminare una risorsa, è sufficiente rilasciare l'interfaccia per tale risorsa.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



La creazione di una risorsa può essere un'operazione costosa, quindi non ricreare le risorse per ogni messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . Creare una risorsa una sola volta e memorizzare nella cache il puntatore alla risorsa fino a quando la risorsa non diventa non valida a causa della perdita del dispositivo o fino a quando la risorsa non è più necessaria.

## <a name="the-direct2d-render-loop"></a>Ciclo di rendering Direct2D

Indipendentemente da quanto disegnato, il programma deve eseguire un ciclo simile a quello riportato di seguito.

1.  Creare risorse indipendenti dal dispositivo.
2.  Esegue il rendering della scena.
    1.  Controllare se esiste una destinazione di rendering valida. In caso contrario, creare la destinazione di rendering e le risorse dipendenti dal dispositivo.
    2.  Chiamare [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Eseguire i comandi di disegno.
    4.  Chiamare [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Se [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) restituisce **la \_ \_ destinazione D2DERR ricreate**, eliminare la destinazione di rendering e le risorse dipendenti dal dispositivo.
3.  Ripetere il passaggio 2 ogni volta che è necessario aggiornare o ricreare la scena.

Se la destinazione di rendering è una finestra, il passaggio 2 si verifica ogni volta che la finestra riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .

Il ciclo riportato di seguito gestisce la perdita del dispositivo ignorando le risorse dipendenti dal dispositivo e creando di nuovo tali risorse all'inizio del ciclo successivo (passaggio 2a).

## <a name="next"></a>Prossima

[DPI e Device-Independent pixel](dpi-and-device-independent-pixels.md)

 

 