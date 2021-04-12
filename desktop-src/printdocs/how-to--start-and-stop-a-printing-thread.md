---
description: In questo argomento viene descritto come avviare e arrestare il thread di elaborazione dei processi di stampa.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Procedura: avviare e arrestare un thread di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233727"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="06390-103">Procedura: avviare e arrestare un thread di stampa</span><span class="sxs-lookup"><span data-stu-id="06390-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="06390-104">In questo argomento viene descritto come avviare e arrestare il thread di elaborazione dei processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="06390-105">Panoramica</span><span class="sxs-lookup"><span data-stu-id="06390-105">Overview</span></span>

<span data-ttu-id="06390-106">Per impedire che le attività di stampa blocchino la risposta dell'interfaccia utente, creare un thread separato per elaborare il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="06390-107">Il thread che viene avviato all'avvio del programma, è il thread che gestisce i messaggi della finestra che risultano dall'interazione dell'utente ed è quindi il thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="06390-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="06390-108">Il programma deve elaborare questi messaggi senza indugio affinché l'interfaccia utente risponda tempestivamente all'input del mouse e della tastiera dell'utente.</span><span class="sxs-lookup"><span data-stu-id="06390-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="06390-109">Affinché il programma sia in grado di rispondere rapidamente a questi messaggi, la quantità di elaborazione che può essere eseguita durante un messaggio è limitata.</span><span class="sxs-lookup"><span data-stu-id="06390-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="06390-110">Quando una richiesta utente richiede un'elaborazione estesa, un thread diverso deve eseguire tale elaborazione per consentire la gestione dell'interazione utente successiva da parte del programma.</span><span class="sxs-lookup"><span data-stu-id="06390-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="06390-111">Per l'elaborazione dei dati in un thread separato è necessario che il programma coordini il funzionamento del thread dell'interfaccia utente e del thread di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="06390-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="06390-112">Ad esempio, mentre il thread di elaborazione elabora i dati, il thread principale non deve modificare i dati.</span><span class="sxs-lookup"><span data-stu-id="06390-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="06390-113">Un modo per gestire questo problema consiste nell'usare oggetti di sincronizzazione thread-safe, ad esempio semafori, eventi e mutex.</span><span class="sxs-lookup"><span data-stu-id="06390-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="06390-114">Allo stesso tempo, è necessario impedire l'intervento dell'utente durante l'esecuzione del thread di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="06390-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="06390-115">Nel programma di esempio, i dati dell'applicazione sono protetti e l'interazione dell'utente è limitata dal fatto che l'elaborazione del processo di stampa viene gestita dalla finestra di dialogo stato modale.</span><span class="sxs-lookup"><span data-stu-id="06390-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="06390-116">Una finestra di dialogo modale impedisce all'utente di interagire con la finestra principale del programma che impedisce all'utente di modificare i dati del programma dell'applicazione mentre vengono stampati i dati.</span><span class="sxs-lookup"><span data-stu-id="06390-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="06390-117">L'unica azione che l'utente può eseguire durante l'elaborazione di un processo di stampa è l'annullamento del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="06390-118">Questa restrizione viene segnalata all'utente dalla forma del cursore.</span><span class="sxs-lookup"><span data-stu-id="06390-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="06390-119">Quando il cursore si trova sul pulsante **Annulla** , viene visualizzato un cursore a freccia che indica che l'utente può fare clic su questo pulsante.</span><span class="sxs-lookup"><span data-stu-id="06390-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="06390-120">Quando il cursore si trova su qualsiasi altra parte dell'area della finestra del programma, viene visualizzato un cursore di attesa che indica che il programma è occupato e non può rispondere all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="06390-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="06390-121">Creazione della procedura relativa al thread di stampa</span><span class="sxs-lookup"><span data-stu-id="06390-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="06390-122">È consigliabile includere queste funzionalità durante l'elaborazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="06390-123">**L'elaborazione della stampa è divisa in passaggi**</span><span class="sxs-lookup"><span data-stu-id="06390-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="06390-124">È possibile dividere l'elaborazione di stampa in passaggi di elaborazione discreti che è possibile interrompere se l'utente fa clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="06390-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="06390-125">Questa operazione è utile perché l'elaborazione di stampa può includere operazioni con utilizzo intensivo del processore.</span><span class="sxs-lookup"><span data-stu-id="06390-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="06390-126">Suddividendo questa elaborazione nei passaggi è possibile impedire che l'elaborazione di stampa blocchi o ritardi altri thread o processi.</span><span class="sxs-lookup"><span data-stu-id="06390-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="06390-127">Suddividendo l'elaborazione in passaggi logici, inoltre, è possibile terminare l'elaborazione di stampa in qualsiasi momento, in modo che l'interruzione di un processo di stampa prima del completamento non elimini le risorse orfane.</span><span class="sxs-lookup"><span data-stu-id="06390-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="06390-128">Di seguito è riportato un elenco di passaggi di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="06390-129">**Verificare la presenza di un evento di annullamento tra i passaggi**</span><span class="sxs-lookup"><span data-stu-id="06390-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="06390-130">Quando l'utente fa clic sul pulsante **Annulla** , il thread dell'interfaccia utente segnala l'evento di annullamento.</span><span class="sxs-lookup"><span data-stu-id="06390-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="06390-131">Il thread di elaborazione deve controllare periodicamente l'evento Cancel per capire quando un utente ha fatto clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="06390-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="06390-132">Le istruzioni [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) eseguono questo controllo e forniscono anche ad altri programmi la possibilità di eseguire in modo che l'elaborazione del processo di stampa non blocchi o ritardi altri thread o processi.</span><span class="sxs-lookup"><span data-stu-id="06390-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="06390-133">Nell'esempio di codice riportato di seguito viene illustrato uno dei test per verificare se si è verificato l'evento di annullamento.</span><span class="sxs-lookup"><span data-stu-id="06390-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="06390-134">**Invia aggiornamenti di stato al thread dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="06390-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="06390-135">Durante ogni passaggio di elaborazione della stampa, il thread di elaborazione della stampa invia i messaggi di aggiornamento alla finestra di dialogo stato di stampa, in modo che possa aggiornare l'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="06390-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="06390-136">Si noti che la finestra di dialogo stato di stampa è in esecuzione nel thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="06390-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="06390-137">Nell'esempio di codice riportato di seguito viene illustrata una delle chiamate di un messaggio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="06390-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="06390-138">Avvio del thread di stampa</span><span class="sxs-lookup"><span data-stu-id="06390-138">Starting the Printing Thread</span></span>

