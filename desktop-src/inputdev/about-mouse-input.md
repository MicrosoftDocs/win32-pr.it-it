---
title: Informazioni sull'input del mouse
description: In questo argomento viene illustrato l'input del mouse.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- input dell'utente, input del mouse
- acquisizione dell'input dell'utente, input del mouse
- input del mouse
- cursore del mouse
- cursori, input del mouse
- acquisizione del mouse
- Funzione Blocca clic mouse
- XBUTTONs
- configurazione del mouse
- messaggi del mouse
- Messaggio WM_NCHITTEST
- Funzionalità di accessibilità del mouse
- Funzionalità di accessibilità sonar del mouse
- rotellina del mouse
- Messaggio WM_MOUSEWHEEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2294027cb4ca2c97371a7a06c90a7e46188e3b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726983"
---
# <a name="about-mouse-input"></a>Informazioni sull'input del mouse

Il mouse è un dispositivo importante, ma facoltativo, di input dell'utente per le applicazioni. Un'applicazione ben scritta deve includere un'interfaccia del mouse, ma non deve dipendere esclusivamente dal mouse per l'acquisizione dell'input dell'utente. L'applicazione deve fornire anche il supporto completo della tastiera.

L'input del mouse viene ricevuto da un'applicazione sotto forma di messaggi inviati o inviati alle relative finestre.

Questa sezione contiene gli argomenti seguenti:

