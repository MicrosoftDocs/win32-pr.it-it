---
title: Finestra di dialogo Stampa
description: La finestra di dialogo Stampa consente all'utente di selezionare le opzioni per un processo di stampa specifico.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,Common Dialog Box Library
- input utente,Libreria di finestre di dialogo comuni
- acquisizione dell'input dell'utente, libreria di finestre di dialogo comune
- Libreria di finestre di dialogo comune
- finestre di dialogo comuni
- Finestra di dialogo Stampa
- Finestra di dialogo Imposta stampa
- personalizzazione della finestra di dialogo Stampa
- finestre di dialogo predefinite
- finestre di dialogo, Stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afd8cfa31a83f664e859cd93acc9d28543b7ab00dcb8f130fdbac329cd1429e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720919"
---
# <a name="print-dialog-box"></a>Finestra di dialogo Stampa

La **finestra di** dialogo Stampa consente all'utente di selezionare le opzioni per un processo di stampa specifico. Ad esempio, l'utente può specificare la stampante da usare, l'intervallo di pagine da stampare e il numero di copie.

È possibile usare la [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare  una finestra delle proprietà di stampa [che](print-property-sheet.md)include una pagina Generale contenente controlli simili alla **finestra di** dialogo Stampa. La finestra delle proprietà può anche avere altre pagine delle proprietà specifiche dell'applicazione e specifiche del driver dopo la **pagina** Generale.

Per creare e visualizzare una **finestra di** dialogo Stampa, inizializzare una [**struttura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e passare la struttura alla [**funzione PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))

Nella figura seguente viene illustrata una tipica **finestra di** dialogo Stampa.

![Finestra di dialogo stampa](images/printdialogboxxp.png)

Se l'utente fa clic sul pulsante **OK,** [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **TRUE** e usa la [**struttura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) per restituire informazioni sulle selezioni dell'utente. Ad esempio, i **membri hDevMode** e **hDevNames** restituiscono in genere handle di memoria globali per le [**strutture DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e . È possibile utilizzare le informazioni in queste strutture per creare un contesto di dispositivo o un contesto di informazioni per la stampante selezionata.

Se l'utente annulla la finestra di dialogo **Stampa** o si verifica un errore, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **FALSE.** È possibile determinare la causa di un errore usando la [**funzione CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

La **finestra** di  dialogo Stampa include un gruppo di pulsanti di opzione Intervallo di stampa che indicano se l'utente desidera stampare tutte le pagine, un intervallo di pagine o solo il testo selezionato. Prima di [**chiamare PrintDlg,**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))è possibile impostare uno dei flag **\_ PD ALLPAGES,** **PD \_ SELECTION** o **PD \_ PAGENUMS** per indicare quale pulsante è inizialmente selezionato. Quando **PrintDlg restituisce** **TRUE,** la funzione imposta uno di questi flag per indicare le selezioni dell'utente. Se **pd \_ PAGENUMS** è impostato, i membri **nFromPage** e **nToPage** della struttura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contengono le pagine iniziale e finale specificate dall'utente. Per disabilitare **il pulsante** di opzione Pagine e i controlli di modifica **From** e **To** associati, impostare il flag **\_ NOPAGENUMS PD.** Per disabilitare **il pulsante** di opzione Selezione, impostare il flag **\_ NOSELECTION PD.**

La finestra di dialogo include un controllo di modifica in cui l'utente può digitare il numero di copie da stampare. Se il **membro hDevMode** della struttura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) è diverso da **NULL,** il membro **dmCopies** della struttura specifica il valore iniziale per questo controllo di modifica. Se **hDevMode** è **NULL,** il **membro nCopies** della **struttura PRINTDLG** specifica il valore iniziale. Quando [**PrintDlg restituisce**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) il risultato, **nCopies** indica in genere il numero di copie specificato dall'utente. Tuttavia, se si imposta il flag **PD \_ USEDEVMODECOPIESANDCOLLATE** quando si crea la finestra di dialogo, **nCopies** viene sempre impostato su 1 al ritorno e il membro **dmCopies** di [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indica il numero di copie da stampare.

La **casella di controllo** Collate (Regole di confronto) indica se l'utente vuole collaminare le pagine se vengono stampate più copie. Il flag **\_ COLLATE PD** viene impostato se la **casella di controllo Collate** è selezionata. Se l'applicazione non supporta più copie o regole di confronto simulate, impostare il flag **PD \_ USEDEVMODECOPIESANDCOLLATE** nel membro **Flags** della [**struttura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) In questo modo vengono **disabilitate le caselle** di controllo Collate (Collazione) e **Number of Copies** (Numero di copie) a meno che il driver della stampante non supporti più copie e regole di confronto.

La **casella di controllo Stampa** su file indica se l'utente desidera inviare l'output a un file anziché a una stampante. È possibile impostare il flag **\_ PRINTTOFILE PD** in modo che la casella di controllo sia inizialmente selezionata. Per nascondere la casella di controllo, impostare il flag **\_ HIDEPRINTTOFILE PD.** Per disabilitarlo, impostare il flag **\_ DISABLEPRINTTOFILE PD.** Se l'utente seleziona l'opzione Stampa su **file,** [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) imposta il flag **\_ PRINTTOFILE PD** e restituisce "FILE:" in corrispondenza dell'offset indicato dal membro **wOutputOffset** della [**struttura DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Quando si chiama la funzione per avviare l'operazione di stampa, specificare questa stringa "FILE:" nel membro **lpszOutput** della struttura . Se si specifica questa stringa, il sottosistema di stampa esegue una query sull'utente per il nome del file di output.

Per impostazione predefinita, **nella finestra** di dialogo Stampa vengono inizialmente visualizzate informazioni sulla stampante predefinita corrente. Per visualizzare informazioni per un'altra stampante installata, inizializzare e una struttura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e assegnare l'handle di memoria globale alla struttura ai **membri hDevMode** e **hDevNames.** Il nome del dispositivo specificato nel membro **dmDeviceName** della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e nel membro **wDriverOffset** della struttura **DEVNAMES** deve identificare un dispositivo stampante elencato anche nella sezione Devices del \[ file \] Win.ini. Se il dispositivo non è elencato, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce un errore.

È possibile impostare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) in modo che crei un contesto di dispositivo o un contesto di informazioni per la stampante impostando il flag **PD \_ RETURNDC** o **PD \_ RETURNIC** nel membro **Flags** della [**struttura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) La funzione restituisce un handle al contesto di dispositivo o al contesto delle informazioni nel **membro hDC.** Se si usa il flag **\_ RETURNDC PD,** è possibile usare il contesto di dispositivo per generare l'output per la stampante.

Per recuperare informazioni sulla stampante predefinita senza visualizzare **la** finestra di dialogo Stampa, impostare il flag **\_ RETURNDEFAULT PD.** In questo [**caso, PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce immediatamente dopo l'impostazione dei membri **hDevMode** e **hDevNames** su handle per le strutture contenenti le informazioni.

Per impostazione predefinita, [**PrintDlg visualizza**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) finestre di messaggio quando si verificano errori. Ad esempio, la funzione visualizza un messaggio di errore se non sono installate stampanti. Per impedire alla funzione di visualizzare questi messaggi di avviso, impostare il flag **PD \_ NOWARNING.**

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Personalizzazione della finestra di dialogo Stampa](#customizing-the-print-dialog-box)
-   [Finestra di dialogo Imposta stampa](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personalizzazione della finestra di dialogo Stampa

È possibile fornire un  modello personalizzato per la finestra di dialogo Stampa, ad esempio se si desidera includere controlli aggiuntivi univoci per l'applicazione. La [**funzione PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.

Per specificare un modello personalizzato per la **finestra di** dialogo Stampa:

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file Prnsetup.dlg. Gli identificatori di controllo usati nel modello della finestra **di** dialogo Stampa predefinito sono definiti nel file Dlgs.h.
2.  Usare la [**struttura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) per abilitare il modello come segue:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ ENABLEPRINTTEMPLATE PD** nel **membro Flags.** Usare i **membri hInstance** **e lpPrintTemplateName** della struttura per identificare il modulo e il nome della risorsa.

        oppure

    -   Se il modello personalizzato è già in memoria, impostare il flag **\_ ENABLEPRINTTEMPLATEHANDLE PD.** Usare il **membro hPrintTemplate** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura hook [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) per la **finestra di** dialogo Stampa. La routine hook può elaborare i messaggi inviati alla finestra di dialogo. Può anche inviare messaggi alla finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura hook per elaborare l'input per i controlli.

Per abilitare una procedura hook per la **finestra di** dialogo Stampa:

1.  Impostare il flag **\_ ENABLEPRINTHOOK PD** nel **membro Flags** della [**struttura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
2.  Specificare l'indirizzo della procedura hook nel **membro lpfnPrintHook.**

Dopo [**l'elaborazione del messaggio WM \_ INITDIALOG,**](wm-initdialog.md) la routine della finestra di dialogo invia un **messaggio WM \_ INITDIALOG** alla routine hook. Il *parametro lParam* di questo messaggio è un puntatore alla [**struttura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) usata per inizializzare la finestra di dialogo.

## <a name="print-setup-dialog-box"></a>Finestra di dialogo Imposta stampa

È possibile creare e visualizzare una **finestra di** dialogo Imposta stampa impostando il flag **\_ PRINTSETUP PD** in una chiamata alla [**funzione PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) Tuttavia, la **finestra di dialogo** Imposta stampa  è stata sostituita dalla finestra di dialogo Imposta pagina e non deve essere usata nelle nuove applicazioni.

I flag seguenti si applicano solo alla **finestra di dialogo Imposta** stampa:

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 