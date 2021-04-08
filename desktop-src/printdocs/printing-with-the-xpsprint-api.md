---
description: In questo argomento viene descritto come utilizzare l'API di stampa XPS per la stampa da un'applicazione Windows.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: "Procedura: stampare con l'API di stampa XPS"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884181"
---
# <a name="how-to-print-with-the-xps-print-api"></a>Procedura: stampare con l'API di stampa XPS

In questo argomento viene descritto come utilizzare l' [API di stampa XPS](xpsprint-api.md) per la stampa da un'applicazione Windows.

L' [API di stampa XPS](xpsprint-api.md) consente alle applicazioni native di Windows di stampare documenti XPS. Un'applicazione può creare un documento XPS utilizzando l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). Nell'argomento della guida sulle [attività comuni di programmazione dei documenti XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) viene descritto come eseguire questa operazione. Una volta creato un documento XPS, l'applicazione può usare l'API di stampa XPS per stamparlo.

L'uso dell' [API di stampa XPS](xpsprint-api.md) per stampare un documento da un'applicazione prevede i passaggi seguenti.

-   [Inizializza interfaccia COM](#initialize-com-interface)
-   [Creare un evento di completamento](#create-a-completion-event)
-   [Avviare un processo di stampa XPS](#start-an-xps-print-job)
-   [Creare un'interfaccia IXpsOMPackageWriter](#create-an-ixpsompackagewriter-interface)
-   [Chiudere l'interfaccia IXpsOMPackageWriter](#close-the-ixpsompackagewriter-interface)
-   [Chiudere il flusso del processo di stampa](#close-the-print-job-stream)
-   [Attendere l'evento di completamento](#wait-for-the-completion-event)
-   [Rilasciare le risorse](#release-resources)

L' [API di stampa XPS](xpsprint-api.md) richiede la stampa di un documento XPS. Nell'esempio seguente, il documento XPS viene creato quando viene inviato alla stampante dall'API di stampa XPS. È anche possibile creare un documento XPS senza inviarlo a una stampante usando l' [API Document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e mantenendolo come XPS om o salvando XPS OM come documento XPS. Per ulteriori informazioni sull'utilizzo di un OM XPS, vedere l'API documento XPS.

### <a name="initialize-com-interface"></a>Inizializza interfaccia COM

Inizializzare l'interfaccia COM, se l'applicazione non è già stata eseguita.


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a>Creare un evento di completamento

Creare un evento di completamento, che l' [API di stampa XPS](xpsprint-api.md) utilizza per notificare all'applicazione quando lo spooler di stampa ha ricevuto l'intero documento dall'applicazione. L'API di stampa XPS supporta inoltre un evento Progress, in modo che un'applicazione possa conoscere altre attività di spooling.


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a>Avviare un processo di stampa XPS

Avviare un processo di stampa XPS chiamando [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob). **StartXpsPrintJob** restituisce un flusso in cui l'applicazione invierà il documento da stampare.


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a>Creare un'interfaccia IXpsOMPackageWriter

Creare un'interfaccia [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) chiamando [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) sul flusso restituito da [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



Per ogni documento di questo processo di stampa, avviare un nuovo documento e quindi aggiungere pagine al documento.

### <a name="start-a-new-document"></a>Avvia un nuovo documento

Avviare un nuovo documento nel writer di pacchetti chiamando [**IXpsOMPackageWriter:: StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument). Se un documento è aperto quando viene chiamato questo metodo, viene chiuso e viene aperto un nuovo documento.


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a>Aggiungere una pagina

Chiamare [**IXpsOMPackageWriter:: AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) per scrivere ogni pagina del documento dall'applicazione al nuovo documento nel writer del pacchetto.

> [!Note]  
> Si presuppone che l'applicazione abbia creato la pagina prima di questo passaggio. Per ulteriori informazioni sulla creazione di pagine di documento e sull'aggiunta di contenuto, vedere le [attività comuni di programmazione dei documenti XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)).

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a>Chiudere l'interfaccia IXpsOMPackageWriter

Una volta scritti tutti i documenti per questo processo di stampa, chiamare [**IXpsOMPackageWriter:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) per chiudere il pacchetto.


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a>Chiudere il flusso del processo di stampa

Chiudere il flusso del processo di stampa chiamando [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), che indica allo spooler di stampa che l'intero processo di stampa è stato inviato dall'applicazione.


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a>Attendere l'evento di completamento

Attendere l'evento di completamento del processo di stampa.


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



Una volta segnalato l'evento di completamento, chiamare [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) per ottenere lo stato del processo.


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a>Rilasciare le risorse

Quando lo stato di un processo indica il completamento, rilasciare le interfacce e le risorse usate per il processo di stampa.


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
