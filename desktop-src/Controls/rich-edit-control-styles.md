---
title: Stili del controllo Rich Edit (Winuser.h)
description: Gli stili di finestra seguenti sono univoci per i controlli Rich Edit.
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
ms.openlocfilehash: bcc88ea2c3c5d32dff9920b2699474a810f29b14dcf50d9b4c2401863c875778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169091"
---
# <a name="rich-edit-control-styles"></a>Stili del controllo Rich Edit

Gli stili di finestra seguenti sono univoci per i controlli Rich Edit.



| Costante                                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_DISABLENOSCROLL"></span><span id="es_disablenoscroll"></span><dl> <dt>**ES \_ DISABLENOSCROLL**</dt> </dl>     | Disabilita le barre di scorrimento invece di nasconderle quando non sono necessarie.<br/>                                                                                                                                                                    |
| <span id="ES_EX_NOCALLOLEINIT"></span><span id="es_ex_nocalloleinit"></span><dl> <dt>**ES \_ EX \_ NOCALLOLEINIT**</dt> </dl> | Impedisce al controllo di chiamare la [**funzione OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) al momento della creazione. Questo stile di finestra è utile solo nei modelli di finestra di dialogo perché [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) non accetta questo stile.<br/> |
| <span id="ES_NOIME_"></span><span id="es_noime_"></span><dl> <dt>**ES \_ NOIME**</dt> </dl>                                | Disabilita l'operazione IME. Questo stile è disponibile solo per il supporto delle lingue asiatiche.<br/>                                                                                                                                                     |
| <span id="ES_NOOLEDRAGDROP"></span><span id="es_nooledragdrop"></span><dl> <dt>**ES \_ NOOLEDRAGDROP**</dt> </dl>           | Disabilita il supporto per il trascinamento della selezione di oggetti OLE.<br/>                                                                                                                                                                                           |
| <span id="ES_SAVESEL"></span><span id="es_savesel"></span><dl> <dt>**ES \_ SAVESEL**</dt> </dl>                             | Mantiene la selezione quando il controllo perde lo stato attivo. Per impostazione predefinita, l'intero contenuto del controllo viene selezionato quando recupera lo stato attivo.<br/>                                                                                         |
| <span id="ES_SELECTIONBAR"></span><span id="es_selectionbar"></span><dl> <dt>**BARRA DI SELEZIONE ES \_**</dt> </dl>              | Aggiunge spazio al margine sinistro in cui il cursore assume la forma di una freccia verso l'alto, consentendo all'utente di selezionare righe di testo complete. <br/>                                                                                                             |
| <span id="ES_SELFIME_"></span><span id="es_selfime_"></span><dl> <dt>**ES \_ SELFIME**</dt> </dl>                          | Indica al controllo Rich Edit di consentire all'applicazione di gestire tutte le operazioni IME. Questo stile è disponibile solo per il supporto delle lingue asiatiche.<br/>                                                                                            |
| <span id="ES_SUNKEN"></span><span id="es_sunken"></span><dl> <dt>**ES \_ SUNKEN**</dt> </dl>                                | Visualizza il controllo con uno stile di bordo incassato in modo che il controllo Rich Edit venga visualizzato nella finestra padre. <br/>                                                                                                                  |
| <span id="ES_VERTICAL"></span><span id="es_vertical"></span><dl> <dt>**ES \_ VERTICAL**</dt> </dl>                          | Disegna testo e oggetti in direzione verticale. Questo stile è disponibile solo per il supporto in lingue asiatiche.<br/>                                                                                                                                 |



I controlli Rich Edit supportano anche gli stili di controllo di modifica seguenti.



| Costante                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt>**ES \_ AUTOHSCROLL**</dt> </dl> | Scorre automaticamente il testo verso destra di 10 caratteri quando l'utente specifica un carattere alla fine della riga. Quando l'utente preme INVIO, il controllo scorre tutto il testo fino alla posizione zero.<br/>                                                                                                                                                    |
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt>**ES \_ AUTOVSCROLL**</dt> </dl> | Scorre automaticamente il testo verso l'alto di una pagina quando l'utente preme INVIO nell'ultima riga.<br/>                                                                                                                                                                                                                                                                 |
| <span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt>**ES \_ CENTER**</dt> </dl>                | Centra il testo in un controllo di modifica a riga singola o su più righe.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt>**ES \_ LEFT**</dt> </dl>                      | Il testo viene allineato a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt>**ES \_ MULTILINE**</dt> </dl>       | Designa un controllo di modifica su più righe. Il valore predefinito è il controllo di modifica a riga singola.<br/>                                                                                                                                                                                                                                                                                |
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt>**ES \_ NOHIDESEL**</dt> </dl>       | Nega il comportamento predefinito per un controllo di modifica. Il comportamento predefinito nasconde la selezione quando il controllo perde lo stato attivo per l'input e inverte la selezione quando il controllo riceve lo stato attivo per l'input. Se si specifica [**ES \_ NOHIDESEL**](edit-control-styles.md), il testo selezionato viene invertito, anche se il controllo non ha lo stato attivo.<br/> |
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt>**NUMERO \_ ES**</dt> </dl>                | Consente l'immissione di solo cifre nel controllo di modifica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt>**ES \_ PASSWORD**</dt> </dl>          | Visualizza un asterisco ( \* ) per ogni carattere digitato nel controllo di modifica. Questo stile è valido solo per i controlli di modifica a riga singola.<br/>                                                                                                                                                                                                                            |
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt>**ES \_ READONLY**</dt> </dl>          | Impedisce all'utente di digitare o modificare il testo nel controllo di modifica.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt>**ES \_ RIGHT**</dt> </dl>                   | Allinea a destra il testo in un controllo di modifica a riga singola o su più righe.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt>**ES \_ WANTRETURN**</dt> </dl>    | Specifica l'inserimento di un ritorno a capo quando l'utente preme INVIO durante l'immissione di testo in un controllo di modifica su più righe in una finestra di dialogo. Se non si specifica questo stile, la pressione del tasto INVIO ha lo stesso effetto della pressione del pulsante di comando predefinito della finestra di dialogo. Questo stile non ha effetto su un controllo di modifica a riga singola.<br/>                   |



I controlli Rich Edit non supportano gli stili di controllo di modifica seguenti.

-   [**ES \_ MINUSCOLA**](edit-control-styles.md)
-   [**ES \_ OEMCONVERT**](edit-control-styles.md)
-   [**ES \_ MAIUSCOLA**](edit-control-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser</dt> </dl> |



 

