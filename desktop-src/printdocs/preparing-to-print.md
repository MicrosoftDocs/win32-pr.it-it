---
description: In questo argomento viene descritto come raccogliere informazioni sui processi di stampa dall'utente.
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: "Procedura: raccogliere informazioni sui processi di stampa dall'utente"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050002"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a>Procedura: raccogliere informazioni sui processi di stampa dall'utente

In questo argomento viene descritto come raccogliere informazioni sui processi di stampa dall'utente.

## <a name="overview"></a>Panoramica

Raccogliere le informazioni sul processo di stampa dall'utente chiamando la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Questa funzione Visualizza all'utente la finestra di dialogo **stampa** comune e restituisce le informazioni sul processo di stampa in una struttura di dati [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

La finestra di dialogo **stampa** comune viene visualizzata quando l'utente avvia un processo di stampa. La finestra di dialogo **stampa** comune è una finestra di dialogo modale, che indica che l'utente non può interagire con la finestra principale fino a quando non viene chiusa la finestra di dialogo comune.

## <a name="collecting-print-job-information"></a>Raccolta di informazioni sul processo di stampa

1.  Inizializzare l'elemento della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

    Prima che un programma possa visualizzare la finestra di dialogo **stampa** comune, deve allocare e inizializzare una struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Passa quindi questa struttura alla funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , che visualizza la finestra di dialogo e restituisce i dati del processo di stampa nella stessa struttura. Nell'esempio di codice seguente viene illustrato il modo in cui il programma di esempio esegue questo passaggio.

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  Visualizza la finestra di dialogo **stampa** comune.

    Chiamare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) con la struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) inizializzata per visualizzare la finestra di dialogo **stampa** comune e raccogliere i dati utente, come illustrato nell'esempio di codice seguente.

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  Salvare i campi dalla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e avviare il processo di stampa.

    La struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contiene i dati che descrivono le selezioni effettuate dall'utente nella finestra di dialogo Stampa. Alcuni membri della struttura **PrintDlg** sono handle per gli oggetti memoria globale. Il [programma di esempio Print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copia i dati dagli oggetti memoria globale in blocchi di memoria gestiti dal programma e copia gli altri campi dalla struttura **PrintDlg** ai campi in una struttura di dati definita dal programma.

    Dopo aver archiviato i dati dalla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) nella struttura dei dati del programma, è possibile aprire la finestra di dialogo stato di stampa. La routine della finestra di dialogo stato stampa gestisce i messaggi della finestra di dialogo e avvia il thread di elaborazione stampa.

    Nell'esempio di codice seguente viene illustrato come copiare i dati dalla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) alla struttura dei dati del programma e come avviare il processo di stampa.

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  Se l'utente fa clic sul pulsante **Annulla** nella finestra di dialogo **stampa** comune, non viene eseguita alcuna ulteriore elaborazione.

 

 
