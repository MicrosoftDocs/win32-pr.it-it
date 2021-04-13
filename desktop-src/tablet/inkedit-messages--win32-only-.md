---
description: Il controllo InkEdit è una classe Super del controllo RichEdit.
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: Messaggi InkEdit (solo Win32)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b403e950ca67523620baab6f90a8fef9a47bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346121"
---
# <a name="inkedit-messages-win32-only"></a>Messaggi InkEdit (solo Win32)

Il controllo [InkEdit](inkedit-control-reference.md) è una classe Super del controllo [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Ogni messaggio **RichEdit** viene passato, direttamente nella maggior parte dei casi, e ha esattamente lo stesso effetto di **RichEdit**. Questo vale anche per i messaggi di notifica degli eventi.

Per inviare questi messaggi, chiamare la funzione SendMessage con i parametri seguenti:



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>LRESULT SendMessage(
  HWND hWnd,      // handle to destination window
  UINT Msg,       // message
  WPARAM wParam,  // first message parameter
  LPARAM lParam   // second message parameter
);</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="message"></a>Message

La finestra padre del controllo [InkEdit](inkedit-control-reference.md) riceve i messaggi di notifica degli eventi tramite il \_ messaggio di notifica WM:


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
| \_GETINKMODE em<br/>           | Ottiene la modalità Inking del controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori definiti nell'enumerazione [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , che specifica se la raccolta di input penna è disabilitata, se l'input penna viene raccolto o se vengono raccolti input penna o movimenti.<br/>                                                                                                                                                                                                                                                         |
| \_SETINKMODE em<br/>           | Imposta la modalità Inking del controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/>*wParam* Specifica uno dei valori dell'enumerazione [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) , che specifica se la raccolta di input penna è disabilitata, se l'input penna viene raccolto o se vengono raccolti input penna o movimenti.<br/>*lParam* Questo parametro non viene utilizzato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Questa operazione deve essere usata solo se EM \_ GetStatus restituisce IES \_ Idle.<br/>                                                                                                               |
| \_GETINKINSERTMODE em<br/>     | Ottiene la modalità di inserimento dell'input penna del controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori dell'enumerazione [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , che specifica se l'input penna viene inserito nel controllo come testo o come input penna.<br/>                                                                                                                                                                                                                                                                                                    |
| \_SETINKINSERTMODE em<br/>     | Imposta la modalità di inserimento dell'input penna del controllo [InkEdit](inkedit-control-reference.md) . L'invio di questo messaggio non ha alcun effetto se utilizzato con qualsiasi sistema operativo installato con Microsoft Windows XP Tablet PC Edition.<br/> Parametri<br/>*wParam* Specifica uno dei valori dell'enumerazione [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) , che specifica se l'input penna viene inserito nel controllo come testo o come input penna.<br/>*lParam* Questo parametro non viene utilizzato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                       |
| \_GETDRAWATTR em<br/>          | Ottiene gli attributi di disegno correnti del controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore (IInkDrawingAttributes \* \* pDrawAttr) per ricevere l'oggetto [**InkDrawingAttributes**](inkdrawingattributes-class.md) corrente.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                |
| \_SETDRAWATTR em<br/>          | Imposta gli attributi di disegno da utilizzare per la raccolta di input penna futura.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore (IInkDrawingAttributes \* pDrawAttr) a un oggetto [**InkDrawingAttributes**](inkdrawingattributes-class.md) .<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                  |
| \_GETRECOTIMEOUT em<br/>       | Ottiene il timeout di riconoscimento, espresso in millisecondi, per il controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce il timeout di riconoscimento, espresso in millisecondi.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_SETRECOTIMEOUT em<br/>       | Imposta il timeout di riconoscimento, espresso in millisecondi, per il controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/>*wParam* Specifica il timeout di riconoscimento, espresso in millisecondi.<br/>*lParam* Questo parametro non viene utilizzato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                                                    |
| \_GETGESTURESTATUS em<br/>     | Ottiene lo stato del movimento per il controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/>*wParam* Specifica il tipo di movimento, come definito nell'enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Questo parametro non viene utilizzato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce **true** se il controllo [InkEdit](inkedit-control-reference.md) sottoscrive il movimento o **false** se il controllo InkEdit non sottoscrive il movimento.<br/>                                                                                                                                                                       |
| \_SETGESTURESTATUS em<br/>     | Imposta lo stato del movimento per il controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/>*wParam* Specifica il tipo di movimento, come definito nell'enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .<br/>*lParam* Specifica **true** se la sottoscrizione del movimento è abilitata o **false** se l'ascolto del movimento non è abilitato.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Questa operazione deve essere usata solo se EM \_ GetStatus restituisce IES \_ Idle.<br/>                                                                                                               |
| getrecognizer EM \_<br/>        | Ottiene il riconoscimento utilizzato dal controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore a un IInkRecognizer \* per ricevere l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) utilizzato dal controllo [InkEdit](inkedit-control-reference.md) .<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                   |
| \_RIconoscitore em<br/>        | Imposta il riconoscimento utilizzato dal controllo [InkEdit](inkedit-control-reference.md) . Se per il controllo [InkEdit viene utilizzato](factoid-constants.md) un controllo oggetto, deve essere riapplicato dopo l'invio del messaggio.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore a un IInkRecognizer \* per impostare l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usato dal controllo [InkEdit](inkedit-control-reference.md) per un uso successivo.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Questa operazione deve essere usata solo se EM \_ GetStatus restituisce IES \_ Idle.<br/> |
| \_GETFACTOID em<br/>           | Ottiene il controllo del controllo da [utilizzare per il](factoid-constants.md) riconoscimento.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore a un BSTR per ricevere la stringa del controllo del controllo.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_SETFACTOID em<br/>           | Imposta il controllo del controllo da [utilizzare per il](factoid-constants.md) riconoscimento.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica il BSTR che contiene la stringa del controllo del controllo.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Questa operazione deve essere usata solo se EM \_ GetStatus restituisce IES \_ Idle.<br/>                                                                                                                                                                                                                                                                          |
| \_GETSELINK em<br/>            | Ottiene l'input penna all'interno della selezione. È necessario riconoscere l'input penna prima di accedervi tramite questo messaggio. Se non viene riconosciuta per prima, EM \_ GETSELINK restituisce sempre zero oggetti [**InkDisp**](inkdisp-class.md) .<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore a una variante per ricevere una matrice sicura per la ricezione di oggetti [**InkDisp**](inkdisp-class.md) all'interno della selezione corrente.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                     |
| \_SETSELINK em<br/>            | Imposta l'input penna nella selezione. L'invio di questo messaggio non ha alcun effetto se utilizzato con qualsiasi sistema operativo installato in Windows XP Tablet PC Edition.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un puntatore a una variante con una matrice sicura di oggetti [**InkDisp**](inkdisp-class.md) per sostituire la selezione corrente.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                     |
| \_GETSELINKDISPLAYMODE em<br/> | Restituisce l'aspetto corrente dell'input penna nell'intervallo selezionato utilizzando uno dei valori dell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori dell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (IDM \_ text o IDM \_ Ink), che specifica il modo in cui una selezione viene visualizzata nel controllo.<br/>                                                                                                                                                                                                                           |
| \_SETSELINKDISPLAYMODE em<br/> | Imposta l'aspetto dell'input penna nell'intervallo selezionato utilizzando uno dei valori dell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica il modo in cui l'input penna viene visualizzato nell'intervallo selezionato, come definito nell'enumerazione [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) .<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore. L'invio di questo messaggio non ha alcun effetto se utilizzato con qualsiasi sistema operativo installato in Windows XP Tablet PC Edition.<br/>                                                                                                   |
| EM \_ GETstatus<br/>            | Ottiene lo stato del controllo [InkEdit](inkedit-control-reference.md) .<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce uno dei valori dell'enumerazione [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) , che specifica se il controllo è inattivo, raccogliendo input penna o riconoscendo l'input penna.<br/>                                                                                                                                                                                                                                                                                                           |
| \_riconoscimento em<br/>            | Forza il riconoscimento.<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_GETMOUSEICON em<br/>         | Ottiene l'icona del mouse.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Specifica un \* puntatore HICON compilato con il HICON [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) corrente. Questo HICON può essere un HICON o un valore **null** .<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                                                                    |
| \_SETMOUSEICON em<br/>         | Imposta l'icona del mouse.<br/> Parametri<br/>*wParam* Specifica un valore BOOLEANo impostato su **true** se il controllo [InkEdit](inkedit-control-reference.md) deve essere proprietario dell'handle HICON o **false** se il controllo InkEdit non deve essere il proprietario dell'handle HICON. Se il controllo InkEdit è proprietario di HICON, viene gestito ed eliminato in modo appropriato il HICON. In caso contrario, il chiamante è proprietario di HICON ed è responsabile dell'eliminazione.<br/>*lParam* Specifica il nuovo valore di HICON. Utilizzare **null** per cancellare il valore. Il valore predefinito è **NULL**.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                |
| \_GETMOUSEPOINTER em<br/>      | Ottiene il puntatore del mouse.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Contiene un \* puntatore InkMousePointer compilato con il valore [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) corrente. Questo comportamento corrisponde alla proprietà **InkCollector:: Get \_ MousePointer** .<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                                            |
| \_SETMOUSEPOINTER em<br/>      | Imposta il puntatore del mouse.<br/> Parametri<br/>*wParam* Questo parametro non viene utilizzato. deve essere 0.<br/>*lParam* Contiene il nuovo valore di [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) , definito nell'enumerazione [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) . Questo comportamento corrisponde alla proprietà **InkCollector::p UT \_ MousePointer** .<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/>                                                                                                                                                                                                                                    |
| \_GETUSEMOUSEFORINPUT em<br/>  | Ottiene lo stato che indica se l'input del mouse viene trattato come input penna.<br/> Parametri<br/> Questo messaggio non ha parametri. *wParam* e *lParam* devono essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 se **false** o 1 se **true**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \_SETUSEMOUSEFORINPUT em<br/>  | Imposta lo stato che indica se l'input del mouse viene trattato come input penna.<br/> Parametri<br/>*wParam* Specifica un valore booleano che determina se trattare l'input del mouse come input penna.<br/>*lParam* Questo parametro non viene utilizzato. deve essere 0.<br/> Valori restituiti:<br/> Questo messaggio restituisce 0 in caso di esito positivo o diverso da zero se si verifica un errore.<br/> Osservazioni:<br/> Questa operazione deve essere usata solo se EM \_ GetStatus restituisce IES \_ Idle.<br/>                                                                                                                                                                                                                                             |



 



| Messaggio di notifica degli eventi         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tratto IECN<br/>            | Notifica alla finestra padre del controllo [InkEdit](inkedit-control-reference.md) che è stato creato un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Questa operazione viene inviata in un \_ messaggio di notifica WM con i parametri seguenti.<br/> Parametri<br/>*wParam* Specifica l'identificatore del controllo che ha inviato il messaggio.<br/>*lParam* Specifica un puntatore alla struttura [**\_ STROKEINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) .<br/> Valori restituiti:<br/> Il client restituisce 0 per accettare il tratto e 1 per annullare il tratto.<br/> |
| IECN \_ movimento<br/>           | Notifica alla finestra padre del controllo [InkEdit](inkedit-control-reference.md) che è stato riconosciuto un movimento. Questa operazione viene inviata in un \_ messaggio di notifica WM con i parametri seguenti.<br/> Parametri<br/>*wParam* Specifica l'identificatore del controllo che ha inviato il messaggio.<br/>*lParam* Specifica un puntatore alla struttura [**\_ GESTUREINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) .<br/> Valori restituiti:<br/> Il client restituisce 0 per accettare il movimento e 1 per annullare il movimento.<br/>                           |
| \_RECOGNITIONRESULT IECN<br/> | Notifica alla finestra padre del controllo [InkEdit](inkedit-control-reference.md) che si è verificato il riconoscimento. Questa operazione viene inviata in un \_ messaggio di notifica WM con i parametri seguenti.<br/> Parametri<br/>*wParam* Specifica l'identificatore del controllo che ha inviato il messaggio.<br/>*lParam* Specifica un puntatore alla struttura [**\_ RECOGNITIONRESULTINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) .<br/> Valori restituiti:<br/> Il client restituisce 0 se elabora il messaggio.<br/>                                  |



 

## <a name="applies-to"></a>Si applica a

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_Struttura GESTUREINFO IEC (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**\_Struttura STROKEINFO IEC (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**\_Struttura RECOGNITIONRESULTINFO IEC (solo Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
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

 

