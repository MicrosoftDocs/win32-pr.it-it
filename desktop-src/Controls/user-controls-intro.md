---
title: Controlli personalizzati
description: Questa sezione contiene informazioni sui controlli personalizzati o definiti dall'applicazione.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82ed9394ec06257e524153b86ef487f4507f35b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118483"
---
# <a name="custom-controls"></a>Controlli personalizzati

Questa sezione contiene informazioni sui controlli personalizzati o definiti dall'applicazione.

Vengono illustrati gli argomenti seguenti.

-   [Creazione di controlli Owner-Drawn](#creating-owner-drawn-controls)
-   [Sottoclasse della classe della finestra di un controllo esistente](#subclassing-the-window-class-of-an-existing-control)
-   [Implementazione di una classe Application-Defined Window](#implementing-an-application-defined-window-class)
-   [Invio di notifiche da un controllo](#sending-notifications-from-a-control)
-   [Accessibilità](#accessibility)
-   [Argomenti correlati](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Creazione di controlli Owner-Drawn

I pulsanti, i menu, i controlli di testo statici, le caselle di riepilogo e le caselle combinate possono essere creati con un flag di stile disegnato dal proprietario. Quando un controllo ha lo stile disegnato dal proprietario, il sistema gestisce l'interazione dell'utente con il controllo come di consueto, eseguendo attività come il rilevamento quando un utente sceglie un pulsante e invia una notifica al proprietario dell'evento. Tuttavia, poiché il controllo è creato dal proprietario, la finestra padre del controllo è responsabile dell'aspetto visivo del controllo. La finestra padre riceve un messaggio ogni volta che è necessario disegnare il controllo.

Per i pulsanti e i controlli di testo statici, lo stile disegnato dal proprietario influiscono sul modo in cui il sistema disegna l'intero controllo. Per le caselle di riepilogo e le caselle combinate, la finestra padre disegna gli elementi all'interno del controllo e il controllo disegna il proprio contorno. Ad esempio, un'applicazione può personalizzare una casella di riepilogo in modo da visualizzare una piccola bitmap accanto a ogni elemento dell'elenco.

Nell'esempio di codice seguente viene illustrato come creare un controllo testo statico creato dal proprietario. Si supponga che Unicode sia definito.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



Nell'esempio seguente, nella procedura della finestra di dialogo che contiene il controllo creato nell'esempio precedente, il messaggio [**WM \_ DrawItem**](wm-drawitem.md) viene gestito visualizzando il testo in un colore personalizzato, usando il tipo di carattere predefinito. Si noti che non è necessario chiamare [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) quando si gestisce **WM \_ DrawItem**.


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



Per ulteriori informazioni sui controlli creati dal proprietario, vedere [creazione di una casella di riepilogo creata dal proprietario](using-list-boxes.md) e [caselle combinate create](about-combo-boxes.md)dal proprietario.

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Sottoclasse della classe della finestra di un controllo esistente

La creazione di una sottoclasse di un controllo esistente è un altro modo per creare un controllo personalizzato. La procedura di sottoclasse può modificare i comportamenti selezionati del controllo elaborando i messaggi che interessano i comportamenti selezionati. Tutti gli altri messaggi passano alla routine della finestra originale per il controllo. Ad esempio, un'applicazione può visualizzare una piccola bitmap accanto al testo in un controllo di sola lettura e di modifica a riga singola eseguendo la sottoclasse del controllo ed elaborando il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . Per ulteriori informazioni, vedere [informazioni sulle routine della finestra e sui controlli di](/windows/desktop/winmsg/about-window-procedures) [sottoclasse](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementazione di una classe Application-Defined Window

Per creare un controllo non basato in modo esplicito su un controllo esistente, l'applicazione deve creare e registrare una classe di finestra. Il processo per la registrazione di una classe di finestra definita dall'applicazione per un controllo personalizzato equivale alla registrazione di una classe per una finestra ordinaria. Per creare un controllo personalizzato, specificare il nome della classe della finestra nella funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o in un modello di finestra di dialogo. Ogni classe deve avere un nome univoco, una routine della finestra corrispondente e altre informazioni.

Come minimo, la routine della finestra Disegna il controllo. Se un'applicazione utilizza il controllo per consentire all'utente di immettere informazioni sul tipo, la procedura della finestra elabora anche i messaggi di input dalla tastiera e il mouse e invia messaggi di notifica alla finestra padre. Inoltre, se il controllo supporta i messaggi di controllo, la routine della finestra elabora i messaggi inviati dalla finestra padre o da altre finestre. I controlli, ad esempio, elaborano spesso il messaggio [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) inviato da finestre di dialogo per indicare a una finestra di dialogo di elaborare l'input da tastiera in un determinato modo.

La routine della finestra per un controllo definito dall'applicazione deve elaborare qualsiasi messaggio di controllo predefinito nella tabella seguente se il messaggio influiscono sul funzionamento del controllo.



| Message                                          | Recommendation                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETDLGCODE WM**](/windows/desktop/dlgbox/wm-getdlgcode)       | Elaborare se il controllo Usa i tasti INVIO, ESC, TAB o freccia. La funzione [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) Invia questo messaggio ai controlli in una finestra di dialogo per determinare se elaborare le chiavi o passarle al controllo. |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)             | Elabora se viene elaborato anche il messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) .                                                                                                                                                                  |
| [**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)             | Elaborare se il testo del controllo non è uguale al titolo specificato dalla funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**\_GETTEXTLENGTH WM**](/windows/desktop/winmsg/wm-gettextlength) | Elaborare se il testo del controllo non è uguale al titolo specificato dalla funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**\_KILLFOCUS WM**](/windows/desktop/inputdev/wm-killfocus)       | Elabora se il controllo Visualizza un accento circonflesso, un rettangolo di attivazione o un altro elemento per indicare che ha lo stato attivo per l'input.                                                                                                                            |
| [**\_stato attivo WM**](/windows/desktop/inputdev/wm-setfocus)         | Elabora se il controllo Visualizza un accento circonflesso, un rettangolo di attivazione o un altro elemento per indicare che ha lo stato attivo per l'input.                                                                                                                            |
| [**\_testo WM**](/windows/desktop/winmsg/wm-settext)             | Elaborare se il testo del controllo non è uguale al titolo specificato dalla funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)             | Elaborare se il controllo Visualizza il testo. Questo messaggio viene inviato dal sistema durante la creazione di una finestra di dialogo con lo \_ stile DS sefont.                                                                                                                  |



 

