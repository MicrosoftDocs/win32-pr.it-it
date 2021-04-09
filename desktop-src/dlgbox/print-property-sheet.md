---
title: Stampa finestra delle proprietà
description: La finestra delle proprietà di stampa è un'interfaccia utente standard che consente all'utente di specificare le proprietà di un particolare processo di stampa.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, libreria finestra di dialogo comune
- input utente, libreria finestra di dialogo comune
- acquisizione dell'input dell'utente, libreria finestra di dialogo comune
- Libreria finestra di dialogo comune
- finestre di dialogo comuni
- Finestra di dialogo finestra delle proprietà di stampa
- personalizzazione della finestra di dialogo finestra delle proprietà di stampa
- finestre di dialogo predefinite
- finestre di dialogo, finestra delle proprietà di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20905f76af290b3978bec828a382604147297998
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047330"
---
# <a name="print-property-sheet"></a>Stampa finestra delle proprietà

La finestra delle proprietà di **stampa** è un'interfaccia utente standard che consente all'utente di specificare le proprietà di un particolare processo di stampa. La finestra delle proprietà è costituita da un set di pagine delle proprietà che varia in base alla stampante o all'applicazione. Per un subset di pagine delle proprietà standard di Windows, alcune stampanti potrebbero aggiungere pagine di proprietà specifiche del driver e alcune applicazioni potrebbero aggiungere pagine delle proprietà specifiche dell'applicazione.

Per creare e visualizzare una finestra delle proprietà di **stampa** , inizializzare una struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) e passare la struttura alla funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

Nella figura seguente viene illustrata una tipica finestra delle proprietà di **stampa** .

![finestra delle proprietà della stampante](images/printerpropertypagexp.png)

La maggior parte dei membri della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) è identica a quella della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Per le descrizioni di come usare i membri della struttura comune per interagire con i controlli della finestra di dialogo, vedere [finestra di dialogo Stampa](print-dialog-box.md). Nella parte restante di questo argomento vengono descritte le caratteristiche della finestra delle proprietà di **stampa** che si differenziano dalla finestra di dialogo **stampa** .

È possibile personalizzare una finestra delle proprietà di **stampa** specificando un modello di finestra di dialogo personalizzato per la parte inferiore della pagina **generale** e specificando pagine delle proprietà aggiuntive per seguire la pagina **generale** . Per ulteriori informazioni, vedere [personalizzazione della finestra delle proprietà di stampa](#customizing-the-print-property-sheet).

È possibile implementare un oggetto callback per ricevere notifiche e messaggi dalla funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mentre viene visualizzata la finestra delle proprietà. Le applicazioni che forniscono modelli personalizzati o pagine aggiuntive utilizzano l'oggetto callback per comunicare con la finestra delle proprietà. Per ulteriori informazioni, vedere [oggetto callback per la finestra delle proprietà di stampa](#callback-object-for-the-print-property-sheet).

La finestra delle proprietà di **stampa** fornisce supporto per la specifica di più intervalli di pagine non contigui da stampare. Il membro **lpPageRanges** della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) specifica una matrice di strutture [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) in cui ogni struttura specifica un intervallo di pagine.

