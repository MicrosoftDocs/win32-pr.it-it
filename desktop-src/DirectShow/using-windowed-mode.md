---
description: Uso della modalità finestra
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Uso della modalità finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314380"
---
# <a name="using-windowed-mode"></a>Uso della modalità finestra

> [!Note]  
> Il [filtro renderer video](video-renderer-filter.md) legacy usa sempre la modalità con finestra. Per impostazione predefinita, i filtri VMR-7 e VMR-9 utilizzano la modalità finestra, ma supportano anche la modalità senza finestra.

 

In modalità finestra, il renderer video crea la propria finestra in cui dipinge i fotogrammi video. Se non diversamente specificato, questa finestra è una finestra di primo livello con i bordi e la barra del titolo. Nella maggior parte dei casi, tuttavia, la finestra video verrà collegata a una finestra dell'applicazione, in modo che il video sia integrato nell'interfaccia utente dell'applicazione. La procedura da adottare è la seguente:

1.  Eseguire una query per **IVideoWindow**.
2.  Impostare la finestra padre.
3.  Imposta nuovi stili della finestra.
4.  Posizionare la finestra del video all'interno della finestra proprietaria.
5.  Invia una notifica alla finestra video dei \_ messaggi di spostamento WM.

**Query per IVideoWindow**

Prima di avviare la riproduzione, eseguire una query su Filter Graph Manager per l'interfaccia **IVideoWindow** :


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Impostare la finestra padre**

Per impostare la finestra padre, chiamare il metodo [**IVideoWindow::p UT \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un handle per la finestra dell'applicazione. Questo metodo accetta una variabile di tipo [**OAHWND**](oahwnd.md), quindi esegue il cast dell'handle a questo tipo:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Imposta nuovi stili della finestra**

Modificare lo stile della finestra video chiamando il metodo [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



Il \_ flag WS Child imposta la finestra come finestra figlio e il \_ flag WS CLIPSIBLINGS impedisce che la finestra venga disegnata all'interno dell'area client di un'altra finestra figlio.

**Posizionare la finestra del video**

Per impostare la posizione del video rispetto all'area client della finestra dell'applicazione, chiamare il metodo [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) . Questo metodo accetta un rettangolo che specifica il bordo sinistro, il bordo superiore, lo spessore e l'altezza della finestra del video. Il codice seguente, ad esempio, estende la finestra video per adattarsi all'intera area client della finestra padre:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Per ottenere la dimensione nativa del video, chiamare il metodo [**IBasicVideo:: GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) sul gestore del grafico del filtro. Queste informazioni possono essere usate per ridimensionare il video e mantengono le proporzioni corrette.

**Rispondere ai \_ messaggi di spostamento WM**

Per ottenere prestazioni ottimali, è consigliabile inviare una notifica al renderer video ogni volta che la finestra si sposta mentre il grafico è sospeso. Chiamare il metodo [**IVideoWindow:: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) per inviare il \_ messaggio di spostamento WM:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Se il renderer utilizza una sovrapposizione hardware, questa notifica determina l'aggiornamento della posizione della sovrapposizione da parte del renderer. (VMR-9 non usa le sovrapposizioni, pertanto non è necessario chiamare questo metodo se si usa VMR-9).

**Pulisci**

Prima della chiusura dell'applicazione, arrestare il grafo e reimpostare il proprietario della finestra video su **null**. In caso contrario, i messaggi della finestra potrebbero essere inviati alla finestra sbagliata, che probabilmente causa errori. Inoltre, nascondere la finestra video, altrimenti è possibile che lo sfarfallio di un'immagine video venga visualizzato momentaneamente:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Se l'elemento padre della finestra del video è un elemento figlio della finestra principale dell'applicazione (in altre parole, se la finestra del video è figlio di un figlio), è necessario creare la finestra video usando **CoCreateInstance** e aggiungerla al grafo, anziché consentire a Filter Graph Manager di aggiungere il renderer video durante la [connessione intelligente](intelligent-connect.md). In questo modo si garantisce che la finestra video e la finestra figlio vengano ridisegnate nello stesso momento. In caso contrario, la finestra figlio può essere disegnata sulla finestra del video.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering video](video-rendering.md)
</dt> </dl>

 

 



