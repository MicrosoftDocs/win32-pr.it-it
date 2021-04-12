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
# <a name="how-to-start-and-stop-a-printing-thread"></a>Procedura: avviare e arrestare un thread di stampa

In questo argomento viene descritto come avviare e arrestare il thread di elaborazione dei processi di stampa.

## <a name="overview"></a>Panoramica

Per impedire che le attività di stampa blocchino la risposta dell'interfaccia utente, creare un thread separato per elaborare il processo di stampa. Il thread che viene avviato all'avvio del programma, è il thread che gestisce i messaggi della finestra che risultano dall'interazione dell'utente ed è quindi il thread dell'interfaccia utente. Il programma deve elaborare questi messaggi senza indugio affinché l'interfaccia utente risponda tempestivamente all'input del mouse e della tastiera dell'utente. Affinché il programma sia in grado di rispondere rapidamente a questi messaggi, la quantità di elaborazione che può essere eseguita durante un messaggio è limitata. Quando una richiesta utente richiede un'elaborazione estesa, un thread diverso deve eseguire tale elaborazione per consentire la gestione dell'interazione utente successiva da parte del programma.

Per l'elaborazione dei dati in un thread separato è necessario che il programma coordini il funzionamento del thread dell'interfaccia utente e del thread di elaborazione. Ad esempio, mentre il thread di elaborazione elabora i dati, il thread principale non deve modificare i dati. Un modo per gestire questo problema consiste nell'usare oggetti di sincronizzazione thread-safe, ad esempio semafori, eventi e mutex.

Allo stesso tempo, è necessario impedire l'intervento dell'utente durante l'esecuzione del thread di elaborazione. Nel programma di esempio, i dati dell'applicazione sono protetti e l'interazione dell'utente è limitata dal fatto che l'elaborazione del processo di stampa viene gestita dalla finestra di dialogo stato modale. Una finestra di dialogo modale impedisce all'utente di interagire con la finestra principale del programma che impedisce all'utente di modificare i dati del programma dell'applicazione mentre vengono stampati i dati.

L'unica azione che l'utente può eseguire durante l'elaborazione di un processo di stampa è l'annullamento del processo di stampa. Questa restrizione viene segnalata all'utente dalla forma del cursore. Quando il cursore si trova sul pulsante **Annulla** , viene visualizzato un cursore a freccia che indica che l'utente può fare clic su questo pulsante. Quando il cursore si trova su qualsiasi altra parte dell'area della finestra del programma, viene visualizzato un cursore di attesa che indica che il programma è occupato e non può rispondere all'input dell'utente.

## <a name="creating-the-printing-thread-procedure"></a>Creazione della procedura relativa al thread di stampa

È consigliabile includere queste funzionalità durante l'elaborazione di stampa.

-   **L'elaborazione della stampa è divisa in passaggi**

    È possibile dividere l'elaborazione di stampa in passaggi di elaborazione discreti che è possibile interrompere se l'utente fa clic sul pulsante **Annulla** . Questa operazione è utile perché l'elaborazione di stampa può includere operazioni con utilizzo intensivo del processore. Suddividendo questa elaborazione nei passaggi è possibile impedire che l'elaborazione di stampa blocchi o ritardi altri thread o processi. Suddividendo l'elaborazione in passaggi logici, inoltre, è possibile terminare l'elaborazione di stampa in qualsiasi momento, in modo che l'interruzione di un processo di stampa prima del completamento non elimini le risorse orfane.

    Di seguito è riportato un elenco di passaggi di stampa.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Verificare la presenza di un evento di annullamento tra i passaggi**

    Quando l'utente fa clic sul pulsante **Annulla** , il thread dell'interfaccia utente segnala l'evento di annullamento. Il thread di elaborazione deve controllare periodicamente l'evento Cancel per capire quando un utente ha fatto clic sul pulsante **Annulla** . Le istruzioni [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) eseguono questo controllo e forniscono anche ad altri programmi la possibilità di eseguire in modo che l'elaborazione del processo di stampa non blocchi o ritardi altri thread o processi.

    Nell'esempio di codice riportato di seguito viene illustrato uno dei test per verificare se si è verificato l'evento di annullamento.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Invia aggiornamenti di stato al thread dell'interfaccia utente**

    Durante ogni passaggio di elaborazione della stampa, il thread di elaborazione della stampa invia i messaggi di aggiornamento alla finestra di dialogo stato di stampa, in modo che possa aggiornare l'indicatore di stato. Si noti che la finestra di dialogo stato di stampa è in esecuzione nel thread dell'interfaccia utente.

    Nell'esempio di codice riportato di seguito viene illustrata una delle chiamate di un messaggio di aggiornamento.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Avvio del thread di stampa

