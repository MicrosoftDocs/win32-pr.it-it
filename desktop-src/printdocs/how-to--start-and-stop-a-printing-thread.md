---
description: In questo argomento viene descritto come avviare e arrestare il thread di elaborazione del processo di stampa.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Procedura: Avviare e arrestare un thread di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393f1f95efbb52c7cdd81316db000de22d45ca9e5dda0eadebb82ebaa3942350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686713"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>Procedura: Avviare e arrestare un thread di stampa

In questo argomento viene descritto come avviare e arrestare il thread di elaborazione del processo di stampa.

## <a name="overview"></a>Panoramica

Per impedire alle attività di stampa di bloccare la risposta dell'interfaccia utente, creare un thread separato per elaborare il processo di stampa. Il thread avviato all'avvio del programma è il thread che gestisce i messaggi della finestra risultati dall'interazione dell'utente e pertanto è il thread dell'interfaccia utente. Il programma deve elaborare questi messaggi senza ritardo perché l'interfaccia utente risponda al mouse e all'input della tastiera dell'utente in modo appropriato. Perché il programma possa rispondere rapidamente a questi messaggi, la quantità di elaborazione che può essere eseguita durante qualsiasi messaggio è limitata. Quando una richiesta dell'utente richiede un'elaborazione estesa, un thread diverso deve eseguire tale elaborazione per consentire la successiva interazione dell'utente da parte del programma.

L'elaborazione dei dati in un thread separato richiede al programma di coordinare il funzionamento del thread dell'interfaccia utente e del thread di elaborazione. Ad esempio, mentre il thread di elaborazione elabora i dati, il thread principale non deve modificare i dati. Un modo per gestire questo problema è tramite oggetti di sincronizzazione thread-safe, ad esempio semafori, eventi e mutex.

Allo stesso tempo, è necessario impedire l'interazione dell'utente durante l'esecuzione del thread di elaborazione. Nel programma di esempio i dati dell'applicazione sono protetti e l'interazione dell'utente è limitata dalla gestione dell'elaborazione del processo di stampa tramite la finestra di dialogo modale di stato. Una finestra di dialogo modale impedisce all'utente di interagire con la finestra principale del programma, impedendo all'utente di modificare i dati del programma dell'applicazione durante la stampa dei dati.

L'unica azione che l'utente può eseguire durante l'elaborazione di un processo di stampa è annullare il processo di stampa. Questa restrizione viene segnalata all'utente dalla forma del cursore. Quando il cursore si trova sul **pulsante** Annulla, viene visualizzato un cursore a freccia che indica che l'utente può fare clic su questo pulsante. Quando il cursore si trova su qualsiasi altra parte dell'area della finestra del programma, viene visualizzato un cursore di attesa che indica che il programma è occupato e non può rispondere all'input dell'utente.

## <a name="creating-the-printing-thread-procedure"></a>Creazione della routine del thread di stampa

È consigliabile includere queste funzionalità durante l'elaborazione della stampa.

