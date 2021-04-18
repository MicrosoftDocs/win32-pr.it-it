---
title: Stili del controllo Rich Edit (winuser. h)
description: Gli stili della finestra seguenti sono univoci per i controlli Rich Edit.
ms.assetid: 0f1b3e01-01cb-4b3e-b959-6f32498f0394
topic_type:
- apiref
api_name:
- ES_DISABLENOSCROLL
- ES_EX_NOCALLOLEINIT
- ES_NOIME
- ES_NOOLEDRAGDROP
- ES_SAVESEL
- ES_SELECTIONBAR
- ES_SELFIME
- ES_SUNKEN
- ES_VERTICAL
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620f73beb726eea065d8c8a63a635ff04fdeba37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327850"
---
# <a name="rich-edit-control-styles"></a>Stili del controllo Rich Edit

Gli stili della finestra seguenti sono univoci per i controlli Rich Edit.



| Costante                                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL es**</dt> </dl>     | Disabilita le barre di scorrimento anziché nasconderle quando non sono necessarie.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ es \_ NOCALLOLEINIT**</dt> </dl> | Impedisce al controllo di chiamare la funzione [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) al momento della creazione. Questo stile di finestra è utile solo nei modelli di finestra di dialogo perché [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) non accetta questo stile.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**Es \_ . Claudio**</dt> </dl>                                | Disabilita l'operazione IME. Questo stile è disponibile solo per il supporto della lingua asiatica.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**\_NOOLEDRAGDROP es**</dt> </dl>           | Disabilita il supporto per il trascinamento della selezione di oggetti OLE.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**\_SAVESEL es**</dt> </dl>                             | Mantiene la selezione quando il controllo perde lo stato attivo. Per impostazione predefinita, l'intero contenuto del controllo viene selezionato quando riacquisisce lo stato attivo.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**\_SELECTIONBAR es**</dt> </dl>              | Aggiunge spazio al margine sinistro in cui il cursore viene modificato in una freccia a destra, consentendo all'utente di selezionare righe complete di testo. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**Es \_ . SELFIME**</dt> </dl>                          | Indica al controllo Rich Edit di consentire all'applicazione di gestire tutte le operazioni IME. Questo stile è disponibile solo per il supporto della lingua asiatica.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**\_incassato es**</dt> </dl>                                | Visualizza il controllo con uno stile del bordo incassato in modo che il controllo Rich Edit appaia incassato nella finestra padre. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**\_verticale es**</dt> </dl>                          | Disegna testo e oggetti in una direzione verticale. Questo stile è disponibile solo per il supporto in lingua asiatica.<br/>                                                                                                                                 |



I controlli Rich Edit supportano anche gli stili dei controlli di modifica seguenti.



| Costante                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**\_AUTOHSCROLL es**</dt> </dl> | Scorre automaticamente il testo a destra di 10 caratteri quando l'utente digita un carattere alla fine della riga. Quando l'utente preme il tasto invio, il controllo scorre tutto il testo fino alla posizione zero.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**\_AUTOVSCROLL es**</dt> </dl> | Scorre automaticamente il testo verso l'alto di una pagina quando l'utente preme il tasto invio sull'ultima riga.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**\_centro es**</dt> </dl>                | Centra il testo in un controllo di modifica a riga singola o su più righe.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**\_sinistra es**</dt> </dl>                      | Allinea a sinistra il testo.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**più \_ righe es**</dt> </dl>       | Definisce un controllo di modifica su più righe. Il valore predefinito è il controllo di modifica a riga singola.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**\_NOHIDESEL es**</dt> </dl>       | Nega il comportamento predefinito per un controllo di modifica. Il comportamento predefinito nasconde la selezione quando il controllo perde lo stato attivo per l'input e inverte la selezione quando il controllo riceve lo stato attivo per l'input. Se si specifica [**es \_ NOHIDESEL**](edit-control-styles.md), il testo selezionato viene invertito, anche se il controllo non ha lo stato attivo.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**\_numero es**</dt> </dl>                | Consente di immettere solo le cifre nel controllo di modifica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**\_password es**</dt> </dl>          | Visualizza un asterisco ( \* ) per ogni carattere digitato nel controllo di modifica. Questo stile è valido solo per i controlli di modifica a riga singola.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ ReadOnly**</dt> </dl>          | Impedisce all'utente di digitare o modificare il testo nel controllo di modifica.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**\_diritto es**</dt> </dl>                   | Allinea a destra il testo in un controllo di modifica a riga singola o su più righe.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**\_WANTRETURN es**</dt> </dl>    | Specifica l'inserimento di un ritorno a capo quando l'utente preme il tasto INVIO mentre immette il testo in un controllo di modifica su più righe in una finestra di dialogo. Se non si specifica questo stile, premendo il tasto invio si avrà lo stesso effetto della pressione del pulsante di push predefinito della finestra di dialogo. Questo stile non ha alcun effetto su un controllo di modifica a riga singola.<br/>                   |



I controlli Rich Edit non supportano gli stili dei controlli di modifica seguenti.

-   [**\_minuscole es**](edit-control-styles.md)
-   [**\_OEMCONVERT es**](edit-control-styles.md)
-   [**\_maiuscole/minuscole**](edit-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

