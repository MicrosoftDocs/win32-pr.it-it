---
title: Informazioni sui controlli statici
description: Questo argomento illustra come vengono usati i controlli statici.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa9b77ff7c1357cede494f60c1d345d0eb4b8f5f8cf63ace13176179d385794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922301"
---
# <a name="about-static-controls"></a>Informazioni sui controlli statici

Le applicazioni usano spesso controlli statici per etichettare altri controlli o per separare un gruppo di controlli. Anche se i controlli statici sono finestre figlio, non possono essere selezionati. Pertanto, non possono ricevere lo stato attivo della tastiera e non possono avere un'interfaccia della tastiera. Un controllo statico con lo stile SS NOTIFY riceve l'input del mouse, inviando una notifica alla finestra padre quando l'utente fa clic o fa doppio clic \_ sul controllo. I controlli statici appartengono alla classe della finestra STATIC.

Anche se i controlli statici possono essere usati in finestre sovrapposte, popup e figlio, sono progettati per l'uso nelle finestre di dialogo, in cui il sistema standardizza il proprio comportamento. Usando controlli statici all'esterno delle finestre di dialogo, uno sviluppatore aumenta il rischio che l'applicazione si comporti in modo non standard. In genere, uno sviluppatore usa controlli statici nelle finestre di dialogo o lo stile SS \_ OWNERDRAW per creare controlli statici personalizzati.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Tipi di controllo statici](#static-control-types)
    -   [Controllo statico di grafica semplice](#simple-graphics-static-control)
    -   [Controllo statico del testo](#text-static-control)
    -   [Controllo statico dell'immagine](#image-static-control)
    -   [Controllo statico disegnato dal proprietario](#owner-drawn-static-control)
-   [Elaborazione dei messaggi predefinita del controllo statico](#static-control-default-message-processing)

## <a name="static-control-types"></a>Tipi di controllo statici

Esistono quattro tipi di controlli statici. Ogni tipo ha uno o più [stili di controllo statici.](static-control-styles.md)

-   [Controllo statico di grafica semplice](#simple-graphics-static-control)
-   [Controllo statico del testo](#text-static-control)
-   [Controllo statico dell'immagine](#image-static-control)
-   [Controllo statico disegnato dal proprietario](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Controllo statico di grafica semplice

Un semplice controllo statico grafico visualizza una cornice o un rettangolo pieno. Una cornice può essere disegnata in diversi stili, inclusi nero, grigio o bianco. Inoltre, una cornice può essere disegnata con uno stile conciso per assegnargli un aspetto tridimensionale. Gli stili dei frame includono SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT e SS \_ ETCHEDFRAME.

Un rettangolo può essere riempito con colore in uno dei tre stili seguenti: nero, grigio o bianco. Questi stili sono definiti dalle costanti SS \_ BLACKRECT, SS \_ GRAYRECT e SS \_ WHITERECT.

Gli stili di grafica non possono essere combinati.

### <a name="text-static-control"></a>Controllo statico del testo

Un controllo statico di testo visualizza il testo in un rettangolo in uno dei cinque stili seguenti:

-   allineato a sinistra senza ritorno a capo automatico
-   allineato a sinistra con ritorno a capo automatico
-   centrata
-   allineata a destra
-   simple

Questi stili sono definiti dalle costanti SS \_ LEFTNOWORDWRAP, \_ SS LEFT, SS \_ CENTER, SS RIGHT e \_ SS \_ SIMPLE, rispettivamente. Il sistema riorganizza il testo in questi controlli in modi predefiniti, ad eccezione del testo "semplice", che non viene ridisporto.

Un'applicazione può modificare il testo in un controllo statico di testo in qualsiasi momento usando la [**funzione SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) o il [**messaggio WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

Il sistema visualizza la quantità di testo possibile nel controllo statico e ritaglia tutto ciò che non rientra. Per calcolare le dimensioni appropriate per il controllo, recuperare le metriche del tipo di carattere per il testo. Per altre informazioni sui tipi di carattere e sulle metriche dei tipi di carattere, vedere [Tipi di carattere e testo](/windows/desktop/gdi/fonts-and-text).

Per impostazione predefinita, il testo della finestra per un controllo statico, come per altri controlli, può contenere una e commerciale che definisce il carattere seguente come tasto di scelta rapida per il controllo (o, nel caso della maggior parte dei controlli statici, per il controllo etichettato, ovvero il controllo successivo nell'ordine di tabulazione). Se si desidera visualizzare le e commerciale nel testo anziché usarle per definire i tasti di scelta rapida, includere lo stile SS \_ NOPREFIX.

### <a name="image-static-control"></a>Controllo statico dell'immagine

Un controllo statico dell'immagine può visualizzare bitmap, icone (incluse le icone animate) o metafile migliorati. Il tipo di immagine visualizzata da un determinato controllo statico dipende dallo stile del controllo: BITMAP \_ SS, ICONA SS \_ o SS \_ ENHMETAFILE. Un'applicazione specifica lo stile quando crea il controllo e specifica anche un handle per la bitmap, l'icona o il metafile da visualizzare. Dopo aver creato il controllo, un'applicazione può associare un elemento grafico diverso al controllo inviando un messaggio [**\_ SETIMAGE STM,**](stm-setimage.md) specificando un handle per il nuovo oggetto grafico. Un'applicazione può recuperare un handle per l'oggetto grafico attualmente associato a un controllo statico inviando un [**messaggio \_ GETIMAGE STM.**](stm-getimage.md) Un'applicazione invia messaggi a un controllo statico usando la [**funzione SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea)

### <a name="owner-drawn-static-control"></a>Owner-Drawn controllo statico

Usando lo stile SS \_ OWNERDRAW, un'applicazione può assumersi la responsabilità di disegnare un controllo statico. La finestra padre di un controllo statico disegnato dal proprietario (il relativo proprietario) riceve un messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) ogni volta che è necessario disegnare il controllo statico. Il messaggio include un puntatore a una [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) che contiene informazioni utilizzate dalla finestra proprietaria durante il disegno del controllo.

## <a name="static-control-default-message-processing"></a>Elaborazione dei messaggi predefinita del controllo statico

La routine della finestra per la classe della finestra di controllo statica predefinita esegue l'elaborazione predefinita per tutti i messaggi che la procedura di controllo statico non elabora. Quando il controllo statico restituisce **FALSE** per qualsiasi messaggio, la routine della finestra predefinita controlla i messaggi ed esegue l'azione predefinita descritta nella tabella seguente. Nella tabella un controllo statico di testo è un controllo statico con lo stile SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS \_ CENTER, SS \_ RIGHT o SS \_ SIMPLE.



| Message                                                | Azione predefinita                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**CREAZIONE \_ DI WM**](/windows/desktop/winmsg/wm-create)                     | Carica l'oggetto grafico e ridimensiona la finestra in base alle dimensioni dell'oggetto, per i controlli statici grafici. Non viene eseguita alcuna azione per altri controlli statici. |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                   | Libera ed elimina qualsiasi oggetto grafico, per i controlli statici grafici. Non viene eseguita alcuna azione per altri controlli statici.                              |
| [**ABILITAZIONE DI \_ WM**](/windows/desktop/winmsg/wm-enable)                     | Ridisegna i controlli statici visibili.                                                                                                           |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)             | Restituisce **TRUE,** che indica che il controllo cancella lo sfondo.                                                                             |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)             | Restituisce DLGC \_ STATIC.                                                                                                                       |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                   | Restituisce un handle per il tipo di carattere per i controlli statici di testo.                                                                                      |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                   | Restituisce il numero di caratteri copiati.                                                                                                    |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength)       | Restituisce la lunghezza, in caratteri, del testo per un controllo statico di testo.                                                                   |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Invia alla finestra padre un [codice di notifica STN \_ DBLCLK](stn-dblclk.md) se lo stile del controllo è SS \_ NOTIFY.                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)         | Invia alla finestra padre un [codice di notifica STN \_ CLICKED](stn-clicked.md) se lo stile del controllo è SS \_ NOTIFY.                            |
| [**WM \_ NCLBUTTONDBLCLK**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Invia alla finestra padre un [codice di notifica STN \_ DBLCLK](stn-dblclk.md) se lo stile del controllo è SS \_ NOTIFY.                              |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown)     | Invia alla finestra padre un [codice di notifica STN \_ CLICKED](stn-clicked.md) se lo stile del controllo è SS \_ NOTIFY.                            |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest)             | Restituisce HTCLIENT se lo stile del controllo è SS \_ NOTIFY; in caso contrario, restituisce HTTRANSPARENT.                                                      |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                          | Ridisegna il controllo.                                                                                                                       |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)                   | Imposta il tipo di carattere e ridisegna per i controlli statici di testo.                                                                                        |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                   | Imposta il testo e ridisegna per i controlli statici di testo.                                                                                        |



 

La routine della finestra predefinita passa tutti gli altri messaggi a [**DefWindowProc per l'elaborazione**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) predefinita.

 

 