-   [Cursore del mouse](#mouse-cursor)
-   [Mouse Capture](#mouse-capture)
-   [Funzione Blocca clic mouse](#mouse-clicklock)
-   [Configurazione del mouse](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Messaggi del mouse](#mouse-messages)
    -   [Messaggi del mouse area client](#client-area-mouse-messages)
    -   [Messaggi del mouse area non client](#nonclient-area-mouse-messages)
    -   [Messaggio WM \_ NCHITTEST](/windows)
-   [Sonar del mouse](#mouse-sonar)
-   [Il mouse svanisce](#mouse-vanish)
-   [Rotellina del mouse](#the-mouse-wheel)
-   [Attivazione di finestre](#window-activation)

## <a name="mouse-cursor"></a>Cursore del mouse

Quando l'utente sposta il mouse, il sistema sposta una bitmap sullo schermo denominata cursore del *mouse*. Il cursore del mouse contiene un punto con un solo pixel denominato area *sensibile, un* punto che il sistema tiene traccia e riconosce come posizione del cursore. Quando si verifica un evento del mouse, la finestra che contiene l'area sensibile riceve in genere il messaggio del mouse risultante dall'evento. Non è necessario che la finestra sia attiva o che lo stato attivo della tastiera riceva un messaggio del mouse.

Il sistema mantiene una variabile che controlla la velocità del mouse, ovvero la distanza con cui il cursore si sposta quando l'utente sposta il mouse. Per recuperare o impostare la velocità del mouse, è possibile usare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il flag **SPI \_ GetMouse** o **SPI \_ del** mouse. Per ulteriori informazioni sui cursori del mouse, vedere [cursori](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Mouse Capture

Il sistema invia in genere un messaggio del mouse alla finestra che contiene l'area sensibile del cursore quando si verifica un evento del mouse. Un'applicazione può modificare questo comportamento usando la funzione [**secapture**](/windows/win32/api/winuser/nf-winuser-setcapture) per indirizzare i messaggi del mouse a una finestra specifica. La finestra riceve tutti i messaggi del mouse fino a quando l'applicazione chiama la funzione [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) o specifica un'altra finestra di acquisizione o fino a quando l'utente non fa clic su una finestra creata da un altro thread.

Quando l'acquisizione del mouse viene modificata, il sistema invia un messaggio [**WM \_ CAPTURECHANGED**](wm-capturechanged.md) alla finestra che sta perdendo l'acquisizione del mouse. Il parametro *lParam* del messaggio specifica un handle per la finestra che sta ottenendo l'acquisizione del mouse.

Solo la finestra in primo piano può acquisire l'input del mouse. Quando una finestra di sfondo tenta di acquisire l'input del mouse, riceve i messaggi solo per gli eventi del mouse che si verificano quando l'area sensibile del cursore si trova all'interno della parte visibile della finestra.

L'acquisizione dell'input del mouse è utile se una finestra deve ricevere tutti gli input del mouse, anche quando il cursore si sposta all'esterno della finestra. Ad esempio, un'applicazione in genere tiene traccia della posizione del cursore dopo un evento di un pulsante del mouse, dopo il cursore fino a quando non si verifica un evento pulsante del mouse. Se un'applicazione non ha acquisito l'input del mouse e l'utente rilascia il pulsante del mouse all'esterno della finestra, la finestra non riceve il messaggio del pulsante.

Un thread può utilizzare la funzione [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) per determinare se una delle finestre ha acquisito il mouse. Se una delle finestre del thread ha acquisito il mouse, **GetCapture** recupera un handle per la finestra.

## <a name="mouse-clicklock"></a>Funzione Blocca clic mouse

La funzionalità di accessibilità del mouse funzione Blocca clic consente a un utente di bloccare il pulsante del mouse primario dopo un solo clic. Per un'applicazione, il pulsante sembra comunque premuto. Per sbloccare il pulsante, un'applicazione può inviare qualsiasi messaggio del mouse oppure l'utente può fare clic su un pulsante del mouse. Questa funzionalità consente a un utente di eseguire in modo più semplice combinazioni di mouse complesse. Ad esempio, gli utenti con determinate limitazioni fisiche possono evidenziare testo, trascinare oggetti o aprire menu in modo più semplice. Per ulteriori informazioni, vedere i flag e le osservazioni seguenti in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **\_GETMOUSECLICKLOCK SPI**
-   **\_SETMOUSECLICKLOCK SPI**
-   **\_GETMOUSECLICKLOCKTIME SPI**
-   **\_SETMOUSECLICKLOCKTIME SPI**

## <a name="mouse-configuration"></a>Configurazione del mouse

Sebbene il mouse sia un dispositivo di input importante per le applicazioni, non tutti gli utenti hanno necessariamente un mouse. Un'applicazione può determinare se il sistema include un mouse passando il valore **\_ MOUSEPRESENT di SM** alla funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

Windows supporta un mouse che presenta fino a tre pulsanti. Con il mouse a tre pulsanti, i pulsanti sono designati come pulsanti a sinistra, a metà e a destra. I messaggi e le costanti denominate correlate ai pulsanti del mouse utilizzano le lettere L, M e R per identificare i pulsanti. Il pulsante su un mouse a pulsante singolo viene considerato il pulsante a sinistra. Sebbene Windows supporti un mouse con più pulsanti, la maggior parte delle applicazioni utilizza il pulsante sinistro principalmente e le altre, se disponibili.

Le applicazioni possono inoltre supportare una rotellina del mouse. È possibile premere o ruotare la rotellina del mouse. Quando si preme la rotellina del mouse, viene usato il pulsante centrale (terzo), che invia i normali messaggi al pulsante centrale all'applicazione. Quando viene ruotato, un messaggio della rotellina viene inviato all'applicazione. Per ulteriori informazioni, vedere [la sezione rotellina del mouse](#the-mouse-wheel) .

Le applicazioni possono supportare i pulsanti di comando dell'applicazione. Questi pulsanti, denominati X Buttons, sono progettati per semplificare l'accesso a un browser Internet, alla posta elettronica e a servizi multimediali. Quando viene premuto un pulsante X, un messaggio [**WM \_ APPCOMMAND**](wm-appcommand.md) viene inviato all'applicazione. Per ulteriori informazioni, vedere la descrizione nel messaggio **WM \_ APPCOMMAND** .

Un'applicazione può determinare il numero di pulsanti sul mouse passando il valore **\_ CMOUSEBUTTONS di SM** alla funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Per configurare il mouse per un utente di sinistra, l'applicazione può usare la funzione [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) per invertire il significato dei pulsanti sinistro e destro del mouse. Il passaggio del valore **\_ SETMOUSEBUTTONSWAP di SPI** alla funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) è un altro modo per invertire il significato dei pulsanti. Si noti, tuttavia, che il mouse è una risorsa condivisa, di conseguenza l'inversione del significato dei pulsanti ha effetto su tutte le applicazioni.

## <a name="xbuttons"></a>XBUTTONs

Windows supporta un mouse con cinque pulsanti. Oltre ai pulsanti sinistro, centrale e destro sono presenti XBUTTON1 e XBUTTON2, che forniscono lo spostamento indietro e avanti quando si usa il browser.

Gestione finestre supporta XBUTTON1 e XBUTTON2 tramite i messaggi **WM \_ XBUTTON \*** e **WM \_ NCXBUTTON \*** . Il HIWORD del **wParam** in questi messaggi contiene un flag che indica quale pulsante X è stato premuto. Poiché questi messaggi del mouse si adattano anche tra le costanti **WM \_ MOUSEFIRST** e **WM \_ MOUSELAST**, un'applicazione può filtrare tutti i messaggi del mouse con [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

Il supporto seguente XBUTTON1 e XBUTTON2:

-   [**\_APPCOMMAND WM**](wm-appcommand.md)
-   [**\_NCXBUTTONDBLCLK WM**](wm-ncxbuttondblclk.md)
-   [**\_NCXBUTTONDOWN WM**](wm-ncxbuttondown.md)
-   [**\_NCXBUTTONUP WM**](wm-ncxbuttonup.md)
-   [**\_XBUTTONDBLCLK WM**](wm-xbuttondblclk.md)
-   [**\_XBUTTONDOWN WM**](wm-xbuttondown.md)
-   [**\_XBUTTONUP WM**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Le API seguenti sono state modificate per supportare questi pulsanti:

-   [**\_evento mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**\_PARENTNOTIFY WM**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

È improbabile che una finestra figlio in un'applicazione componente possa implementare direttamente i comandi per XBUTTON1 e XBUTTON2. Quindi [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Invia un messaggio [**WM \_ APPCOMMAND**](wm-appcommand.md) a una finestra quando si fa clic su un pulsante X. **DefWindowProc** invia anche il messaggio **WM \_ APPCOMMAND** alla relativa finestra padre. Questa operazione è simile al modo in cui i menu di scelta rapida vengono richiamati con un clic destro:**DefWindowProc** Invia un messaggio [**WM \_ ContextMenu**](/windows/desktop/menurc/wm-contextmenu) al menu e lo invia anche al relativo padre. Inoltre, se **DefWindowProc** riceve un messaggio **WM \_ APPCOMMAND** per una finestra di primo livello, chiama un hook della shell con il codice HSHELL \_ APPCOMMAND.

È disponibile il supporto per le tastiere che includono chiavi aggiuntive per funzioni del browser, funzioni multimediali, avvio delle applicazioni e risparmio energia. Per ulteriori informazioni, vedere [tasti di scelta rapida per l'esplorazione e altre funzioni](about-keyboard-input.md).

## <a name="mouse-messages"></a>Messaggi del mouse

Il mouse genera un evento di input quando l'utente sposta il mouse oppure preme o rilascia un pulsante del mouse. Il sistema converte gli eventi di input del mouse in messaggi e li invia alla coda di messaggi del thread appropriato. Quando i messaggi del mouse vengono pubblicati più velocemente di quanto un thread possa elaborarli, il sistema ignora tutti i messaggi del mouse, tranne quelli più recenti.

Una finestra riceve un messaggio del mouse quando si verifica un evento del mouse mentre il cursore si trova all'interno dei bordi della finestra o quando la finestra ha acquisito il mouse. I messaggi del mouse sono divisi in due gruppi: messaggi dell'area client e messaggi dell'area non client. In genere, un'applicazione elabora i messaggi dell'area client e ignora i messaggi dell'area non client.

Questa sezione contiene gli argomenti seguenti:

-   [Messaggi del mouse area client](#client-area-mouse-messages)
-   [Messaggi del mouse area non client](#nonclient-area-mouse-messages)
-   [Messaggio WM \_ NCHITTEST](/windows)

### <a name="client-area-mouse-messages"></a>Messaggi del mouse area client

Una finestra riceve un messaggio del mouse dell'area client quando si verifica un evento del mouse all'interno dell'area client della finestra. Il sistema invia il messaggio di [**WM \_ MOUSEMOVE**](wm-mousemove.md) alla finestra quando l'utente sposta il cursore all'interno dell'area client. Invia uno dei messaggi seguenti quando l'utente preme o rilascia un pulsante del mouse mentre il cursore si trova all'interno dell'area client.



| Messaggio                                       | Significato                                     |
|-----------------------------------------------|---------------------------------------------|
| [**\_LBUTTONDBLCLK WM**](wm-lbuttondblclk.md) | È stato fatto doppio clic sul pulsante sinistro del mouse.   |
| [**\_LBUTTONDOWN WM**](wm-lbuttondown.md)     | È stato premuto il pulsante sinistro del mouse.          |
| [**\_LBUTTONUP WM**](wm-lbuttonup.md)         | Il pulsante sinistro del mouse è stato rilasciato.         |
| [**\_MBUTTONDBLCLK WM**](wm-mbuttondblclk.md) | È stato fatto doppio clic sul pulsante centrale del mouse. |
| [**\_MBUTTONDOWN WM**](wm-mbuttondown.md)     | È stato premuto il pulsante centrale del mouse.        |
| [**\_MBUTTONUP WM**](wm-mbuttonup.md)         | Il pulsante centrale del mouse è stato rilasciato.       |
| [**\_RBUTTONDBLCLK WM**](wm-rbuttondblclk.md) | È stato fatto doppio clic con il pulsante destro del mouse.  |
| [**\_RBUTTONDOWN WM**](wm-rbuttondown.md)     | È stato premuto il pulsante destro del mouse.         |
| [**\_RBUTTONUP WM**](wm-rbuttonup.md)         | Il pulsante destro del mouse è stato rilasciato.        |
| [**\_XBUTTONDBLCLK WM**](wm-xbuttondblclk.md) | È stato fatto doppio clic su un pulsante X del mouse.       |
| [**\_XBUTTONDOWN WM**](wm-xbuttondown.md)     | È stato premuto un pulsante X del mouse.              |
| [**\_XBUTTONUP WM**](wm-xbuttonup.md)         | È stato rilasciato un pulsante X del mouse.             |



 

Inoltre, un'applicazione può chiamare la funzione [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) per fare in modo che il sistema invii altri due messaggi. Invia il messaggio [**WM \_ MOUSEHOVER**](wm-mousehover.md) quando il cursore passa sull'area client per un determinato periodo di tempo. Invia il messaggio [**di \_ MOUSELEAVE di WM**](wm-mouseleave.md) quando il cursore esce dall'area client.

### <a name="message-parameters"></a>Parametri del messaggio

Il parametro *lParam* di un messaggio del mouse dell'area client indica la posizione dell'area sensibile del cursore. La parola di basso livello indica la coordinata x dell'area sensibile e la parola di ordine superiore indica la coordinata y. Le coordinate sono specificate nelle coordinate del client. Nel sistema di coordinate client tutti i punti sullo schermo vengono specificati in relazione alle coordinate (0,0) dell'angolo superiore sinistro dell'area client.

Il parametro *wParam* contiene i flag che indicano lo stato degli altri pulsanti del mouse e i tasti CTRL e MAIUSC al momento dell'evento del mouse. È possibile verificare questi flag quando l'elaborazione del messaggio del mouse dipende dallo stato di un altro pulsante del mouse o del tasto CTRL o MAIUSC. Il parametro *wParam* può essere una combinazione dei valori seguenti.



| Valore            | Descrizione                      |
|------------------|----------------------------------|
| **MK ( \_ controllo)**  | Il tasto CTRL è premuto.            |
| **\_LBUTTON MK**  | Il pulsante sinistro del mouse è premuto.   |
| **\_MBUTTON MK**  | Il pulsante centrale del mouse è inattivo. |
| **\_RBUTTON MK**  | Il pulsante destro del mouse è inattivo.  |
| **\_turno MK**    | Il tasto MAIUSC è premuto.           |
| **\_XBUTTON1 MK** | Il primo pulsante X è inattivo.      |
| **\_XBUTTON2 MK** | Il secondo pulsante X è inattivo.     |



 

### <a name="double-click-messages"></a>Messaggi di Double-Click

Il sistema genera un messaggio di doppio clic quando l'utente fa doppio clic con un pulsante del mouse in rapida successione. Quando l'utente fa clic su un pulsante, il sistema stabilisce un rettangolo centrato intorno all'area sensibile del cursore. Contrassegna anche l'ora in cui si è verificato il clic. Quando l'utente fa clic con lo stesso pulsante una seconda volta, il sistema determina se l'area sensibile è ancora all'interno del rettangolo e calcola il tempo trascorso dal primo clic. Se l'area sensibile è ancora all'interno del rettangolo e il tempo trascorso non supera il valore di timeout doppio clic, il sistema genera un messaggio di doppio clic.

Un'applicazione può ottenere e impostare i valori di timeout di doppio clic usando rispettivamente le funzioni [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) e [**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) . In alternativa, l'applicazione può impostare il valore di timeout doppio clic usando il flag **\_ SETDOUBLECLICKTIME di SPI** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) . È anche possibile impostare le dimensioni del rettangolo usato dal sistema per rilevare i doppio clic passando i flag **SPI \_ SETDOUBLECLKWIDTH** e **SPI \_ SETDOUBLECLKHEIGHT** a **SystemParametersInfo**. Si noti, tuttavia, che l'impostazione del valore del doppio clic-timeout e del rettangolo influiscono su tutte le applicazioni.

Per impostazione predefinita, una finestra definita dall'applicazione non riceve messaggi di doppio clic. A causa dell'overhead di sistema per la generazione di messaggi di doppio clic, questi messaggi vengono generati solo per le finestre appartenenti alle classi con lo stile della classe **cs \_ DBLCLKS** . Quando si registra la classe della finestra, l'applicazione deve impostare questo stile. Per altre informazioni, vedere [classi di finestra](/windows/desktop/winmsg/window-classes).

Un messaggio di doppio clic è sempre il terzo messaggio in una serie di quattro messaggi. I primi due messaggi sono i messaggi button-down e Button-up generati dal primo clic. Il secondo clic genera il messaggio di doppio clic seguito da un altro messaggio pulsante in alto. Se, ad esempio, si fa doppio clic con il pulsante sinistro del mouse, viene generata la seguente sequenza di messaggi:

1.  [**\_LBUTTONDOWN WM**](wm-lbuttondown.md)
2.  [**\_LBUTTONUP WM**](wm-lbuttonup.md)
3.  [**\_LBUTTONDBLCLK WM**](wm-lbuttondblclk.md)
4.  [**\_LBUTTONUP WM**](wm-lbuttonup.md)

Poiché una finestra riceve sempre un messaggio di pulsante di selezione prima di ricevere un messaggio di doppio clic, un'applicazione usa in genere un messaggio di doppio clic per estendere un'attività iniziata durante un messaggio di un pulsante. Ad esempio, quando l'utente fa clic su un colore nella tavolozza dei colori di Microsoft Paint, Paint Visualizza il colore selezionato accanto alla tavolozza. Quando l'utente fa doppio clic su un colore, Paint Visualizza il colore e apre la finestra di dialogo **modifica colori** .

### <a name="nonclient-area-mouse-messages"></a>Messaggi del mouse area non client

Una finestra riceve un messaggio del mouse dell'area non client quando si verifica un evento del mouse in qualsiasi parte di una finestra, ad eccezione dell'area client. L'area non client di una finestra è costituita dal bordo, dalla barra dei menu, dalla barra del titolo, dalla barra di scorrimento, dal menu finestra, dal pulsante Riduci a icona e dal pulsante Ingrandisci.

Il sistema genera messaggi di area non client principalmente per uso personale. Ad esempio, il sistema utilizza messaggi dell'area non client per modificare il cursore in una freccia a due punte quando l'area sensibile del cursore viene spostata sul bordo di una finestra. Una finestra deve passare i messaggi del mouse dell'area non client alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per sfruttare l'interfaccia del mouse incorporata.

È presente un messaggio del mouse dell'area non client corrispondente per ogni messaggio del mouse dell'area client. I nomi di questi messaggi sono simili, ad eccezione del fatto che le costanti denominate per i messaggi dell'area non client includono le lettere NC. Se, ad esempio, lo spostamento del cursore nell'area non client genera un messaggio [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md) e si preme il pulsante sinistro del mouse mentre il cursore si trova nell'area non client, genera un messaggio [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md) .

Il parametro *lParam* di un messaggio del mouse dell'area non client è una struttura che contiene le coordinate x e y dell'area sensibile del cursore. Diversamente dalle coordinate dei messaggi del mouse dell'area client, le coordinate vengono specificate nelle coordinate dello schermo anziché nelle coordinate del client. Nel sistema di coordinate dello schermo tutti i punti sullo schermo sono relativi alle coordinate (0, 0) dell'angolo superiore sinistro dello schermo.

Il parametro *wParam* contiene un valore di hit test, un valore che indica la posizione in cui si è verificato l'evento del mouse nell'area non client. La sezione seguente illustra lo scopo dei valori di hit test.

### <a name="the-wm_nchittest-message"></a>Messaggio WM \_ NCHITTEST

Ogni volta che si verifica un evento del mouse, il sistema invia un messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) alla finestra che contiene l'area sensibile del cursore o alla finestra che ha acquisito il mouse. Il sistema utilizza questo messaggio per determinare se inviare un'area client o un messaggio del mouse dell'area non client. Un'applicazione che deve ricevere messaggi di spostamento del mouse e di un pulsante del mouse deve passare il messaggio **WM \_ NCHITTEST** alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

Il parametro *lParam* del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) contiene le coordinate dello schermo dell'area sensibile del cursore. La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esamina le coordinate e restituisce un valore di hit test che indica la posizione dell'area sensibile. Il valore di hit test può essere uno dei valori seguenti.



| Valore             | Posizione dell'area sensibile                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | Nel bordo di una finestra che non dispone di un bordo di ridimensionamento.                                                                                                                                       |
| **HTBOTTOM**      | Il bordo inferiore orizzontale di una finestra.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | Nell'angolo inferiore sinistro del bordo di una finestra.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | Nell'angolo inferiore destro del bordo di una finestra.                                                                                                                                                       |
| **HTCAPTION**     | In una barra del titolo.                                                                                                                                                                                     |
| **HTCLIENT**      | In un'area client.                                                                                                                                                                                   |
| **HTCLOSE**       | In un pulsante **Chiudi** .                                                                                                                                                                              |
| **HTERROR**       | Sullo sfondo dello schermo o su una linea di divisione tra le finestre (uguale a HTNOWHERE, con la differenza che la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un segnale acustico di sistema per indicare un errore). |
| **HTGROWBOX**     | In una casella delle dimensioni (uguale a **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | In un pulsante della **Guida** .                                                                                                                                                                               |
| **HTHSCROLL**     | In una barra di scorrimento orizzontale.                                                                                                                                                                         |
| **HTLEFT**        | Sul bordo sinistro di una finestra.                                                                                                                                                                     |
| **HTMENU**        | In un menu.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | In un pulsante **Ingrandisci** .                                                                                                                                                                           |
| **HTMINBUTTON**   | In un pulsante **Riduci a icona** .                                                                                                                                                                           |
| **HTNOWHERE**     | Sullo sfondo dello schermo o su una linea di divisione tra le finestre.                                                                                                                                     |
| **HTREDUCE**      | In un pulsante **Riduci a icona** .                                                                                                                                                                           |
| **HTRIGHT**       | Sul bordo destro di una finestra.                                                                                                                                                                    |
| **HTSIZE**        | In una casella delle dimensioni (uguale a **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | In un menu di **sistema** o in un pulsante **Chiudi** in una finestra figlio.                                                                                                                                    |
| **HTTOP**         | Nel bordo superiore orizzontale di una finestra.                                                                                                                                                         |
| **HTTOPLEFT**     | Nell'angolo superiore sinistro del bordo di una finestra.                                                                                                                                                        |
| **HTTOPRIGHT**    | Nell'angolo superiore destro del bordo di una finestra.                                                                                                                                                       |
| **HTTRANSPARENT** | In una finestra attualmente coperta da un'altra finestra nello stesso thread.                                                                                                                                 |
| **HTVSCROLL**     | Sulla barra di scorrimento verticale.                                                                                                                                                                         |
| **HTZOOM**        | In un pulsante **Ingrandisci** .                                                                                                                                                                           |



 

Se il cursore si trova nell'area client di una finestra, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce il valore di hit test **HTCLIENT** alla routine della finestra. Quando la routine della finestra restituisce questo codice al sistema, il sistema converte le coordinate dello schermo dell'area sensibile del cursore in coordinate client, quindi invia il messaggio del mouse dell'area client appropriato.

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce uno degli altri valori di hit test quando l'area sensibile del cursore si trova nell'area non client di una finestra. Quando la routine della finestra restituisce uno di questi valori di hit test, il sistema invia un messaggio del mouse sull'area non client, inserendo il valore di hit test nel parametro *wParam* del messaggio e le coordinate del cursore nel parametro *lParam* .

## <a name="mouse-sonar"></a>Sonar del mouse

La funzionalità di accessibilità del sonar del mouse Mostra brevemente diversi cerchi concentrici intorno al puntatore quando l'utente preme e rilascia il tasto CTRL. Questa funzionalità consente a un utente di individuare il puntatore del mouse su una schermata ingombrante o con una risoluzione impostata su alta, su un monitor di qualità scadente o per gli utenti con visione disaccoppiata. Per ulteriori informazioni, vedere i flag seguenti in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**\_GETMOUSESONAR SPI**

**\_SETMOUSESONAR SPI**

## <a name="mouse-vanish"></a>Il mouse svanisce

La funzionalità di accessibilità del mouse consente di nascondere il puntatore quando l'utente sta digitando. Il puntatore del mouse viene visualizzato nuovamente quando l'utente sposta il mouse. Questa funzionalità impedisce al puntatore di nascondere il testo digitato, ad esempio in un messaggio di posta elettronica o in un altro documento. Per ulteriori informazioni, vedere i flag seguenti in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**\_GETMOUSEVANISH SPI**

**\_SETMOUSEVANISH SPI**

## <a name="the-mouse-wheel"></a>Rotellina del mouse

La rotellina del mouse combina le funzionalità di una rotellina e un pulsante del mouse. La rotellina ha ricavi discreti, distanziati in modo uniforme. Quando si ruota la rotellina, viene inviato un messaggio della rotellina all'applicazione quando viene rilevata ogni tacca. Il pulsante della rotellina può anche funzionare come un normale pulsante di Windows al centro (terzo). Premendo e rilasciando la rotellina del mouse si inviano i messaggi standard [**WM \_ MBUTTONUP**](wm-mbuttonup.md) e [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) . Se si fa doppio clic sul terzo pulsante, viene inviato il messaggio standard [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) .

La rotellina del mouse è supportata tramite il messaggio [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) .

La rotazione del mouse consente di inviare il messaggio [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) alla finestra messa a fuoco. La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga il messaggio all'elemento padre della finestra. Non deve essere presente alcun inoltro interno del messaggio, poiché **DefWindowProc** lo propaga alla catena padre fino a quando non viene trovata una finestra che lo elabora.

### <a name="determining-the-number-of-scroll-lines"></a>Determinazione del numero di righe di scorrimento

Le applicazioni devono usare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per recuperare il numero di righe Scorrete da un documento per ogni operazione di scorrimento (Notch della rotellina). Per recuperare il numero di righe, un'applicazione effettua la chiamata seguente:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



La variabile "pulScrollLines" punta a un valore Unsigned Integer che riceve il numero suggerito di righe da scorrere quando la rotellina del mouse viene ruotata senza tasti di modifica:

-   Se questo numero è 0, non si verificherà alcuno scorrimento.
-   Se questo numero è **\_ PAGESCROLL della rotellina**, è necessario interpretare un rullo della rotellina facendo clic una volta nella pagina verso il basso o le aree della barra di scorrimento.
-   Se il numero di righe da scorrere è maggiore del numero di righe visualizzabili, l'operazione di scorrimento deve essere interpretata anche come operazione di paging o di paging.

Il valore predefinito per il numero di righe di scorrimento sarà 3. Se un utente modifica il numero di righe di scorrimento, usando il foglio delle proprietà del mouse nel pannello di controllo, il sistema operativo trasmette un messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) a tutte le finestre di primo livello con **SPI \_ SETWHEELSCROLLLINES** specificato. Quando un'applicazione riceve il messaggio **WM \_ SETTINGCHANGE** , può ottenere il nuovo numero di righe di scorrimento chiamando:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Controlli che scorrono

La tabella seguente elenca i controlli con funzionalità di scorrimento (incluse le righe di scorrimento impostate dall'utente). 

| Control                 | Scorrimento                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modifica controllo            | Verticale e orizzontale.                                                                                                                                                |
| Controllo casella di riepilogo        | Verticale e orizzontale.                                                                                                                                                |
| Casella combinata               | Quando non viene rilasciata, ogni scorrimento recupera l'elemento successivo o precedente. Quando viene rilasciata, ogni scorrimento esegue il rollforward del messaggio alla casella di riepilogo, che scorre di conseguenza. |
| CMD (riga di comando)      | Verticale.                                                                                                                                                               |
| Visualizzazione ad albero               | Verticale e orizzontale.                                                                                                                                                |
| Visualizzazione elenco               | Verticale e orizzontale.                                                                                                                                                |
| Scorrimento verso l'alto o verso il basso         | Un elemento alla volta.                                                                                                                                                     |
| Scorrimenti TrackBar        | Un elemento alla volta.                                                                                                                                                     |
| Microsoft Rich Edit 1,0 | Verticale. Si noti che il client di Exchange dispone di versioni proprie dei controlli visualizzazione elenco e visualizzazione albero che non dispongono del supporto per la rotellina.                                        |
| Microsoft Rich Edit 2,0 | Verticale.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Rilevamento di un mouse con una rotellina

Per determinare se un mouse con una rotellina è connesso, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ MOUSEWHEELPRESENT**. Un valore restituito **true** indica che il mouse è connesso.

L'esempio seguente è relativo alla routine della finestra per un controllo di modifica su più righe:


```
BOOL ScrollLines(
     PWNDDATA pwndData,   //scrolls the window indicated
     int cLinesToScroll); //number of times

short gcWheelDelta; //wheel delta from roll
PWNDDATA pWndData; //pointer to structure containing info about the window
UINT gucWheelScrollLines=0;//number of lines to scroll on a wheel rotation

gucWheelScrollLines = SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 
                             0, 
                             pulScrollLines, 
                             0);

case WM_MOUSEWHEEL:
    /*
     * Do not handle zoom and datazoom.
     */
    if (wParam & (MK_SHIFT | MK_CONTROL)) {
        goto PassToDefaultWindowProc;
    }

    gcWheelDelta -= (short) HIWORD(wParam);
    if (abs(gcWheelDelta) >= WHEEL_DELTA && gucWheelScrollLines > 0) 
    {
        int cLineScroll;

        /*
         * Limit a roll of one (1) WHEEL_DELTA to
         * scroll one (1) page.
         */
        cLineScroll = (int) min(
                (UINT) pWndData->ichLinesOnScreen - 1,
                gucWheelScrollLines);

        if (cLineScroll == 0) {
            cLineScroll++;
        }

        cLineScroll *= (gcWheelDelta / WHEEL_DELTA);
        assert(cLineScroll != 0);

        gcWheelDelta = gcWheelDelta % WHEEL_DELTA;
        return ScrollLines(pWndData, cLineScroll);
    }

    break;
```



## <a name="window-activation"></a>Attivazione di finestre

Quando l'utente fa clic su una finestra di primo livello inattiva o sulla finestra figlio di una finestra di primo livello inattiva, il sistema invia il messaggio [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) (tra gli altri) alla finestra di primo livello o figlio. Il sistema invia questo messaggio dopo l'invio del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) alla finestra, ma prima di pubblicare il messaggio del pulsante. Quando **WM \_ MOUSEACTIVATE** viene passato alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , il sistema attiva la finestra di primo livello e quindi inserisce il messaggio del pulsante verso il basso nella finestra di primo livello o nella finestra figlio.

Elaborando [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md), una finestra può controllare se la finestra di primo livello diventa la finestra attiva in seguito a un clic del mouse e se la finestra su cui è stato fatto clic riceve il messaggio di pulsante successivo. A tale scopo, viene restituito uno dei valori seguenti dopo l'elaborazione di **WM \_ MOUSEACTIVATE**.



| Valore                    | Significato                                                              |
|--------------------------|----------------------------------------------------------------------|
| **\_attivazione ma**         | Attiva la finestra e non rimuove il messaggio del mouse.         |
| **MA \_ NOactivate**       | Non attiva la finestra e non rimuove il messaggio del mouse. |
| **\_ACTIVATEANDEAT ma**   | Attiva la finestra ed Elimina il messaggio del mouse.                 |
| **\_NOACTIVATEANDEAT ma** | Non attiva la finestra, ma elimina il messaggio del mouse.         |

## <a name="see-also"></a>Vedi anche

[Sfruttamento del movimento del mouse High-Definition](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)