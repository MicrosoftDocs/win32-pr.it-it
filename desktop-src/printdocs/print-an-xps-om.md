---
description: Viene descritto come inviare un OM XPS a una stampante come documento XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Stampare un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f1386352cff1556a5ce2403f34ebe4258c4110d4c3bf455990f3f1eb226d17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470904"
---
# <a name="print-an-xps-om"></a>Stampare un OM XPS

Viene descritto come inviare un OM XPS a una stampante come documento XPS.

Per istruzioni su come stampare un file XPS OM contenente un documento XPS completo, vedere [Print a complete XPS OM](#print-a-complete-xps-om). Per contenere un documento XPS, un OM XPS deve includere gli elementi elencati in [Creare un OM XPS vuoto.](create-a-blank-xps-om.md)

Per istruzioni su come stampare un OM XPS che viene creato o elaborato una pagina alla volta, vedere Stampare in modo incrementale [un OM XPS.](#incrementally-print-an-xps-om)

Prima di usare questi esempi di codice nel programma, leggere la dichiarazione di non responsabilità in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).

In questo argomento si apprenderà come eseguire le attività seguenti:

-   [Stampare un OM XPS completo](#print-a-complete-xps-om)
-   [Stampare in modo incrementale un OM XPS](#incrementally-print-an-xps-om)
-   [Argomenti correlati](#related-topics)

## <a name="print-a-complete-xps-om"></a>Stampare un OM XPS completo

Quando un OM XPS contiene un documento XPS completo, il metodo [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) può inviare il contenuto dell'OM XPS a una stampante o a una coda di stampa.

Per rilevare il completamento del processo di stampa, creare un handle di evento come illustrato nell'esempio seguente.


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



Per stampare un OM XPS completo:

1.  Creare un nuovo flusso del processo di stampa chiamando [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).
2.  Inviare il contenuto dell'OM XPS al flusso chiamando il metodo [**WriteToStream del**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) pacchetto.
3.  Chiudere il flusso del processo di stampa chiamando il metodo **Close del** flusso.
4.  Attendere che il processo di stampa segnali che è stato completato.
5.  Controllare lo stato di completamento.
6.  Chiudere e rilasciare le risorse.


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a>Stampare in modo incrementale un OM XPS

È possibile inviare i componenti del documento di un OM XPS a un processo di stampa in modo incrementale, creando un flusso del processo di stampa XPS e quindi passando i singoli componenti del documento al flusso del processo di stampa, uno alla volta. La sequenza in cui vengono inviati i componenti del documento determina come verranno visualizzati nel documento completato. Pertanto, prima che un programma possa chiamare il codice in questo esempio, deve organizzare correttamente i componenti del documento.

Prima di usare le interfacce OM XPS, inizializzare COM nel thread come illustrato nel codice di esempio seguente.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Per monitorare il completamento del processo di stampa, creare un handle di evento come illustrato nel codice di esempio seguente.


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



Creare un nuovo flusso del processo di stampa e un nuovo writer di pacchetti. Passare ognuno dei componenti del documento ai metodi del writer di pacchetti corrispondenti nella stessa sequenza in cui verranno visualizzati nel documento completato.

Avviare ogni documento nuovo e quindi aggiungerne le pagine. Dopo aver passato tutti i componenti del documento al flusso del processo di stampa, chiudere il flusso, attendere il completamento del processo di stampa, quindi chiudere e rilasciare le risorse aperte.

1.  Creare un nuovo flusso del processo di stampa chiamando [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).
2.  Creare un URI di parte per la parte FixedDocumentSequence.
3.  Creare un nuovo writer di pacchetti nel flusso del processo di stampa.
4.  Per ogni documento da scrivere:
    1.  Creare un nuovo URI di parte per la parte FixedDocument.
    2.  Avviare un nuovo documento nel writer del pacchetto.
    3.  Per ogni pagina del documento corrente, creare un URI di parte per la parte FixedPage e aggiungere la pagina al writer del pacchetto.
5.  Dopo aver aggiunto tutte le pagine al writer del pacchetto, chiuderlo.
6.  Chiudere il flusso del processo di stampa.
7.  Attendere il completamento del processo di stampa.
8.  Controllare lo stato di completamento.
9.  Chiudere e rilasciare le risorse aperte.


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



Quando il programma scrive i componenti del documento in modo incrementale, come illustrato in questo esempio, deve generare i nomi delle parti per ogni parte del documento inviata al flusso del processo di stampa. Nell'esempio precedente l'URI della parte FixedDocumentSequence viene creato da una stringa statica perché nel documento XPS è presente una sola parte di questo tipo. L'URI di ogni parte FixedPage e FixedDocument deve essere univoco all'interno del documento XPS. La compilazione dell'URI della parte usando l'indice di questi componenti consente di garantire che la stringa URI risultante sia univoca all'interno del documento XPS.


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



Per altre informazioni sulla struttura di un documento XPS, vedere l'XML Paper Specification [.](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Scrivere un OM XPS in un documento XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsPrintJob**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[**IXpsPrintJobStream**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[Inizializzare un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
