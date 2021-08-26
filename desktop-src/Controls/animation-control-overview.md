---
title: Informazioni sui controlli di animazione
description: Un controllo animazione è una finestra che visualizza Audio-Video clip AVI (Interleaved). Un clip AVI è una serie di fotogrammi bitmap come un film. I controlli di animazione possono visualizzare solo clip AVI che non contengono audio.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2a579334fe266499884ccf40ad1154b3465ffd301c92643f248ff2664ed4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921791"
---
# <a name="about-animation-controls"></a>Informazioni sui controlli di animazione

Un *controllo animazione* è una finestra che visualizza Audio-Video clip AVI (Interleaved). Un clip AVI è una serie di fotogrammi bitmap come un film. I controlli di animazione possono visualizzare solo clip AVI che non contengono audio.

Un uso comune per un controllo di animazione è quello di indicare l'attività del sistema durante un'operazione di lunga durata. Ciò è possibile perché il thread dell'operazione continua l'esecuzione mentre viene visualizzato il clip AVI. Ad esempio, nella finestra di dialogo Trova Windows Explorer viene visualizzata una lente di ingrandimento mobile mentre il sistema cerca un file.

> [!Note]  
> Se si usa la ComCtl32.dll versione 6, il thread non è supportato. Assicurarsi che l'applicazione non blocchi l'interfaccia utente, altrimenti l'animazione non verrà eseguita.

 

Un controllo animazione può visualizzare un clip AVI proveniente da un file AVI non compresso o da un file AVI compresso usando la codifica a lunghezza di esecuzione (BI \_ RLE8). È possibile aggiungere il clip AVI all'applicazione come risorsa AVI oppure il clip può accompagnare l'applicazione come file AVI separato.

> [!Note]  
> Il file AVI, o risorsa, non deve avere un canale audio. Le funzionalità del controllo animazione sono molto limitate e sono soggette a modifiche. Se è necessario un controllo per fornire funzionalità di riproduzione e registrazione multimediali per l'applicazione, è possibile usare il controllo MCIWnd. Per altre informazioni, vedere [McIWnd Window Class](/windows/desktop/Multimedia/mciwnd-window-class).

 

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Creazione del controllo Animation](#animation-control-creation)
-   [Informazioni sui messaggi di controllo animazione](#about-animation-control-messages)
-   [Elaborazione dei messaggi predefinita](#default-message-processing)

## <a name="animation-control-creation"></a>Creazione del controllo Animation

Un controllo di animazione appartiene alla [**classe di finestra ANIMATE \_ CLASS.**](common-control-window-classes.md) È possibile creare un controllo animazione usando [**la funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la macro [**Animate \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) La macro posiziona il controllo di animazione nell'angolo superiore sinistro della finestra padre e, se lo stile [**ACS \_ CENTER**](animation-control-styles.md) non è specificato, imposta la larghezza e l'altezza del controllo in base alle dimensioni di un frame nel clip AVI. Se **si specifica ACS \_ CENTER,** **Animate \_ Create** imposta la larghezza e l'altezza del controllo su zero. È possibile usare la [**funzione SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare la posizione e le dimensioni del controllo.

Se si crea un controllo animazione all'interno di una finestra di dialogo o da una risorsa finestra di dialogo, il controllo viene eliminato automaticamente quando l'utente chiude la finestra di dialogo. Se si crea un controllo animazione all'interno di una finestra, è necessario eliminare in modo esplicito il controllo.

## <a name="about-animation-control-messages"></a>Informazioni sui messaggi di controllo animazione

Un'applicazione invia messaggi a un controllo di animazione per aprire, riprodurre, arrestare e chiudere il clip AVI corrispondente. Ogni messaggio ha una o più macro che è possibile usare invece di inviare il messaggio in modo esplicito.

Dopo aver creato un controllo di animazione, un'applicazione invia il messaggio [**ACM \_ OPEN**](acm-open.md) per aprire un clip AVI e caricarlo in memoria. Il messaggio specifica il percorso di un file AVI o il nome di una risorsa AVI. Il sistema carica la risorsa AVI dal modulo che ha creato il controllo animazione.

Se il controllo animazione ha lo stile [**ACS \_ AUTOPLAY,**](animation-control-styles.md) il controllo inizia a riprodurre il clip AVI immediatamente dopo l'apertura del file AVI o della risorsa AVI. In caso contrario, un'applicazione può usare il [**messaggio \_ PLAY ACM**](acm-play.md) per avviare il clip AVI. Un'applicazione può arrestare il clip in qualsiasi momento inviando il [**messaggio STOP di ACM. \_**](acm-stop.md) L'ultimo fotogramma riprodotto rimane visualizzato quando il controllo termina la riproduzione del clip AVI o quando viene inviato **ACM \_ STOP.**

Un controllo animazione può inviare due codici di notifica alla relativa finestra padre: [ACN \_ START](acn-start.md) e [ACN \_ STOP.](acn-stop.md) La maggior parte delle applicazioni non gestisce le notifiche.

Per chiudere il file AVI o la risorsa AVI e rimuoverlo dalla memoria, un'applicazione può usare la macro [**Animate \_ Close,**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) che invia [**ACM \_ OPEN**](acm-open.md) con il nome file o il nome della risorsa impostato su **NULL.**

## <a name="default-message-processing"></a>Elaborazione dei messaggi predefinita

Questa sezione descrive i messaggi della finestra gestiti dalla routine della finestra per la [**classe di finestra ANIMATE \_ CLASS.**](common-control-window-classes.md)



| Message                                    | Elaborazione eseguita                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)           | Libera il file AVI o la risorsa AVI associata al controllo animazione.                                                                                                                                                                                                                   |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)       | Libera il file AVI o la risorsa AVI, libera una struttura di dati interna e quindi chiama [**la funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)                                                                                                                                                |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd) | Cancella lo sfondo della finestra usando il colore di sfondo corrente per i controlli statici.                                                                                                                                                                                                        |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)     | Alloca e inizializza una struttura di dati interna e quindi chiama [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)                                                                                                                                                                              |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) | Restituisce il valore dell'hit test HTTRANSPARENT.                                                                                                                                                                                                                                                   |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)              | Disegna un frame AVI nel controllo di animazione.                                                                                                                                                                                                                                                |
| [**DIMENSIONI \_ WM**](/windows/desktop/winmsg/wm-size)             | Controlla se il controllo ha lo [**stile ACS \_ CENTER.**](animation-control-styles.md) In caso contrario, il controllo chiama [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) In caso contrario, centra l'animazione nel controllo, invalida il controllo e quindi chiama **DefWindowProc.** |



 

 

 