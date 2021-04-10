---
description: Il controllo InkEdit consente di raccogliere input penna, riconoscere input penna e visualizzare input penna come testo.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Riferimento al controllo InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53edfdc6a72a7792c60a6c7c7bf0e38ffc5e0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058199"
---
# <a name="inkedit-control-reference"></a>Riferimento al controllo InkEdit

Il controllo InkEdit consente di raccogliere input penna, riconoscere input penna e visualizzare input penna come testo. Questo controllo consente di abilitare i form intelligenti, che migliorano l'accuratezza dell'input di testo.

Questo controllo è un superset del controllo [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Estende il controllo **RichEdit** con la possibilità di acquisire, riconoscere e visualizzare input penna.

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

La creazione del controllo InkEdit dietro un controllo trasparente, ad esempio un GroupBox con il \_ set di proprietà WS ex \_ trasparente, impedisce a InkEdit di raccogliere input penna.

## <a name="members"></a>Membri



| Enumerazione                                            | Descrizione                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Definisce i valori che specificano se il controllo appare flat o 3D.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Definisce i valori che specificano se il controllo ha un bordo.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Definisce i valori che impostano l'interesse in un set di movimenti specifici dell'applicazione.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Definisce i valori che specificano se una selezione viene visualizzata come input penna o testo.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Definisce valori che specificano se il controllo InkEdit è inattivo, raccogliendo input penna o riconoscendo l'input penna.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Definisce i valori che specificano la modalità di inserimento dell'input penna sul controllo InkEdit.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Definisce i valori che specificano le impostazioni della modalità di raccolta per input penna, se la raccolta di input penna è disabilitata, l'input penna viene raccolto o vengono raccolti input penna e movimenti.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Definisce i valori che specificano quale pulsante del mouse è stato premuto.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Definisce i valori che specificano il tipo di puntatore del mouse visualizzato.<br/>                                                                                             |
| [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Definisce i valori che specificano quale pulsante del mouse è stato premuto.<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Definisce i valori che specificano la modalità di visualizzazione delle barre di scorrimento di un controllo InkEdit sullo schermo.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Definisce i valori che specificano l'allineamento del paragrafo rispetto ai margini del controllo InkEdit.<br/>                                                      |



 



| Messaggio di notifica degli eventi                                   | Descrizione                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [\_tratto IECN](inkedit-messages--win32-only-.md)            | Questo messaggio viene inviato tramite un \_ messaggio di notifica WM quando un tratto viene completato (solo Win32).<br/>  |
| [IECN \_ movimento](inkedit-messages--win32-only-.md)           | Questo messaggio viene inviato tramite un \_ messaggio di notifica WM quando viene completato un movimento (solo Win32).<br/> |
| [\_RECOGNITIONRESULT IECN](inkedit-messages--win32-only-.md) | Questo messaggio viene inviato tramite un \_ messaggio di notifica WM quando si verifica il riconoscimento (solo Win32).<br/>     |



 



| Event                                                  | Descrizione                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modificare**](inkedit-change.md)                       | Si verifica in seguito alla modifica del contenuto del controllo o del valore di una proprietà.<br/>                                                                                                              |
| [**Clic**](inkedit-click.md)                         | Si verifica quando si fa clic sul controllo.<br/>                                                                                                                                              |
| [**DblClick**](inkedit-dblclick.md)                   | Si verifica quando si fa doppio clic sul controllo.<br/>                                                                                                                                       |
| [**Movimento**](inkedit-gesture.md)                     | Si verifica quando viene riconosciuto un movimento dell'applicazione.<br/>                                                                                                                                |
| [**KeyDown**](inkedit-keydown.md)                     | Si verifica quando l'utente preme un tasto mentre il controllo InkEdit dispone dello stato attivo.<br/>                                                                                                          |
| [**KeyPress**](inkedit-keypress.md)                   | Si verifica quando viene premuto un tasto mentre il controllo InkEdit dispone dello stato attivo.<br/>                                                                                                                |
| [**KeyUp**](inkedit-keyup.md)                         | Si verifica quando viene rilasciato un tasto mentre il controllo InkEdit dispone dello stato attivo.<br/>                                                                                                               |
| [**MouseDown**](inkedit-mousedown.md)                 | Si verifica quando il puntatore del mouse si trova sul controllo InkEdit e viene premuto un pulsante del mouse.<br/>                                                                                         |
| [**MouseMove**](inkedit-mousemove.md)                 | Si verifica quando il puntatore del mouse viene spostato sul controllo InkEdit.<br/>                                                                                                                 |
| [**MouseUp**](inkedit-mouseup.md)                     | Si verifica quando il puntatore del mouse si trova sul controllo InkEdit e viene rilasciato un pulsante del mouse.<br/>                                                                                        |
| [**RecognitionResult**](inkedit-recognitionresult.md) | Si verifica quando il controllo InkEdit ottiene manualmente i risultati da una chiamata al metodo [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automaticamente dopo che il timeout di riconoscimento è stato attivato.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Si verifica quando la selezione dell'input penna all'interno del controllo InkEdit viene modificata.<br/>                                                                                                             |
| [**Stroke**](inkedit-stroke.md)                       | Si verifica quando l'utente disegna un nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in un oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .<br/>                                                 |



 



| Ottenere/impostare un messaggio                                               | Descrizione                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_GETINKMODE em](inkedit-messages--win32-only-.md)           | Ottiene la modalità input penna del controllo (solo Win32).<br/>                                                                                                                       |
| [\_SETINKMODE em](inkedit-messages--win32-only-.md)           | Imposta la modalità input penna del controllo (solo Win32).<br/>                                                                                                                       |
| [\_GETINKINSERTMODE em](inkedit-messages--win32-only-.md)     | Ottiene la modalità di inserimento dell'input penna del controllo (solo Win32).<br/>                                                                                                             |
| [\_SETINKINSERTMODE em](inkedit-messages--win32-only-.md)     | Imposta la modalità di inserimento dell'input penna del controllo (solo Win32).<br/>                                                                                                             |
| [\_GETDRAWATTR em](inkedit-messages--win32-only-.md)          | Ottiene gli attributi di disegno correnti del controllo (solo Win32).<br/>                                                                                                     |
| [\_SETDRAWATTR em](inkedit-messages--win32-only-.md)          | Imposta gli attributi di disegno da utilizzare per la raccolta di input penna futura (solo Win32).<br/>                                                                                           |
| [\_GETRECOTIMEOUT em](inkedit-messages--win32-only-.md)       | Ottiene il timeout di riconoscimento per il controllo (solo Win32).<br/>                                                                                                           |
| [\_SETRECOTIMEOUT em](inkedit-messages--win32-only-.md)       | Imposta il timeout di riconoscimento per il controllo (solo Win32).<br/>                                                                                                           |
| [\_GETGESTURESTATUS em](inkedit-messages--win32-only-.md)     | Ottiene lo stato del movimento per il controllo (solo Win32).<br/>                                                                                                                |
| [\_SETGESTURESTATUS em](inkedit-messages--win32-only-.md)     | Imposta lo stato del movimento per il controllo (solo Win32).<br/>                                                                                                                |
| [getrecognizer EM \_](inkedit-messages--win32-only-.md)        | Ottiene il riconoscimento utilizzato dal controllo (solo Win32).<br/>                                                                                                              |
| [\_RIconoscitore em](inkedit-messages--win32-only-.md)        | Imposta il riconoscimento utilizzato dal controllo (solo Win32).<br/>                                                                                                              |
| [\_GETFACTOID em](inkedit-messages--win32-only-.md)           | Ottiene il controllo del controllo da utilizzare per il riconoscimento (solo Win32).<br/>                                                                                                                |
| [\_SETFACTIOD em](inkedit-messages--win32-only-.md)           | Imposta il controllo del controllo da utilizzare per il riconoscimento (solo Win32).<br/>                                                                                                                |
| [\_GETSELINK em](inkedit-messages--win32-only-.md)            | Ottiene l'input penna nella selezione (solo Win32).<br/>                                                                                                                          |
| [\_SETSELINK em](inkedit-messages--win32-only-.md)            | Imposta l'input penna nella selezione (solo Win32).<br/>                                                                                                                          |
| [\_GETSELINKDISPLAYMODE em](inkedit-messages--win32-only-.md) | Restituisce l'aspetto corrente dell'input penna nell'intervallo selezionato utilizzando uno dei valori dell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/> |
| [\_SETSELINKDISPLAYMODE em](inkedit-messages--win32-only-.md) | Imposta l'aspetto dell'input penna nell'intervallo selezionato utilizzando uno dei valori dell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (solo Win32).<br/>            |
| [EM \_ GETstatus](inkedit-messages--win32-only-.md)            | Ottiene lo stato del controllo (solo Win32).<br/>                                                                                                                         |
| [\_riconoscimento em](inkedit-messages--win32-only-.md)            | Forza il riconoscimento (solo Win32).<br/>                                                                                                                                     |
| [\_GETMOUSEICON em](inkedit-messages--win32-only-.md)         | Ottiene l'icona del mouse (solo Win32).<br/>                                                                                                                                    |
| [\_SETMOUSEICON em](inkedit-messages--win32-only-.md)         | Imposta l'icona del mouse (solo Win32).<br/>                                                                                                                                    |
| [\_GETMOUSEPOINTER em](inkedit-messages--win32-only-.md)      | Ottiene il puntatore del mouse (solo Win32).<br/>                                                                                                                                 |
| [\_SETMOUSEPOINTER em](inkedit-messages--win32-only-.md)      | Imposta solo il puntatore del mouse su Win32).<br/>                                                                                                                                  |
| [\_GETUSEMOUSEFORINPUT em](inkedit-messages--win32-only-.md)  | Ottiene lo stato che indica se l'input del mouse viene trattato come input penna (solo Win32).<br/>                                                                                        |
| [\_SETUSEMOUSEFORINPUT em](inkedit-messages--win32-only-.md)  | Imposta lo stato che indica se l'input del mouse viene trattato come input penna (solo Win32).<br/>                                                                                        |



 



