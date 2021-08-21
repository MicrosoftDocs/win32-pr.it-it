---
title: Personalizzazione di finestre di dialogo comuni
description: Questo argomento illustra come usare le finestre di dialogo comuni.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Libreria di finestre di dialogo comuni, personalizzazione
- finestre di dialogo comuni, personalizzazione
- personalizzazione di finestre di dialogo comuni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6272cbff88b7544ea945851f4f347cb43031b93ae08852bc139c7fb7ca6dd91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786121"
---
# <a name="customizing-common-dialog-boxes"></a>Personalizzazione di finestre di dialogo comuni

È possibile usare le finestre di dialogo comuni nel modulo standard oppure personalizzarle. Dal punto di vista dell'utente, il vantaggio principale della finestra di dialogo comune è l'aspetto e le funzionalità coerenti da applicazione a applicazione. Pertanto, è importante personalizzare una finestra di dialogo comune solo quando è assolutamente necessaria per un'applicazione. In caso contrario, l'aspetto coerente e l'interfaccia di codifica semplice vengono persi. Le personalizzazioni appropriate lasciano intatti il maggior numero possibile di controlli originali. L'aumento delle dimensioni della finestra di dialogo o l'aggiunta di nuovi controlli nello spazio già disponibile nella finestra di dialogo è una personalizzazione appropriata. Nascondere i controlli originali o modificare in altro modo la funzionalità prevista dei controlli originali è una personalizzazione meno appropriata.

In questa sezione vengono illustrati i metodi seguenti per la personalizzazione di una finestra di dialogo comune:

