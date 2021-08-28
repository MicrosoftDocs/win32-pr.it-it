---
description: Il controllo InkEdit è una superclasse del controllo RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: Messaggi InkEdit (solo Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cb1d390bf8e37d6affbbd96c34c53ea889b268
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475037"
---
# <a name="inkedit-messages-win32-only"></a>Messaggi InkEdit (solo Win32)

Il [controllo InkEdit](inkedit-control-reference.md) è una superclasse del [**controllo RichEdit.**](/windows/desktop/api/richole/nn-richole-iricheditole) Ogni **messaggio RichEdit** viene passato direttamente nella maggior parte dei casi e ha esattamente lo stesso effetto di in **RichEdit**. Questo vale anche per i messaggi di notifica degli eventi.

Per inviare questi messaggi, chiamare la funzione SendMessage con i parametri seguenti:




| C++ | 
|-----|
| <pre data-space="preserve"><code>LRESULT SendMessage(  HWND hWnd,      // handle to destination window  UINT Msg,       // message  WPARAM wParam,  // first message parameter  LPARAM lParam   // second message parameter);</code></pre> | 




 

## <a name="message"></a>Message

La finestra padre del controllo [InkEdit](inkedit-control-reference.md) riceve messaggi di notifica degli eventi tramite il messaggio WM \_ NOTIFY:


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| Ottenere/impostare un messaggio                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EM \_ GETINKMODE<br/>           | Ottiene la modalità di input penna del [controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori definiti nell'enumerazione [**InkMode,**](/windows/desktop/api/inked/ne-inked-inkmode) che specifica se la raccolta input penna è disabilitata, se l'input penna viene raccolto o se vengono raccolti input penna e movimenti.<br/>                                                                                                                                                                                                                                                         |
| EM \_ SETINKMODE<br/>           | Imposta la modalità di input penna del [controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/>*wParam* Specifica uno dei valori dell'enumerazione [**InkMode,**](/windows/desktop/api/inked/ne-inked-inkmode) che specifica se la raccolta di input penna è disabilitata, se l'input penna viene raccolto o se vengono raccolti input penna e movimenti.<br/>*lParam* Questo parametro non viene usato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Deve essere usato solo se EM \_ GETSTATUS restituisce IES \_ Idle.<br/>                                                                                                               |
| EM \_ GETINKINSERTMODE<br/>     | Ottiene la modalità di inserimento input penna [del controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori [**dell'enumerazione InkInsertMode,**](/windows/desktop/api/inked/ne-inked-inkinsertmode) che specifica se l'input penna viene inserito nel controllo come testo o come input penna.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETINKINSERTMODE<br/>     | Imposta la modalità di inserimento input penna [del controllo InkEdit.](inkedit-control-reference.md) L'invio di questo messaggio non ha alcun effetto se usato con qualsiasi sistema operativo installato diverso da Microsoft Windows XP Tablet PC Edition.<br/> Parametri<br/>*wParam* Specifica uno dei valori dell'enumerazione [**InkInsertMode,**](/windows/desktop/api/inked/ne-inked-inkinsertmode) che specifica se l'input penna viene inserito nel controllo come testo o come input penna.<br/>*lParam* Questo parametro non viene usato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                       |
| EM \_ GETDRAWATTR<br/>          | Ottiene gli attributi di disegno correnti del [controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore (IInkDrawingAttributes pDrawAttr) per ricevere \* \* [**l'oggetto InkDrawingAttributes**](inkdrawingattributes-class.md) corrente.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                |
| EM \_ SETDRAWATTR<br/>          | Imposta gli attributi di disegno da utilizzare per la raccolta di input penna futura.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore (IInkDrawingAttributes \* pDrawAttr) a un [**oggetto InkDrawingAttributes.**](inkdrawingattributes-class.md)<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                  |
| EM \_ GETRECOTIMEOUT<br/>       | Ottiene il timeout di riconoscimento, in millisecondi, per il [controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce il timeout di riconoscimento, espresso in millisecondi.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ SETRECOTIMEOUT<br/>       | Imposta il timeout di riconoscimento, in millisecondi, per il [controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/>*wParam* Specifica il timeout di riconoscimento, espresso in millisecondi.<br/>*lParam* Questo parametro non viene usato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                                                    |
| EM \_ GETGESTURESTATUS<br/>     | Ottiene lo stato del movimento per [il controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/>*wParam* Specifica il tipo di movimento, come definito [**nell'enumerazione InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)<br/>*lParam* Questo parametro non viene usato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce **TRUE se** il [controllo InkEdit](inkedit-control-reference.md) sottoscrive il movimento o **FALSE** se il controllo InkEdit non sottoscrive il movimento.<br/>                                                                                                                                                                       |
| EM \_ SETGESTURESTATUS<br/>     | Imposta lo stato del movimento per [il controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/>*wParam* Specifica il tipo di movimento, come definito [**nell'enumerazione InkApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)<br/>*lParam* Specifica **TRUE se** la sottoscrizione al movimento è abilitata o **FALSE** se l'ascolto del movimento non è abilitato.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Deve essere usato solo se EM \_ GETSTATUS restituisce IES \_ Idle.<br/>                                                                                                               |
| EM \_ GETRECOGNIZER<br/>        | Ottiene il riconoscitore utilizzato [dal controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore a un oggetto IInkRecognizer per ricevere \* [**l'oggetto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilizzato dal [controllo InkEdit.](inkedit-control-reference.md)<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                   |
| EM \_ SETRECOGNIZER<br/>        | Imposta il riconoscimento utilizzato [dal controllo InkEdit.](inkedit-control-reference.md) Se un [factoid](factoid-constants.md) viene usato per il controllo InkEdit, deve essere riapplicato dopo l'invio del messaggio.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore a un oggetto IInkRecognizer per impostare l'oggetto \* [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilizzato dal controllo [InkEdit](inkedit-control-reference.md) per un uso successivo.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Deve essere usato solo se EM \_ GETSTATUS restituisce IES \_ Idle.<br/> |
| EM \_ GETFACTOID<br/>           | Ottiene [l'oggetto Factoid](factoid-constants.md) da utilizzare per il riconoscimento.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore a un BSTR per ricevere la stringa factoid.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETFACTOID<br/>           | Imposta il [Factoid da](factoid-constants.md) utilizzare per il riconoscimento.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica il BSTR che contiene la stringa factoid.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Deve essere usato solo se EM \_ GETSTATUS restituisce IES \_ Idle.<br/>                                                                                                                                                                                                                                                                          |
| EM \_ GETSELINK<br/>            | Ottiene l'input penna all'interno della selezione. L'input penna deve essere riconosciuto prima dell'accesso tramite questo messaggio. Se non viene riconosciuto per primo, EM \_ GETSELINK restituisce sempre zero [**oggetti InkDisp.**](inkdisp-class.md)<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore a un variant per ricevere una matrice sicura per ricevere [**oggetti InkDisp**](inkdisp-class.md) all'interno della selezione corrente.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                     |
| EM \_ SETSELINK<br/>            | Imposta l'input penna all'interno della selezione. L'invio di questo messaggio non ha alcun effetto se usato con qualsiasi sistema operativo installato diverso da Windows XP Tablet PC Edition.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore a un variant con una matrice sicura di [**oggetti InkDisp**](inkdisp-class.md) per sostituire la selezione corrente.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                     |
| EM \_ GETSELINKDISPLAYMODE<br/> | Restituisce l'aspetto corrente dell'input penna nell'intervallo selezionato usando uno dei valori [**dell'enumerazione InkDisplayMode.**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori dell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (testo IDM o input penna IDM), che specifica come viene visualizzata \_ una selezione nel \_ controllo.<br/>                                                                                                                                                                                                                           |
| EM \_ SETSELINKDISPLAYMODE<br/> | Imposta l'aspetto dell'input penna nell'intervallo selezionato usando uno dei valori [**dell'enumerazione InkDisplayMode.**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica la modalità di visualizzazione dell'input penna nell'intervallo selezionato, come definito [**nell'enumerazione InkDisplayMode.**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore. L'invio di questo messaggio non ha alcun effetto se usato con qualsiasi sistema operativo installato diverso da Windows XP Tablet PC Edition.<br/>                                                                                                   |
| EM \_ GETSTATUS<br/>            | Ottiene lo stato del [controllo InkEdit.](inkedit-control-reference.md)<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori dell'enumerazione [**InkEditStatus,**](/windows/desktop/api/inked/ne-inked-inkeditstatus) che specifica se il controllo è inattivo, raccoglie input penna o riconosce l'input penna.<br/>                                                                                                                                                                                                                                                                                                           |
| RICONOSCIMENTO \_ EM<br/>            | Forza il riconoscimento.<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ GETMOUSEICON<br/>         | Ottiene l'icona del mouse.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Specifica un puntatore HICON \* compilato con l'oggetto [**HICON MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) corrente. HiCON può essere un valore HICON o **NULL.**<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETMOUSEICON<br/>         | Imposta l'icona del mouse.<br/> Parametri<br/>*wParam* Specifica un valore BOOLEAN impostato su **TRUE se** il controllo [InkEdit](inkedit-control-reference.md) deve essere proprietario dell'handle HICON o **FALSE se** il controllo InkEdit non deve essere proprietario dell'handle HICON. Se il controllo InkEdit è proprietario dell'HICON, si occupa e lo elimina in modo appropriato. In caso contrario, il chiamante è proprietario dell'hiCON ed è responsabile dell'eliminazione.<br/>*lParam* Specifica il nuovo valore HICON. Usare **NULL** per cancellare il valore. Il valore predefinito è **NULL**.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                |
| EM \_ GETMOUSEPOINTER<br/>      | Ottiene il puntatore del mouse.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Contiene un puntatore InkMousePointer \* compilato con il valore [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) corrente. Si comporta come la **proprietà InkCollector::get \_ MousePointer.**<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                            |
| EM \_ SETMOUSEPOINTER<br/>      | Imposta il puntatore del mouse.<br/> Parametri<br/>*wParam* Questo parametro non viene usato. deve essere 0.<br/>*lParam* Contiene il nuovo [**valore MousePointer,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) definito nell'enumerazione [**InkMousePointer.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) Si comporta come la proprietà **InkCollector::p ut \_ MousePointer.**<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                    |
| EM \_ GETUSEMOUSEFORINPUT<br/>  | Ottiene lo stato di se l'input del mouse viene considerato come input penna.<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 se **FALSE** o 1 se **TRUE.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETUSEMOUSEFORINPUT<br/>  | Imposta lo stato di se l'input del mouse viene considerato come input penna.<br/> Parametri<br/>*wParam* Specifica un valore booleano che determina se considerare l'input del mouse come input penna.<br/>*lParam* Questo parametro non viene usato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Deve essere usato solo se EM \_ GETSTATUS restituisce IES \_ Idle.<br/>                                                                                                                                                                                                                                             |



 



| Messaggio di notifica degli eventi         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TRATTO IECN \_<br/>            | Notifica alla finestra padre del controllo [InkEdit](inkedit-control-reference.md) che è stato creato [**un oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Viene inviato in un messaggio WM \_ NOTIFY con i parametri seguenti.<br/> Parametri<br/>*wParam* Specifica l'identificatore del controllo che ha inviato il messaggio.<br/>*lParam* Specifica un puntatore alla [**struttura \_ STROKEINFO IEC.**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)<br/> Valori restituiti:<br/> Il client restituisce 0 per accettare il tratto e 1 per annullare il tratto.<br/> |
| MOVIMENTO \_ IECN<br/>           | Notifica alla finestra [padre del controllo InkEdit](inkedit-control-reference.md) che è stato riconosciuto un movimento. Viene inviato in un messaggio WM \_ NOTIFY con i parametri seguenti.<br/> Parametri<br/>*wParam* Specifica l'identificatore del controllo che ha inviato il messaggio.<br/>*lParam* Specifica un puntatore alla [**struttura IEC \_ GESTUREINFO.**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)<br/> Valori restituiti:<br/> Il client restituisce 0 per accettare il movimento e 1 per annullare il movimento.<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | Notifica alla finestra [padre del controllo InkEdit](inkedit-control-reference.md) che si è verificato il riconoscimento. Viene inviato in un messaggio WM \_ NOTIFY con i parametri seguenti.<br/> Parametri<br/>*wParam* Specifica l'identificatore del controllo che ha inviato il messaggio.<br/>*lParam* Specifica un puntatore alla [**struttura \_ IEC RECOGNITIONRESULTINFO.**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)<br/> Valori restituiti:<br/> Il client restituisce 0 se elabora il messaggio.<br/>                                  |



 

## <a name="applies-to"></a>Si applica a

-   [Inkedit](inkedit-control-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Struttura IEC \_ GESTUREINFO (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**Struttura STROKEINFO IEC \_ (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**Struttura IEC \_ RECOGNITIONRESULTINFO (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**Proprietà MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**Enumerazione InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**Enumerazione InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**Enumerazione InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**Interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Classe InkDrawingAttributes**](inkdrawingattributes-class.md)
</dt> <dt>

[**Interfaccia IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**Interfaccia IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Interfaccia IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

