---
title: Finestra delle proprietà Stampa
description: La finestra delle proprietà Stampa è un'interfaccia utente standard che consente all'utente di specificare le proprietà di un processo di stampa specifico.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,Common Dialog Box Library
- input utente,Libreria di finestre di dialogo comuni
- acquisizione dell'input dell'utente, libreria di finestre di dialogo comune
- Libreria di finestre di dialogo comune
- finestre di dialogo comuni
- Finestra di dialogo Stampa finestra delle proprietà
- personalizzazione della finestra di dialogo Finestra delle proprietà di stampa
- finestre di dialogo predefinite
- finestre di dialogo, Finestra delle proprietà Stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54bc8065ada207702755e8fc0a1586620f660db9f3acf2a67e32b56e393143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280510"
---
# <a name="print-property-sheet"></a>Finestra delle proprietà Stampa

La **finestra** delle proprietà Stampa è un'interfaccia utente standard che consente all'utente di specificare le proprietà di un processo di stampa specifico. La finestra delle proprietà è costituita da un set di pagine delle proprietà che varia a seconda della stampante o dell'applicazione. Per un subset di pagine Windows standard, alcune stampanti potrebbero aggiungere pagine delle proprietà specifiche del driver e alcune applicazioni potrebbero aggiungere pagine delle proprietà specifiche dell'applicazione.

Per creare e visualizzare una finestra delle proprietà **Print,** inizializzare una [**struttura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) e passare la struttura alla [**funzione PrintDlgEx.**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))

La figura seguente mostra una tipica **finestra delle proprietà** Stampa.

![finestra delle proprietà della stampante](images/printerpropertypagexp.png)

