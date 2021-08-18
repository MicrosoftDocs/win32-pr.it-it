---
title: Finestra delle proprietà
description: Questa sezione contiene informazioni sugli elementi di programmazione utilizzati con le finestre delle proprietà.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50661ece6985c16f299b514fa59068bf06f115b49c0f0bbea783cf637c2c921
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826031"
---
# <a name="property-sheet"></a>Finestra delle proprietà

Questa sezione contiene informazioni sugli elementi di programmazione utilizzati con le finestre delle proprietà.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                              | Contenuto                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle finestre delle proprietà](property-sheets.md)       | Una *finestra delle proprietà* è una finestra che consente all'utente di visualizzare e modificare le proprietà di un elemento.<br/>                  |
| [Creazione guidata](wizards.md)                    | Una procedura guidata è un tipo di finestra delle proprietà che offre un modo semplice e potente per guidare gli utenti attraverso una procedura.<br/> |
| [Uso delle finestre delle proprietà](using-property-sheets.md) | In questa sezione vengono fornite informazioni dettagliate sull'implementazione e codice di esempio per l'utilizzo delle finestre delle proprietà.<br/>                     |



 

### <a name="functions"></a>Funzioni



| Argomento                                                        | Contenuto                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Specifica una funzione di callback definita dall'applicazione utilizzata da un'estensione della finestra delle proprietà per aggiungere una pagina a una finestra delle proprietà.<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Crea una nuova pagina per una finestra delle proprietà.<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Elimina una pagina della finestra delle proprietà. Un'applicazione deve chiamare questa funzione per le pagine che non sono state passate alla [**funzione PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)<br/>                                                                              |
| [**Propertysheets**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Crea una finestra delle proprietà e aggiunge le pagine definite nella struttura di intestazione della finestra delle proprietà specificata.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Specifica una funzione di callback definita dall'applicazione chiamata da una finestra delle proprietà quando viene creata una pagina e quando sta per essere distrutta. Un'applicazione può usare questa funzione per eseguire operazioni di inizializzazione e pulizia per la pagina.<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Funzione di callback definita dall'applicazione chiamata dal sistema durante la creazione e l'inizializzazione della finestra delle proprietà.<br/>                                                                                                                        |



 

### <a name="messages"></a>Messaggi



| Argomento                                                               | Contenuto                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PSM \_ ADDPAGE**](psm-addpage.md)                                 | Aggiunge una nuova pagina alla fine di una finestra delle proprietà esistente. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet AddPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage)<br/>                                                                                                |
| [**PSM \_ APPLY**](psm-apply.md)                                     | Simula la selezione del **pulsante Applica,** a indicare che una o più pagine sono state modificate e che le modifiche devono essere convalidate e registrate.<br/>                                                                                                                   |
| [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md)                     | Inviato da un'applicazione quando ha apportato modifiche dopo la notifica [PSN \_ APPLY](psn-apply.md) più recente che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet CancelToClose.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose)<br/> |
| [**PSM \_ MODIFICATO**](psm-changed.md)                                 | Informa una finestra delle proprietà che le informazioni in una pagina sono state modificate. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ Changed.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed)<br/>                                                                                         |
| [**PSM \_ ENABLEWIZBUTTONS**](psm-enablewizbuttons.md)               | Abilita o disabilita uno dei pulsanti standard in una procedura guidata Dio. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ EnableWizButtons di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons)<br/>                                                                          |
| [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md)           | Recupera un handle per la finestra della pagina corrente di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet GetCurrentPageHwnd.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd)<br/>                                                          |
| [**PSM \_ GETRESULT**](psm-getresult.md)                             | Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali [**da PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet GetResult.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)<br/>                 |
| [**PSM \_ GETTABCONTROL**](psm-gettabcontrol.md)                     | Recupera l'handle per il controllo Struttura a schede di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ GetTabControl di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol)<br/>                                                                                 |
| [**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)                         | Accetta l'handle della finestra della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet HwndToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex)<br/>                                                                  |
| [**PSM \_ IDTOINDEX**](psm-idtoindex.md)                             | Accetta l'ID risorsa di una pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet IdToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex)<br/>                                                                          |
| [**PSM \_ INDEXTOHWND**](psm-indextohwnd.md)                         | Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle di finestra. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet IndexToHwnd.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd)<br/>                                                                               |
| [**PSM \_ INDEXTOID**](psm-indextoid.md)                             | Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo ID risorsa. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet IndexToId.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid)<br/>                                                                                     |
| [**PSM \_ INDEXTOPAGE**](psm-indextopage.md)                         | Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle HPROPSHEETPAGE. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet IndexToPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage)<br/>                                                                       |
| [**PSM \_ INSERTPAGE**](psm-insertpage.md)                           | Inserisce una nuova pagina in una finestra delle proprietà esistente. La pagina può essere inserita in corrispondenza di un indice specificato o dopo una pagina specificata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ InsertPage di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage)<br/>                |
| [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md)                 | Passa un messaggio a una finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ IsDialogMessage di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage)<br/>                              |
| [**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)                         | Accetta l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PageToIndex di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex)<br/>                                                          |
| [**PSM \_ PRESSBUTTON**](psm-pressbutton.md)                         | Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PressButton di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton)<br/>                                                                                              |
| [**QUERY \_ PSMIBLINGS**](psm-querysiblings.md)                     | Inviato a una finestra delle proprietà, che inoltra quindi il messaggio a ognuna delle relative pagine. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet QuerySiblings.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings)<br/>                                                              |
| [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md)                       | Indica che è necessario riavviare il sistema per l'applicazione delle modifiche. È possibile inviare il [**messaggio \_ REBOOTSYSTEM PSM**](psm-rebootsystem.md) in modo esplicito o tramite la macro [**\_ RebootSystem di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem)<br/>                        |
| [**PSM \_ RECALCPAGESIZES**](psm-recalcpagesizes.md)                 | Ricalcola le dimensioni della pagina di una finestra delle proprietà standard o di una procedura guidata dopo l'aggiunta o la rimozione di pagine. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet RecalcPageSizes.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes)<br/>                                     |
| [**PSM \_ REMOVEPAGE**](psm-removepage.md)                           | Rimuove una pagina da una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ RemovePage di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage)<br/>                                                                                                              |
| [**RIAVVIO \_ PSMWINDOWS**](psm-restartwindows.md)                   | Indica che Windows necessario riavviare l'applicazione delle modifiche.<br/>                                                                                                                                                                                         |
| [**PSM \_ SETBUTTONTEXT**](psm-setbuttontext.md)                     | Imposta il testo di un pulsante in una procedura guidata DiMita. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ PropSheet SetButtonText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext)<br/>                                                                                                 |
| [**PSM \_ SETCURSEL**](psm-setcursel.md)                             | Attiva la pagina specificata in una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetCurSel.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel)<br/>                                                                                                    |
| [**PSM \_ SETCURSELID**](psm-setcurselid.md)                         | Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetCurSelByID.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid)<br/>                                                   |
| [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md)                     | Imposta il testo del **pulsante Fine** in una procedura guidata, visualizza e abilita il pulsante e nasconde i **pulsanti** Avanti **e** Indietro. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetFinishText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext)<br/>               |
| [**PSM \_ SETHEADERBITMAP**](psm-setheaderbitmap.md)                 | Questo messaggio non è implementato.<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERBITMAPRESOURCE**](psm-setheaderbitmapresource.md) | Questo messaggio non è implementato.<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERSUBTITLE**](psm-setheadersubtitle.md)             | Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet SetHeaderSubTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle)<br/>                                                                        |
| [**PSM \_ SETHEADERTITLE**](psm-setheadertitle.md)                   | Imposta il testo del titolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet SetHeaderTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle)<br/>                                                                                 |
| [**PSM \_ SETNEXTTEXT**](psm-setnexttext.md)                         | Imposta il testo del **pulsante Avanti** in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetNextText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext)<br/>                                                                                                |
| [**PSM \_ SETTITLE**](psm-settitle.md)                               | Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle)<br/>                                                                                                                    |
| [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md)                     | Abilita o disabilita i **pulsanti Indietro**, **Avanti** **e** Fine in una procedura guidata. È anche possibile usare la macro [**\_ SetWizButtons di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) per pubblicare il messaggio.<br/>                                                                          |
| [**PSM \_ SHOWWIZBUTTONS**](psm-showwizbuttons.md)                   | Mostra o nasconde i pulsanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ShowWizButtons di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons)<br/>                                                                                                        |
| [**PSM \_ UNCHANGED**](psm-unchanged.md)                             | Informa una finestra delle proprietà che le informazioni in una pagina sono state ripristinate allo stato salvato in precedenza. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ UnChanged.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged)<br/>                                                      |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                     | Contenuto                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN \_ APPLY](psn-apply.md)                               | Inviato a ogni pagina nella finestra delle proprietà per indicare che l'utente ha fatto clic sul pulsante OK, Chiudi o Applica e vuole che tutte le modifiche appartienino. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>      |
| [PSN \_ GETOBJECT](psn-getobject.md)                       | Inviato da una finestra delle proprietà per richiedere un oggetto destinazione di rilascio quando il cursore passa su uno dei pulsanti del controllo Struttura a schede.<br/>                                                                                                                       |
| [GUIDA \_ DI PSN](psn-help.md)                                 | Notifica a una pagina che l'utente ha fatto clic sul pulsante ? . Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                          |
| [PSN \_ KILLACTIVE](psn-killactive.md)                     | Notifica a una pagina che sta per perdere l'attivazione perché è in corso l'attivazione di un'altra pagina o l'utente ha fatto clic sul **pulsante OK.** Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>       |
| [PSN \_ QUERYCANCEL](psn-querycancel.md)                   | Indica che l'utente ha annullato la finestra delle proprietà. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                            |
| [PSN \_ QUERYINITIALFOCUS](psn-queryinitialfocus.md)       | Inviato da una finestra delle proprietà per fornire a una pagina della finestra delle proprietà la possibilità di specificare quale controllo della finestra di dialogo deve ricevere lo stato attivo iniziale. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>           |
| [PSN \_ RESET](psn-reset.md)                               | Notifica a una pagina che la finestra delle proprietà sta per essere distrutta. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                   |
| [PSN \_ SETACTIVE](psn-setactive.md)                       | Notifica a una pagina che sta per essere attivata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                                   |
| [PSN \_ TRANSLATEACCELERATOR](psn-translateaccelerator.md) | Notifica a una finestra delle proprietà che è stato ricevuto un messaggio della tastiera. Offre alla pagina la possibilità di eseguire la traduzione privata dei tasti di scelta rapida. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/> |
| [PSN \_ WIZBACK](psn-wizback.md)                           | Notifica a una pagina che l'utente ha fatto clic sul **pulsante** Indietro in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                          |
| [PSN \_ WIZFINISH](psn-wizfinish.md)                       | Notifica a una pagina che l'utente ha fatto clic sul **pulsante** Fine in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                        |
| [PSN \_ WIZNEXT](psn-wiznext.md)                           | Notifica a una pagina che l'utente ha fatto clic sul **pulsante** Avanti in una procedura guidata. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                          |



 

### <a name="structures"></a>Strutture



| Argomento                                      | Contenuto                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Definisce il frame e le pagine di una finestra delle proprietà.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Definisce una pagina in una finestra delle proprietà.<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Contiene informazioni per i codici di notifica della finestra delle proprietà.<br/> |



 

 