<span data-ttu-id="06390-139">Il thread di elaborazione della stampa viene eseguito fino a quando la funzione PrintThreadProc non restituisce.</span><span class="sxs-lookup"><span data-stu-id="06390-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="06390-140">I passaggi seguenti avviano il thread di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="06390-141">**Preparare i dati e gli elementi dell'interfaccia utente per la stampa.**</span><span class="sxs-lookup"><span data-stu-id="06390-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="06390-142">Prima di avviare il thread di elaborazione stampa, è necessario inizializzare gli elementi dati che descrivono il processo di stampa e gli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="06390-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="06390-143">Questi elementi includono lo stato del cursore, in modo che il cursore di attesa venga visualizzato in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="06390-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="06390-144">È inoltre necessario configurare l'indicatore di stato in modo da riflettere le dimensioni del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="06390-145">Questi passaggi di preparazione sono descritti in dettaglio in [procedura: raccogliere informazioni sui processi di stampa dall'utente](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="06390-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="06390-146">Nell'esempio di codice seguente viene illustrato come configurare l'indicatore di stato in modo da riflettere le dimensioni del processo di stampa richiesto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="06390-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  <span data-ttu-id="06390-147">**Avviare il thread di elaborazione stampa.**</span><span class="sxs-lookup"><span data-stu-id="06390-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="06390-148">Chiamare [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per avviare il thread di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="06390-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="06390-149">Nell'esempio di codice seguente viene avviato il thread di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="06390-149">The following code example starts the processing thread.</span></span>

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  <span data-ttu-id="06390-150">**Controllare se l'elaborazione della stampa non è riuscita all'avvio.**</span><span class="sxs-lookup"><span data-stu-id="06390-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="06390-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) restituisce un handle al thread creato se il thread è stato creato correttamente.</span><span class="sxs-lookup"><span data-stu-id="06390-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="06390-152">La funzione PrintThreadProc avviata nel nuovo thread verifica alcune condizioni prima di avviare l'elaborazione effettiva del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="06390-153">Se vengono rilevati errori in questi controlli, PrintThreadProc potrebbe restituire senza elaborare i dati del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="06390-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="06390-154">Il thread dell'interfaccia utente può verificare se il thread di elaborazione è stato avviato correttamente attendendo l'handle del thread per un periodo di tempo maggiore di quello necessario per eseguire i test iniziali, ma non più necessario.</span><span class="sxs-lookup"><span data-stu-id="06390-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="06390-155">Quando il thread viene chiuso, l'handle per il thread viene segnalato.</span><span class="sxs-lookup"><span data-stu-id="06390-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="06390-156">Il codice controlla lo stato del thread per un breve periodo di tempo dopo l'avvio del thread di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="06390-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="06390-157">La funzione [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) restituisce quando si verifica il timeout o viene segnalato l'handle del thread.</span><span class="sxs-lookup"><span data-stu-id="06390-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="06390-158">Se la funzione **WaitForSingleObject** restituisce lo stato di un **oggetto di attesa \_ \_ 0** , il thread è stato terminato in anticipo ed è quindi necessario chiudere la finestra di dialogo dello stato di stampa, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="06390-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="06390-159">Arresto del thread di stampa</span><span class="sxs-lookup"><span data-stu-id="06390-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="06390-160">Quando l'utente fa clic sul pulsante **Annulla** nella finestra di dialogo stato stampa, il thread di stampa riceve una notifica in modo che possa arrestare l'elaborazione del processo di stampa in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="06390-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="06390-161">Mentre il pulsante **Annulla** e l'evento **quitEvent** sono aspetti importanti di questa elaborazione, è necessario progettare l'intera sequenza di elaborazione affinché venga interrotta correttamente.</span><span class="sxs-lookup"><span data-stu-id="06390-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="06390-162">Ciò significa che i passaggi della sequenza non devono lasciare le risorse allocate che non vengono liberate se un utente annulla la sequenza prima del completamento.</span><span class="sxs-lookup"><span data-stu-id="06390-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="06390-163">Nell'esempio di codice seguente viene illustrato il modo in cui il programma di esempio controlla il **quitEvent** prima di elaborare ogni pagina del documento da stampare.</span><span class="sxs-lookup"><span data-stu-id="06390-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="06390-164">Se il **quitEvent** è segnalato o è stato rilevato un errore, l'elaborazione di stampa viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="06390-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