I messaggi di controllo definiti dall'applicazione sono specifici del controllo specificato e devono essere inviati in modo esplicito al controllo tramite una funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) . Il valore numerico per ogni messaggio deve essere univoco e non deve essere in conflitto con i valori di altri messaggi della finestra. Per assicurarsi che i valori dei messaggi definiti dall'applicazione non siano in conflitto, un'applicazione deve creare ogni valore aggiungendo un numero univoco al valore [**\_ utente WM**](/windows/desktop/winmsg/wm-user) .

## <a name="sending-notifications-from-a-control"></a>Invio di notifiche da un controllo

I controlli personalizzati potrebbero essere necessari per inviare notifiche di eventi alla finestra padre in modo che l'applicazione host possa rispondere a questi eventi. Ad esempio, una visualizzazione elenco personalizzata può inviare una notifica quando l'utente seleziona un elemento e un'altra notifica quando si fa doppio clic su un elemento.

Le notifiche vengono inviate come i messaggi [**WM \_ Command**](/windows/desktop/menurc/wm-command) o [**WM \_ Notify**](wm-notify.md) . **WM \_** I messaggi di notifica contengono più informazioni rispetto ai messaggi di **\_ comando WM** .

L'identificatore di controllo è un numero univoco usato dall'applicazione per identificare il controllo che invia il messaggio. L'applicazione imposta l'identificatore per un controllo quando crea il controllo. Tramite l'applicazione viene specificato l'identificatore nel parametro *HMENU* della funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o nel membro **ID** della struttura [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) .

Poiché il controllo stesso non imposta l'identificatore del controllo, il controllo deve recuperare l'identificatore prima di poter inviare i messaggi di notifica. Un controllo deve usare la funzione [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) per recuperare il proprio identificatore del controllo. Sebbene l'identificatore di controllo venga specificato come handle di menu quando viene creato il controllo, non è possibile utilizzare la funzione [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) per recuperare l'identificatore. In alternativa, un controllo può recuperare l'identificatore dal membro **HMENU** nella struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) durante l'elaborazione del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) .

Gli esempi seguenti, in cui *hwndControl* è l'handle della finestra di controllo e CN \_ VALUECHANGED è una definizione di notifica personalizzata, mostrano le due modalità di invio di una notifica specifica del controllo.


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



Si noti che la struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) può far parte di una struttura più ampia definita dal controllo che contiene informazioni aggiuntive. Nell'esempio, i valori vecchi e nuovi del controllo potrebbero essere contenuti in questa struttura. Queste strutture estese vengono usate con molte notifiche standard. ad esempio, vedere [LVN \_ INSERTITEM](lvn-insertitem.md), che usa la struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .

## <a name="accessibility"></a>Accessibilità

Tutti i controlli comuni supportano Microsoft Active Accessibility (MSAA), che consente l'accesso a livello di codice alle applicazioni tecnologiche accessibili, ad esempio i lettori dello schermo. MSAA consente inoltre l'automazione dell'interfaccia utente, una tecnologia più recente, per interagire con i controlli.

I controlli personalizzati devono implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (per supportare MSAA) o le interfacce di automazione interfaccia utente o entrambi. In caso contrario, i prodotti con tecnologia accessibile potranno ottenere solo informazioni molto limitate sulla finestra di controllo, non avranno accesso alle proprietà del controllo e non saranno in grado di attivare eventi nel controllo.

Per altre informazioni su come rendere accessibile il controllo, vedere [API di automazione di Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Riferimento al controllo generale](common-control-reference.md)
</dt> <dt>

[Personalizzazione dell'aspetto di un controllo mediante il progetto personalizzato](custom-draw.md)
</dt> <dt>

[Messaggi di controllo](control-messages.md)
</dt> <dt>

[Uso di stili di visualizzazione con controlli Owner-Drawn](using-visual-styles.md)
</dt> </dl>

 

 