La maggior parte dei [**membri della struttura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) è identica a quella della [**struttura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Per descrizioni su come usare i membri della struttura comuni per interagire con i controlli della finestra di dialogo, vedere [Finestra di dialogo Stampa](print-dialog-box.md). Nella parte restante di questo argomento vengono descritte le **funzionalità della** finestra delle proprietà Stampa che differiscono dalla **finestra di** dialogo Stampa .

È possibile personalizzare **una** finestra delle proprietà Stampa specificando un modello  di finestra di dialogo personalizzato per la parte inferiore della pagina Generale e specificando pagine delle proprietà aggiuntive per seguire la **pagina** Generale. Per altre informazioni, vedere [Personalizzazione della finestra delle proprietà Stampa](#customizing-the-print-property-sheet).

È possibile implementare un oggetto callback per ricevere notifiche e messaggi dalla [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mentre viene visualizzata la finestra delle proprietà. Le applicazioni che forniscono modelli personalizzati o pagine aggiuntive usano l'oggetto callback per comunicare con la finestra delle proprietà. Per altre informazioni, vedere [Oggetto callback per la finestra delle proprietà stampa](#callback-object-for-the-print-property-sheet).

La **finestra** delle proprietà Stampa fornisce il supporto per specificare più intervalli di pagine non contigui da stampare. Il **membro lpPageRanges** della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) specifica una matrice di strutture [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) in cui ogni struttura specifica un intervallo di pagine.

Nella **finestra delle** proprietà Stampa viene visualizzato un pulsante di opzione **Pagina** corrente come parte del gruppo **Intervallo** di pagine di pulsanti di opzione. Per controllare il **pulsante di** opzione Pagina corrente, usare i flag **PD \_ CURRENTPAGE** e **\_ PD NOCURRENTPAGE** nel membro **Flags** della [**struttura PRINTDLGEX.**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Personalizzazione della finestra delle proprietà Di stampa](#customizing-the-print-property-sheet)
-   [Oggetto callback per la finestra delle proprietà di stampa](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Personalizzazione della finestra delle proprietà Di stampa

È possibile personalizzare la **finestra** delle proprietà Stampa nei modi seguenti:

-   Specificare un modello personalizzato per la parte inferiore della **pagina** Generale. In questo modo è possibile includere controlli aggiuntivi univoci per l'applicazione. La [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.
-   Specificare pagine delle proprietà aggiuntive da seguire nella **pagina** Generale.
-   Fornire un oggetto callback. Per altre informazioni, vedere [Oggetto callback per la finestra delle proprietà stampa](#callback-object-for-the-print-property-sheet).

Non è possibile modificare la parte superiore della **pagina** Generale. Non è possibile modificare le pagine delle proprietà fornite dal driver della stampante.

Per fornire un modello personalizzato per la pagina Generale:

1.  Creare un modello personalizzato per  la parte inferiore della pagina Generale modificando il modello PRINTDLGEXORD specificato nel file Prnsetup.dlg. In genere, il modello personalizzato deve avere le stesse dimensioni del modello predefinito. Tuttavia, è possibile ingrandire il modello personalizzato se si specifica il flag **\_ USELARGETEMPLATE PD** per creare una pagina **Generale più** grande. Gli identificatori di controllo usati nel modello della finestra **di** dialogo Stampa predefinito sono definiti nel file Dlgs.h.
2.  Usare la [**struttura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) per abilitare il modello come segue:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ ENABLEPRINTTEMPLATE PD** nel **membro Flags.** Usare i **membri hInstance** **e lpPrintTemplateName** della struttura per identificare il modulo e il nome della risorsa.

        oppure

    -   Se il modello personalizzato è già in memoria, impostare il flag **\_ ENABLEPRINTTEMPLATEHANDLE PD.** Usare il **membro hInstance** per identificare l'oggetto memoria che contiene il modello.

3.  Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire un oggetto callback per elaborare l'input per i controlli. L'oggetto callback implementa [**un metodo IPrintDialogCallback::HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) che riceve i messaggi inviati alla finestra di dialogo personalizzata.

Per fornire pagine delle proprietà aggiuntive

1.  Usare la funzione per creare le pagine aggiuntive.
2.  Usare il **membro lphPropertyPages** della [**struttura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) per specificare una matrice di handle per le pagine aggiuntive.

    Le procedure della finestra di dialogo specificate al momento della creazione di ogni pagina elaborano i messaggi inviati alle pagine.

3.  Può essere necessario fornire un oggetto callback che implementa l'interfaccia . La [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa questa interfaccia per passare all'applicazione un puntatore a [**un'interfaccia IPrintDialogServices.**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) Le procedure della finestra di dialogo per le pagine delle proprietà aggiuntive possono utilizzare questa interfaccia per recuperare informazioni sulla stampante attualmente selezionata.

## <a name="callback-object-for-the-print-property-sheet"></a>Oggetto callback per la finestra delle proprietà di stampa

Un'applicazione che visualizza **una** finestra delle proprietà Stampa può implementare un oggetto callback per ricevere notifiche e messaggi dalla funzione [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mentre viene visualizzata la finestra delle proprietà. Per fornire un oggetto callback, specificare un puntatore all'oggetto nel membro **lpCallback** della [**struttura PRINTDLGEX.**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

L'oggetto callback deve implementare [**l'interfaccia IPrintDialogCallback.**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) La [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) chiama **i metodi IPrintDialogCallback** nelle situazioni seguenti:

-   Quando la finestra di dialogo è stata inizializzata
-   Quando l'utente seleziona una stampante diversa dall'elenco delle stampanti installate visualizzate dalla finestra delle proprietà
-   Quando riceve messaggi per la finestra di dialogo figlio nella parte inferiore della pagina Generale della finestra **delle** proprietà

L'oggetto callback deve implementare anche [**l'interfaccia IObjectWithSite.**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) La [**funzione PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) chiama il metodo per passare un puntatore a [**un'interfaccia IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) a un'applicazione. I [**metodi IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) possono usare **l'interfaccia IPrintDialogServices** per recuperare informazioni sulla stampante attualmente selezionata. **L'interfaccia IPrintDialogServices** è utile anche per le applicazioni che creano pagine aggiuntive per seguire la **pagina Generale** della finestra **delle proprietà** Stampa. Le procedure della finestra di dialogo per le pagine aggiuntive possono chiamare **i metodi IPrintDialogServices.**

 

 