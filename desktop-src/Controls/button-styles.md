---
title: Stili dei pulsanti (Winuser.h)
description: Specifica una combinazione di stili dei pulsanti. Se si crea un pulsante usando la classe BUTTON con la funzione CreateWindow o CreateWindowEx, è possibile specificare uno degli stili del pulsante elencati di seguito.
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
ms.openlocfilehash: 60419d947036516e093d481f3fc0d8caa097671c13bd4fe3fc8e95d21cc3cb83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832481"
---
# <a name="button-styles"></a>Stili dei pulsanti

Specifica una combinazione di stili dei pulsanti. Se si crea un pulsante usando la classe BUTTON con la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) è possibile specificare uno degli stili del pulsante elencati di seguito.

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
Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/directshow/common/button.cpp) in GitHub.


## <a name="constants"></a>Costanti
| Costante                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BS_3STATE"></span><span id="bs_3state"></span><dl> <dt>**BS \_ 3STATE**</dt> </dl>                            | Crea un pulsante uguale a una casella di controllo, ad eccezione del fatto che la casella può essere in grigio, nonché selezionata o deselezionata. Usare lo stato in grigio per mostrare che lo stato della casella di controllo non è determinato.<br/>                                                                                                                                                                                              |
| <span id="BS_AUTO3STATE"></span><span id="bs_auto3state"></span><dl> <dt>**BS \_ AUTO3STATE**</dt> </dl>                | Crea un pulsante uguale a una casella di controllo a tre stati, ad eccezione del fatto che la casella cambia stato quando l'utente lo seleziona. Lo stato scorre in ciclo checked, indeterminate e cleared.<br/>                                                                                                                                                                                                     |
| <span id="BS_AUTOCHECKBOX"></span><span id="bs_autocheckbox"></span><dl> <dt>**BS \_ AUTOCHECKBOX**</dt> </dl>          | Crea un pulsante uguale a una casella di controllo, ad eccezione del fatto che lo stato del controllo passa automaticamente da selezionato a deselezionato ogni volta che l'utente seleziona la casella di controllo.<br/>                                                                                                                                                                                                                       |
| <span id="BS_AUTORADIOBUTTON"></span><span id="bs_autoradiobutton"></span><dl> <dt>**BS \_ AUTORADIOBUTTON**</dt> </dl> | Crea un pulsante uguale a un pulsante di opzione, ad eccezione del fatto che quando l'utente lo seleziona, il sistema imposta automaticamente lo stato di controllo del pulsante su checked e imposta automaticamente lo stato del controllo per tutti gli altri pulsanti nello stesso gruppo su cleared.<br/>                                                                                                                                         |
| <span id="BS_BITMAP"></span><span id="bs_bitmap"></span><dl> <dt>**BS \_ BITMAP**</dt> </dl>                            | Specifica che il pulsante visualizza una bitmap. Vedere la sezione Osservazioni per l'interazione con BS \_ ICON.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="BS_BOTTOM"></span><span id="bs_bottom"></span><dl> <dt>**BS \_ INFERIORE**</dt> </dl>                            | Posiziona il testo nella parte inferiore del rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CENTER"></span><span id="bs_center"></span><dl> <dt>**BS \_ CENTER**</dt> </dl>                            | Centra il testo orizzontalmente nel rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="BS_CHECKBOX"></span><span id="bs_checkbox"></span><dl> <dt>**CASELLA DI CONTROLLO BS \_**</dt> </dl>                      | Crea una piccola casella di controllo vuota con testo. Per impostazione predefinita, il testo viene visualizzato a destra della casella di controllo. Per visualizzare il testo a sinistra della casella di controllo, combinare questo flag con lo stile BS LEFTTEXT (o con lo stile \_ RIGHTBUTTON BS \_ equivalente).<br/>                                                                                                                                    |
| <span id="BS_COMMANDLINK"></span><span id="bs_commandlink"></span><dl> <dt>**BS \_ COMMANDLINK**</dt> </dl>             | Crea un pulsante di collegamento di comando che si comporta come un pulsante di stile BS PUSHBUTTON, ma il pulsante di collegamento di comando ha una freccia verde a sinistra che punta al \_ testo del pulsante. È possibile impostare una didascalia per il testo del pulsante inviando il messaggio \_ BCM SETNOTE al pulsante.<br/>                                                                                                                               |
| <span id="BS_DEFCOMMANDLINK"></span><span id="bs_defcommandlink"></span><dl> <dt>**BS \_ DEFCOMMANDLINK**</dt> </dl>    | Crea un pulsante di collegamento di comando che si comporta come un pulsante di stile \_ BS PUSHBUTTON. Se il pulsante si trova in una finestra di dialogo, l'utente può selezionare il pulsante di collegamento al comando premendo INVIO, anche quando il pulsante di collegamento al comando non ha lo stato attivo per l'input. Questo stile è utile per consentire all'utente di selezionare rapidamente l'opzione più probabile (predefinita).<br/>                                         |
| <span id="BS_DEFPUSHBUTTON"></span><span id="bs_defpushbutton"></span><dl> <dt>**BS \_ DEFPUSHBUTTON**</dt> </dl>       | Crea un pulsante push che si comporta come un pulsante di stile \_ BS PUSHBUTTON, ma ha un aspetto distinto. Se il pulsante si trova in una finestra di dialogo, l'utente può selezionare il pulsante premendo INVIO, anche quando il pulsante non ha lo stato attivo per l'input. Questo stile è utile per consentire all'utente di selezionare rapidamente l'opzione più probabile (predefinita).<br/>                                            |
| <span id="BS_DEFSPLITBUTTON"></span><span id="bs_defsplitbutton"></span><dl> <dt>**BS \_ DEFSPLITBUTTON**</dt> </dl>    | Crea un pulsante di divisione che si comporta come un pulsante di stile \_ BS PUSHBUTTON, ma ha anche un aspetto distintivo. Se il pulsante di divisione si trova in una finestra di dialogo, l'utente può selezionare il pulsante di divisione premendo INVIO, anche quando il pulsante di divisione non ha lo stato attivo per l'input. Questo stile è utile per consentire all'utente di selezionare rapidamente l'opzione più probabile (predefinita).<br/>                 |
| <span id="BS_GROUPBOX"></span><span id="bs_groupbox"></span><dl> <dt>**BS \_ GROUPBOX**</dt> </dl>                      | Crea un rettangolo in cui è possibile raggruppare altri controlli. Qualsiasi testo associato a questo stile viene visualizzato nell'angolo superiore sinistro del rettangolo.<br/>                                                                                                                                                                                                                                              |
| <span id="BS_ICON"></span><span id="bs_icon"></span><dl> <dt>**ICONA DI \_ BS**</dt> </dl>                                  | Specifica che il pulsante visualizza un'icona. Vedere la sezione Osservazioni per l'interazione con BS \_ BITMAP.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="BS_FLAT"></span><span id="bs_flat"></span><dl> <dt>**BS \_ FLAT**</dt> </dl>                                  | Specifica che il pulsante è bidimensionale. non usa l'ombreggiatura predefinita per creare un'immagine 3D. <br/>                                                                                                                                                                                                                                                                                       |
| <span id="BS_LEFT"></span><span id="bs_left"></span><dl> <dt>**BS \_ A SINISTRA**</dt> </dl>                                  | Giustifica a sinistra il testo nel rettangolo del pulsante. Tuttavia, se il pulsante è una casella di controllo o un pulsante di opzione che non ha lo stile BS RIGHTBUTTON, il testo viene giustificato a sinistra sul lato destro della casella di controllo o del pulsante \_ di opzione.<br/>                                                                                                                                                             |
| <span id="BS_LEFTTEXT"></span><span id="bs_lefttext"></span><dl> <dt>**BS \_ LEFTTEXT**</dt> </dl>                      | Posiziona il testo sul lato sinistro del pulsante di opzione o della casella di controllo quando viene combinato con uno stile di pulsante di opzione o casella di controllo. Uguale allo stile \_ RIGHTBUTTON BS.<br/>                                                                                                                                                                                                                                          |
| <span id="BS_MULTILINE"></span><span id="bs_multiline"></span><dl> <dt>**BS \_ MULTILINE**</dt> </dl>                   | Esegue il wrapping del testo del pulsante su più righe se la stringa di testo è troppo lunga per essere adattata a una singola riga nel rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                         |
| <span id="BS_NOTIFY"></span><span id="bs_notify"></span><dl> <dt>**NOTIFICA \_ BS**</dt> </dl>                            | Consente a un pulsante di inviare codici di notifica [BN \_ KILLFOCUS](bn-killfocus.md) e [BN \_ SETFOCUS](bn-setfocus.md) alla finestra padre. <br/> Si noti che i pulsanti inviano il codice di notifica [BN \_ CLICKED](bn-clicked.md) indipendentemente dal fatto che abbia questo stile. Per ottenere [i codici di notifica \_ BN DBLCLK,](bn-dblclk.md) il pulsante deve avere lo stile BS \_ RADIOBUTTON o BS \_ OWNERDRAW.<br/> |
| <span id="BS_OWNERDRAW"></span><span id="bs_ownerdraw"></span><dl> <dt>**BS \_ OWNERDRAW**</dt> </dl>                   | Crea un pulsante disegnato dal proprietario. La finestra proprietaria riceve un [**messaggio WM \_ DRAWITEM**](wm-drawitem.md) quando viene modificato un aspetto visivo del pulsante. Non combinare lo stile BS \_ OWNERDRAW con altri stili di pulsante.<br/>                                                                                                                                                                     |
| <span id="BS_PUSHBUTTON"></span><span id="bs_pushbutton"></span><dl> <dt>**PULSANTE DI \_ PUSH BS**</dt> </dl>                | Crea un pulsante push che invia un [**messaggio WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla finestra del proprietario quando l'utente seleziona il pulsante.<br/>                                                                                                                                                                                                                                                           |
| <span id="BS_PUSHLIKE"></span><span id="bs_pushlike"></span><dl> <dt>**BS \_ PUSHLIKE**</dt> </dl>                      | Rende un pulsante (ad esempio una casella di controllo, una casella di controllo a tre stati o un pulsante di opzione) che ha l'aspetto di un pulsante di scelta. Il pulsante viene visualizzato quando non viene sottoposto a push o selezionato e viene inserito quando viene sottoposto a push o selezionato.<br/>                                                                                                                                                                                 |
| <span id="BS_RADIOBUTTON"></span><span id="bs_radiobutton"></span><dl> <dt>**PULSANTE DI \_ OPZIONE BS**</dt> </dl>             | Crea un piccolo cerchio con testo. Per impostazione predefinita, il testo viene visualizzato a destra del cerchio. Per visualizzare il testo a sinistra del cerchio, combinare questo flag con lo stile BS LEFTTEXT (o con lo stile \_ RIGHTBUTTON BS \_ equivalente). Usare i pulsanti di opzione per gruppi di scelte correlate, ma che si escludono a vicenda.<br/>                                                                           |
| <span id="BS_RIGHT"></span><span id="bs_right"></span><dl> <dt>**BS \_ RIGHT**</dt> </dl>                               | Giustifica a destra il testo nel rettangolo del pulsante. Tuttavia, se il pulsante è una casella di controllo o un pulsante di opzione che non ha lo stile BS RIGHTBUTTON, il testo viene giustificato a destra sul lato destro della casella di controllo o del pulsante \_ di opzione.<br/>                                                                                                                                                               |
| <span id="BS_RIGHTBUTTON"></span><span id="bs_rightbutton"></span><dl> <dt>**PULSANTE DESTRO DI BS \_**</dt> </dl>             | Posiziona il cerchio di un pulsante di opzione o il quadrato di una casella di controllo sul lato destro del rettangolo del pulsante. Uguale allo stile \_ LEFTTEXT BS.<br/>                                                                                                                                                                                                                                                            |
| <span id="BS_SPLITBUTTON"></span><span id="bs_splitbutton"></span><dl> <dt>**BS \_ SPLITBUTTON**</dt> </dl>             | Crea un pulsante di divisione. Un pulsante di divisione ha una freccia a discesa.<br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="BS_TEXT"></span><span id="bs_text"></span><dl> <dt>**TESTO \_ BS**</dt> </dl>                                  | Specifica che il pulsante visualizza il testo.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BS_TOP"></span><span id="bs_top"></span><dl> <dt>**BS \_ TOP**</dt> </dl>                                     | Posiziona il testo nella parte superiore del rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="BS_TYPEMASK"></span><span id="bs_typemask"></span><dl> <dt>**MASCHERA DI \_ TIPO BS**</dt> </dl>                      | Non usare questo stile. Bit di stile composito derivato dall'uso dell'operatore OR sui bit di \_ \* stile BS. Può essere usato per mascherare i bit BS \_ \* validi da una maschera di bit specificata. Si noti che non è aggiornato e non include correttamente tutti gli stili validi. Pertanto, non è consigliabile usare questo stile.<br/>                                                                                               |
| <span id="BS_USERBUTTON"></span><span id="bs_userbutton"></span><dl> <dt>**BS \_ USERBUTTON**</dt> </dl>                | Obsoleto, ma fornito per la compatibilità con le versioni a 16 bit di Windows. In alternativa, le applicazioni devono usare BS \_ OWNERDRAW.<br/>                                                                                                                                                                                                                                                                        |
| <span id="BS_VCENTER"></span><span id="bs_vcenter"></span><dl> <dt>**BS \_ VCENTER**</dt> </dl>                         | Posiziona il testo al centro (verticalmente) del rettangolo del pulsante.<br/>                                                                                                                                                                                                                                                                                                                                 |



## <a name="remarks"></a>Commenti

Per illustrazioni degli stili dei pulsanti principali, ad esempio BS \_ CHECKBOX e BS \_ GROUPBOX, vedere [Tipi di pulsante.](button-types-and-styles.md)

L'aspetto del testo, di un'icona o di entrambi i controlli pulsante dipende dagli stili BS ICON e BS BITMAP e dall'invio del messaggio \_ \_ [**\_ BM SETIMAGE.**](bm-setimage.md) I risultati possibili sono i seguenti.



| BS \_ ICON o BS BITMAP \_ set? | BM \_ SETIMAGE chiamato? | Risultato              |
|-----------------------------|----------------------|---------------------|
| Sì                         | Sì                  | Mostra solo icona.     |
| No                          | Sì                  | Mostra icona e testo. |
| Sì                         | No                   | Mostra solo testo.     |
| No                          | No                   | Mostra solo testo      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser</dt> </dl> |



 

