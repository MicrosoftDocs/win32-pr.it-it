---
description: Il controllo InkEdit consente di raccogliere input penna, riconoscere l'input penna e visualizzare l'input penna come testo.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Informazioni di riferimento sul controllo InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe2aad6b7d8b536f2ede35fd93bd19840e69fc
ms.sourcegitcommit: f8f06d7ad2ff6599e90b0493b355e0c1811d898f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113369313"
---
# <a name="inkedit-control-reference"></a>Informazioni di riferimento sul controllo InkEdit

Il controllo InkEdit consente di raccogliere input penna, riconoscere l'input penna e visualizzare l'input penna come testo. Questo controllo consente di abilitare moduli intelligenti, che migliorano l'accuratezza dell'input di testo.

Questo controllo è un superset del [**controllo RichEdit.**](/windows/desktop/api/richole/nn-richole-iricheditole) Estende il controllo **RichEdit** con la possibilità di acquisire, riconoscere e visualizzare l'input penna.

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

La creazione del controllo InkEdit dietro un controllo trasparente (ad esempio un controllo GroupBox con la proprietà WS EX TRANSPARENT impostata) impedirà a InkEdit di \_ raccogliere input \_ penna.

## <a name="members"></a>Membri



| Enumerazione                                            | Descrizione                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Definisce i valori che specificano se il controllo viene visualizzato flat o 3D.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Definisce valori che specificano se il controllo ha un bordo.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Definisce i valori che impostano l'interesse per un set di movimenti specifici dell'applicazione.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Definisce valori che specificano se una selezione viene visualizzata come input penna o testo.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Definisce valori che specificano se il controllo InkEdit è inattivo, raccogliendo input penna o riconoscendo l'input penna.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Definisce i valori che specificano la modalità di inserimento dell'input penna nel controllo InkEdit.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Definisce i valori che specificano le impostazioni della modalità raccolta per l'input penna disegnato, indipendentemente dal fatto che la raccolta dell'input penna sia disabilitata, che l'input penna sia raccolto o che l'input penna e i movimenti siano raccolti.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Definisce i valori che specificano quale pulsante del mouse è stato premuto.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Definisce i valori che specificano il tipo di puntatore del mouse visualizzato.<br/>                                                                                             |
| [**Mousebutton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Definisce i valori che specificano quale pulsante del mouse è stato premuto.<br/>                                                                                                     |
| [**Controlli ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Definisce i valori che specificano la modalità di visualizzazione delle barre di scorrimento di un controllo InkEdit sullo schermo.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Definisce i valori che specificano l'allineamento del paragrafo rispetto ai margini del controllo InkEdit.<br/>                                                      |



 



| Messaggio di notifica degli eventi                                   | Descrizione                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [TRATTO IECN \_](inkedit-messages--win32-only-.md)            | Questo messaggio viene inviato tramite un messaggio WM \_ NOTIFY al completamento di un tratto (solo Win32).<br/>  |
| [MOVIMENTO IECN \_](inkedit-messages--win32-only-.md)           | Questo messaggio viene inviato tramite un messaggio WM \_ NOTIFY al completamento di un movimento (solo Win32).<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | Questo messaggio viene inviato tramite un messaggio WM \_ NOTIFY quando si verifica il riconoscimento (solo Win32).<br/>     |



 



| Event                                                  | Descrizione                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cambiare**](inkedit-change.md)                       | Si verifica quando il contenuto del controllo o di un valore della proprietà cambia.<br/>                                                                                                              |
| [**Clic**](inkedit-click.md)                         | Si verifica quando si fa clic sul controllo.<br/>                                                                                                                                              |
| [**Dblclick**](inkedit-dblclick.md)                   | Si verifica quando si fa doppio clic sul controllo.<br/>                                                                                                                                       |
| [**Movimento**](inkedit-gesture.md)                     | Si verifica quando viene riconosciuto un movimento dell'applicazione.<br/>                                                                                                                                |
| [**KeyDown**](inkedit-keydown.md)                     | Si verifica quando l'utente preme un tasto mentre il controllo InkEdit ha lo stato attivo.<br/>                                                                                                          |
| [**Keypress**](inkedit-keypress.md)                   | Si verifica quando viene premuto un tasto mentre il controllo InkEdit ha lo stato attivo.<br/>                                                                                                                |
| [**KeyUp**](inkedit-keyup.md)                         | Si verifica quando viene rilasciato un tasto mentre il controllo InkEdit ha lo stato attivo.<br/>                                                                                                               |
| [**Mousedown**](inkedit-mousedown.md)                 | Si verifica quando il puntatore del mouse viene posizionato sul controllo InkEdit e viene premuto un pulsante del mouse.<br/>                                                                                         |
| [**Mousemove**](inkedit-mousemove.md)                 | Si verifica quando il puntatore del mouse viene spostato sul controllo InkEdit.<br/>                                                                                                                 |
| [**Mouseup**](inkedit-mouseup.md)                     | Si verifica quando il puntatore del mouse viene posizionato sul controllo InkEdit e viene rilasciato un pulsante del mouse.<br/>                                                                                        |
| [**Recognitionresult**](inkedit-recognitionresult.md) | Si verifica quando il controllo InkEdit ottiene i risultati manualmente da una chiamata al metodo [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automaticamente dopo l'avvio del timeout di riconoscimento.<br/> |
| [**Selchange**](inkedit-selchange.md)                 | Si verifica quando la selezione dell'input penna all'interno del controllo InkEdit cambia.<br/>                                                                                                             |
| [**infarto**](inkedit-stroke.md)                       | Si verifica quando l'utente disegna un nuovo [**oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in qualsiasi [**oggetto IInkTablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)<br/>                                                 |



 



| Messaggio Get/Set                                               | Descrizione                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EM \_ GETINKMODE](inkedit-messages--win32-only-.md)           | Ottiene la modalità input penna del controllo (solo Win32).<br/>                                                                                                                       |
| [EM \_ SETINKMODE](inkedit-messages--win32-only-.md)           | Imposta la modalità input penna del controllo (solo Win32).<br/>                                                                                                                       |
| [EM \_ GETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Ottiene la modalità di inserimento input penna del controllo (solo Win32).<br/>                                                                                                             |
| [EM \_ SETINKINSERTMODE](inkedit-messages--win32-only-.md)     | Imposta la modalità di inserimento input penna del controllo (solo Win32).<br/>                                                                                                             |
| [EM \_ GETDRAWATTR](inkedit-messages--win32-only-.md)          | Ottiene gli attributi di disegno correnti del controllo (solo Win32).<br/>                                                                                                     |
| [EM \_ SETDRAWATTR](inkedit-messages--win32-only-.md)          | Imposta gli attributi di disegno da utilizzare per la raccolta di input penna futura (solo Win32).<br/>                                                                                           |
| [EM \_ GETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Ottiene il timeout di riconoscimento per il controllo (solo Win32).<br/>                                                                                                           |
| [EM \_ SETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | Imposta il timeout di riconoscimento per il controllo (solo Win32).<br/>                                                                                                           |
| [EM \_ GETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Ottiene lo stato del movimento per il controllo (solo Win32).<br/>                                                                                                                |
| [EM \_ SETGESTURESTATUS](inkedit-messages--win32-only-.md)     | Imposta lo stato del movimento per il controllo (solo Win32).<br/>                                                                                                                |
| [EM \_ GETRECOGNIZER](inkedit-messages--win32-only-.md)        | Ottiene il riconoscimento utilizzato dal controllo (solo Win32).<br/>                                                                                                              |
| [EM \_ SETRECOGNIZER](inkedit-messages--win32-only-.md)        | Imposta il riconoscimento utilizzato dal controllo (solo Win32).<br/>                                                                                                              |
| [EM \_ GETFACTOID](inkedit-messages--win32-only-.md)           | Ottiene il factoid da utilizzare per il riconoscimento (solo Win32).<br/>                                                                                                                |
| [EM \_ SETFACTIOD](inkedit-messages--win32-only-.md)           | Imposta il factoid da usare per il riconoscimento (solo Win32).<br/>                                                                                                                |
| [EM \_ GETSELINK](inkedit-messages--win32-only-.md)            | Ottiene l'input penna nella selezione (solo Win32).<br/>                                                                                                                          |
| [EM \_ SETSELINK](inkedit-messages--win32-only-.md)            | Imposta l'input penna nella selezione (solo Win32).<br/>                                                                                                                          |
| [EM \_ GETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Restituisce l'aspetto corrente dell'input penna nell'intervallo selezionato usando uno dei valori [**dell'enumerazione InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/> |
| [EM \_ SETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | Imposta l'aspetto dell'input penna nell'intervallo selezionato usando uno dei valori [**dell'enumerazione InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/>            |
| [EM \_ GETSTATUS](inkedit-messages--win32-only-.md)            | Ottiene lo stato del controllo (solo Win32).<br/>                                                                                                                         |
| [RICONOSCIMENTO \_ EM](inkedit-messages--win32-only-.md)            | Forza il riconoscimento (solo Win32).<br/>                                                                                                                                     |
| [EM \_ GETMOUSEICON](inkedit-messages--win32-only-.md)         | Ottiene l'icona del mouse (solo Win32).<br/>                                                                                                                                    |
| [EM \_ SETMOUSEICON](inkedit-messages--win32-only-.md)         | Imposta l'icona del mouse (solo Win32).<br/>                                                                                                                                    |
| [EM \_ GETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | Ottiene il puntatore del mouse (solo Win32).<br/>                                                                                                                                 |
| [EM \_ SETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | Imposta il puntatore del mouse solo su Win32.<br/>                                                                                                                                  |
| [EM \_ GETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Ottiene lo stato di se l'input del mouse viene considerato come input penna (solo Win32).<br/>                                                                                        |
| [EM \_ SETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | Imposta lo stato di se l'input del mouse viene considerato come input penna (solo Win32).<br/>                                                                                        |



 



| Metodo                                               | Descrizione                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Ottiene l'interesse del controllo InkEdit in un set noto di movimenti.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Specifica che deve essere eseguito il riconoscimento.<br/>                             |
| [**Aggiorna**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Determina il ridisegno del controllo.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Imposta l'interesse del controllo InkEdit in un set noto di movimenti.<br/> |



 



| Proprietà                                                 | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspetto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Ottiene o imposta un valore che determina se il controllo InkEdit è flat o 3D.<br/>                                                                                      |
| [**Backcolor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Ottiene o imposta il colore di sfondo per il controllo InkEdit.<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Ottiene o imposta un valore che determina se il controllo InkEdit ha un bordo.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Ottiene o imposta un valore che determina se le barre di scorrimento nel controllo InkEdit sono disabilitate.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Ottiene o imposta gli attributi di disegno per l'input penna che deve ancora essere disegnato sul controllo InkEdit.<br/>                                                                                |
| [**Attivato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Ottiene o imposta un valore che determina se il controllo InkEdit può rispondere agli eventi generati dall'utente.<br/>                                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Ottiene o imposta la [costante Factoid](factoid-constants.md) utilizzata da un [**oggetto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) per vincolare la ricerca del risultato del riconoscimento.<br/> |
| [**Carattere**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Ottiene o imposta il tipo di carattere del testo visualizzato dal controllo InkEdit.<br/>                                                                                                       |
| [**Hwnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Ottiene l'handle di finestra a cui è associato il controllo [**InkDisp.**](inkdisp-class.md)<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Ottiene o imposta un valore che specifica la modalità di inserimento dell'input penna nel controllo InkEdit, come testo o come input penna.<br/>                                                                |
| [**Modalità input penna**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Ottiene o imposta un valore che specifica se la raccolta di input penna è disabilitata, se l'input penna viene raccolto o se vengono raccolti input penna e movimenti.<br/>                                               |
| [**Bloccato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Ottiene o imposta un valore che specifica se il controllo InkEdit è di sola lettura o meno.<br/>                                                                                       |
| [**Maxlength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Ottiene o imposta un valore che indica se un controllo InkEdit può contenere un numero massimo di caratteri e, in tal caso, specifica il numero massimo di caratteri.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Ottiene o imposta l'icona del mouse personalizzata corrente.<br/>                                                                                                                                |
| [**Mousepointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo InkEdit.<br/>                                |
| [**Multilinea**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Ottiene o imposta un valore che indica se si tratta di un controllo InkEdit su più righe.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Ottiene o imposta l'intervallo di tempo, in millisecondi, tra l'ultimo [**oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto e l'inizio del riconoscimento del testo.<br/>        |
| [**Riconoscimento**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Ottiene o imposta [**l'oggetto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) da utilizzare per il riconoscimento.<br/>                                                                                   |
| [**BarreScorrimento**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Ottiene o imposta il tipo di barre di scorrimento visualizzate nel controllo InkEdit.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Ottiene o imposta l'allineamento da applicare alla selezione o al punto di inserimento corrente (solo in fase di esecuzione).<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Ottiene o imposta un valore che specifica se lo stile del carattere del testo attualmente selezionato nel controllo InkEdit è in grassetto (solo in fase di esecuzione).<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Ottiene o imposta un valore che indica se il testo nel controllo InkEdit viene visualizzato nella linea di base, come apice o come indice (solo in fase di esecuzione).<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Ottiene o imposta il colore del testo della selezione di testo o del punto di inserimento corrente (solo in fase di esecuzione).<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Ottiene o imposta il nome del tipo di carattere del testo selezionato all'interno del controllo InkEdit (solo in fase di esecuzione).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Ottiene o imposta le dimensioni del carattere del testo selezionato all'interno del controllo InkEdit (solo in fase di esecuzione).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Ottiene o imposta la matrice di oggetti [**InkDisp**](inkdisp-class.md) incorporati (se visualizzati come input penna) contenuti nella selezione corrente.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Ottiene o imposta un valore che consente di modificare l'aspetto della selezione tra input penna e testo.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Ottiene o imposta un valore che specifica se lo stile del carattere del testo attualmente selezionato nel controllo InkEdit è in corsivo (solo in fase di esecuzione).<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Ottiene o imposta il numero di caratteri selezionati nel controllo InkEdit (solo in fase di esecuzione).<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Ottiene o imposta il testo formattato RTF (Rich Text Format) attualmente selezionato nel controllo InkEdit (solo in fase di esecuzione).<br/>                                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Ottiene o imposta il punto iniziale del testo selezionato nella casella di testo (solo in fase di esecuzione).<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Ottiene o imposta il testo selezionato all'interno del controllo InkEdit (solo in fase di esecuzione).<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Ottiene o imposta un valore che specifica se lo stile del carattere del testo attualmente selezionato nel controllo InkEdit è sottolineato (solo in fase di esecuzione).<br/>                            |
| [**Stato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Ottiene un valore che specifica se il controllo InkEdit è inattivo, raccoglie input penna o riconosce l'input penna (solo in fase di esecuzione).<br/>                                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Ottiene o imposta il testo corrente nella casella di testo.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Ottiene o imposta il testo del controllo InkEdit, inclusi tutti i codici RTF.<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Ottiene o imposta un valore che indica se il mouse può essere utilizzato come dispositivo di input.<br/>                                                                                      |

| Struttura                                                                    | Descrizione                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Contiene informazioni su un [**evento Stroke**](inkedit-stroke.md) (solo Win32).<br/> |
| [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Contiene informazioni su un movimento specifico (solo Win32).<br/>                       |
| [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Contiene informazioni su un risultato di riconoscimento (solo Win32).<br/>                     |

## <a name="com-implementation"></a>Implementazione COM

Questo oggetto implementa [l'interfaccia COM IInkEdit.](/windows/win32/api/inked/nn-inked-iinkedit)

## <a name="related-topics"></a>Argomenti correlati

- [**Classe InkOverlay**](inkoverlay-class.md), 
- [Informazioni di riferimento sul controllo InkPicture](inkpicture-control-reference.md)
- [**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
