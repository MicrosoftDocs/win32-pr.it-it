---
title: Controlli personalizzati
description: Questa sezione contiene informazioni sui controlli definiti dall'applicazione o personalizzati.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d1a31a44f1f71d99088f7729c2de6d5fdb597e14507f5f994dfaca1b96613d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059711"
---
# <a name="custom-controls"></a>Controlli personalizzati

Questa sezione contiene informazioni sui controlli definiti dall'applicazione o personalizzati.

Vengono illustrati gli argomenti seguenti.

-   [Creazione di Owner-Drawn personalizzati](#creating-owner-drawn-controls)
-   [Sottoclasse della classe Window di un controllo esistente](#subclassing-the-window-class-of-an-existing-control)
-   [Implementazione di una Application-Defined finestra personalizzata](#implementing-an-application-defined-window-class)
-   [Invio di notifiche da un controllo](#sending-notifications-from-a-control)
-   [Accessibilità](#accessibility)
-   [Argomenti correlati](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Creazione di Owner-Drawn personalizzati

È possibile creare pulsanti, menu, controlli di testo statico, caselle di riepilogo e caselle combinate con un flag di stile creato dal proprietario. Quando un controllo ha lo stile disegnato dal proprietario, il sistema gestisce l'interazione dell'utente con il controllo come di consueto, eseguendo attività come il rilevamento del momento in cui un utente ha scelto un pulsante e notificando al proprietario del pulsante l'evento. Tuttavia, poiché il controllo è disegnato dal proprietario, la finestra padre del controllo è responsabile dell'aspetto visivo del controllo. La finestra padre riceve un messaggio ogni volta che è necessario disegnare il controllo.

Per i pulsanti e i controlli di testo statico, lo stile disegnato dal proprietario influisce sul modo in cui il sistema disegna l'intero controllo. Per le caselle di riepilogo e le caselle combinate, la finestra padre disegna gli elementi all'interno del controllo e il controllo disegna il proprio contorno. Ad esempio, un'applicazione può personalizzare una casella di riepilogo in modo da visualizzare una piccola bitmap accanto a ogni elemento dell'elenco.

Nell'esempio di codice seguente viene illustrato come creare un controllo di testo statico creato dal proprietario. Si supponga che sia definito Unicode.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



Nell'esempio seguente, dalla routine della finestra per la finestra di dialogo che contiene il controllo creato nell'esempio precedente, il messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) viene gestito visualizzando il testo con un colore personalizzato, usando il tipo di carattere predefinito. Si noti che non è necessario chiamare [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) ed [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) quando si gestisce **WM \_ DRAWITEM.**


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



Per altre informazioni sui controlli disegnati dal proprietario, vedere [Creazione di](using-list-boxes.md) una casella di riepilogo disegnata dal proprietario e Caselle combinate [disegnate dal proprietario.](about-combo-boxes.md)

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Sottoclasse della classe Window di un controllo esistente

La creazione di una sottoclasse di un controllo esistente è un altro modo per creare un controllo personalizzato. La routine della sottoclasse può modificare i comportamenti selezionati del controllo elaborando i messaggi che influiscono sui comportamenti selezionati. Tutti gli altri messaggi passano alla routine della finestra originale per il controllo. Ad esempio, un'applicazione può visualizzare una piccola bitmap accanto al testo in un controllo di modifica a riga singola di sola lettura sottoclassando il controllo ed elaborando il [**messaggio WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Per altre informazioni, vedere [About Window Procedures](/windows/desktop/winmsg/about-window-procedures) and [Subclassing Controls](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementazione di una Application-Defined finestra personalizzata

Per creare un controllo non basato in modo esplicito su un controllo esistente, l'applicazione deve creare e registrare una classe finestra. Il processo per la registrazione di una classe di finestra definita dall'applicazione per un controllo personalizzato è identico a quello per la registrazione di una classe per una finestra normale. Per creare un controllo personalizzato, specificare il nome della classe della finestra nella [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o in un modello di finestra di dialogo. Ogni classe deve avere un nome univoco, una routine della finestra corrispondente e altre informazioni.

Come minimo, la routine della finestra disegna il controllo. Se un'applicazione usa il controllo per consentire all'utente di digitare informazioni, la routine della finestra elabora anche i messaggi di input dalla tastiera e dal mouse e invia messaggi di notifica alla finestra padre. Inoltre, se il controllo supporta i messaggi di controllo, la routine della finestra elabora i messaggi inviati dalla finestra padre o da altre finestre. Ad esempio, i controlli spesso elaborano il messaggio [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) inviato dalle finestre di dialogo per indirizzare una finestra di dialogo all'elaborazione dell'input da tastiera in un determinato modo.

La routine della finestra per un controllo definito dall'applicazione deve elaborare qualsiasi messaggio di controllo predefinito nella tabella seguente se il messaggio influisce sul funzionamento del controllo.



| Message                                          | Recommendation                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)       | Elaborare se il controllo usa INVIO, ESC, TAB o i tasti di direzione. La [**funzione IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) invia questo messaggio ai controlli in una finestra di dialogo per determinare se elaborare i tasti o passarli al controllo. |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)             | Elaborare se viene elaborato anche il messaggio [**\_ WM SETFONT.**](/windows/desktop/winmsg/wm-setfont)                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)             | Elaborare se il testo del controllo non corrisponde al titolo specificato dalla [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) | Elaborare se il testo del controllo non corrisponde al titolo specificato dalla [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)       | Elaborare se il controllo visualizza un punto di inserimento, un rettangolo di attivazione o un altro elemento per indicare che ha lo stato attivo per l'input.                                                                                                                            |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)         | Elaborare se il controllo visualizza un punto di inserimento, un rettangolo di attivazione o un altro elemento per indicare che ha lo stato attivo per l'input.                                                                                                                            |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)             | Elaborare se il testo del controllo non corrisponde al titolo specificato dalla [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)             | Elaborare se il controllo visualizza testo. Il sistema invia questo messaggio durante la creazione di una finestra di dialogo con lo stile \_ DS SETFONT.                                                                                                                  |



 

I messaggi di controllo definiti dall'applicazione sono specifici del controllo specificato e devono essere inviati in modo esplicito al controllo tramite una funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) Il valore numerico per ogni messaggio deve essere univoco e non deve essere in conflitto con i valori di altri messaggi finestra. Per garantire che i valori dei messaggi definiti dall'applicazione non siano in conflitto, un'applicazione deve creare ogni valore aggiungendo un numero univoco al [**valore WM \_ USER.**](/windows/desktop/winmsg/wm-user)

## <a name="sending-notifications-from-a-control"></a>Invio di notifiche da un controllo

I controlli personalizzati potrebbero essere necessari per inviare notifiche di eventi alla finestra padre in modo che l'applicazione host possa rispondere a questi eventi. Ad esempio, una visualizzazione elenco personalizzata potrebbe inviare una notifica quando l'utente seleziona un elemento e un'altra notifica quando si fa doppio clic su un elemento.

Le notifiche vengono inviate [**come messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) [**o WM \_ NOTIFY.**](wm-notify.md) **WM \_ I messaggi NOTIFY** hanno più informazioni rispetto ai **messaggi WM \_ COMMAND.**

L'identificatore di controllo è un numero univoco utilizzato dall'applicazione per identificare il controllo che invia il messaggio. L'applicazione imposta l'identificatore per un controllo quando crea il controllo. L'applicazione specifica l'identificatore nel parametro *hMenu* della [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o nel **membro id** della [**struttura DLGITEMTEMPLATEEX.**](/windows/desktop/dlgbox/dlgitemtemplateex)

Poiché il controllo stesso non imposta l'identificatore del controllo, il controllo deve recuperare l'identificatore prima di poter inviare messaggi di notifica. Un controllo deve usare la [**funzione GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) per recuperare il proprio identificatore di controllo. Anche se l'identificatore del controllo viene specificato come handle di menu quando viene creato il controllo, non è possibile usare la [**funzione GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) per recuperare l'identificatore. In alternativa, un controllo può recuperare l'identificatore dal membro **hMenu** nella [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) durante l'elaborazione [**del messaggio WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)

Gli esempi seguenti, in cui *hwndControl* è l'handle della finestra di controllo e CN VALUECHANGED è una definizione di notifica personalizzata, illustra i due modi per inviare una notifica specifica \_ del controllo.


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



Si noti che [**la struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) può far parte di una struttura più ampia definita dal controllo che contiene informazioni aggiuntive. Nell'esempio i valori precedente e nuovo del controllo potrebbero essere contenuti in questa struttura . Queste strutture estese vengono usate con molte notifiche standard. Ad esempio, vedere [LVN \_ INSERTITEM,](lvn-insertitem.md)che usa la [**struttura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)

## <a name="accessibility"></a>Accessibilità

Tutti i controlli comuni supportano Microsoft Active Accessibility (MSAA), che consente l'accesso a livello di codice da applicazioni tecnologiche accessibili, ad esempio utilità per la lettura dello schermo. MSAA consente anche Automazione interfaccia utente, una tecnologia più recente, di interagire con i controlli.

I controlli personalizzati devono implementare [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (per supportare MSAA) o le interfacce Automazione interfaccia utente o entrambe. In caso contrario, i prodotti con tecnologia accessibile saranno in grado di ottenere solo informazioni molto limitate sulla finestra di controllo, non avranno accesso alle proprietà del controllo e non potranno attivare eventi nel controllo.

Per altre informazioni sull'accessibilità del controllo, vedere API [Windows Automation](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni di riferimento generali sul controllo](common-control-reference.md)
</dt> <dt>

[Personalizzazione dell'aspetto di un controllo tramite disegno personalizzato](custom-draw.md)
</dt> <dt>

[Messaggi di controllo](control-messages.md)
</dt> <dt>

[Uso degli stili di visualizzazione con Owner-Drawn personalizzati](using-visual-styles.md)
</dt> </dl>

 

 