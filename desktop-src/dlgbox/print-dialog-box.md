---
title: Finestra di dialogo Stampa
description: La finestra di dialogo Stampa consente all'utente di selezionare le opzioni per un particolare processo di stampa.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, libreria finestra di dialogo comune
- input utente, libreria finestra di dialogo comune
- acquisizione dell'input dell'utente, libreria finestra di dialogo comune
- Libreria finestra di dialogo comune
- finestre di dialogo comuni
- Finestra di dialogo Stampa
- Finestra di dialogo Imposta stampa
- personalizzazione della finestra di dialogo Stampa
- finestre di dialogo predefinite
- finestre di dialogo, stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fae1dd244391ea16478a0cb4f10803cf622dc64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118407"
---
# <a name="print-dialog-box"></a>Finestra di dialogo Stampa

La finestra di dialogo **stampa** consente all'utente di selezionare le opzioni per un particolare processo di stampa. Ad esempio, l'utente può specificare la stampante da usare, l'intervallo di pagine da stampare e il numero di copie.

È possibile utilizzare la funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) per visualizzare una [finestra delle proprietà di stampa](print-property-sheet.md), che include una pagina **generale** contenente controlli simili alla finestra di dialogo **stampa** . Nella finestra delle proprietà possono inoltre essere presenti pagine di proprietà aggiuntive specifiche per l'applicazione e specifiche del driver che seguono la pagina **generale** .

Per creare e visualizzare una finestra di dialogo di **stampa** , inizializzare una struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e passare la struttura alla funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .

Nella figura seguente viene illustrata una tipica finestra di dialogo **stampa** .

![finestra di dialogo Stampa](images/printdialogboxxp.png)

Se l'utente fa clic sul pulsante **OK** , [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **true** e usa la struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) per restituire informazioni sulle selezioni dell'utente. I membri **hDevMode** e **hDevNames** , ad esempio, restituiscono in genere handle di memoria globali per le strutture e [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . È possibile utilizzare le informazioni contenute in queste strutture per creare un contesto di dispositivo o un contesto di informazioni per la stampante selezionata.

Se l'utente annulla la finestra di dialogo **stampa** o si verifica un errore, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce **false**. È possibile determinare la provocazione di un errore utilizzando la funzione [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

Nella finestra di dialogo **stampa** è incluso un gruppo di pulsanti di opzione di **stampa** che indica se l'utente desidera stampare tutte le pagine, un intervallo di pagine o solo il testo selezionato. Prima di chiamare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)), è possibile impostare uno dei flag **PD \_ ALLPAGES**, **PD \_ Selection** o **PD \_ PAGENUMS** per indicare quale pulsante inizialmente è selezionato. Quando **PrintDlg** restituisce **true**, la funzione imposta uno di questi flag per indicare le selezioni dell'utente. Se è impostato **PD \_ PAGENUMS** , i membri **nFromPage** e **nToPage** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contengono le pagine iniziale e finale specificate dall'utente. Per disabilitare il pulsante di opzione **pagine** e il relativo oggetto associato **da** e **per** modificare i controlli, impostare il flag **PD \_ NOPAGENUMS** . Per disabilitare il pulsante di opzione **selezione** , impostare il flag **PD \_ noselection** .

Nella finestra di dialogo è incluso un controllo di modifica in cui l'utente può digitare il numero di copie da stampare. Se il membro **hDevMode** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) è diverso da **null**, il membro **dmCopies** della struttura specifica il valore iniziale per questo controllo di modifica. Se **hDevMode** è **null**, il membro **nCopies** della struttura **PrintDlg** specifica il valore iniziale. Quando [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce, **nCopies** in genere indica il numero di copie specificato dall'utente. Tuttavia, se si imposta il **flag PD \_ USEDEVMODECOPIESANDCOLLATE** quando si crea la finestra di dialogo, **nCopies** viene sempre impostato su 1 in fase di restituzione e il membro **dmCopies** di [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indica il numero di copie da stampare.

La casella di controllo **COLLATE** indica se l'utente desidera eseguire l'ordinamento delle pagine se vengono stampate più copie. Se è selezionata la casella di controllo **COLLATE** , il flag di **\_ ordinamento PD** viene impostato. Se l'applicazione non supporta più copie o regole di confronto simulate, impostare il flag **PD \_ USEDEVMODECOPIESANDCOLLATE** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . In questo modo vengono disabilitate la casella di controllo **COLLATE** e il controllo **di modifica numero di copie** , a meno che il driver della stampante non supporti più copie e regole di confronto.

La casella **di controllo stampa su file** indica se l'utente desidera inviare l'output a un file anziché a una stampante. È possibile impostare il flag **PD \_ PrintToFile** in modo che la casella di controllo sia selezionata inizialmente. Per nascondere la casella di controllo, impostare il flag **PD \_ HIDEPRINTTOFILE** . Per disabilitarlo, impostare il flag **PD \_ DISABLEPRINTTOFILE** . Se l'utente seleziona l'opzione **stampa su file** , [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) imposta il flag **PD \_ PrintToFile** e restituisce "file:" in corrispondenza dell'offset indicato dal membro **wOutputOffset** della struttura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Quando si chiama la funzione per avviare l'operazione di stampa, specificare la stringa "FILE:" nel membro **lpszOutput** della struttura. Se si specifica questa stringa, il sottosistema di stampa esegue una query sull'utente per il nome del file di output.

Per impostazione predefinita, nella finestra di dialogo **stampa** vengono inizialmente visualizzate informazioni sulla stampante predefinita corrente. Per visualizzare informazioni per un'altra stampante installata, inizializzare una struttura e una struttura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e assegnare l'handle di memoria globale alla struttura ai membri **hDevMode** e **hDevNames** . Il nome del dispositivo specificato nel membro **dmDeviceName** della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e nel membro **wDriverOffset** della struttura **DEVNAMES** deve identificare un dispositivo di stampa che è elencato anche nella \[ sezione Devices \] del file di Win.ini. Se il dispositivo non è elencato, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) restituisce un errore.

È possibile indirizzare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) per creare un contesto di dispositivo o un contesto di informazioni per la stampante impostando il flag **PD \_ RETURNDC** o **PD \_ Returnal** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . La funzione restituisce un handle per il contesto di dispositivo o il contesto delle informazioni nel membro **HDC** . Se si usa il flag **PD \_ RETURNDC** , è possibile usare il contesto di dispositivo per generare l'output per la stampante.

