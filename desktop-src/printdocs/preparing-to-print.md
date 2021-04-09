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
# <a name="how-to-collect-print-job-information-from-the-user"></a><span data-ttu-id="a5414-103">Procedura: raccogliere informazioni sui processi di stampa dall'utente</span><span class="sxs-lookup"><span data-stu-id="a5414-103">How To: Collect Print Job Information from the User</span></span>

<span data-ttu-id="a5414-104">In questo argomento viene descritto come raccogliere informazioni sui processi di stampa dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a5414-104">This topic describes how to collect print job information from the user.</span></span>

## <a name="overview"></a><span data-ttu-id="a5414-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="a5414-105">Overview</span></span>

<span data-ttu-id="a5414-106">Raccogliere le informazioni sul processo di stampa dall'utente chiamando la funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a5414-106">Collect print job information from the user by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="a5414-107">Questa funzione Visualizza all'utente la finestra di dialogo **stampa** comune e restituisce le informazioni sul processo di stampa in una struttura di dati [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="a5414-107">This function displays the **Print** common dialog box to the user, and returns the print job information in a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>

<span data-ttu-id="a5414-108">La finestra di dialogo **stampa** comune viene visualizzata quando l'utente avvia un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="a5414-108">The **Print** common dialog box is displayed when the user starts a print job.</span></span> <span data-ttu-id="a5414-109">La finestra di dialogo **stampa** comune è una finestra di dialogo modale, che indica che l'utente non può interagire con la finestra principale fino a quando non viene chiusa la finestra di dialogo comune.</span><span class="sxs-lookup"><span data-stu-id="a5414-109">The **Print** common dialog box is a modal dialog box, which means that the user cannot interact with the main window until the common dialog box is closed.</span></span>

## <a name="collecting-print-job-information"></a><span data-ttu-id="a5414-110">Raccolta di informazioni sul processo di stampa</span><span class="sxs-lookup"><span data-stu-id="a5414-110">Collecting Print Job Information</span></span>

1.  <span data-ttu-id="a5414-111">Inizializzare l'elemento della struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="a5414-111">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure element.</span></span>

    <span data-ttu-id="a5414-112">Prima che un programma possa visualizzare la finestra di dialogo **stampa** comune, deve allocare e inizializzare una struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="a5414-112">Before a program can display the **Print** common dialog box , it must allocate and initialize a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="a5414-113">Passa quindi questa struttura alla funzione [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , che visualizza la finestra di dialogo e restituisce i dati del processo di stampa nella stessa struttura.</span><span class="sxs-lookup"><span data-stu-id="a5414-113">It then passes this structure to the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, which displays the dialog and returns the print job data in the same structure.</span></span> <span data-ttu-id="a5414-114">Nell'esempio di codice seguente viene illustrato il modo in cui il programma di esempio esegue questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="a5414-114">The following code example shows how the sample program performs this step.</span></span>

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

    

2.  <span data-ttu-id="a5414-115">Visualizza la finestra di dialogo **stampa** comune.</span><span class="sxs-lookup"><span data-stu-id="a5414-115">Display the **Print** common dialog box.</span></span>

    <span data-ttu-id="a5414-116">Chiamare [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) con la struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) inizializzata per visualizzare la finestra di dialogo **stampa** comune e raccogliere i dati utente, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="a5414-116">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) with the initialized [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to display the **Print** common dialog box and collect the user data, as shown in the following code example.</span></span>

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  <span data-ttu-id="a5414-117">Salvare i campi dalla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e avviare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="a5414-117">Save the fields from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and start the print job.</span></span>

    <span data-ttu-id="a5414-118">La struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contiene i dati che descrivono le selezioni effettuate dall'utente nella finestra di dialogo Stampa.</span><span class="sxs-lookup"><span data-stu-id="a5414-118">The [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure contains the data that describes the selections that the user made in the print dialog box.</span></span> <span data-ttu-id="a5414-119">Alcuni membri della struttura **PrintDlg** sono handle per gli oggetti memoria globale.</span><span class="sxs-lookup"><span data-stu-id="a5414-119">Some members of the **PRINTDLG** structure are handles to global memory objects.</span></span> <span data-ttu-id="a5414-120">Il [programma di esempio Print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copia i dati dagli oggetti memoria globale in blocchi di memoria gestiti dal programma e copia gli altri campi dalla struttura **PrintDlg** ai campi in una struttura di dati definita dal programma.</span><span class="sxs-lookup"><span data-stu-id="a5414-120">The [Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copies the data from the global memory objects to memory blocks that the program manages and copies other fields from the **PRINTDLG** structure to fields in a data structure that the program defined.</span></span>

    <span data-ttu-id="a5414-121">Dopo aver archiviato i dati dalla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) nella struttura dei dati del programma, è possibile aprire la finestra di dialogo stato di stampa.</span><span class="sxs-lookup"><span data-stu-id="a5414-121">After you store the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure in the program's data structure, you can open the print progress dialog box.</span></span> <span data-ttu-id="a5414-122">La routine della finestra di dialogo stato stampa gestisce i messaggi della finestra di dialogo e avvia il thread di elaborazione stampa.</span><span class="sxs-lookup"><span data-stu-id="a5414-122">The print progress dialog box procedure handles the dialog box messages and starts the print processing thread.</span></span>

    <span data-ttu-id="a5414-123">Nell'esempio di codice seguente viene illustrato come copiare i dati dalla struttura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) alla struttura dei dati del programma e come avviare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="a5414-123">The following code example shows how to copy the data from the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure to the program's data structure and how to start the print job.</span></span>

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

    

4.  <span data-ttu-id="a5414-124">Se l'utente fa clic sul pulsante **Annulla** nella finestra di dialogo **stampa** comune, non viene eseguita alcuna ulteriore elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a5414-124">If the user clicks the **Cancel** button in the **Print** common dialog box, no further processing is performed.</span></span>

 

 
