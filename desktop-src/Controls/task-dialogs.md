---
title: Finestra di dialogo attività
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con una finestra di dialogo attività. Una finestra di dialogo attività è simile a, ma molto più flessibile di una finestra di messaggio di base.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f115531b9f872c824e9d1822be07777b2bc439
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/24/2020
ms.locfileid: "103873109"
---
# <a name="task-dialog"></a>Finestra di dialogo attività

Questa sezione contiene informazioni sugli elementi di programmazione usati con una finestra di dialogo attività. Una *finestra di dialogo attività* è simile a, ma molto più flessibile di una finestra di messaggio di base.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                           | Contenuto                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Informazioni sulle finestre di dialogo delle attività](task-dialogs-overview.md) | Descrive gli elementi di una finestra di dialogo attività.<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Crea, Visualizza e gestisce una finestra di dialogo attività. La finestra di dialogo attività contiene testo e titolo del messaggio definiti dall'applicazione, icone e qualsiasi combinazione di pulsanti di push predefiniti. Questa funzione non supporta la registrazione di una funzione di callback per la ricezione di notifiche.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Funzione definita dall'applicazione utilizzata con la funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Riceve i messaggi dalla finestra di dialogo attività quando si verificano diversi eventi.<br/> Il tipo **PFTASKDIALOGCALLBACK** definisce un puntatore a questa funzione di callback. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) è un segnaposto per il nome della funzione definita dall'applicazione.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Crea, Visualizza e gestisce una finestra di dialogo attività. La finestra di dialogo attività contiene le icone, i messaggi, il titolo, la casella di controllo di verifica, i collegamenti ai comandi, i pulsanti e i pulsanti di opzione definiti dall'applicazione. Questa funzione può registrare una funzione di callback per ricevere i messaggi di notifica.<br/>                                                                                                               |



 

### <a name="messages"></a>Messaggi



| Argomento                                                                                           | Contenuto                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_pulsante di clic TDM \_**](tdm-click-button.md)                                                  | Simula l'azione di un clic su un pulsante in una finestra di dialogo attività.<br/>                                                                                                                                  |
| [**\_pulsante di \_ opzione TDM clic \_**](tdm-click-radio-button.md)                                     | Simula l'azione di un pulsante di opzione fare clic in una finestra di dialogo attività.<br/>                                                                                                                            |
| [**\_Verifica clic \_ TDM**](tdm-click-verification.md)                                      | Simula l'azione di una casella di controllo di verifica fare clic in una finestra di dialogo attività.<br/>                                                                                                                   |
| [**\_pulsante Abilita \_ TDM**](tdm-enable-button.md)                                                | Abilita o Disabilita un pulsante di push in una finestra di dialogo attività.<br/>                                                                                                                                       |
| [**\_pulsante di \_ opzione \_ Abilita TDM**](tdm-enable-radio-button.md)                                   | Abilita o Disabilita un pulsante di opzione in una finestra di dialogo attività.<br/>                                                                                                                                      |
| [**\_pagina di esplorazione TDM \_**](tdm-navigate-page.md)                                                | Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.<br/>                                                                                           |
| [**\_stato richiesto per l' \_ \_ elevazione dei pulsanti \_ del set \_ TDM**](tdm-set-button-elevation-required-state.md) | Specifica se un pulsante o un collegamento di comando di una determinata attività deve avere un'icona di schermatura controllo dell'account utente. ovvero se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi. <br/> |
| [**\_testo dell' \_ elemento del set TDM \_**](tdm-set-element-text.md)                                         | Aggiorna un elemento di testo in una finestra di dialogo attività.<br/>                                                                                                                                                  |
| [**\_indicatore di \_ \_ stato selezione set TDM \_**](tdm-set-marquee-progress-bar.md)                        | Indica se l'indicatore di stato ospitato deve essere visualizzato in modalità marquee.<br/>                                                                                                            |
| [**Marquee indicatore di \_ stato set TDM \_ \_ \_**](tdm-set-progress-bar-marquee.md)                        | Avvia e arresta la visualizzazione Marquee dell'indicatore di stato e imposta la velocità del Marquee.<br/>                                                                                              |
| [**indicatore \_ di \_ stato set TDM \_ \_ pos**](tdm-set-progress-bar-pos.md)                                | Imposta la posizione corrente per un indicatore di stato.<br/>                                                                                                                                             |
| [**\_intervallo della \_ barra di stato set \_ TDM \_**](tdm-set-progress-bar-range.md)                            | Imposta i valori minimo e massimo per l'indicatore di stato ospitato.<br/>                                                                                                                          |
| [**\_ \_ \_ stato indicatore di \_ stato set TDM**](tdm-set-progress-bar-state.md)                            | Imposta lo stato corrente dell'indicatore di stato.<br/>                                                                                                                                               |
| [**\_testo dell' \_ elemento di aggiornamento TDM \_**](tdm-update-element-text.md)                                   | Aggiorna un elemento di testo in una finestra di dialogo attività. <br/>                                                                                                                                                 |
| [**\_icona di aggiornamento TDM \_**](tdm-update-icon.md)                                                    | Aggiorna l'icona di una finestra di dialogo attività. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                           | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_pulsante TDN \_ selezionato](tdn-button-clicked.md)                  | Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento al comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                   |
| [TDN \_ creato](tdn-created.md)                                 | Inviato da una finestra di dialogo attività dopo che la finestra di dialogo attività è stata creata e prima che venga visualizzata. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [TDN \_ distrutto](tdn-destroyed.md)                             | Inviato da una finestra di dialogo attività quando viene eliminato definitivamente e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |
| [\_finestra di dialogo TDN \_ costruita](tdn-dialog-constructed.md)          | Inviato da una finestra di dialogo attività dopo che la finestra di dialogo attività è stata creata e prima che venga visualizzata. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [\_pulsante TDN expando \_ \_ selezionato](tdn-expando-button-clicked.md) | Inviato da una finestra di dialogo attività quando l'utente fa clic sul pulsante expando della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                            |
| [Guida di TDN \_](tdn-help.md)                                       | Inviato da una finestra di dialogo attività quando l'utente preme F1 sulla tastiera mentre la finestra di dialogo attività ha lo stato attivo. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                            |
| [\_collegamento ipertestuale TDN \_ selezionato](tdn-hyperlink-clicked.md)            | Inviato da una finestra di dialogo attività quando l'utente fa clic su un collegamento ipertestuale nel contenuto della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                        |
| [TDN \_ navigato](tdn-navigated.md)                             | Inviato da una finestra di dialogo attività quando si è verificata una navigazione. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                                                     |
| [\_pulsante di opzione TDN \_ \_ selezionato](tdn-radio-button-clicked.md)     | Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento al comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [\_timer TDN](tdn-timer.md)                                     | Inviato da una finestra di dialogo attività approssimativamente ogni 200 millisecondi. Questo codice di notifica viene inviato quando il \_ \_ flag del timer di callback TDF è stato impostato nel membro **DwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) che è stato passato alla funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo **TaskDialogIndirect** .<br/> |
| [\_Verifica TDN \_ clic](tdn-verification-clicked.md)      | Inviato dalla finestra di dialogo attività quando l'utente fa clic sulla casella di controllo Verifica finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Strutture



| Argomento                                           | Contenuto                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_pulsante TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contiene informazioni utilizzate per visualizzare un pulsante in una finestra di dialogo attività. La struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizza questa struttura.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contiene informazioni utilizzate per visualizzare una finestra di dialogo attività. La funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) usa questa struttura.<br/>          |



 

 