-   **L'elaborazione della stampa è suddivisa in passaggi**

    È possibile dividere l'elaborazione di stampa in passaggi di elaborazione discreti che è possibile interrompere se l'utente fa clic sul **pulsante** Annulla. Ciò è utile perché l'elaborazione di stampa può includere operazioni a elevato utilizzo di processore. Suddividendo questa elaborazione in passaggi, è possibile impedire che l'elaborazione di stampa blocchi o ritardi altri thread o processi. Suddividendo l'elaborazione in passaggi logici, è anche possibile terminare in modo pulito l'elaborazione di stampa in qualsiasi momento, in modo che la terminazione di un processo di stampa prima del suo termine non lasci le risorse orfane.

    Questo è un elenco di esempio di passaggi di stampa.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Verificare la presenza di un evento di annullamento tra i passaggi**

    Quando l'utente fa clic sul **pulsante Annulla,** il thread dell'interfaccia utente segnala l'evento di annullamento. Il thread di elaborazione deve controllare periodicamente l'evento di annullamento per sapere quando un utente ha fatto clic sul **pulsante** Annulla. Le [**istruzioni WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) eseguono questo controllo e offrono anche la possibilità di eseguire altri programmi in modo che l'elaborazione del processo di stampa non blocchi o ritardi altri thread o processi.

    Nell'esempio di codice seguente viene illustrato uno dei test per verificare se si è verificato l'evento di annullamento.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Inviare aggiornamenti dello stato al thread dell'interfaccia utente**

    Come ogni passaggio di elaborazione della stampa, il thread di elaborazione della stampa invia messaggi di aggiornamento alla finestra di dialogo di stato della stampa in modo che possa aggiornare l'indicatore di stato. Si noti che la finestra di dialogo dello stato di stampa è in esecuzione nel thread dell'interfaccia utente.

    Nell'esempio di codice seguente viene illustrata una delle chiamate ai messaggi di aggiornamento.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Avvio del thread di stampa

Il thread di elaborazione della stampa viene eseguito fino a quando non viene restituita la funzione PrintThreadProc. La procedura seguente avvia il thread di stampa.

1.  **Preparare i dati e gli elementi dell'interfaccia utente per la stampa.**

    Prima di avviare il thread di elaborazione della stampa, è necessario inizializzare gli elementi dati che descrivono il processo di stampa e gli elementi dell'interfaccia utente. Questi elementi includono lo stato del cursore, in modo che il cursore di attesa verrà visualizzato in modo appropriato. È inoltre necessario configurare l'indicatore di stato in modo da riflettere le dimensioni del processo di stampa. Questi passaggi di preparazione sono descritti in dettaglio in [Procedura: Raccogliere informazioni sul processo di stampa dall'utente.](preparing-to-print.md)

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

    

2.  **Avviare il thread di elaborazione della stampa.**

    Chiamare [**CreateThread per**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) avviare il thread di elaborazione.

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

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) restituisce un handle al thread creato se il thread è stato creato correttamente. La funzione PrintThreadProc avviata nel nuovo thread controlla alcune condizioni prima di avviare l'elaborazione effettiva del processo di stampa. Se rileva errori in questi controlli, PrintThreadProc potrebbe restituire senza elaborare i dati del processo di stampa. Il thread dell'interfaccia utente può controllare se il thread di elaborazione è stato avviato correttamente attendendo l'handle del thread per un periodo di tempo più lungo del necessario per eseguire i test iniziali, ma non più del necessario. Quando il thread viene chiuso, l'handle per il thread viene segnalato. Il codice controlla lo stato del thread per un breve periodo di tempo dopo l'avvio del thread di elaborazione. La [**funzione WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) restituisce quando si verifica il timeout o viene segnalato l'handle del thread. Se la **funzione WaitForSingleObject** restituisce uno stato **WAIT OBJECT \_ \_ 0,** il thread è terminato in anticipo ed è quindi necessario chiudere la finestra di dialogo dello stato di stampa, come illustrato nell'esempio di codice seguente.

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

Quando l'utente  fa clic sul pulsante Annulla nella finestra di dialogo dello stato di avanzamento della stampa, il thread di stampa viene avvisato in modo che possa interrompere l'elaborazione del processo di stampa in modo ordinato. Mentre il **pulsante Annulla** e l'evento **quitEvent** sono aspetti importanti di questa elaborazione, è necessario progettare l'intera sequenza di elaborazione in modo che sia interrotta correttamente. Ciò significa che i passaggi nella sequenza non devono lasciare le risorse allocate che non vengono liberate se un utente annulla la sequenza prima del completamento.

Nell'esempio di codice seguente viene illustrato come il programma di esempio controlla **quitEvent** prima di elaborare ogni pagina del documento da stampare. Se **quitEvent viene segnalato** o è stato rilevato un errore, l'elaborazione di stampa viene arrestata.


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



 

 