Il thread di elaborazione della stampa viene eseguito fino a quando la funzione PrintThreadProc non restituisce. I passaggi seguenti avviano il thread di stampa.

1.  **Preparare i dati e gli elementi dell'interfaccia utente per la stampa.**

    Prima di avviare il thread di elaborazione stampa, è necessario inizializzare gli elementi dati che descrivono il processo di stampa e gli elementi dell'interfaccia utente. Questi elementi includono lo stato del cursore, in modo che il cursore di attesa venga visualizzato in modo appropriato. È inoltre necessario configurare l'indicatore di stato in modo da riflettere le dimensioni del processo di stampa. Questi passaggi di preparazione sono descritti in dettaglio in [procedura: raccogliere informazioni sui processi di stampa dall'utente](preparing-to-print.md).

    Nell'esempio di codice seguente viene illustrato come configurare l'indicatore di stato in modo da riflettere le dimensioni del processo di stampa richiesto dall'utente.

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

    

2.  **Avviare il thread di elaborazione stampa.**

    Chiamare [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per avviare il thread di elaborazione.

    Nell'esempio di codice seguente viene avviato il thread di elaborazione.

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

    

3.  **Controllare se l'elaborazione della stampa non è riuscita all'avvio.**

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) restituisce un handle al thread creato se il thread è stato creato correttamente. La funzione PrintThreadProc avviata nel nuovo thread verifica alcune condizioni prima di avviare l'elaborazione effettiva del processo di stampa. Se vengono rilevati errori in questi controlli, PrintThreadProc potrebbe restituire senza elaborare i dati del processo di stampa. Il thread dell'interfaccia utente può verificare se il thread di elaborazione è stato avviato correttamente attendendo l'handle del thread per un periodo di tempo maggiore di quello necessario per eseguire i test iniziali, ma non più necessario. Quando il thread viene chiuso, l'handle per il thread viene segnalato. Il codice controlla lo stato del thread per un breve periodo di tempo dopo l'avvio del thread di elaborazione. La funzione [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) restituisce quando si verifica il timeout o viene segnalato l'handle del thread. Se la funzione **WaitForSingleObject** restituisce lo stato di un **oggetto di attesa \_ \_ 0** , il thread è stato terminato in anticipo ed è quindi necessario chiudere la finestra di dialogo dello stato di stampa, come illustrato nell'esempio di codice seguente.

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

    

## <a name="stopping-the-printing-thread"></a>Arresto del thread di stampa

Quando l'utente fa clic sul pulsante **Annulla** nella finestra di dialogo stato stampa, il thread di stampa riceve una notifica in modo che possa arrestare l'elaborazione del processo di stampa in modo ordinato. Mentre il pulsante **Annulla** e l'evento **quitEvent** sono aspetti importanti di questa elaborazione, è necessario progettare l'intera sequenza di elaborazione affinché venga interrotta correttamente. Ciò significa che i passaggi della sequenza non devono lasciare le risorse allocate che non vengono liberate se un utente annulla la sequenza prima del completamento.

Nell'esempio di codice seguente viene illustrato il modo in cui il programma di esempio controlla il **quitEvent** prima di elaborare ogni pagina del documento da stampare. Se il **quitEvent** è segnalato o è stato rilevato un errore, l'elaborazione di stampa viene arrestata.


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



 

 
