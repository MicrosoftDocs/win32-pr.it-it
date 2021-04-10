---
title: Finestra delle proprietà
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con le finestre delle proprietà.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c42b7b4c1be7d0dc11613da36f78abbad847d6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963479"
---
# <a name="property-sheet"></a>Finestra delle proprietà

Questa sezione contiene informazioni sugli elementi di programmazione usati con le finestre delle proprietà.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                              | Contenuto                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle finestre delle proprietà](property-sheets.md)       | Una finestra delle *Proprietà* è una finestra che consente all'utente di visualizzare e modificare le proprietà di un elemento.<br/>                  |
| [Creazione di procedure guidate](wizards.md)                    | Una procedura guidata è un tipo di finestra delle proprietà che fornisce un modo semplice e potente per guidare gli utenti attraverso una procedura.<br/> |
| [Utilizzo delle finestre delle proprietà](using-property-sheets.md) | In questa sezione vengono fornite informazioni dettagliate sull'implementazione e codice di esempio per l'utilizzo delle finestre delle proprietà.<br/>                     |



 

### <a name="functions"></a>Funzioni



| Argomento                                                        | Contenuto                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Specifica una funzione di callback definita dall'applicazione utilizzata da un'estensione della finestra delle proprietà per aggiungere una pagina a una finestra delle proprietà.<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Crea una nuova pagina per una finestra delle proprietà.<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Elimina definitivamente una pagina della finestra delle proprietà. Un'applicazione deve chiamare questa funzione per le pagine che non sono state passate alla funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .<br/>                                                                              |
| [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Crea una finestra delle proprietà e aggiunge le pagine definite nella struttura dell'intestazione della finestra delle proprietà specificata.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Specifica una funzione di callback definita dall'applicazione che viene chiamata da una finestra delle proprietà quando viene creata una pagina e quando sta per essere eliminata definitivamente. Un'applicazione può usare questa funzione per eseguire operazioni di inizializzazione e pulizia per la pagina.<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Funzione di callback definita dall'applicazione chiamata dal sistema durante la creazione e l'inizializzazione della finestra delle proprietà.<br/>                                                                                                                        |



 

### <a name="messages"></a>Messaggi



| Argomento                                                               | Contenuto                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDPAGE di PSM \_**](psm-addpage.md)                                 | Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o usando la macro [**PropSheet di \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .<br/>                                                                                                |
| [**\_applicazione PSM**](psm-apply.md)                                     | Simula la selezione del pulsante **applica** , che indica che una o più pagine sono state modificate ed è necessario convalidare e registrare le modifiche.<br/>                                                                                                                   |
| [**CANCELTOCLOSE di PSM \_**](psm-canceltoclose.md)                     | Inviato da un'applicazione quando ha eseguito modifiche dopo la notifica di applicazione [PSN \_ ](psn-apply.md) più recente che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .<br/> |
| [**PSM \_ modificato**](psm-changed.md)                                 | Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ modificata**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .<br/>                                                                                         |
| [**ENABLEWIZBUTTONS di PSM \_**](psm-enablewizbuttons.md)               | Abilita o Disabilita uno dei pulsanti standard in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ EnableWizButtons di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .<br/>                                                                          |
| [**GETCURRENTPAGEHWND di PSM \_**](psm-getcurrentpagehwnd.md)           | Recupera un handle per la finestra della pagina corrente di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .<br/>                                                          |
| [**RISULTATO di PSM \_**](psm-getresult.md)                             | Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetResult PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .<br/>                 |
| [**PSM \_ GETtabcontrol**](psm-gettabcontrol.md)                     | Recupera l'handle per il controllo struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o usando la macro [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .<br/>                                                                                 |
| [**HWNDTOINDEX di PSM \_**](psm-hwndtoindex.md)                         | Accetta l'handle della finestra della pagina delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ HwndToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .<br/>                                                                  |
| [**IDTOINDEX di PSM \_**](psm-idtoindex.md)                             | Accetta l'ID di una pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IdToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .<br/>                                                                          |
| [**INDEXTOHWND di PSM \_**](psm-indextohwnd.md)                         | Accetta l'indice di una pagina della finestra delle proprietà e restituisce l'handle della finestra. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToHwnd di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .<br/>                                                                               |
| [**INDEXTOID di PSM \_**](psm-indextoid.md)                             | Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID di risorsa. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToId di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .<br/>                                                                                     |
| [**INDEXTOPAGE di PSM \_**](psm-indextopage.md)                         | Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle HPROPSHEETPAGE. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToPage di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .<br/>                                                                       |
| [**INSERTPAGE di PSM \_**](psm-insertpage.md)                           | Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .<br/>                |
| [**ISDIALOGMESSAGE di PSM \_**](psm-isdialogmessage.md)                 | Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .<br/>                              |
| [**PAGETOINDEX di PSM \_**](psm-pagetoindex.md)                         | Accetta l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PageToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .<br/>                                                          |
| [**PRESSBUTTON di PSM \_**](psm-pressbutton.md)                         | Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .<br/>                                                                                              |
| [**QUERYSIBLINGS di PSM \_**](psm-querysiblings.md)                     | Inviato a una finestra delle proprietà che quindi inoltra il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .<br/>                                                              |
| [**REBOOTSYSTEM di PSM \_**](psm-rebootsystem.md)                       | Indica che è necessario riavviare il sistema per rendere effettive le modifiche. È possibile inviare il messaggio [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) in modo esplicito o usando la macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .<br/>                        |
| [**RECALCPAGESIZES di PSM \_**](psm-recalcpagesizes.md)                 | Ricalcola le dimensioni di pagina di una finestra delle proprietà standard o della procedura guidata dopo l'aggiunta o la rimozione di pagine. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ RecalcPageSizes di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .<br/>                                     |
| [**REMOVEPAGE di PSM \_**](psm-removepage.md)                           | Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .<br/>                                                                                                              |
| [**RESTARTWINDOWS di PSM \_**](psm-restartwindows.md)                   | Indica che è necessario riavviare Windows per rendere effettive le modifiche.<br/>                                                                                                                                                                                         |
| [**SETBUTTONTEXT di PSM \_**](psm-setbuttontext.md)                     | Imposta il testo su un pulsante in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .<br/>                                                                                                 |
| [**di \_ PSM**](psm-setcursel.md)                             | Attiva la pagina specificata in una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .<br/>                                                                                                    |
| [**SETCURSELID di PSM \_**](psm-setcurselid.md)                         | Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .<br/>                                                   |
| [**SETFINISHTEXT di PSM \_**](psm-setfinishtext.md)                     | Imposta il testo del pulsante **fine** in una procedura guidata, Mostra e Abilita il pulsante e nasconde i pulsanti **Avanti** e **indietro** . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .<br/>               |
| [**SETHEADERBITMAP di PSM \_**](psm-setheaderbitmap.md)                 | Questo messaggio non è implementato.<br/>                                                                                                                                                                                                                                     |
| [**SETHEADERBITMAPRESOURCE di PSM \_**](psm-setheaderbitmapresource.md) | Questo messaggio non è implementato.<br/>                                                                                                                                                                                                                                     |
| [**SETHEADERSUBTITLE di PSM \_**](psm-setheadersubtitle.md)             | Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHeaderSubTitle di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .<br/>                                                                        |
| [**SETHEADERTITLE di PSM \_**](psm-setheadertitle.md)                   | Imposta il testo del titolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHeaderTitle di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .<br/>                                                                                 |
| [**SETNEXTTEXT di PSM \_**](psm-setnexttext.md)                         | Imposta il testo del pulsante **Avanti** in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .<br/>                                                                                                |
| [**\_nome del titolo PSM**](psm-settitle.md)                               | Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .<br/>                                                                                                                    |
| [**SETWIZBUTTONS di PSM \_**](psm-setwizbuttons.md)                     | Abilita o Disabilita i pulsanti **indietro**, **Avanti** e **fine** in una procedura guidata. È anche possibile usare la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per inviare il messaggio.<br/>                                                                          |
| [**SHOWWIZBUTTONS di PSM \_**](psm-showwizbuttons.md)                   | Consente di visualizzare o nascondere i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .<br/>                                                                                                        |
| [**PSM non \_ modificato**](psm-unchanged.md)                             | Informa una finestra delle proprietà che le informazioni in una pagina sono state ripristinate allo stato salvato in precedenza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet non \_ modificata**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .<br/>                                                      |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                     | Contenuto                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_applica PSN](psn-apply.md)                               | Inviato a ogni pagina della finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o applica e desidera che tutte le modifiche abbiano effetto. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>      |
| [GetObject PSN \_](psn-getobject.md)                       | Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo struttura a schede.<br/>                                                                                                                       |
| [Guida di PSN \_](psn-help.md)                                 | Notifica a una pagina che l'utente ha fatto clic sul pulsante della guida. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                          |
| [\_KILLACTIVE PSN](psn-killactive.md)                     | Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o se l'utente ha fatto clic sul pulsante **OK** . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>       |
| [\_QUERYCANCEL PSN](psn-querycancel.md)                   | Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                            |
| [\_QUERYINITIALFOCUS PSN](psn-queryinitialfocus.md)       | Inviato da una finestra delle proprietà per fornire una pagina della finestra delle proprietà la possibilità di specificare quale controllo finestra di dialogo deve ricevere lo stato attivo iniziale. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>           |
| [ripristino di PSN \_](psn-reset.md)                               | Notifica a una pagina che la finestra delle proprietà sta per essere eliminata definitivamente. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                   |
| [seactive PSN \_](psn-setactive.md)                       | Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                   |
| [\_TRANSLATEACCELERATOR PSN](psn-translateaccelerator.md) | Notifica a una finestra delle proprietà che è stato ricevuto un messaggio da tastiera. Fornisce alla pagina la possibilità di eseguire la conversione dell'acceleratore di tastiera privata. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/> |
| [\_WIZBACK PSN](psn-wizback.md)                           | Notifica a una pagina che l'utente ha fatto clic sul pulsante **indietro** in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                          |
| [\_WIZFINISH PSN](psn-wizfinish.md)                       | Notifica a una pagina che l'utente ha fatto clic sul pulsante **fine** in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                        |
| [\_WIZNEXT PSN](psn-wiznext.md)                           | Notifica a una pagina che l'utente ha fatto clic sul pulsante **Avanti** in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                          |



 

### <a name="structures"></a>Strutture



| Argomento                                      | Contenuto                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Definisce il frame e le pagine di una finestra delle proprietà.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Definisce una pagina in una finestra delle proprietà.<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Contiene informazioni per i codici di notifica della finestra delle proprietà.<br/> |



 

 

