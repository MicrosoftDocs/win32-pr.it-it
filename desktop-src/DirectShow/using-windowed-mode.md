---
description: Uso della modalità finestra
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Uso della modalità finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f71bfa58e46ade8c779e562278f908c8b8fd593989ed4007e6b98cb7916da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633091"
---
# <a name="using-windowed-mode"></a>Uso della modalità finestra

> [!Note]  
> Il filtro [del renderer video legacy](video-renderer-filter.md) usa sempre la modalità finestra. I filtri VMR-7 e VMR-9 usano la modalità finestra per impostazione predefinita, ma supportano anche la modalità senza finestra.

 

In modalità finestra, il renderer video crea la propria finestra in cui disegna i fotogrammi video. Se non diversamente specificato, questa finestra è una finestra di primo livello con bordi e barra del titolo propri. Nella maggior parte dei casi, tuttavia, la finestra video verrà collegata a una finestra dell'applicazione, in modo che il video sia integrato nell'interfaccia utente dell'applicazione. La procedura da adottare è la seguente:

1.  Eseguire una query **per IVideoWindow**.
2.  Impostare la finestra padre.
3.  Impostare nuovi stili di finestra.
4.  Posizionare la finestra video all'interno della finestra proprietaria.
5.  Notificare alla finestra video i messaggi WM \_ MOVE.

**Query per IVideoWindow**

Prima di avviare la riproduzione, eseguire una query su Filter Graph Manager per **l'interfaccia IVideoWindow:**


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Impostare la finestra padre**

Per impostare la finestra padre, chiamare il metodo [**IVideoWindow::p ut \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un handle per la finestra dell'applicazione. Questo metodo accetta una variabile di tipo [**OAHWND,**](oahwnd.md)quindi eseguire il cast dell'handle a questo tipo:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Impostare nuovi stili di finestra**

Modificare lo stile della finestra video chiamando il [**metodo IVideoWindow::p ut \_ WindowStyle:**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle)


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



Il flag WS CHILD imposta la finestra come finestra figlio e il \_ flag WS CLIPSIBLINGS impedisce alla finestra di disegnare all'interno dell'area client di \_ un'altra finestra figlio.

**Posizionare la finestra video**

Per impostare la posizione del video rispetto all'area client della finestra dell'applicazione, chiamare il [**metodo IVideoWindow::SetWindowPosition.**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) Questo metodo accetta un rettangolo che specifica il bordo sinistro, il bordo superiore, la larghezza e l'altezza della finestra video. Ad esempio, il codice seguente estende la finestra video per adattarla all'intera area client della finestra padre:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Per ottenere le dimensioni native del video, chiamare il metodo [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) nell'Graph Filtro. È possibile usare queste informazioni per ridimensionare il video e mantenere le proporzioni corrette.

**Rispondere ai messaggi MOVE WM \_**

Per ottenere prestazioni ottimali, è consigliabile inviare una notifica al renderer video ogni volta che la finestra si sposta mentre il grafico è in pausa. Chiamare il [**metodo IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) per inoltrare il messaggio MOVE \_ WM:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Se il renderer usa una sovrimpressione hardware, questa notifica fa sì che il renderer aggiornerà la posizione della sovrimpressione. VmR-9 non usa sovrimpressione, quindi non è necessario chiamare questo metodo se si usa VMR-9.

**Eseguire la pulizia**

Prima della chiusura dell'applicazione, arrestare il grafico e reimpostare il proprietario della finestra video su **NULL.** In caso contrario, i messaggi della finestra potrebbero essere inviati alla finestra errata, che probabilmente causerà errori. È anche possibile nascondere la finestra video. In caso contrario, è possibile che sullo schermo venga visualizzato temporaneamente uno sfarfallio dell'immagine video:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Se l'elemento padre della finestra video è un elemento figlio della finestra principale dell'applicazione (in altre parole, se la finestra video è figlio di un elemento figlio), è necessario creare la finestra video usando **CoCreateInstance** e aggiungerla al grafo, anziché consentire a Filter Graph Manager di aggiungere il renderer video durante [l'esecuzione di Intelligent Connessione](intelligent-connect.md). Ciò garantisce che la finestra video e la finestra figlio siano ridisegnate contemporaneamente. In caso contrario, la finestra figlio potrebbe essere disegnata sulla finestra video.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video Rendering](video-rendering.md)
</dt> </dl>

 

 