| Metodo                                               | Descrizione                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Ottiene l'interesse del controllo InkEdit in un set di movimenti noto.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Specifica che deve essere eseguito il riconoscimento.<br/>                             |
| [**Aggiorna**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Consente di ricreare il controllo.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Imposta l'interesse del controllo InkEdit in un set di movimenti noto.<br/> |



 



| Proprietà                                                 | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspetto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Ottiene o imposta un valore che determina se il controllo InkEdit viene visualizzato come flat o 3D.<br/>                                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Ottiene o imposta il colore di sfondo per il controllo InkEdit.<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Ottiene o imposta un valore che determina se il controllo InkEdit dispone di un bordo.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Ottiene o imposta un valore che determina se le barre di scorrimento nel controllo InkEdit sono disabilitate.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Ottiene o imposta gli attributi di disegno per l'input penna ancora da disegnare sul controllo InkEdit.<br/>                                                                                |
| [**Abilitato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Ottiene o imposta un valore che determina se il controllo InkEdit può rispondere agli eventi generati dall'utente.<br/>                                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Ottiene o [imposta la costante del controllo del controllo](factoid-constants.md) utilizzata da un oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) per limitare la ricerca del risultato del riconoscimento.<br/> |
| [**Carattere**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Ottiene o imposta il tipo di carattere del testo visualizzato dal controllo InkEdit.<br/>                                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Ottiene l'handle di finestra a cui è associato il controllo [**InkDisp**](inkdisp-class.md) .<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Ottiene o imposta un valore che specifica la modalità di inserimento dell'input penna sul controllo InkEdit, come testo o come input penna.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Ottiene o imposta un valore che specifica se la raccolta di input penna è disabilitata, l'input penna viene raccolto o viene raccolto input penna e movimenti.<br/>                                               |
| [**Bloccato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Ottiene o imposta un valore che specifica se il controllo InkEdit è di sola lettura o meno.<br/>                                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Ottiene o imposta un valore che indica se un controllo InkEdit può conservare un numero massimo di caratteri e, in tal caso, specifica il numero massimo di caratteri.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Ottiene o imposta l'icona del mouse personalizzata corrente.<br/>                                                                                                                                |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo InkEdit.<br/>                                |
| [**MultiLine**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Ottiene o imposta un valore che indica se si tratta di un controllo InkEdit su più righe.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Ottiene o imposta il periodo di tempo, in millisecondi, tra l'ultimo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto e l'inizio del riconoscimento del testo.<br/>        |
| [**Sistema di riconoscimento**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Ottiene o imposta l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) da utilizzare per il riconoscimento.<br/>                                                                                   |
| [**BarreScorrimento**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Ottiene o imposta il tipo di barre di scorrimento visualizzate nel controllo InkEdit.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Ottiene o imposta l'allineamento da applicare alla selezione o al punto di inserimento corrente (solo in fase di esecuzione).<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Ottiene o imposta un valore che specifica se lo stile del tipo di carattere del testo attualmente selezionato nel controllo InkEdit è in grassetto (solo in fase di esecuzione).<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Ottiene o imposta un valore che indica se il testo nel controllo InkEdit viene visualizzato nella linea di base, come apice o come indice (solo in fase di esecuzione).<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Ottiene o imposta il colore del testo della selezione di testo o del punto di inserimento corrente (solo in fase di esecuzione).<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Ottiene o imposta il nome del tipo di carattere del testo selezionato all'interno del controllo InkEdit (solo in fase di esecuzione).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Ottiene o imposta la dimensione del carattere del testo selezionato all'interno del controllo InkEdit (solo in fase di esecuzione).<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Ottiene o imposta la matrice di oggetti [**InkDisp**](inkdisp-class.md) incorporati (se visualizzati come input penna) contenuti nella selezione corrente.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Ottiene o imposta un valore che consente di alternare l'aspetto della selezione tra input penna e testo.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Ottiene o imposta un valore che specifica se lo stile del tipo di carattere del testo attualmente selezionato nel controllo InkEdit è in corsivo (solo in fase di esecuzione).<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Ottiene o imposta il numero di caratteri selezionati nel controllo InkEdit (solo in fase di esecuzione).<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Ottiene o imposta il testo formattato RTF (Rich Text Format) attualmente selezionato nel controllo InkEdit (solo in fase di esecuzione).<br/>                                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Ottiene o imposta il punto iniziale del testo selezionato nella casella di testo (solo in fase di esecuzione).<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Ottiene o imposta il testo selezionato all'interno del controllo InkEdit (solo in fase di esecuzione).<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Ottiene o imposta un valore che specifica se lo stile del tipo di carattere del testo attualmente selezionato nel controllo InkEdit è sottolineato (solo in fase di esecuzione).<br/>                            |
| [**Stato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Ottiene un valore che specifica se il controllo InkEdit è inattivo, raccogliendo input penna o riconoscendo l'input penna (solo in fase di esecuzione).<br/>                                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Ottiene o imposta il testo corrente nella casella di testo.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Ottiene o imposta il testo del controllo InkEdit, inclusi tutti i codici RTF.<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Ottiene o imposta un valore che indica se il mouse può essere utilizzato come dispositivo di input.<br/>                                                                                      |



 



| Struttura                                                                    | Descrizione                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_STROKEINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Contiene informazioni su un evento [**Stroke**](inkedit-stroke.md) (solo Win32).<br/> |
| [**\_GESTUREINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Contiene informazioni su un movimento specifico (solo Win32).<br/>                       |
| [**\_RECOGNITIONRESULTINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Contiene informazioni su un risultato del riconoscimento (solo Win32).<br/>                     |



 

## <a name="com-implementation"></a>Implementazione COM

Questo oggetto implementa l'interfaccia com **IInkEdit** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> <dt>

[Riferimento al controllo InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