La finestra delle proprietà **stampa** Visualizza un pulsante di opzione **pagina corrente** come parte del gruppo di **intervalli di pagine** di pulsanti di opzione. Per controllare il pulsante di opzione della **pagina corrente** , usare i flag **PD \_ CURRENTPAGE** e **PD \_ NOCURRENTPAGE** nel membro **Flags** della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Personalizzazione della finestra delle proprietà di stampa](#customizing-the-print-property-sheet)
-   [Oggetto callback per la finestra delle proprietà di stampa](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Personalizzazione della finestra delle proprietà di stampa

È possibile personalizzare la finestra delle proprietà di **stampa** nei modi seguenti:

-   Fornire un modello personalizzato per la parte inferiore della pagina **generale** . Ciò consente di includere controlli aggiuntivi che sono univoci per l'applicazione. La funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa il modello personalizzato al posto del modello predefinito.
-   Fornire pagine di proprietà aggiuntive per seguire la pagina **generale** .
-   Fornire un oggetto callback. Per ulteriori informazioni, vedere [oggetto callback per la finestra delle proprietà di stampa](#callback-object-for-the-print-property-sheet).

Non è possibile modificare la parte superiore della pagina **generale** . Non è possibile modificare le pagine delle proprietà fornite dal driver della stampante.

Per fornire un modello personalizzato per la pagina generale:

1.  Creare un modello personalizzato per la parte inferiore della pagina **generale** modificando il modello PRINTDLGEXORD specificato nel file prnsetup. dlg. In genere, il modello personalizzato deve avere le stesse dimensioni del modello predefinito. Tuttavia, è possibile ingrandire il modello personalizzato se si specifica il flag **PD \_ USELARGETEMPLATE** per creare una pagina **generale** di dimensioni maggiori. Gli identificatori di controllo utilizzati nel modello della finestra di dialogo di **stampa** predefinita sono definiti nel file Dlgs. h.
2.  Utilizzare la struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) per abilitare il modello nel modo seguente:
    -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **PD \_ ENABLEPRINTTEMPLATE** nel membro **Flags** . Usare i membri **HINSTANCE** e **lpPrintTemplateName** della struttura per identificare il modulo e il nome della risorsa.

        oppure

    -   Se il modello personalizzato è già in memoria, impostare il flag **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Usare il membro **HINSTANCE** per identificare l'oggetto memoria che contiene il modello.

3.  Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire un oggetto callback per elaborare l'input per i controlli. L'oggetto callback implementa un metodo [**IPrintDialogCallback:: HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) che riceve i messaggi inviati alla finestra di dialogo personalizzata.

Per fornire pagine di proprietà aggiuntive

1.  Utilizzare la funzione per creare le pagine aggiuntive.
2.  Usare il membro **lphPropertyPages** della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) per specificare una matrice di handle per le pagine aggiuntive.

    Le routine della finestra di dialogo specificate al momento della creazione di ogni pagina messaggi di processo inviati alle pagine.

3.  Potrebbe essere necessario fornire un oggetto callback che implementi l'interfaccia. La funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa questa interfaccia per passare all'applicazione un puntatore a un'interfaccia [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) . Le procedure della finestra di dialogo per le pagine delle proprietà aggiuntive possono utilizzare questa interfaccia per recuperare informazioni sulla stampante attualmente selezionata.

## <a name="callback-object-for-the-print-property-sheet"></a>Oggetto callback per la finestra delle proprietà di stampa

Un'applicazione che visualizza una finestra delle proprietà di **stampa** può implementare un oggetto callback per ricevere notifiche e messaggi dalla funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mentre viene visualizzata la finestra delle proprietà. Per fornire un oggetto callback, specificare un puntatore all'oggetto nel membro **lpCallback** della struttura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

L'oggetto callback deve implementare l'interfaccia [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) . La funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) chiama i metodi **IPrintDialogCallback** nelle situazioni seguenti:

-   Quando la finestra di dialogo è stata inizializzata
-   Quando l'utente seleziona una stampante diversa dall'elenco delle stampanti installate visualizzate dalla finestra delle proprietà
-   Quando riceve i messaggi per la finestra di dialogo figlio nella parte inferiore della pagina **generale** della finestra delle proprietà

Anche l'oggetto callback deve implementare l'interfaccia [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) . La funzione [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) chiama il metodo per passare un puntatore a un'interfaccia [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) a un'applicazione. I metodi [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) possono usare l'interfaccia **IPrintDialogServices** per recuperare informazioni sulla stampante attualmente selezionata. L'interfaccia **IPrintDialogServices** è utile anche per le applicazioni che creano pagine aggiuntive per seguire la pagina **generale** della finestra delle proprietà di **stampa** . Le routine della finestra di dialogo per le pagine aggiuntive possono chiamare i metodi **IPrintDialogServices** .

 

 