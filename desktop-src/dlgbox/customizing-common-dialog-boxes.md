---
title: Personalizzazione delle finestre di dialogo comuni
description: In questo argomento viene illustrato come utilizzare le finestre di dialogo comuni.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Libreria finestra di dialogo comune, personalizzazione
- finestre di dialogo comuni, personalizzazione
- personalizzazione delle finestre di dialogo comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7eaa71c4f6fc6aa038ef150eb53935f6b3ec280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399616"
---
# <a name="customizing-common-dialog-boxes"></a>Personalizzazione delle finestre di dialogo comuni

È possibile usare le finestre di dialogo comuni nel formato standard oppure è possibile personalizzarle. Dal punto di vista dell'utente, il vantaggio principale della finestra di dialogo comune è l'aspetto e la funzionalità coerenti dell'applicazione all'applicazione. È pertanto importante personalizzare una finestra di dialogo comune solo quando è assolutamente necessaria per un'applicazione. In caso contrario, l'aspetto coerente e l'interfaccia di codifica semplice andranno perduti. Le personalizzazioni appropriate lasciano intatto il maggior numero possibile di controlli originali. L'aumento delle dimensioni della finestra di dialogo o l'aggiunta di nuovi controlli nello spazio già disponibile nella finestra di dialogo è una personalizzazione appropriata. Nascondere i controlli originali o modificare in altro modo la funzionalità desiderata dei controlli originali è una personalizzazione meno appropriata.

In questa sezione vengono illustrati i metodi seguenti per la personalizzazione di una finestra di dialogo comune:

-   [Modelli personalizzati](#custom-templates)
-   [Procedure hook per le finestre di dialogo comuni](#hook-procedures-for-common-dialog-boxes)
-   [Messaggi comuni della finestra di dialogo](#common-dialog-messages)
-   [Supporto della Guida](#help-support)
    -   [Guida sensibile al contesto](#context-sensitive-help)
    -   [Pulsante ?](#the-help-button)

## <a name="custom-templates"></a>Modelli personalizzati

Nelle finestre di dialogo comuni sono disponibili modelli predefiniti che definiscono il numero, il tipo e la posizione dei controlli standard nella finestra di dialogo. È possibile definire un modello personalizzato per concedere agli utenti l'accesso a controlli aggiuntivi che sono univoci per l'applicazione.

Per tutte le finestre di dialogo comuni ad eccezione delle finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse, è possibile modificare il modello predefinito per creare un modello personalizzato che sostituisce il modello predefinito. Il modello personalizzato definisce il tipo e la posizione dei controlli standard, oltre a eventuali controlli aggiuntivi.

Quando si crea un modello di finestra di dialogo personalizzato modificando il modello predefinito della finestra di dialogo, verificare che gli identificatori per i controlli aggiunti siano univoci e non siano in conflitto con gli identificatori dei controlli standard. Nella tabella seguente sono elencati il nome del file di modello predefinito e il file di inclusione per ognuno dei tipi di finestra di dialogo comuni.



| Tipo di finestra di dialogo               | File modello | File di inclusione |
|-------------------------------|---------------|--------------|
| **Colore**                     | Color. dlg     | ColorDlg. h   |
| **Find**                      | FindText. dlg  | Dlgs. h       |
| **Carattere**                      | Font. dlg      | Dlgs. h       |
| **Apri** (selezione multipla) | FileOpen. dlg  | Dlgs. h       |
| **Apri** (selezione singola)   | FileOpen. dlg  | Dlgs. h       |
| **Imposta pagina**                | Prnsetup. dlg  | Dlgs. h       |
| **Stampa**                     | Prnsetup. dlg  | Dlgs. h       |
| **Imposta di stampa** (obsoleto)    | Prnsetup. dlg  | Dlgs. h       |
| **Replace**                   | FindText. dlg  | Dlgs. h       |



 

Per abilitare un modello personalizzato, è necessario impostare un flag nel membro **Flags** della struttura corrispondente per la finestra di dialogo. Se il modello è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare un flag **ENABLETEMPLATE** nel membro **Flags** e usare i membri **HINSTANCE** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa. Se il modello è già in memoria, impostare un flag **ENABLETEMPLATEHANDLE** nel membro **Flags** e usare il membro **HINSTANCE** per identificare l'oggetto Memory che contiene il modello.

Nella maggior parte dei casi, è necessario abilitare anche una procedura di hook per la finestra di dialogo per supportare ed elaborare l'input per i controlli aggiuntivi nel modello personalizzato.

Per le finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse, i modelli predefiniti non sono disponibili per la modifica. Al contrario, il modello personalizzato definisce una finestra di dialogo figlio che include solo gli elementi da aggiungere alla finestra di dialogo standard. Il modello personalizzato può anche definire un controllo statico che specifica il percorso del cluster di controlli standard nella finestra di dialogo figlio. Per ulteriori informazioni, vedere [modelli personalizzati di tipo Esplora risorse](open-and-save-as-dialog-boxes.md).

## <a name="hook-procedures-for-common-dialog-boxes"></a>Procedure hook per le finestre di dialogo comuni

Per ognuna delle finestre di dialogo comuni, è possibile abilitare una procedura hook per elaborare i messaggi dalla procedura predefinita della finestra di dialogo. Esistono due tipi generali di procedure comuni di hook della finestra di dialogo:

-   Procedura di hook standard utilizzata con le finestre di dialogo più comuni
-   Procedura di hook di tipo Esplora risorse supportata dalle finestre di dialogo **Apri** e **Salva con nome**

Quando si fornisce una procedura di Hook Standard per una delle finestre di dialogo comuni, la routine della finestra di dialogo predefinita gestisce i messaggi nel modo seguente.



| Message                                 | Gestione                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_INITDIALOG WM**](wm-initdialog.md) | La routine predefinita della finestra di dialogo elabora il messaggio prima di passarlo alla routine hook. Il parametro *lParam* del messaggio è un puntatore alla struttura di inizializzazione specificata al momento della creazione della finestra di dialogo. |
| Tutti gli altri messaggi                      | La routine hook riceve prima il messaggio. Quindi, il valore restituito della routine hook determina se la routine della finestra di dialogo predefinita elabora il messaggio o lo ignora.                                     |



 

Per le finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse, la routine hook non riceve messaggi destinati ai controlli standard nella finestra di dialogo. Al contrario, riceve i messaggi di notifica dalla finestra di dialogo e i messaggi per qualsiasi altro controllo definito in un modello personalizzato. Per ulteriori informazioni, vedere [procedure hook di tipo Esplora risorse](open-and-save-as-dialog-boxes.md).

Per abilitare una routine hook, impostare un valore **ENABLEHOOK** nel membro **Flags** della struttura corrispondente per la finestra di dialogo. Se è impostato un flag **ENABLEHOOK** , è necessario che un membro **lpfnHook** della struttura specifichi l'indirizzo della routine hook.

Nella tabella seguente viene illustrato il tipo di routine hook da fornire per ognuna delle finestre di dialogo comuni.



| Tipo di finestra di dialogo                          | Routine hook                                      |
|------------------------------------------|-----------------------------------------------------|
| **Colore**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Trova** o **Sostituisci**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Carattere**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Apri** o **Salva con nome** (stile Explorer) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Apri** o **Salva con nome** (obsoleto)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Stampa**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Imposta pagina**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Per la finestra di dialogo **Imposta pagina** , è anche possibile specificare una procedura hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) . Si tratta di una procedura di hook speciale che è possibile utilizzare per personalizzare l'aspetto della pagina di esempio visualizzata dalla finestra di dialogo **Imposta pagina** .

> [!Note]  
> La finestra di dialogo imposta **stampa** è stata sostituita dalla finestra di dialogo **Imposta pagina** . Le applicazioni devono utilizzare la finestra di dialogo **Imposta pagina** . Tuttavia, per compatibilità, la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) continua a supportare la visualizzazione della finestra di dialogo di **installazione di stampa** . È possibile specificare una procedura di hook [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) per la finestra di dialogo **Imposta stampa** .

 

## <a name="common-dialog-messages"></a>Messaggi comuni della finestra di dialogo

Nelle finestre di dialogo comuni vengono utilizzati messaggi per notificare alla routine della finestra o all'hook la procedura quando si verificano determinati eventi. Sono inoltre disponibili messaggi che è possibile inviare a una finestra di dialogo comune per recuperare informazioni o controllare il comportamento o l'aspetto della finestra di dialogo. In questa sezione vengono descritti i messaggi di dialogo comuni registrati dalla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , i messaggi utilizzati dalla finestra di dialogo **tipo di carattere** e la finestra di dialogo **Imposta pagina** e i messaggi utilizzati dalle finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse.

La libreria finestra di dialogo comune definisce un set di stringhe di messaggio. È possibile passare una costante associata a una di queste stringhe di messaggio a [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore del messaggio. È quindi possibile utilizzare l'identificatore per rilevare ed elaborare i messaggi inviati da una finestra di dialogo comune o per inviare messaggi a una finestra di dialogo comune. Nella tabella seguente vengono illustrate le costanti del messaggio e ne viene descritto l'utilizzo.



| Contante                               | Uso                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Una finestra di dialogo **colore** Invia questo messaggio alla procedura hook quando l'utente seleziona un colore e fa clic sul pulsante **OK** . La routine hook può accettare il colore o rifiutarla e forzare la finestra di dialogo in modo che rimanga aperta.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Una finestra di dialogo **Apri** o **Salva con** nome Invia questo messaggio alla procedura hook quando l'utente seleziona un nome file e fa clic sul pulsante **OK** . La procedura di hook può accettare il nome del file o rifiutarla e forzare la finestra di dialogo in modo che rimanga aperta. Per le finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse, questo messaggio è stato sostituito dal messaggio di notifica [**\_ FILEOK**](cdn-fileok.md) della rete CDN.<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Una finestra di dialogo **trova** o **Sostituisci** Invia questo messaggio alla routine della finestra della finestra padre quando l'utente fa clic sulla finestra di dialogo **Trova successivo**, **Sostituisci** o **Sostituisci tutto** oppure chiude la finestra di dialogo. Il parametro *lParam* del messaggio è un puntatore a una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) contenente l'input dell'utente.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Tutte le finestre di dialogo comuni inviano questo messaggio alla routine della finestra della finestra padre quando l'utente fa clic sul pulsante della **Guida** . Per le finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse, questo messaggio è stato sostituito dal messaggio di notifica della [**\_ Guida**](cdn-help.md) della rete CDN.<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Una finestra di dialogo **Apri** o **Salva con** nome Invia questo messaggio alla procedura hook quando l'utente modifica la selezione nella casella di riepilogo **nome file** . Per le finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse, questo messaggio è stato sostituito dal messaggio di notifica [**\_ selChange**](cdn-selchange.md) della rete CDN.<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Una procedura hook può inviare questo messaggio a una finestra di dialogo **colore** per impostare la selezione del colore corrente.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Una finestra di dialogo **Apri** o **Salva con nome** Invia questo messaggio alla procedura hook se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante **OK** . Per le finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse, questo messaggio è stato sostituito dal messaggio di notifica [**\_ SHAREVIOLATION**](cdn-shareviolation.md) della rete CDN.<br/>                                                        |



 

Alcune finestre di dialogo comuni inviano e ricevono altri messaggi della finestra. La procedura hook per una finestra di dialogo **tipo di carattere** può inviare qualsiasi messaggio **WM \_ ChooseFont \_ \*** alla finestra di dialogo **tipo di carattere** . Per ulteriori informazioni, vedere finestra di [dialogo tipo di carattere](font-dialog-box.md). Se è stata abilitata una procedura [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Hook, la finestra di dialogo **Imposta pagina** invia i messaggi di **WM \_ PSD \_ \*** . Per ulteriori informazioni, vedere finestra di [dialogo Imposta pagina](page-setup-dialog-box.md).

Le finestre di dialogo **Apri** e **Salva con nome di** tipo Esplora risorse supportano un set di messaggi predefiniti. Sono inclusi i messaggi di notifica inviati sotto forma di un messaggio di [**\_ notifica WM**](../controls/wm-notify.md) alla routine hook e i messaggi che la procedura di hook può inviare alla finestra di dialogo. Per un elenco completo di questi messaggi, vedere [procedure hook di tipo Esplora risorse](open-and-save-as-dialog-boxes.md).

## <a name="help-support"></a>Supporto della Guida

Le finestre di dialogo comuni forniscono la Guida sensibile al contesto per i controlli standard della finestra di dialogo. Per fornire una Guida aggiuntiva per una finestra di dialogo comune, è possibile visualizzare un pulsante della **Guida** ed elaborare i messaggi generati quando l'utente fa clic sul pulsante. Il pulsante della **Guida** è un supplemento alla Guida sensibile al contesto predefinita. Il **pulsante?** è utile per descrivere lo scopo generale della finestra di dialogo che si applica all'applicazione.

-   [Guida sensibile al contesto](#context-sensitive-help)
-   [Pulsante ?](#the-help-button)

### <a name="context-sensitive-help"></a>Guida Context-Sensitive

Tutte le finestre di dialogo comuni forniscono la Guida sensibile al contesto per i controlli standard della finestra di dialogo. L'utente può visualizzare la guida per i singoli controlli mediante uno dei metodi seguenti:

-   Selezione del controllo e pressione del tasto F1.
-   Fare clic su **?** nella barra del titolo e quindi facendo clic su un controllo.
-   Fare clic con il pulsante destro del mouse su un controllo.

Se si personalizza una finestra di dialogo aggiungendo nuovi controlli, è necessario estendere anche il supporto della Guida per questi controlli elaborando le richieste di supporto nella procedura hook. La routine hook riceve i messaggi seguenti quando l'utente richiede la guida.



| Azione utente                                                           | Message                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Fare clic con il pulsante destro del mouse su un controllo.                          | [**ContextMenu di WM \_**](/windows/desktop/menurc/wm-contextmenu) |
| Premere il tasto F1.                                                   | [**Guida di WM \_**](../shell/wm-help.md)               |
| Fai clic sul pulsante **?** sulla barra del titolo, quindi fare clic su un controllo. | [**Guida di WM \_**](../shell/wm-help.md)               |



 

È necessario elaborare questi messaggi per i controlli aggiunti, ma lasciare che la routine della finestra di dialogo predefinita elabori i messaggi per i controlli standard. Per ulteriori informazioni su come elaborare questi messaggi, vedere la [Guida](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85))di.

### <a name="the-help-button"></a>Pulsante ?

È possibile visualizzare un pulsante della **Guida** in una delle finestre di dialogo comuni impostando un valore **SHOWHELP** nel membro **Flags** della struttura di inizializzazione per la finestra di dialogo. Se viene visualizzato il **pulsante?** , è necessario elaborare la richiesta dell'utente per la guida. L'elaborazione può essere eseguita in una delle routine della finestra dell'applicazione o in una procedura di hook per la finestra di dialogo. In genere, la richiesta di assistenza viene elaborata chiamando la funzione [**WinHelp**](/windows/win32/api/winuser/nf-winuser-winhelpa) .

Per elaborare i messaggi della Guida in una delle routine della finestra, è necessario ottenere un identificatore di messaggio per la stringa definita dal valore [**HELPMSGSTRING**](helpmsgstring.md) e identificare la finestra per la ricezione dei messaggi. Per ottenere l'identificatore del messaggio, specificare **HELPMSGSTRING** come parametro in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) . Quando si crea la finestra di dialogo, utilizzare il membro **hwndOwner** della struttura di inizializzazione della finestra di dialogo per identificare la finestra che riceverà i messaggi. La routine della finestra di dialogo Invia il messaggio alla routine della finestra ogni volta che l'utente fa clic sul pulsante della **Guida** .

Per elaborare i messaggi della Guida in una procedura hook, è necessario elaborare il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . La routine hook fornisce la guida se il parametro *wParam* di questo messaggio indica che l'utente ha fatto clic **sul pulsante?** . **L'identificatore del pulsante?** è la costante **pshHelp** definita nel file Dlgs. h.

Le procedure hook per le finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse non ricevono i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per il pulsante **Guida** . Al contrario, la finestra di dialogo Invia un messaggio di notifica della [**\_ Guida**](cdn-help.md) della rete CDN alla procedura hook quando si fa clic **sul pulsante?** .

 