Per recuperare le informazioni sulla stampante predefinita senza visualizzare la finestra di dialogo **stampa** , impostare il flag **PD \_ RETURNDEFAULT** . In questo caso, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) viene restituito immediatamente dopo aver impostato i membri **hDevMode** e **hDevNames** su handle per le strutture che contengono le informazioni.

Per impostazione predefinita, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) Visualizza le finestre di messaggio quando si verificano errori. La funzione, ad esempio, Visualizza un messaggio di errore se non sono installate stampanti. Per impedire la visualizzazione di questi messaggi di avviso da parte della funzione, impostare il flag **PD \_ nowarning** .

In questa sezione vengono descritti gli argomenti seguenti.

-   [Personalizzazione della finestra di dialogo Stampa](#customizing-the-print-dialog-box)
-   [Finestra di dialogo Imposta stampa](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personalizzazione della finestra di dialogo Stampa

È possibile specificare un modello personalizzato per la finestra di dialogo **stampa** , ad esempio se si desidera includere controlli aggiuntivi che siano univoci per l'applicazione. La funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.

Per fornire un modello personalizzato per la finestra di dialogo **stampa** :

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file prnsetup. dlg. Gli identificatori di controllo utilizzati nel modello della finestra di dialogo di **stampa** predefinita sono definiti nel file Dlgs. h.
2.  Utilizzare la struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) per abilitare il modello nel modo seguente:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **PD \_ ENABLEPRINTTEMPLATE** nel membro **Flags** . Usare i membri **HINSTANCE** e **lpPrintTemplateName** della struttura per identificare il modulo e il nome della risorsa.

        oppure

    -   Se il modello personalizzato è già in memoria, impostare il flag **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Usare il membro **hPrintTemplate** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura di hook [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) per la finestra di dialogo **stampa** . La procedura hook può elaborare i messaggi inviati alla finestra di dialogo. Può inoltre inviare messaggi alla finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura di hook per elaborare l'input per i controlli.

Per abilitare una procedura di hook per la finestra di dialogo **stampa** :

1.  Impostare il flag **PD \_ ENABLEPRINTHOOK** nel membro **Flags** della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Specificare l'indirizzo della routine hook nel membro **lpfnPrintHook** .

Dopo l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la routine della finestra di dialogo Invia un messaggio **WM \_ INITDIALOG** alla routine hook. Il parametro *lParam* di questo messaggio è un puntatore alla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) utilizzata per inizializzare la finestra di dialogo.

## <a name="print-setup-dialog-box"></a>Finestra di dialogo Imposta stampa

È possibile creare e visualizzare una finestra di dialogo di **stampa** impostando il flag **PD \_ PRINTSETUP** in una chiamata alla funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Tuttavia, la finestra di dialogo **Imposta stampa** è stata sostituita dalla finestra di dialogo **Imposta pagina** e non deve essere utilizzata nelle nuove applicazioni.

I flag seguenti si applicano solo alla finestra di dialogo **Imposta stampa** :

-   **\_ENABLESETUPHOOK PD**
-   **\_ENABLESETUPTEMPLATE PD**
-   **\_ENABLESETUPTEMPLATEHANDLE PD**

 

 