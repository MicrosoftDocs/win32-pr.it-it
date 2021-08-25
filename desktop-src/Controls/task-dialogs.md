---
title: Finestra di dialogo Attività
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con una finestra di dialogo attività. Una finestra di dialogo dell'attività è simile, anche se molto più flessibile, a una finestra di messaggio di base.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6797314b75fff46ddf8a4f64638fefb5ea0181d2353bd1a1d3caa57325d28e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168551"
---
# <a name="task-dialog"></a>Finestra di dialogo Attività

Questa sezione contiene informazioni sugli elementi di programmazione usati con una finestra di dialogo attività. Una *finestra di dialogo* dell'attività è simile, anche se molto più flessibile, a una finestra di messaggio di base.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                           | Contenuto                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Informazioni sui dialoghe attività](task-dialogs-overview.md) | Descrive gli elementi di una finestra di dialogo attività.<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Finestra di dialogo Attività**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Crea, visualizza e gestisce una finestra di dialogo attività. La finestra di dialogo dell'attività contiene il testo e il titolo del messaggio definiti dall'applicazione, le icone e qualsiasi combinazione di pulsanti di push predefiniti. Questa funzione non supporta la registrazione di una funzione di callback per ricevere notifiche.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Funzione definita dall'applicazione usata con la [**funzione TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Riceve messaggi dalla finestra di dialogo attività quando si verificano vari eventi.<br/> Il **tipo PFTASKDIALOGCALLBACK** definisce un puntatore a questa funzione di callback. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) è un segnaposto per il nome della funzione definita dall'applicazione.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Crea, visualizza e gestisce una finestra di dialogo attività. La finestra di dialogo dell'attività contiene icone, messaggi, titolo, casella di controllo di verifica, collegamenti ai comandi, pulsanti di push e pulsanti di opzione definiti dall'applicazione. Questa funzione può registrare una funzione di callback per ricevere messaggi di notifica.<br/>                                                                                                               |



 

### <a name="messages"></a>Messaggi



