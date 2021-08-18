---
title: Informazioni sull'input del mouse
description: In questo argomento viene illustrato l'input del mouse.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- input utente, input del mouse
- acquisizione dell'input dell'utente, input del mouse
- input del mouse
- cursore del mouse
- cursori, input del mouse
- mouse capture
- Mouse ClickLock
- XBUTTON
- configurazione del mouse
- messaggi del mouse
- WM_NCHITTEST messaggio
- Funzionalità di accessibilità Mouse Disaserzione
- Funzionalità di accessibilità sonar del mouse
- rotellina del mouse
- WM_MOUSEWHEEL messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c4978babd6322102908699dbf88b68e2d3b92f57fa9bfa79b9b8c3eae88931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105790"
---
# <a name="about-mouse-input"></a>Informazioni sull'input del mouse

Il mouse è un dispositivo di input utente importante, ma facoltativo, per le applicazioni. Un'applicazione ben scritta deve includere un'interfaccia del mouse, ma non deve dipendere esclusivamente dal mouse per l'acquisizione dell'input dell'utente. L'applicazione deve fornire anche il supporto completo della tastiera.

Un'applicazione riceve l'input del mouse sotto forma di messaggi inviati o inviati alle relative finestre.

Questa sezione contiene gli argomenti seguenti:

