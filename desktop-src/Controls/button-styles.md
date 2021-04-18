---
title: Stili di pulsanti (winuser. h)
description: Specifica una combinazione di stili dei pulsanti. Se si crea un pulsante usando la classe BUTTON con la funzione CreateWindow o CreateWindowEx, è possibile specificare uno degli stili dei pulsanti elencati di seguito.
ms.assetid: 30254cb5-43cd-407f-8ad6-bd7f9ec3edc7
topic_type:
- apiref
api_name:
- BS_3STATE
- BS_AUTO3STATE
- BS_AUTOCHECKBOX
- BS_AUTORADIOBUTTON
- BS_BITMAP
- BS_BOTTOM
- BS_CENTER
- BS_CHECKBOX
- BS_COMMANDLINK
- BS_DEFCOMMANDLINK
- BS_DEFPUSHBUTTON
- BS_DEFSPLITBUTTON
- BS_GROUPBOX
- BS_ICON
- BS_FLAT
- BS_LEFT
- BS_LEFTTEXT
- BS_MULTILINE
- BS_NOTIFY
- BS_OWNERDRAW
- BS_PUSHBUTTON
- BS_PUSHLIKE
- BS_RADIOBUTTON
- BS_RIGHT
- BS_RIGHTBUTTON
- BS_SPLITBUTTON
- BS_TEXT
- BS_TOP
- BS_TYPEMASK
- BS_USERBUTTON
- BS_VCENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 2b0054920f3cb2ae323a9655b1b028da473e119f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327250"
---
# <a name="button-styles"></a>Stili dei pulsanti

Specifica una combinazione di stili dei pulsanti. Se si crea un pulsante usando la classe BUTTON con la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , è possibile specificare uno degli stili dei pulsanti elencati di seguito.

## <a name="example"></a>Esempio

```cpp
HRESULT Button::CreateText(HWND hParent, const TCHAR *szCaption, int nID, 
                               const Rect& rcBound)
{
    CREATESTRUCT create;
    ZeroMemory(&create, sizeof(CREATESTRUCT));

    create.x = rcBound.left;
    create.y = rcBound.top;
    create.cx = rcBound.right - create.x;
    create.cy = rcBound.bottom - create.y;

    create.hwndParent = hParent;
    create.lpszName = szCaption;
    create.hMenu = (HMENU)(INT_PTR)nID;
    create.lpszClass = TEXT("BUTTON");
    create.style = BS_PUSHBUTTON | BS_FLAT;
    return Control::Create(create);
}
```
Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) in GitHub.