| Argomento                                                                                           | Contenuto                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PULSANTE TDM \_ \_ CLICK**](tdm-click-button.md)                                                  | Simula l'azione di un clic su un pulsante in una finestra di dialogo attività.<br/>                                                                                                                                  |
| [**TDM \_ FARE CLIC SUL PULSANTE DI \_ \_ OPZIONE**](tdm-click-radio-button.md)                                     | Simula l'azione di un clic su un pulsante di opzione in una finestra di dialogo attività.<br/>                                                                                                                            |
| [**VERIFICA DEI CLIC DI TDM \_ \_**](tdm-click-verification.md)                                      | Simula l'azione di un clic di una casella di controllo di verifica in una finestra di dialogo attività.<br/>                                                                                                                   |
| [**PULSANTE ABILITA \_ \_ TDM**](tdm-enable-button.md)                                                | Abilita o disabilita un pulsante push in una finestra di dialogo attività.<br/>                                                                                                                                       |
| [**PULSANTE DI OPZIONE ABILITA TDM \_ \_ \_**](tdm-enable-radio-button.md)                                   | Abilita o disabilita un pulsante di opzione in una finestra di dialogo attività.<br/>                                                                                                                                      |
| [**PAGINA DI NAVIGAZIONE \_ DI TDM \_**](tdm-navigate-page.md)                                                | Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.<br/>                                                                                           |
| [**STATO RICHIESTO PER \_ L'ELEVAZIONE \_ DEI PULSANTI \_ \_ SET \_ TDM**](tdm-set-button-elevation-required-state.md) | Specifica se un determinato pulsante della finestra di dialogo attività o un collegamento di comando deve avere un'icona di schermatura controllo dell'account utente. indica se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi. <br/> |
| [**TESTO DELL'ELEMENTO SET TDM \_ \_ \_**](tdm-set-element-text.md)                                         | Aggiorna un elemento di testo in una finestra di dialogo attività.<br/>                                                                                                                                                  |
| [**INDICATORE DI STATO \_ DEL \_ SET MARQUEE \_ TDM \_**](tdm-set-marquee-progress-bar.md)                        | Indica se l'indicatore di stato ospitato deve essere visualizzato in modalità di selezione.<br/>                                                                                                            |
| [**SELEZIONE INDICATORE DI STATO SET TDM \_ \_ \_ \_**](tdm-set-progress-bar-marquee.md)                        | Avvia e arresta la visualizzazione del riquadro di selezione dell'indicatore di stato e imposta la velocità del rettangolo di selezione.<br/>                                                                                              |
| [**POS INDICATORE DI STATO SET TDM \_ \_ \_ \_**](tdm-set-progress-bar-pos.md)                                | Imposta la posizione corrente per un indicatore di stato.<br/>                                                                                                                                             |
| [**TDM \_ SET \_ PROGRESS \_ BAR \_ RANGE**](tdm-set-progress-bar-range.md)                            | Imposta i valori minimo e massimo per l'indicatore di stato ospitato.<br/>                                                                                                                          |
| [**TDM \_ SET \_ PROGRESS \_ BAR \_ STATE**](tdm-set-progress-bar-state.md)                            | Imposta lo stato corrente dell'indicatore di stato.<br/>                                                                                                                                               |
| [**TESTO DELL'ELEMENTO \_ UPDATE \_ TDM \_**](tdm-update-element-text.md)                                   | Aggiorna un elemento di testo in una finestra di dialogo attività. <br/>                                                                                                                                                 |
| [**ICONA DI AGGIORNAMENTO \_ \_ TDM**](tdm-update-icon.md)                                                    | Aggiorna l'icona di una finestra di dialogo attività. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                           | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PULSANTE TDN \_ SU CUI È STATO FATTO \_ CLIC](tdn-button-clicked.md)                  | Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento di comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                   |
| [TDN \_ CREATO](tdn-created.md)                                 | Inviato da una finestra di dialogo attività dopo che la finestra di dialogo attività è stata creata e prima che venga visualizzata. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [TDN \_ ELIMINATO](tdn-destroyed.md)                             | Inviato da una finestra di dialogo attività quando viene eliminato e il relativo handle di finestra non è più valido. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                       |
| [FINESTRA DI DIALOGO TDN \_ \_ COSTRUITA](tdn-dialog-constructed.md)          | Inviato da una finestra di dialogo attività dopo che la finestra di dialogo attività è stata creata e prima che venga visualizzata. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [PULSANTE EXPANDO TDN \_ SU CUI È STATO FATTO \_ \_ CLIC](tdn-expando-button-clicked.md) | Inviato da una finestra di dialogo attività quando l'utente fa clic sul pulsante expando della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                            |
| [Guida di TDN \_](tdn-help.md)                                       | Inviato da una finestra di dialogo di attività quando l'utente preme F1 sulla tastiera mentre la finestra di dialogo dell'attività ha lo stato attivo. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                            |
| [COLLEGAMENTO IPERTESTUALE TDN \_ \_ SELEZIONATO](tdn-hyperlink-clicked.md)            | Inviato da una finestra di dialogo attività quando l'utente fa clic su un collegamento ipertestuale nel contenuto della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                        |
| [TDN \_ ESPLORATO](tdn-navigated.md)                             | Inviato da una finestra di dialogo attività quando si è verificata una navigazione. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                                                     |
| [PULSANTE DI OPZIONE TDN \_ \_ \_ SELEZIONATO](tdn-radio-button-clicked.md)     | Inviato da una finestra di dialogo attività quando l'utente seleziona un pulsante o un collegamento di comando nella finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [TDN \_ TIMER](tdn-timer.md)                                     | Inviato da una finestra di dialogo attività circa ogni 200 millisecondi. Questo codice di notifica viene inviato quando il flag TIMER CALLBACK TDF è stato impostato nel membro \_ \_ **dwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) passato alla [**funzione TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il **metodo TaskDialogIndirect.**<br/> |
| [VERIFICA TDN \_ SU CUI È STATO FATTO \_ CLIC](tdn-verification-clicked.md)      | Inviato dalla finestra di dialogo attività quando l'utente fa clic sulla casella di controllo di verifica della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il [**metodo TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Strutture



| Argomento                                           | Contenuto                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PULSANTE \_ TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contiene informazioni utilizzate per visualizzare un pulsante in una finestra di dialogo attività. La [**struttura TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usa questa struttura.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contiene informazioni utilizzate per visualizzare una finestra di dialogo attività. La [**funzione TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) usa questa struttura.<br/>          |



 

 

