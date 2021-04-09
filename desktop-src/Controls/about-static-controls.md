---
title: Informazioni sui controlli statici
description: In questo argomento viene illustrato il modo in cui vengono utilizzati i controlli statici.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064c1814b4f4ed6283b2fe22af06aed107e2c4d2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963499"
---
# <a name="about-static-controls"></a>Informazioni sui controlli statici

Le applicazioni spesso utilizzano controlli statici per etichettare altri controlli o separare un gruppo di controlli. Sebbene i controlli statici siano finestre figlio, non possono essere selezionati. Pertanto, non possono ricevere lo stato attivo della tastiera e non possono avere un'interfaccia della tastiera. Un controllo statico con lo stile di \_ notifica SS riceve l'input del mouse, inviando una notifica alla finestra padre quando l'utente fa clic o fa doppio clic sul controllo. I controlli statici appartengono alla classe della finestra statica.

Sebbene i controlli statici possano essere utilizzati nelle finestre sovrapposte, popup e figlio, sono progettati per l'utilizzo nelle finestre di dialogo, in cui il sistema standardizza il comportamento. Utilizzando i controlli statici all'esterno delle finestre di dialogo, uno sviluppatore aumenta il rischio che l'applicazione possa comportarsi in modo non standard. In genere, uno sviluppatore utilizza controlli statici nelle finestre di dialogo o utilizza lo \_ stile OWNERDRAW SS per creare controlli statici personalizzati.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Tipi di controllo statici](#static-control-types)
    -   [Controllo statico grafico semplice](#simple-graphics-static-control)
    -   [Controllo statico testo](#text-static-control)
    -   [Controllo statico immagine](#image-static-control)
    -   [Controllo statico creato dal proprietario](#owner-drawn-static-control)
-   [Elaborazione dei messaggi predefiniti del controllo statico](#static-control-default-message-processing)

## <a name="static-control-types"></a>Tipi di controllo statici

Sono disponibili quattro tipi di controlli statici. Ogni tipo ha uno o più [stili del controllo statico](static-control-styles.md).

-   [Controllo statico grafico semplice](#simple-graphics-static-control)
-   [Controllo statico testo](#text-static-control)
-   [Controllo statico immagine](#image-static-control)
-   [Controllo statico creato dal proprietario](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Controllo statico grafico semplice

Un semplice controllo statico di grafica Visualizza un frame o un rettangolo pieno. Un frame può essere disegnato in un certo numero di stili, incluso nero, grigio o bianco. Inoltre, è possibile disegnare un frame con uno stile inciso per assegnargli un aspetto tridimensionale. Gli stili dei fotogrammi includono SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT e SS \_ ETCHEDFRAME.

Un rettangolo può essere riempito con un colore in uno dei tre stili seguenti: nero, grigio o bianco. Questi stili sono definiti dalle costanti SS \_ BLACKRECT, SS \_ GRAYRECT e SS \_ WHITERECT.

Gli stili di grafica non possono essere combinati.

### <a name="text-static-control"></a>Controllo statico testo

Un controllo statico di testo Visualizza il testo in un rettangolo in uno dei cinque stili seguenti:

-   allineato a sinistra senza ritorno a capo automatico
-   allineato a sinistra con ritorno a capo automatico
-   centrata
-   allineata a destra
-   simple

Questi stili sono definiti rispettivamente dalle costanti SS \_ LEFTNOWORDWRAP, SS \_ Left, SS \_ Center, SS \_ right e SS \_ Simple. Il sistema riorganizza il testo in questi controlli in modi predefiniti, ad eccezione del testo "Simple", che non viene ridisposto.

Un'applicazione può modificare il testo in un controllo statico di testo in qualsiasi momento usando la funzione [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) o il messaggio di [**\_ testo WM**](/windows/desktop/winmsg/wm-settext) .

Nel sistema viene visualizzato il testo che si può inserire nel controllo statico e vengono ritagliate tutte le dimensioni. Per calcolare le dimensioni appropriate per il controllo, recuperare la metrica del tipo di carattere per il testo. Per altre informazioni sui tipi di carattere e sulle metriche dei tipi di carattere, vedere [caratteri e testo](/windows/desktop/gdi/fonts-and-text).

Per impostazione predefinita, il testo della finestra per un controllo statico, come per gli altri controlli, può contenere una e commerciale che definisce il carattere seguente come tasto di scelta rapida per il controllo (o, nel caso della maggior parte dei controlli statici, per il controllo che etichetta, che è il controllo successivo nell'ordine di tabulazione). Se si desidera visualizzare le e commerciali nel testo anziché utilizzarle per definire i collegamenti, includere lo stile SS \_ NoPrefix.

### <a name="image-static-control"></a>Controllo statico immagine

Un controllo statico Image può visualizzare bitmap, icone (incluse icone animate) o metafile avanzati. Il tipo di grafico visualizzato da un particolare controllo statico dipende dallo stile del controllo: SS \_ bitmap, SS \_ Icon o SS \_ ENHMETAFILE. Un'applicazione specifica lo stile quando crea il controllo e specifica anche un handle per la bitmap, l'icona o il metafile per la visualizzazione del controllo. Dopo la creazione del controllo, un'applicazione può associare un grafico diverso al controllo inviando un messaggio di [**\_ Immagine STM**](stm-setimage.md) , specificando un handle per il nuovo oggetto grafico. Un'applicazione può recuperare un handle per l'oggetto grafico attualmente associato a un controllo statico inviando un messaggio [**STM \_ GetImage**](stm-getimage.md) . Un'applicazione invia messaggi a un controllo statico tramite la funzione [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

### <a name="owner-drawn-static-control"></a>Owner-Drawn controllo statico

Utilizzando lo \_ stile OWNERDRAW SS, un'applicazione può assumere la responsabilità di disegnare un controllo statico. La finestra padre di un controllo statico creato dal proprietario (proprietario) riceve un messaggio [**WM \_ DrawItem**](wm-drawitem.md) ogni volta che è necessario disegnare il controllo statico. Il messaggio include un puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che contiene informazioni utilizzate dalla finestra proprietaria per il disegno del controllo.

## <a name="static-control-default-message-processing"></a>Elaborazione dei messaggi predefiniti del controllo statico

La routine della finestra per la classe della finestra di controllo statico predefinita esegue l'elaborazione predefinita per tutti i messaggi non elaborati dalla procedura di controllo statico. Quando il controllo statico restituisce **false** per qualsiasi messaggio, la routine della finestra predefinita controlla i messaggi ed esegue l'azione predefinita descritta nella tabella seguente. Nella tabella un controllo statico di testo è un controllo statico con lo stile SS \_ LEFTNOWORDWRAP, SS \_ Left, SS \_ Center, SS \_ right o SS \_ Simple.



| Message                                                | Azione predefinita                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**creazione di WM \_**](/windows/desktop/winmsg/wm-create)                     | Carica l'oggetto grafico e ridimensiona la finestra sulle dimensioni dell'oggetto, per i controlli statici grafici. Non esegue alcuna azione per altri controlli statici. |
| [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)                   | Libera ed elimina qualsiasi oggetto grafico, per i controlli statici grafici. Non esegue alcuna azione per altri controlli statici.                              |
| [**\_Abilitazione WM**](/windows/desktop/winmsg/wm-enable)                     | Consente di ridisegnare i controlli statici visibili.                                                                                                           |
| [**\_ERASEBKGND WM**](/windows/desktop/winmsg/wm-erasebkgnd)             | Restituisce **true**, che indica che il controllo Cancella lo sfondo.                                                                             |
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)             | Restituisce un DLGC \_ statico.                                                                                                                       |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)                   | Restituisce un handle per il tipo di carattere per i controlli statici di testo.                                                                                      |
| [**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)                   | Restituisce il numero di caratteri copiati.                                                                                                    |
| [**\_GETTEXTLENGTH WM**](/windows/desktop/winmsg/wm-gettextlength)       | Restituisce la lunghezza, in caratteri, del testo di un controllo statico di testo.                                                                   |
| [**\_LBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Invia alla finestra padre un codice di notifica di [STN \_ DBLCLK](stn-dblclk.md) se lo stile del controllo è SS \_ Notify.                              |
| [**\_LBUTTONDOWN WM**](/windows/desktop/inputdev/wm-lbuttondown)         | Invia alla finestra padre un codice di notifica [ \_ selezionato da STN](stn-clicked.md) se lo stile del controllo è SS \_ Notify.                            |
| [**\_NCLBUTTONDBLCLK WM**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Invia alla finestra padre un codice di notifica di [STN \_ DBLCLK](stn-dblclk.md) se lo stile del controllo è SS \_ Notify.                              |
| [**\_NCLBUTTONDOWN WM**](/windows/desktop/inputdev/wm-nclbuttondown)     | Invia alla finestra padre un codice di notifica [ \_ selezionato da STN](stn-clicked.md) se lo stile del controllo è SS \_ Notify.                            |
| [**\_NCHITTEST WM**](/windows/desktop/inputdev/wm-nchittest)             | Restituisce HTCLIENT se lo stile del controllo è SS \_ Notify; in caso contrario, restituisce HTTRANSPARENT.                                                      |
| [**\_disegno WM**](/windows/desktop/gdi/wm-paint)                          | Ridisegna il controllo.                                                                                                                       |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)                   | Imposta il tipo di carattere e i ridisegni per i controlli statici del testo.                                                                                        |
| [**\_testo WM**](/windows/desktop/winmsg/wm-settext)                   | Imposta il testo e i ridisegni per i controlli statici del testo.                                                                                        |



 

La routine della finestra predefinita passa tutti gli altri messaggi a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

 

 