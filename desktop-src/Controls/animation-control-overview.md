---
title: Informazioni sui controlli di animazione
description: Un controllo di animazione è una finestra che visualizza un Audio-Video clip con interfoliazione (AVI). Un clip AVI è costituito da una serie di frame bitmap come un film. I controlli di animazione possono visualizzare solo le clip AVI che non contengono audio.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625828e5f4febce7314da365c9db93ce3a07136
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300541"
---
# <a name="about-animation-controls"></a>Informazioni sui controlli di animazione

Un *controllo di animazione* è una finestra che visualizza un Audio-Video clip con INTERFOLIAZIONE (AVI). Un clip AVI è costituito da una serie di frame bitmap come un film. I controlli di animazione possono visualizzare solo le clip AVI che non contengono audio.

Un controllo di animazione viene comunemente usato per indicare l'attività di sistema durante un'operazione di lunga durata. Questo è possibile perché il thread dell'operazione continua l'esecuzione durante la visualizzazione del clip AVI. La finestra di dialogo trova di Esplora risorse, ad esempio, consente di visualizzare una lente di ingrandimento quando il sistema cerca un file.

> [!Note]  
> Se si usa ComCtl32.dll versione 6, il thread non è supportato. Assicurarsi che l'applicazione non blocchi l'interfaccia utente. in caso contrario, l'animazione non viene eseguita.

 

Un controllo animazione può visualizzare un clip AVI originato da un file AVI non compresso o da un file AVI compresso usando la codifica di Run-Length (BI \_ RLE8). È possibile aggiungere il clip AVI all'applicazione come risorsa AVI oppure il clip può accompagnare l'applicazione come file AVI separato.

> [!Note]  
> Il file AVI o la risorsa non deve avere un canale audio. Le funzionalità del controllo animazione sono molto limitate e sono soggette a modifiche. Se è necessario un controllo per fornire funzionalità di riproduzione e registrazione multimediali per l'applicazione, è possibile usare il controllo MCIWnd. Per altre informazioni, vedere [classe della finestra MCIWnd](/windows/desktop/Multimedia/mciwnd-window-class).

 

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Creazione del controllo animazione](#animation-control-creation)
-   [Informazioni sui messaggi di controllo animazione](#about-animation-control-messages)
-   [Elaborazione del messaggio predefinita](#default-message-processing)

## <a name="animation-control-creation"></a>Creazione del controllo animazione

Un controllo di animazione appartiene alla classe della finestra della [**\_ classe animata**](common-control-window-classes.md) . Per creare un controllo di animazione, usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la macro [**\_ create animate**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) . La macro posiziona il controllo dell'animazione nell'angolo superiore sinistro della finestra padre e, se non si specifica lo stile del [**\_ centro ACS**](animation-control-styles.md) , imposta la larghezza e l'altezza del controllo in base alle dimensioni di un frame nel clip AVI. Se viene specificato il **\_ centro ACS** , **animate \_ create** imposta la larghezza e l'altezza del controllo su zero. È possibile utilizzare la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare la posizione e le dimensioni del controllo.

Se si crea un controllo animazione in una finestra di dialogo o in una risorsa della finestra di dialogo, il controllo viene eliminato automaticamente quando l'utente chiude la finestra di dialogo. Se si crea un controllo animazione in una finestra, è necessario eliminare in modo esplicito il controllo.

## <a name="about-animation-control-messages"></a>Informazioni sui messaggi di controllo animazione

Un'applicazione invia messaggi a un controllo animazione per aprire, riprodurre, arrestare e chiudere il clip AVI corrispondente. Ogni messaggio ha una o più macro che è possibile usare anziché inviare il messaggio in modo esplicito.

Dopo aver creato un controllo di animazione, un'applicazione invia il messaggio di [**\_ apertura di ACM**](acm-open.md) per aprire una clip AVI e caricarla in memoria. Il messaggio specifica il percorso di un file AVI o il nome di una risorsa AVI. Il sistema carica la risorsa AVI dal modulo che ha creato il controllo dell'animazione.

Se il controllo dell'animazione dispone dello stile di [**\_ riproduzione automatica ACS**](animation-control-styles.md) , il controllo inizia a riprodurre il clip AVI immediatamente dopo l'apertura del file AVI o della risorsa AVI. In caso contrario, un'applicazione può usare il messaggio [**ACM \_ Play**](acm-play.md) per avviare il clip AVI. Un'applicazione può arrestare il clip in qualsiasi momento inviando il messaggio di [**\_ arresto di ACM**](acm-stop.md) . L'ultimo frame riprodotto rimane visualizzato quando il controllo termina la riproduzione del clip AVI o quando viene inviato il punto di **\_ arresto di ACM** .

Un controllo animazione può inviare due codici di notifica alla relativa finestra padre: [ACN \_ Start](acn-start.md) e [ACN \_ Stop](acn-stop.md). La maggior parte delle applicazioni non gestisce alcuna notifica.

Per chiudere il file AVI o la risorsa AVI e rimuoverlo dalla memoria, un'applicazione può usare la macro di [**animazione \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) , che invia ad [**ACM \_ Open**](acm-open.md) con il nome file o il nome della risorsa impostato su **null**.

## <a name="default-message-processing"></a>Elaborazione del messaggio predefinita

In questa sezione vengono descritti i messaggi della finestra gestiti dalla routine della finestra per la classe della finestra [**anima \_ classe**](common-control-window-classes.md) .



| Message                                    | Elaborazione eseguita                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_chiusura WM**](/windows/desktop/winmsg/wm-close)           | Libera il file AVI o la risorsa AVI associata al controllo dell'animazione.                                                                                                                                                                                                                   |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)       | Libera il file AVI o la risorsa AVI, libera una struttura di dati interna, quindi chiama la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                                                                                                                                                |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd) | Cancella lo sfondo della finestra usando il colore di sfondo corrente per i controlli statici.                                                                                                                                                                                                        |
| [**\_NCCREATE WM**](/windows/desktop/winmsg/wm-nccreate)     | Alloca e Inizializza una struttura di dati interna, quindi chiama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).                                                                                                                                                                              |
| [**\_NCHITTEST WM**](/windows/desktop/inputdev/wm-nchittest) | Restituisce il valore dell'hit test di HTTRANSPARENT.                                                                                                                                                                                                                                                   |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)              | Disegna un frame AVI nel controllo dell'animazione.                                                                                                                                                                                                                                                |
| [**\_dimensioni WM**](/windows/desktop/winmsg/wm-size)             | Verifica se il controllo ha lo stile del [**\_ centro ACS**](animation-control-styles.md) . Se il controllo non lo è, viene chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). In caso contrario, centra l'animazione nel controllo, invalida il controllo e quindi chiama **DefWindowProc**. |



 

 

 