## <a name="constants"></a>Costanti
| Costante                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**\_3STATE BS**</dt> </dl>                            | Crea un pulsante che corrisponde a una casella di controllo, ad eccezione del fatto che la casella può essere visualizzata in grigio, oltre a essere selezionata o deselezionata. Utilizzare lo stato grigio per indicare che lo stato della casella di controllo non è determinato.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**\_AUTO3STATE BS**</dt> </dl>                | Crea un pulsante che corrisponde a una casella di controllo a tre stati, ad eccezione del fatto che la casella Cambia il proprio stato quando viene selezionato dall'utente. Lo stato viene ciclicamente controllato, indeterminato e deselezionato.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**casella di controllo \_ AUTOCHECKBOX BS**</dt> </dl>          | Consente di creare un pulsante che corrisponde a una casella di controllo, ad eccezione del fatto che lo stato di selezione passa automaticamente tra l'elemento selezionato e il deselezionato ogni volta che l'utente seleziona la casella di controllo.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**\_RadioButton**</dt> </dl> | Crea un pulsante che corrisponde a un pulsante di opzione, ad eccezione del fatto che quando viene selezionato dall'utente, il sistema imposta automaticamente lo stato di controllo del pulsante su selezionato e imposta automaticamente lo stato di selezione di tutti gli altri pulsanti nello stesso gruppo su deselezionato.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**\_bitmap BS**</dt> </dl>                            | Specifica che il pulsante Visualizza una bitmap. Vedere la sezione Osservazioni per l'interazione con l' \_ icona BS.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS in \_ basso**</dt> </dl>                            | Inserisce il testo nella parte inferiore del rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**\_centro BS**</dt> </dl>                            | Centra il testo orizzontalmente nel rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**casella di controllo BS \_**</dt> </dl>                      | Crea una casella di controllo piccola, vuota con testo. Per impostazione predefinita, il testo viene visualizzato a destra della casella di controllo. Per visualizzare il testo a sinistra della casella di controllo, combinare questo flag con lo stile BS \_ LEFTTEXT (o con lo \_ stile BS RIGHTBUTTON equivalente).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**\_COMMANDLINK BS**</dt> </dl>             | Crea un pulsante di collegamento al comando che si comporta come un \_ pulsante di stile del pulsante BS, ma il pulsante di collegamento del comando ha una freccia verde a sinistra che punta al testo del pulsante. È possibile impostare una didascalia per il testo del pulsante inviando il \_ messaggio di nota BCM al pulsante.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**\_DEFCOMMANDLINK BS**</dt> </dl>    | Crea un pulsante di collegamento al comando che si comporta come un pulsante di stile del pulsante BS \_ . Se il pulsante si trova in una finestra di dialogo, l'utente può selezionare il pulsante di collegamento al comando premendo il tasto invio, anche quando il pulsante di collegamento del comando non dispone dello stato attivo per l'input. Questo stile è utile per consentire all'utente di selezionare rapidamente l'opzione (impostazione predefinita) più probabile.<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**\_DEFPUSHBUTTON BS**</dt> </dl>       | Crea un pulsante di push che si comporta come un pulsante di stile del pulsante BS \_ , ma ha un aspetto distinto. Se il pulsante si trova in una finestra di dialogo, l'utente può selezionare il pulsante premendo il tasto invio, anche quando il pulsante non ha lo stato attivo per l'input. Questo stile è utile per consentire all'utente di selezionare rapidamente l'opzione (impostazione predefinita) più probabile.<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**\_DEFSPLITBUTTON BS**</dt> </dl>    | Crea un pulsante di suddivisione che si comporta come un pulsante di stile del pulsante BS \_ , ma ha anche un aspetto distintivo. Se il pulsante di suddivisione si trova in una finestra di dialogo, l'utente può selezionare il pulsante di suddivisione premendo il tasto invio, anche quando il pulsante di suddivisione non ha lo stato attivo per l'input. Questo stile è utile per consentire all'utente di selezionare rapidamente l'opzione (impostazione predefinita) più probabile.<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**casella di \_ GroupBox BS**</dt> </dl>                      | Crea un rettangolo in cui è possibile raggruppare altri controlli. Qualsiasi testo associato a questo stile viene visualizzato nell'angolo superiore sinistro del rettangolo.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**\_icona BS**</dt> </dl>                                  | Specifica che il pulsante Visualizza un'icona. Vedere la sezione Osservazioni per l'interazione con la \_ bitmap BS.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ Flat**</dt> </dl>                                  | Specifica che il pulsante è bidimensionale. non usa l'ombreggiatura predefinita per creare un'immagine 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS a \_ sinistra**</dt> </dl>                                  | Giustifica a sinistra il testo nel rettangolo del pulsante. Tuttavia, se il pulsante è una casella di controllo o un pulsante di opzione che non ha lo \_ stile BS RIGHTBUTTON, il testo viene lasciato giustificato sul lato destro della casella di controllo o del pulsante di opzione.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**\_LEFTTEXT BS**</dt> </dl>                      | Inserisce il testo a sinistra del pulsante di opzione o della casella di controllo in combinazione con un pulsante di opzione o uno stile di casella di controllo. Uguale allo \_ stile RIGHTBUTTON BS.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS su più \_ righe**</dt> </dl>                   | Esegue il wrapping del testo del pulsante su più righe se la stringa di testo è troppo lungo per essere adattata a una singola riga nel rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**\_notifica BS**</dt> </dl>                            | Consente a un pulsante di inviare i codici di notifica di [ \_ KILLFOCUS](bn-killfocus.md) BN e [BN \_ ](bn-setfocus.md) alla finestra padre. <br/> Si noti che i pulsanti inviano il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) , indipendentemente dal fatto che abbia questo stile. Per ottenere i codici di notifica di [BN \_ DBLCLK](bn-dblclk.md) , il pulsante deve avere lo \_ stile BS RadioButton o BS \_ OWNERDRAW.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**\_OWNERDRAW BS**</dt> </dl>                   | Crea un pulsante creato dal proprietario. La finestra proprietaria riceve un messaggio [**WM \_ DrawItem**](wm-drawitem.md) quando un aspetto visivo del pulsante è stato modificato. Non combinare lo stile BS \_ OWNERDRAW con altri stili dei pulsanti.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**\_pulsante BS**</dt> </dl>                | Crea un pulsante di push che invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla finestra proprietaria quando l'utente seleziona il pulsante.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**\_PUSHLIKE BS**</dt> </dl>                      | Rende un pulsante, ad esempio una casella di controllo, una casella di controllo a tre Stati o un pulsante di opzione, che funge da pulsante di push. Il pulsante viene generato quando non viene eseguito il push o la verifica e viene incassato quando viene eseguito il push o il controllo.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**\_RadioButton BS**</dt> </dl>             | Crea un cerchio di piccole dimensioni con testo. Per impostazione predefinita, il testo viene visualizzato a destra del cerchio. Per visualizzare il testo a sinistra del cerchio, combinare questo flag con lo \_ stile BS LEFTTEXT (o con lo stile BS RIGHTBUTTON equivalente \_ ). Usare pulsanti di opzione per gruppi di scelte correlate, ma che si escludono a vicenda.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS a \_ destra**</dt> </dl>                               | Giustifica a destra il testo nel rettangolo del pulsante. Tuttavia, se il pulsante è una casella di controllo o un pulsante di opzione che non ha lo \_ stile BS RIGHTBUTTON, il testo è giustificato a destra sul lato destro della casella di controllo o del pulsante di opzione.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**\_RIGHTBUTTON BS**</dt> </dl>             | Posiziona il cerchio di un pulsante di opzione o un quadrato della casella di controllo sul lato destro del rettangolo del pulsante. Uguale allo \_ stile LEFTTEXT BS.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**\_SPLITBUTTON BS**</dt> </dl>             | Crea un pulsante di suddivisione. Un pulsante di suddivisione presenta una freccia a discesa.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**\_testo BS**</dt> </dl>                                  | Specifica che il pulsante Visualizza il testo.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS in \_ alto**</dt> </dl>                                     | Inserisce il testo nella parte superiore del rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**\_TYPEMASK BS**</dt> </dl>                      | Non usare questo stile. Bit di stile composto risultante dall'utilizzo dell'operatore OR sui bit di \_ \* stile BS. Può essere usato per mascherare i bit BS validi \_ \* da una maschera di bit specificata. Si noti che questo non è aggiornato e non include correttamente tutti gli stili validi. Pertanto, non utilizzare questo stile.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**\_UserButton BS**</dt> </dl>                | Obsoleto, ma fornito per la compatibilità con le versioni di Windows a 16 bit. Le applicazioni devono invece usare BS \_ OWNERDRAW.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**\_vCenter BS**</dt> </dl>                         | Inserisce il testo al centro (verticalmente) del rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Commenti

Per illustrazioni degli stili dei pulsanti principali, ad esempio la casella di controllo BS e la casella di controllo \_ BS \_ , vedere [tipi di pulsanti](button-types-and-styles.md).

L'aspetto di un testo o di un'icona o di un controllo Button dipende dall'icona BS \_ e dagli stili di bitmap BS e dal \_ fatto che il messaggio [**BM \_ diImage**](bm-setimage.md) venga inviato. I risultati possibili sono i seguenti.



| \_Icona BS o \_ set di bitmap BS? | \_Nome dell'immagine BM | Risultato              |
|-----------------------------|----------------------|---------------------|
| Sì                         | Sì                  | Mostra solo l'icona.     |
| No                          | Sì                  | Mostra icona e testo. |
| Sì                         | No                   | Mostra solo testo.     |
| No                          | No                   | Mostra solo testo      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