-   [Cursore del mouse](#mouse-cursor)
-   [Mouse Capture](#mouse-capture)
-   [Mouse ClickLock](#mouse-clicklock)
-   [Configurazione del mouse](#mouse-configuration)
-   [XBUTTON](#xbuttons)
-   [Messaggi del mouse](#mouse-messages)
    -   [Messaggi del mouse nell'area client](#client-area-mouse-messages)
    -   [Messaggi del mouse dell'area non client](#nonclient-area-mouse-messages)
    -   [Messaggio \_ WM NCHITTEST](/windows)
-   [Mouse Sonar](#mouse-sonar)
-   [Mouse Disasato](#mouse-vanish)
-   [Rotellina del mouse](#the-mouse-wheel)
-   [Attivazione di finestre](#window-activation)

## <a name="mouse-cursor"></a>Cursore del mouse

Quando l'utente sposta il mouse, il sistema sposta una bitmap sullo schermo denominata *cursore del mouse.* Il cursore del mouse contiene un punto a pixel singolo denominato *area* sensibile, un punto che il sistema tiene traccia e riconosce come posizione del cursore. Quando si verifica un evento del mouse, la finestra che contiene l'area sensibile riceve in genere il messaggio del mouse risultante dall'evento . La finestra non deve essere attiva o avere lo stato attivo della tastiera per ricevere un messaggio del mouse.

Il sistema mantiene una variabile che controlla la velocità del mouse, ovvero la distanza di spostamento del cursore quando l'utente sposta il mouse. È possibile usare la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il flag **SPI \_ GETMOUSE** o **SPI \_ SETMOUSE** per recuperare o impostare la velocità del mouse. Per altre informazioni sui cursori del mouse, vedere [Cursori](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Mouse Capture

Il sistema invia in genere un messaggio del mouse alla finestra che contiene l'area sensibile del cursore quando si verifica un evento del mouse. Un'applicazione può modificare questo comportamento usando la [**funzione SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) per indirizzare i messaggi del mouse a una finestra specifica. La finestra riceve tutti i messaggi del mouse fino a quando l'applicazione non chiama la funzione [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) o non specifica un'altra finestra di acquisizione oppure finché l'utente non fa clic su una finestra creata da un altro thread.

Quando il mouse capture cambia, il sistema invia un messaggio [**WM \_ CAPTURECHANGED**](wm-capturechanged.md) alla finestra che perde l'acquisizione del mouse. Il *parametro lParam* del messaggio specifica un handle per la finestra che sta acquisiscendo l'acquisizione del mouse.

Solo la finestra in primo piano può acquisire l'input del mouse. Quando una finestra in background tenta di acquisire l'input del mouse, riceve messaggi solo per gli eventi del mouse che si verificano quando l'area sensibile del cursore si trova all'interno della parte visibile della finestra.

L'acquisizione dell'input del mouse è utile se una finestra deve ricevere tutto l'input del mouse, anche quando il cursore si sposta all'esterno della finestra. Ad esempio, un'applicazione tiene traccia in genere della posizione del cursore dopo un evento di scorrimento del pulsante del mouse, dopo il cursore fino a quando non si verifica un evento di scorrimento del pulsante del mouse. Se un'applicazione non ha acquisito l'input del mouse e l'utente rilascia il pulsante del mouse all'esterno della finestra, la finestra non riceve il messaggio di selezione del pulsante.

Un thread può usare la [**funzione GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) per determinare se una delle finestre ha acquisito il mouse. Se una delle finestre del thread ha acquisito il mouse, **GetCapture** recupera un handle per la finestra.

## <a name="mouse-clicklock"></a>Mouse ClickLock

La funzionalità di accessibilità ClickLock del mouse consente all'utente di bloccare il pulsante principale del mouse dopo un singolo clic. Per un'applicazione, il pulsante sembra ancora essere premuto. Per sbloccare il pulsante, un'applicazione può inviare qualsiasi messaggio del mouse o l'utente può fare clic su qualsiasi pulsante del mouse. Questa funzionalità consente all'utente di eseguire combinazioni complesse del mouse in modo più semplice. Ad esempio, quelli con determinate limitazioni fisiche possono evidenziare più facilmente testo, trascinare oggetti o aprire menu. Per altre informazioni, vedere i flag seguenti e le osservazioni in [**SystemParametersInfo:**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>Configurazione del mouse

Anche se il mouse è un dispositivo di input importante per le applicazioni, non tutti gli utenti hanno necessariamente un mouse. Un'applicazione può determinare se il sistema include un mouse passando il **valore \_ SM MOUSEPRESENT** alla [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

Windows supporta un mouse con un massimo di tre pulsanti. Con un mouse a tre pulsanti, i pulsanti vengono designati come pulsanti sinistro, centrale e destro. I messaggi e le costanti denominate correlate ai pulsanti del mouse usano le lettere L, M e R per identificare i pulsanti. Il pulsante su un mouse a pulsante singolo è considerato il pulsante sinistro. Anche Windows supporta un mouse con più pulsanti, la maggior parte delle applicazioni usa principalmente il pulsante sinistro e le altre, se non del tutto.

Le applicazioni possono anche supportare una rotellina del mouse. La rotellina del mouse può essere premuta o ruotata. Quando la rotellina del mouse viene premuta, funge da pulsante centrale (terzo), inviando normali messaggi di pulsante centrale all'applicazione. Quando viene ruotata, all'applicazione viene inviato un messaggio con la rotellina. Per altre informazioni, vedere [la sezione Rotellina del mouse.](#the-mouse-wheel)

Le applicazioni possono supportare i pulsanti di comando dell'applicazione. Questi pulsanti, denominati pulsanti X, sono progettati per consentire un accesso più semplice a un browser Internet, posta elettronica e servizi multimediali. Quando viene premuto un pulsante X, all'applicazione viene inviato un messaggio [**\_ APPCOMMAND WM.**](wm-appcommand.md) Per altre informazioni, vedere la descrizione nel **messaggio \_ WM APPCOMMAND.**

Un'applicazione può determinare il numero di pulsanti sul mouse passando il valore **\_ SM CMOUSEBUTTONS** alla [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Per configurare il mouse per un utente mancino, l'applicazione può usare la funzione [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) per invertire il significato dei pulsanti sinistro e destro del mouse. Il passaggio **del valore SPI \_ SETMOUSEBUTTONSWAP** alla funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) è un altro modo per invertire il significato dei pulsanti. Si noti, tuttavia, che il mouse è una risorsa condivisa, quindi l'invertimento del significato dei pulsanti influisce su tutte le applicazioni.

## <a name="xbuttons"></a>XBUTTON

Windows supporta un mouse con cinque pulsanti. Oltre ai pulsanti sinistro, centrale e destro, sono disponibili XBUTTON1 e XBUTTON2, che consentono lo spostamento all'indietro e in avanti quando si usa il browser.

Gestione finestre supporta XBUTTON1 e XBUTTON2 tramite i messaggi **WM \_ XBUTTON \* *_ e _* WM \_ NCXBUTTON \* *_. La parola chiave HIWORD di _* WPARAM** in questi messaggi contiene un flag che indica quale pulsante X è stato premuto. Poiché questi messaggi del mouse si adattano anche tra le costanti **WM \_ MOUSEFIRST** e **WM \_ MOUSELAST,** un'applicazione può filtrare tutti i messaggi del mouse con [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**o PeekMessage.**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)

Gli elementi seguenti supportano XBUTTON1 e XBUTTON2:

-   [**WM \_ APPCOMMAND**](wm-appcommand.md)
-   [**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
-   [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
-   [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
-   [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
-   [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
-   [**WM \_ XBUTTONUP**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Le API seguenti sono state modificate per supportare questi pulsanti:

-   [**evento \_ mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

È improbabile che una finestra figlio in un'applicazione componente sia in grado di implementare direttamente i comandi per XBUTTON1 e XBUTTON2. [**DefWindowProc invia**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) quindi un [**messaggio WM \_ APPCOMMAND**](wm-appcommand.md) a una finestra quando si fa clic su un pulsante X. **DefWindowProc** invia anche il **messaggio WM \_ APPCOMMAND** alla finestra padre. Questo è simile al modo in cui i menu di scelta rapida vengono richiamati con un clic con il pulsante destro del mouse.**DefWindowProc** invia un messaggio [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) al menu e lo invia anche al relativo elemento padre. Inoltre, se **DefWindowProc** riceve un messaggio **WM \_ APPCOMMAND** per una finestra di primo livello, chiama un hook della shell con codice HSHELL \_ APPCOMMAND.

È disponibile il supporto per le tastiere con tasti aggiuntivi per funzioni del browser, funzioni multimediali, avvio di applicazioni e risparmio energia. Per altre informazioni, vedere [Tasti di scelta rapida per l'esplorazione e Altre funzioni](about-keyboard-input.md).

## <a name="mouse-messages"></a>Messaggi del mouse

Il mouse genera un evento di input quando l'utente sposta il mouse o preme o rilascia un pulsante del mouse. Il sistema converte gli eventi di input del mouse in messaggi e li invia alla coda di messaggi del thread appropriato. Quando i messaggi del mouse vengono inviati più velocemente di quanto un thread possa elaborarli, il sistema rimuove tutti i messaggi del mouse, ma il messaggio più recente.

Una finestra riceve un messaggio del mouse quando si verifica un evento del mouse mentre il cursore si trova all'interno dei bordi della finestra o quando la finestra ha acquisito il mouse. I messaggi del mouse sono suddivisi in due gruppi: messaggi dell'area client e messaggi dell'area non client. In genere, un'applicazione elabora i messaggi dell'area client e ignora i messaggi dell'area non client.

Questa sezione contiene gli argomenti seguenti:

-   [Messaggi del mouse nell'area client](#client-area-mouse-messages)
-   [Messaggi del mouse nell'area non client](#nonclient-area-mouse-messages)
-   [Messaggio WM \_ NCHITTEST](/windows)

### <a name="client-area-mouse-messages"></a>Messaggi del mouse nell'area client

Una finestra riceve un messaggio del mouse nell'area client quando si verifica un evento del mouse all'interno dell'area client della finestra. Il sistema invia il [**messaggio WM \_ MOUSEMOVE**](wm-mousemove.md) alla finestra quando l'utente sposta il cursore all'interno dell'area client. Invia uno dei messaggi seguenti quando l'utente preme o rilascia un pulsante del mouse mentre il cursore si trova all'interno dell'area client.



| Messaggio                                       | Significato                                     |
|-----------------------------------------------|---------------------------------------------|
| [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md) | È stato fatto doppio clic sul pulsante sinistro del mouse.   |
| [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)     | È stato premuto il pulsante sinistro del mouse.          |
| [**WM \_ LBUTTONUP**](wm-lbuttonup.md)         | Il pulsante sinistro del mouse è stato rilasciato.         |
| [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) | È stato fatto doppio clic sul pulsante centrale del mouse. |
| [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)     | È stato premuto il pulsante centrale del mouse.        |
| [**WM \_ MBUTTONUP**](wm-mbuttonup.md)         | Il pulsante centrale del mouse è stato rilasciato.       |
| [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) | È stato fatto doppio clic con il pulsante destro del mouse.  |
| [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)     | È stato premuto il pulsante destro del mouse.         |
| [**WM \_ RBUTTONUP**](wm-rbuttonup.md)         | È stato rilasciato il pulsante destro del mouse.        |
| [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md) | È stato fatto doppio clic su un pulsante X del mouse.       |
| [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)     | È stato premuto un pulsante X del mouse.              |
| [**WM \_ XBUTTONUP**](wm-xbuttonup.md)         | È stato rilasciato un pulsante X del mouse.             |



 

Inoltre, un'applicazione può chiamare la [**funzione TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) per fare in modo che il sistema invii altri due messaggi. Invia il messaggio [**WM \_ MOUSEHOVER**](wm-mousehover.md) quando il cursore passa sull'area client per un determinato periodo di tempo. Invia il messaggio [**WM \_ MOUSELEAVE**](wm-mouseleave.md) quando il cursore esce dall'area client.

### <a name="message-parameters"></a>Parametri del messaggio

Il *parametro lParam* di un messaggio del mouse nell'area client indica la posizione dell'area sensibile del cursore. La parola di ordine basso indica la coordinata x dell'area sensibile e la parola di ordine superiore indica la coordinata y. Le coordinate vengono specificate nelle coordinate client. Nel sistema di coordinate client tutti i punti sullo schermo vengono specificati in relazione alle coordinate (0,0) dell'angolo superiore sinistro dell'area client.

Il *parametro wParam* contiene flag che indicano lo stato degli altri pulsanti del mouse e i tasti CTRL e MAIUSC al momento dell'evento del mouse. È possibile controllare questi flag quando l'elaborazione del messaggio del mouse dipende dallo stato di un altro pulsante del mouse o del tasto CTRL o MAIUSC. Il *parametro wParam* può essere una combinazione dei valori seguenti.



| Valore            | Descrizione                      |
|------------------|----------------------------------|
| **CONTROLLO \_ MK**  | Il tasto CTRL è premuto.            |
| **MK \_ LBUTTON**  | Il pulsante sinistro del mouse è verso il basso.   |
| **MK \_ MBUTTON**  | Il pulsante centrale del mouse è in basso. |
| **MK \_ RBUTTON**  | Il pulsante destro del mouse è verso il basso.  |
| **MK \_ SHIFT**    | Il tasto MAIUSC è premuto.           |
| **MK \_ XBUTTON1** | Il primo pulsante X è in basso.      |
| **MK \_ XBUTTON2** | Il secondo pulsante X è in basso.     |



 

### <a name="double-click-messages"></a>Double-Click messaggi

Il sistema genera un messaggio con doppio clic quando l'utente fa clic due volte su un pulsante del mouse in rapida successione. Quando l'utente fa clic su un pulsante, il sistema stabilisce un rettangolo centrato intorno all'area sensibile del cursore. Contrassegna anche l'ora in cui si è verificato il clic. Quando l'utente fa clic sullo stesso pulsante una seconda volta, il sistema determina se l'area sensibile è ancora all'interno del rettangolo e calcola il tempo trascorso dal primo clic. Se l'area sensibile è ancora all'interno del rettangolo e il tempo trascorso non supera il valore di timeout del doppio clic, il sistema genera un messaggio di doppio clic.

Un'applicazione può ottenere e impostare valori di timeout del doppio clic usando rispettivamente le [**funzioni GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) e [**SetDoubleClickTime.**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) In alternativa, l'applicazione può impostare il valore di timeout del doppio clic usando il flag **SPI \_ SETDOUBLECLICKTIME** con la [**funzione SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) Può anche impostare le dimensioni del rettangolo utilizzato dal sistema per rilevare i doppio clic passando i flag **SPI \_ SETDOUBLECLKWIDTH** e **SPI \_ SETDOUBLECLKHEIGHT** **a SystemParametersInfo**. Si noti, tuttavia, che l'impostazione del valore di timeout del doppio clic e del rettangolo influisce su tutte le applicazioni.

Per impostazione predefinita, una finestra definita dall'applicazione non riceve messaggi con doppio clic. A causa dell'overhead di sistema associato alla generazione di messaggi con doppio clic, questi messaggi vengono generati solo per le finestre appartenenti a classi con lo stile di classe **\_ CS DBLCLKS.** L'applicazione deve impostare questo stile durante la registrazione della classe della finestra. Per altre informazioni, vedere [Classi window](/windows/desktop/winmsg/window-classes).

Un messaggio con doppio clic è sempre il terzo messaggio di una serie di quattro messaggi. I primi due messaggi sono i messaggi button-down e button-up generati dal primo clic. Il secondo clic genera il messaggio di doppio clic seguito da un altro messaggio di scelta. Ad esempio, facendo doppio clic sul pulsante sinistro del mouse viene generata la sequenza di messaggi seguente:

1.  [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)
2.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)
3.  [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)
4.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)

Poiché una finestra riceve sempre un messaggio di pulsante giù prima di ricevere un messaggio con doppio clic, un'applicazione usa in genere un messaggio con doppio clic per estendere un'attività avviata durante un messaggio a discesa. Ad esempio, quando l'utente fa clic su un colore nella tavolozza dei Microsoft Paint, Paint il colore selezionato accanto alla tavolozza. Quando l'utente fa doppio clic su un colore, Paint il colore e apre la **finestra di** dialogo Modifica colori.

### <a name="nonclient-area-mouse-messages"></a>Messaggi del mouse nell'area non client

Una finestra riceve un messaggio del mouse nell'area non client quando si verifica un evento del mouse in qualsiasi parte di una finestra ad eccezione dell'area client. L'area non client di una finestra è costituita da bordo, barra dei menu, barra del titolo, barra di scorrimento, menu della finestra, pulsante di riduzione a icona e pulsante di ingrandimento.

Il sistema genera messaggi di area non client principalmente per uso personale. Ad esempio, il sistema usa messaggi di area non client per modificare il cursore in una freccia a due punte quando l'area sensibile del cursore si sposta sul bordo di una finestra. Una finestra deve passare messaggi non client del mouse nell'area alla [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per sfruttare l'interfaccia del mouse predefinita.

È presente un messaggio del mouse nell'area non client corrispondente per ogni messaggio del mouse nell'area client. I nomi di questi messaggi sono simili ad eccezione del fatto che le costanti denominate per i messaggi dell'area non client includono le lettere NC. Ad esempio, lo spostamento del cursore nell'area non client genera un messaggio [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md) e la pressione del pulsante sinistro del mouse mentre il cursore si trova nell'area non client genera un messaggio [**WM \_ NCLBUTTONDOWN.**](wm-nclbuttondown.md)

Il *parametro lParam* di un messaggio del mouse nell'area non client è una struttura che contiene le coordinate x e y dell'area sensibile del cursore. A differenza delle coordinate dei messaggi del mouse nell'area client, le coordinate vengono specificate nelle coordinate dello schermo anziché nelle coordinate client. Nel sistema di coordinate dello schermo tutti i punti sullo schermo sono relativi alle coordinate (0,0) dell'angolo superiore sinistro dello schermo.

Il *parametro wParam* contiene un valore di hit test, un valore che indica dove nell'area non client si è verificato l'evento del mouse. La sezione seguente illustra lo scopo dei valori di hit test.

### <a name="the-wm_nchittest-message"></a>Messaggio WM \_ NCHITTEST

Ogni volta che si verifica un evento del mouse, il sistema invia un messaggio [**\_ WM NCHITTEST**](wm-nchittest.md) alla finestra che contiene l'area sensibile del cursore o alla finestra che ha acquisito il mouse. Il sistema usa questo messaggio per determinare se inviare un messaggio mouse di area client o non client. Un'applicazione che deve ricevere messaggi di spostamento del mouse e pulsante del mouse deve passare il **messaggio WM \_ NCHITTEST** alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Il *parametro lParam* del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) contiene le coordinate dello schermo dell'area sensibile del cursore. La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esamina le coordinate e restituisce un valore di hit test che indica la posizione dell'area sensibile. Il valore dell'hit test può essere uno dei valori seguenti.



| Valore             | Posizione dell'area sensibile                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | Nel bordo di una finestra che non ha un bordo di ridimensionamento.                                                                                                                                       |
| **HTBOTTOM**      | Nel bordo orizzontale inferiore di una finestra.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | Nell'angolo inferiore sinistro del bordo di una finestra.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | Nell'angolo inferiore destro del bordo di una finestra.                                                                                                                                                       |
| **GESTIONE DEI DISPOSITIVI DI GESTIONE DEI DISPOSITIVI DI GESTIONE DELLE APPLICAZIONI**     | In una barra del titolo.                                                                                                                                                                                     |
| **HTCLIENT**      | In un'area client.                                                                                                                                                                                   |
| **HTCLOSE**       | In un **pulsante** Chiudi.                                                                                                                                                                              |
| **HTERROR**       | Sullo sfondo dello schermo o su una linea di divisione tra le finestre (come HTNOWHERE, ad eccezione del fatto che la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) produce un segnale acustico di sistema per indicare un errore). |
| **HTGROWBOX**     | In una casella delle dimensioni (uguale a **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | In un **pulsante ?**                                                                                                                                                                               |
| **HTHSCROLL**     | In una barra di scorrimento orizzontale.                                                                                                                                                                         |
| **HTLEFT**        | Nel bordo sinistro di una finestra.                                                                                                                                                                     |
| **HTMENU**        | In un menu.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | In un **pulsante Ingrandisci.**                                                                                                                                                                           |
| **HTMINBUTTON**   | In un **pulsante Riduci** a icona.                                                                                                                                                                           |
| **HTNOWHERE**     | Sullo sfondo dello schermo o su una linea di divisione tra le finestre.                                                                                                                                     |
| **HTREDUCE**      | In un **pulsante Riduci** a icona.                                                                                                                                                                           |
| **HTRIGHT**       | Nel bordo destro di una finestra.                                                                                                                                                                    |
| **HTSIZE**        | In una casella delle dimensioni (uguale a **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | In un menu **di** sistema o in un **pulsante** Chiudi in una finestra figlio.                                                                                                                                    |
| **HTTOP**         | Bordo superiore orizzontale di una finestra.                                                                                                                                                         |
| **HTTOPLEFT**     | Nell'angolo superiore sinistro del bordo di una finestra.                                                                                                                                                        |
| **HTTOPRIGHT**    | Nell'angolo superiore destro del bordo di una finestra.                                                                                                                                                       |
| **HTTRANSPARENT** | In una finestra attualmente coperta da un'altra finestra nello stesso thread.                                                                                                                                 |
| **HTVSCROLL**     | Nella barra di scorrimento verticale.                                                                                                                                                                         |
| **HTZOOM**        | In un **pulsante Ingrandisci.**                                                                                                                                                                           |



 

Se il cursore si trova nell'area client di una finestra, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce il valore dell'hit test **HTCLIENT** alla routine della finestra. Quando la routine della finestra restituisce questo codice al sistema, il sistema converte le coordinate dello schermo dell'area sensibile del cursore in coordinate client e quindi invia il messaggio appropriato del mouse nell'area client.

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce uno degli altri valori di hit test quando l'area sensibile del cursore si trova nell'area non client di una finestra. Quando la routine della finestra restituisce uno di questi valori di hit test, il sistema invia un messaggio del mouse nell'area non client, inserendo il valore dell'hit test nel parametro *wParam* del messaggio e le coordinate del cursore *nel parametro lParam.*

## <a name="mouse-sonar"></a>Mouse Sonar

La funzionalità di accessibilità Sonar del mouse mostra brevemente diversi cerchi concentrici intorno al puntatore quando l'utente preme e rilascia il tasto CTRL. Questa funzionalità consente a un utente di individuare il puntatore del mouse su uno schermo disordinato o con risoluzione impostata su alta, su un monitor di scarsa qualità o per gli utenti con problemi di vista. Per altre informazioni, vedere i flag seguenti in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>Sparizione del mouse

La funzionalità di accessibilità Scomparsa del mouse nasconde il puntatore quando l'utente digita. Il puntatore del mouse viene visualizzato di nuovo quando l'utente sposta il mouse. Questa funzionalità impedisce al puntatore di nascondere il testo digitato, ad esempio in un messaggio di posta elettronica o in un altro documento. Per altre informazioni, vedere i flag seguenti in [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSEVANISH**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>Rotellina del mouse

La rotellina del mouse combina le funzionalità di una rotellina e di un pulsante del mouse. La rotellina ha notche discrete e con spazi uniforme. Quando si ruota la rotellina, all'applicazione viene inviato un messaggio con la rotellina quando viene rilevata ogni notch. Il pulsante rotellina può anche funzionare come un normale Windows centrale (terzo) pulsante. Premendo e rilasciando la rotellina del mouse vengono inviati messaggi [**\_ MBUTTONUP**](wm-mbuttonup.md) e [**\_ MBUTTONDOWN WM**](wm-mbuttondown.md) standard. Facendo doppio clic sul terzo pulsante viene inviato il messaggio [**\_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) di WM standard.

La rotellina del mouse è supportata tramite [**il \_ messaggio WM MOUSEWHEEL.**](wm-mousewheel.md)

Ruotando il mouse viene inviato il [**messaggio \_ WM MOUSEWHEEL**](wm-mousewheel.md) alla finestra attiva. La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga il messaggio all'elemento padre della finestra. Non deve essere presente alcun inoltro interno del messaggio, poiché **DefWindowProc** lo propaga fino alla catena padre fino a quando non viene trovata una finestra che lo elabora.

### <a name="determining-the-number-of-scroll-lines"></a>Determinazione del numero di righe di scorrimento

Le applicazioni devono usare la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per recuperare il numero di righe di scorrimento di un documento per ogni operazione di scorrimento (rotellina della rotellina). Per recuperare il numero di righe, un'applicazione effettua la chiamata seguente:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



La variabile "pulScrollLines" punta a un valore intero senza segno che riceve il numero suggerito di righe da scorrere quando la rotellina del mouse viene ruotata senza tasti di modifica:

-   Se questo numero è 0, non deve verificarsi alcuno scorrimento.
-   Se questo numero è **WHEEL \_ PAGESCROLL,** un rullo della rotellina deve essere interpretato come fare clic una volta nelle aree di scorrimento della pagina verso il basso o verso l'alto.
-   Se il numero di righe da scorrere è maggiore del numero di righe visualizzabili, l'operazione di scorrimento deve essere interpretata anche come un'operazione di scorrimento verso il basso o verso l'alto.

Il valore predefinito per il numero di righe di scorrimento sarà 3. Se un utente modifica il numero di righe di scorrimento, usando il foglio Proprietà mouse in Pannello di controllo, il sistema operativo trasmette un messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) a tutte le finestre di primo livello con **SPI \_ SETWHEELSCROLLLINES** specificato. Quando un'applicazione riceve il **messaggio WM \_ SETTINGCHANGE,** può quindi ottenere il nuovo numero di righe di scorrimento chiamando:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Controlli che scorrono

La tabella seguente elenca i controlli con funzionalità di scorrimento (incluse le righe di scorrimento impostate dall'utente). 

| Control                 | Scorrimento                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Controllo Edit            | Verticale e orizzontale.                                                                                                                                                |
| Controllo Casella di riepilogo        | Verticale e orizzontale.                                                                                                                                                |
| Casella combinata               | Quando non viene rilasciato verso il basso, ogni scorrimento recupera l'elemento successivo o precedente. Quando viene rilasciato verso il basso, ogni scorrimento inoltra il messaggio alla casella di riepilogo, che scorre di conseguenza. |
| CMD (riga di comando)      | Verticale.                                                                                                                                                               |
| Visualizzazione ad albero               | Verticale e orizzontale.                                                                                                                                                |
| Visualizzazione elenco               | Verticale e orizzontale.                                                                                                                                                |
| Scorrimenti su/giù         | Un elemento alla volta.                                                                                                                                                     |
| Scorrimenti trackbar        | Un elemento alla volta.                                                                                                                                                     |
| Microsoft Rich Edit 1.0 | Verticale. Si noti che Exchange client dispone di versioni specifiche della visualizzazione elenco e dei controlli visualizzazione albero che non supportano la rotellina del mouse.                                        |
| Microsoft Rich Edit 2.0 | Verticale.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Rilevamento di un mouse con una rotellina

Per determinare se un mouse con rotellina è connesso, chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **\_ SM MOUSEWHEELPRESENT.** Il valore restituito **TRUE** indica che il mouse è connesso.

L'esempio seguente è dalla routine della finestra per un controllo di modifica su più righe:


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

Quando l'utente fa clic su una finestra di primo livello inattiva o sulla finestra figlio di una finestra di primo livello inattiva, il sistema invia il messaggio [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) (tra le altre) alla finestra di primo livello o figlio. Il sistema invia questo messaggio dopo aver pubblicato il messaggio [**\_ WM NCHITTEST**](wm-nchittest.md) nella finestra, ma prima di pubblicare il messaggio di menu a discesa. Quando **WM \_ MOUSEACTIVATE** viene passato alla funzione [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) il sistema attiva la finestra di primo livello e quindi invia il messaggio di pulsante verso il basso nella finestra di primo livello o figlio.

Elaborando [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md), una finestra può controllare se la finestra di primo livello diventa la finestra attiva in seguito a un clic del mouse e se la finestra su cui è stato fatto clic riceve il successivo messaggio di selezione del pulsante. A tale scopo, restituisce uno dei valori seguenti dopo l'elaborazione **di WM \_ MOUSEACTIVATE.**



| Valore                    | Significato                                                              |
|--------------------------|----------------------------------------------------------------------|
| **ATTIVAZIONE \_ MA**         | Attiva la finestra e non rimuove il messaggio del mouse.         |
| **MA \_ NOACTIVATE**       | Non attiva la finestra e non rimuove il messaggio del mouse. |
| **MA \_ ACTIVATEANDEAT**   | Attiva la finestra ed elimina il messaggio del mouse.                 |
| **MA \_ NOACTIVATEANDEAT** | Non attiva la finestra ma rimuove il messaggio del mouse.         |

## <a name="see-also"></a>Vedi anche

[Sfruttare i vantaggi del High-Definition del mouse](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)