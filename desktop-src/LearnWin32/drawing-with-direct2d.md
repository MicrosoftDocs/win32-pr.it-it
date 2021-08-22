---
title: Disegno con Direct2D
description: Dopo aver creato le risorse grafiche, si è pronti per disegnare.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d8a346300b32fe1c716e51efe6bfb8fdbf6220fb2ff17df6de617de27ba1a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535077"
---
# <a name="drawing-with-direct2d"></a>Disegno con Direct2D

Dopo aver creato le risorse grafiche, si è pronti per disegnare.

## <a name="drawing-an-ellipse"></a>Disegno di un'ellisse

Il [programma Circle](your-first-direct2d-program.md) esegue una logica di disegno molto semplice:

1.  Riempire lo sfondo con un colore a tinta unita.
2.  Disegnare un cerchio pieno.

![screenshot del programma circle.](images/graphics08.png)

Poiché la destinazione di rendering è una finestra (anziché una bitmap o un'altra superficie fuori schermo), il disegno viene eseguito in risposta ai [**messaggi WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Il codice seguente illustra la procedura della finestra per il programma Circle.


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



[**L'interfaccia ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) viene usata per tutte le operazioni di disegno. Il metodo del `OnPaint` programma esegue le operazioni seguenti:

1.  Il [**metodo ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) segnala l'inizio del disegno.
2.  Il [**metodo ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) riempie l'intera destinazione di rendering con un colore a tinta unita. Il colore viene specificato come [**struttura COLOR \_ \_ F D2D1.**](/windows/desktop/Direct2D/d2d1-color-f) È possibile usare la [**classe D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) per inizializzare la struttura. Per altre informazioni, vedere [Uso del colore in Direct2D.](using-color-in-direct2d.md)
3.  Il [**metodo ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) disegna un'ellisse riempita usando il pennello specificato per il riempimento. Un'ellisse viene specificata da un punto centrale e dai raggi x e y. Se i raggi x e y sono uguali, il risultato è un cerchio.
4.  Il [**metodo ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) segnala il completamento del disegno per questo frame. Tutte le operazioni di disegno devono essere inserite tra le chiamate a [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ed **EndDraw.**

I [**metodi BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)e [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) hanno tutti un **tipo restituito void.** Se si verifica un errore durante l'esecuzione di uno di questi metodi, l'errore viene segnalato tramite il valore restituito del [**metodo EndDraw.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Il `CreateGraphicsResources` metodo è illustrato nell'argomento Creazione di risorse [Direct2D](render-targets--devices--and-resources.md). Questo metodo crea la destinazione di rendering e il pennello a tinta unita.

Il dispositivo potrebbe bufferare i comandi di disegno e rinviare l'esecuzione fino a [**quando non viene chiamato EndDraw.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) È possibile forzare il dispositivo a eseguire tutti i comandi di disegno in sospeso chiamando [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). Lo scaricamento può tuttavia ridurre le prestazioni.

## <a name="handling-device-loss"></a>Gestione della perdita di dispositivi

Mentre il programma è in esecuzione, il dispositivo grafico in uso potrebbe diventare non disponibile. Ad esempio, il dispositivo può essere perso se la risoluzione dello schermo cambia o se l'utente rimuove la scheda di visualizzazione. Se il dispositivo viene perso, anche la destinazione di rendering diventa non valida, insieme alle risorse dipendenti dal dispositivo associate al dispositivo. Direct2D segnala un dispositivo perso restituisce il codice di errore **D2DERR \_ RECREATE \_ TARGET** dal [**metodo EndDraw.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Se si riceve questo codice di errore, è necessario creare nuovamente la destinazione di rendering e tutte le risorse dipendenti dal dispositivo.

Per rimuovere una risorsa, è sufficiente rilasciare l'interfaccia per tale risorsa.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



La creazione di una risorsa può essere un'operazione costosa, quindi non ricreare le risorse per ogni [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Creare una risorsa una sola volta e memorizzare nella cache il puntatore della risorsa fino a quando la risorsa non diventa non valida a causa della perdita del dispositivo o fino a quando non è più necessaria tale risorsa.

## <a name="the-direct2d-render-loop"></a>Ciclo di rendering Direct2D

Indipendentemente da ciò che si disegna, il programma deve eseguire un ciclo simile al seguente.

1.  Creare risorse indipendenti dal dispositivo.
2.  Eseguire il rendering della scena.
    1.  Controllare se esiste una destinazione di rendering valida. In caso contrario, creare la destinazione di rendering e le risorse dipendenti dal dispositivo.
    2.  Chiamare [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Eseguire comandi di disegno.
    4.  Chiamare [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Se [**EndDraw restituisce**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) **D2DERR \_ RECREATE \_ TARGET,** rimuovere la destinazione di rendering e le risorse dipendenti dal dispositivo.
3.  Ripetere il passaggio 2 ogni volta che è necessario aggiornare o ridisegnare la scena.

Se la destinazione di rendering è una finestra, il passaggio 2 si verifica ogni volta che la finestra riceve un [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)

Il ciclo illustrato in questo articolo gestisce la perdita di dispositivi rimuovendo le risorse dipendenti dal dispositivo e creandole di nuovo all'inizio del ciclo successivo (passaggio 2a).

## <a name="next"></a>Prossima

[DPI e Device-Independent pixel](dpi-and-device-independent-pixels.md)

 

 