-   [Modelli personalizzati](#custom-templates)
-   [Procedure hook per finestre di dialogo comuni](#hook-procedures-for-common-dialog-boxes)
-   [Messaggi di dialogo comuni](#common-dialog-messages)
-   [Supporto tecnico della Guida](#help-support)
    -   [Guida sensibile al contesto](#context-sensitive-help)
    -   [Pulsante ?](#the-help-button)

## <a name="custom-templates"></a>Modelli personalizzati

Le finestre di dialogo comuni hanno modelli predefiniti che definiscono il numero, il tipo e la posizione dei controlli standard nella finestra di dialogo. È possibile definire un modello personalizzato per concedere agli utenti l'accesso a controlli aggiuntivi univoci per l'applicazione.

Per tutte le finestre di  dialogo  comuni, ad eccezione delle finestre di dialogo Apri e Salva con nome in stile Esplora risorse, modificare il modello predefinito per creare un modello personalizzato che sostituisca il modello predefinito. Il modello personalizzato definisce il tipo e la posizione dei controlli standard, nonché eventuali controlli aggiuntivi.

Quando si crea un modello di finestra di dialogo personalizzato modificando il modello di finestra di dialogo predefinito, assicurarsi che gli identificatori per i controlli aggiunti siano univoci e non siano in conflitto con gli identificatori dei controlli standard. Nella tabella seguente sono elencati il nome del file modello predefinito e il file di inclusione per ogni tipo di finestra di dialogo comune.



| Tipo di finestra di dialogo               | File modello | File di inclusione |
|-------------------------------|---------------|--------------|
| **Colore**                     | Color.dlg     | ColorDlg.h   |
| **Find**                      | Findtext.dlg  | Dlgs.h       |
| **Font**                      | Font.dlg      | Dlgs.h       |
| **Apri** (selezione multipla) | Fileopen.dlg  | Dlgs.h       |
| **Apri** (selezione singola)   | Fileopen.dlg  | Dlgs.h       |
| **Imposta pagina**                | Prnsetup.dlg  | Dlgs.h       |
| **Stampa**                     | Prnsetup.dlg  | Dlgs.h       |
| **Impostazione di stampa** (obsoleta)    | Prnsetup.dlg  | Dlgs.h       |
| **Replace**                   | Findtext.dlg  | Dlgs.h       |



 

Per abilitare un modello personalizzato, è necessario impostare un flag nel membro **Flags** della struttura corrispondente per la finestra di dialogo. Se il modello è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare un flag **ENABLETEMPLATE** nel membro **Flags** e usare i membri **hInstance** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa. Se il modello è già in memoria, impostare un flag **ENABLETEMPLATEHANDLE** nel membro **Flags** e usare il membro **hInstance** per identificare l'oggetto memoria che contiene il modello.

Nella maggior parte dei casi, è necessario abilitare anche una procedura hook per la finestra di dialogo per supportare ed elaborare l'input per i controlli aggiuntivi nel modello personalizzato.

Per le finestre di dialogo **Apri** **e** Salva con nome in stile Esplora risorse, i modelli predefiniti non sono disponibili per la modifica. Il modello personalizzato definisce invece una finestra di dialogo figlio che include solo gli elementi da aggiungere alla finestra di dialogo standard. Il modello personalizzato può anche definire un controllo statico che specifica la posizione del cluster di controlli standard nella finestra di dialogo figlio. Per altre informazioni, vedere [Modelli personalizzati in stile Explorer.](open-and-save-as-dialog-boxes.md)

## <a name="hook-procedures-for-common-dialog-boxes"></a>Procedure hook per finestre di dialogo comuni

Per ognuna delle finestre di dialogo comuni, è possibile abilitare una procedura hook per elaborare i messaggi dalla procedura predefinita della finestra di dialogo. Esistono due tipi generali di procedure hook comuni per i dialoghe:

-   Procedura hook standard usata con le finestre di dialogo più comuni
-   Procedura hook di tipo Esplora risorse supportata dalle **finestre di** **dialogo** Apri e Salva con nome

Quando si specifica una procedura hook standard per una delle finestre di dialogo comuni, la procedura predefinita della finestra di dialogo gestisce i messaggi come indicato di seguito.



| Message                                 | Gestione                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](wm-initdialog.md) | La procedura predefinita della finestra di dialogo elabora il messaggio prima di passarlo alla procedura hook. Il parametro *lParam* del messaggio è un puntatore alla struttura di inizializzazione specificata al momento della creazione del dialogo. |
| Tutti gli altri messaggi                      | La routine hook riceve prima il messaggio. Il valore restituito della routine hook determina quindi se la procedura predefinita del dialogo elabora il messaggio o lo ignora.                                     |



 

Per le finestre di  dialogo **Apri** e Salva con nome in stile Esplora risorse, la procedura hook non riceve messaggi destinati ai controlli standard nella finestra di dialogo. Riceve invece messaggi di notifica dalla finestra di dialogo e messaggi per eventuali controlli aggiuntivi definiti in un modello personalizzato. Per altre informazioni, vedere [Procedure hook in stile Explorer](open-and-save-as-dialog-boxes.md).

Per abilitare una routine hook, impostare un **valore ENABLEHOOK** nel membro **Flags** della struttura corrispondente per la finestra di dialogo. Se è impostato un flag **ENABLEHOOK,** un membro **lpfnHook** della struttura deve specificare l'indirizzo della procedura hook.

Nella tabella seguente viene illustrato il tipo di routine hook da fornire per ognuna delle finestre di dialogo comuni.



| Tipo di finestra di dialogo                          | Procedura hook                                      |
|------------------------------------------|-----------------------------------------------------|
| **Colore**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Trovare** o **sostituire**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Font**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Apri** o **Salva con nome** (in stile Explorer) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Apri** o **Salva con nome** (stile precedente)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Stampa**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Imposta pagina**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Per la **finestra di dialogo** Imposta pagina è anche possibile specificare una procedura hook [*PagePaintHook.*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Si tratta di una procedura hook speciale che è possibile usare per personalizzare l'aspetto della pagina di esempio visualizzata nella **finestra di dialogo Imposta** pagina .

> [!Note]  
> La **finestra di dialogo** Imposta stampa è stata sostituita dalla finestra di dialogo **Imposta** pagina . Le applicazioni devono usare la **finestra di dialogo Imposta** pagina . Tuttavia, per motivi di compatibilità, la [**funzione PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) continua a supportare la visualizzazione della finestra **di dialogo Imposta** stampa . È possibile specificare una procedura hook [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) per la **finestra di dialogo Imposta** stampa .

 

## <a name="common-dialog-messages"></a>Messaggi di dialogo comuni

Le finestre di dialogo comuni usano messaggi per notificare alla routine della finestra o alla routine hook quando si verificano determinati eventi. Sono inoltre disponibili messaggi che è possibile inviare a una finestra di dialogo comune per recuperare informazioni o per controllare il comportamento o l'aspetto della finestra di dialogo. Questa sezione descrive i messaggi di finestra di dialogo comuni  registrati dalla  funzione [**RegisterWindowMessage,**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) i messaggi usati  dalle  finestre di dialogo Tipo di carattere e Imposta pagina e i messaggi usati dalle finestre di dialogo Apri e Salva con nome in stile Esplora risorse.

Common Dialog Box Library definisce un set di stringhe di messaggio. È possibile passare una costante associata a una di queste stringhe di messaggio a [**RegisterWindowMessage per**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) ottenere un identificatore di messaggio. È quindi possibile utilizzare l'identificatore per rilevare ed elaborare i messaggi inviati da una finestra di dialogo comune o per inviare messaggi a una finestra di dialogo comune. Nella tabella seguente vengono illustrate le costanti messaggio e ne viene descritto l'utilizzo.



| Contants                               | Uso                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Una **finestra di** dialogo Colore invia questo messaggio alla procedura hook quando l'utente seleziona un colore e fa clic sul pulsante **OK.** La procedura hook può accettare il colore o rifiutarlo e forzare la finestra di dialogo a rimanere aperta.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Una **finestra di** dialogo Apri o **Salva** con nome invia questo messaggio alla procedura hook quando l'utente seleziona un nome di file e fa clic sul **pulsante OK.** La procedura hook può accettare il nome del file o rifiutarlo e forzare la finestra di dialogo a rimanere aperta. Per le finestre  di **dialogo** Apri e Salva con nome di tipo Esplora risorse, questo messaggio è stato sostituito dal messaggio rete CDN [**di \_ notifica FILEOK.**](cdn-fileok.md)<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Una **finestra di** **dialogo** Trova o sostituisci invia questo messaggio alla routine della finestra padre quando l'utente fa clic su Trova successivo **,** Sostituisci **o** Sostituisci tutto oppure chiude la finestra di dialogo. Il parametro *lParam del* messaggio è un puntatore a una [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) contenente l'input dell'utente.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Tutte le finestre di dialogo comuni inviano questo messaggio alla routine della finestra padre quando l'utente fa clic sul **pulsante** ? . Per le finestre  di **dialogo** Apri e Salva con nome in stile Esplora risorse, questo messaggio è stato sostituito dal messaggio rete CDN [**\_ help.**](cdn-help.md)<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Una **finestra di** dialogo Apri o **Salva** con nome invia questo messaggio alla procedura hook quando l'utente modifica la selezione nella casella di **riepilogo Nome** file . Per le finestre  di **dialogo** Apri e Salva con nome di tipo Esplora risorse, questo messaggio è stato sostituito dal messaggio di notifica [**\_ SELCHANGE**](cdn-selchange.md) rete CDN visualizzato.<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Una routine hook può inviare questo messaggio a una **finestra di** dialogo Colore per impostare la selezione del colore corrente.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Una **finestra di** dialogo Apri o **Salva** con nome invia questo messaggio alla procedura hook se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul **pulsante OK.** Per le finestre **di** dialogo Apri e Salva con nome di tipo Esplora risorse, questo messaggio è stato sostituito dal messaggio di notifica [**\_ SHAREVIOLATION**](cdn-shareviolation.md) rete CDN visualizzato. <br/>                                                        |



 

Alcune finestre di dialogo comuni inviano e ricevono altri messaggi di finestra. La procedura hook per una **finestra di** dialogo Tipo di carattere può inviare qualsiasi messaggio **WM \_ CHOOSEFONT _ alla finestra \_ \* *di*** dialogo _ Tipo di carattere . Per altre informazioni, vedere [Finestra di dialogo Tipo di carattere](font-dialog-box.md). La **finestra di dialogo** Imposta pagina invia i messaggi * WM *\_ \_ \* PSD* _ se è stata abilitata una procedura hook [_PagePaintHook*.](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Per altre informazioni, vedere [Finestra di dialogo Imposta pagina](page-setup-dialog-box.md).

Le finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse supportano un set di messaggi predefiniti. Sono inclusi i messaggi di notifica inviati sotto forma di messaggio [**WM \_ NOTIFY**](../controls/wm-notify.md) alla procedura hook e i messaggi che la procedura hook può inviare alla finestra di dialogo. Per un elenco completo di questi messaggi, vedere [Explorer-Style Hook Procedures](open-and-save-as-dialog-boxes.md).

## <a name="help-support"></a>Supporto tecnico

Le finestre di dialogo comuni forniscono la Guida sensibile al contesto per i controlli standard della finestra di dialogo. Per fornire informazioni aggiuntive per una finestra  di dialogo comune, è possibile visualizzare un pulsante ? ed elaborare i messaggi generati quando l'utente fa clic sul pulsante. Il **pulsante ?** è un supplemento alla Guida sensibile al contesto predefinita. Il **pulsante** ? è utile per descrivere l'utilizzo generico della finestra di dialogo come si applica all'applicazione.

-   [Guida sensibile al contesto](#context-sensitive-help)
-   [Pulsante ?](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive guida

Tutte le finestre di dialogo comuni forniscono la Guida sensibile al contesto per i controlli standard della finestra di dialogo. L'utente può visualizzare la Guida per i singoli controlli con uno dei metodi seguenti:

-   Selezionare il controllo e premere F1.
-   Fare clic sul **pulsante ?** nella barra del titolo e successivamente facendo clic su un controllo .
-   Fare clic con il pulsante destro del mouse su un controllo .

Se si personalizza una finestra di dialogo aggiungendo nuovi controlli, è necessario estendere anche il supporto della Guida per questi controlli elaborando le richieste di assistenza nella procedura hook. La procedura hook riceve i messaggi seguenti quando l'utente richiede assistenza.



| Azione utente                                                           | Message                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Fare clic con il pulsante destro del mouse su un controllo.                          | [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) |
| Premere F1.                                                   | [**GUIDA DI \_ WM**](../shell/wm-help.md)               |
| È stato fatto clic sul **pulsante ?** sulla barra del titolo e quindi si è fatto clic su un controllo . | [**GUIDA DI \_ WM**](../shell/wm-help.md)               |



 

È consigliabile elaborare questi messaggi per i controlli aggiunti, ma consentire alla procedura predefinita della finestra di dialogo di elaborare i messaggi per i controlli standard. Per altre informazioni su come elaborare questi messaggi, vedere [la Guida](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85)).

### <a name="the-help-button"></a>Pulsante ?

È possibile visualizzare un **pulsante** ? in una delle finestre di dialogo comuni impostando un valore **SHOWHELP** nel membro **Flags** della struttura di inizializzazione per la finestra di dialogo. Se si visualizza il **pulsante Guida,** è necessario elaborare la richiesta di assistenza dell'utente. L'elaborazione può essere eseguita in una delle routine della finestra dell'applicazione o in una routine hook per la finestra di dialogo. In genere, la richiesta di assistenza viene elaborata chiamando la [**funzione WinHelp.**](/windows/win32/api/winuser/nf-winuser-winhelpa)

Per elaborare i messaggi della Guida in una delle procedure della finestra, è necessario ottenere un identificatore di messaggio per la stringa definita dal valore [**HELPMSGSTRING**](helpmsgstring.md) e identificare la finestra per la ricezione dei messaggi. Per ottenere l'identificatore del messaggio, **specificare HELPMSGSTRING** come parametro in una chiamata alla [**funzione RegisterWindowMessage.**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) Quando si crea la finestra di dialogo, usare il membro **hwndOwner** della struttura di inizializzazione della finestra di dialogo per identificare la finestra che deve ricevere i messaggi. La routine della finestra di dialogo invia il messaggio alla routine della finestra ogni volta che l'utente fa clic sul **pulsante** ? .

Per elaborare i messaggi della Guida in una routine hook, è necessario elaborare il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) La procedura hook fornisce informazioni se il *parametro wParam* di questo messaggio indica che l'utente ha fatto clic sul **pulsante ?** . L'identificatore **del** pulsante ? è la **costante pshHelp** definita nel file Dlgs.h.

Le routine hook per le finestre di dialogo **Apri** e **Salva** con nome in stile Esplora risorse non ricevono messaggi [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) per il **pulsante** ? . Al contrario, la finestra di dialogo [**rete CDN \_ messaggio**](cdn-help.md) di notifica help alla procedura hook quando **si** fa clic sul pulsante ? .

 

