---
description: Viene descritto come inviare un oggetto XPS OM a una stampante come documento XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Stampare un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050194"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="f3085-103">Stampare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f3085-103">Print an XPS OM</span></span>

<span data-ttu-id="f3085-104">Viene descritto come inviare un oggetto XPS OM a una stampante come documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f3085-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="f3085-105">Per istruzioni su come stampare un OM XPS che contiene un documento XPS completo, vedere [stampare un OM XPS completo](#print-a-complete-xps-om).</span><span class="sxs-lookup"><span data-stu-id="f3085-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="f3085-106">Per contenere un documento XPS, un OM XPS deve includere gli elementi elencati nella pagina relativa alla [creazione di un OM XPS vuoto](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="f3085-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="f3085-107">Per istruzioni su come stampare un OM XPS creato o elaborato una pagina alla volta, vedere la pagina relativa alla [stampa incrementale di un OM XPS](#incrementally-print-an-xps-om).</span><span class="sxs-lookup"><span data-stu-id="f3085-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="f3085-108">Prima di usare questi esempi di codice nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="f3085-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="f3085-109">In questo argomento si apprenderà come eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3085-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="f3085-110">Stampa un OM XPS completo</span><span class="sxs-lookup"><span data-stu-id="f3085-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="f3085-111">Stampare in modo incrementale un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f3085-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="f3085-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3085-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="f3085-113">Stampa un OM XPS completo</span><span class="sxs-lookup"><span data-stu-id="f3085-113">Print a complete XPS OM</span></span>

<span data-ttu-id="f3085-114">Quando un oggetto XPS OM contiene un documento XPS completo, il metodo [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) può inviare il contenuto di XPS om a una stampante o a una coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="f3085-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="f3085-115">Per rilevare il completamento del processo di stampa, creare un handle di evento, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="f3085-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="f3085-116">Per stampare un OM XPS completo:</span><span class="sxs-lookup"><span data-stu-id="f3085-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="f3085-117">Creare un nuovo flusso del processo di stampa chiamando [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="f3085-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="f3085-118">Inviare il contenuto di XPS OM al flusso chiamando il metodo [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f3085-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="f3085-119">Chiudere il flusso del processo di stampa chiamando il metodo **Close** del flusso.</span><span class="sxs-lookup"><span data-stu-id="f3085-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="f3085-120">Attendere che il processo di stampa segnali che è stato completato.</span><span class="sxs-lookup"><span data-stu-id="f3085-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="f3085-121">Verificare lo stato di completamento.</span><span class="sxs-lookup"><span data-stu-id="f3085-121">Check the completion status.</span></span>
6.  <span data-ttu-id="f3085-122">Chiudere e rilasciare le risorse.</span><span class="sxs-lookup"><span data-stu-id="f3085-122">Close and release resources.</span></span>


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



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="f3085-123">Stampare in modo incrementale un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f3085-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="f3085-124">È possibile inviare i componenti del documento di un OM XPS a un processo di stampa in modo incrementale, creando un flusso del processo di stampa XPS e passando quindi i singoli componenti del documento al flusso del processo di stampa, uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="f3085-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="f3085-125">La sequenza in cui vengono inviati i componenti del documento determina il modo in cui verranno visualizzati nel documento terminato.</span><span class="sxs-lookup"><span data-stu-id="f3085-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="f3085-126">Pertanto, prima che un programma possa chiamare il codice in questo esempio, è necessario che organizzi correttamente i componenti del documento.</span><span class="sxs-lookup"><span data-stu-id="f3085-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="f3085-127">Prima di usare le interfacce XPS OM, inizializzare COM nel thread come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="f3085-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="f3085-128">Per monitorare il completamento del processo di stampa, creare un handle di evento, come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="f3085-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


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



<span data-ttu-id="f3085-129">Creare un nuovo flusso del processo di stampa e un nuovo writer del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f3085-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="f3085-130">Passare ogni componente del documento ai corrispondenti metodi del writer di pacchetti nella stessa sequenza in cui verranno visualizzati nel documento terminato.</span><span class="sxs-lookup"><span data-stu-id="f3085-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="f3085-131">Avviare ogni documento nuovo, quindi aggiungere pagine.</span><span class="sxs-lookup"><span data-stu-id="f3085-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="f3085-132">Dopo aver passato tutti i componenti del documento al flusso del processo di stampa, chiudere il flusso, attendere il completamento del processo di stampa, quindi chiudere e rilasciare le risorse aperte.</span><span class="sxs-lookup"><span data-stu-id="f3085-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="f3085-133">Creare un nuovo flusso del processo di stampa chiamando [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="f3085-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="f3085-134">Creare un URI della parte per la parte FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="f3085-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="f3085-135">Creare un nuovo writer di pacchetti nel flusso del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f3085-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="f3085-136">Per ogni documento da scrivere:</span><span class="sxs-lookup"><span data-stu-id="f3085-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="f3085-137">Creare un nuovo URI della parte per la parte FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="f3085-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="f3085-138">Avviare un nuovo documento nel writer del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f3085-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="f3085-139">Per ogni pagina del documento corrente, creare un URI della parte per la parte FixedPage e aggiungere la pagina al writer del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f3085-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="f3085-140">Dopo che tutte le pagine sono state aggiunte al writer del pacchetto, chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="f3085-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="f3085-141">Chiudere il flusso del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f3085-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="f3085-142">Attendere il completamento del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f3085-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="f3085-143">Verificare lo stato di completamento.</span><span class="sxs-lookup"><span data-stu-id="f3085-143">Check the completion status.</span></span>
9.  <span data-ttu-id="f3085-144">Chiudere e rilasciare le risorse aperte.</span><span class="sxs-lookup"><span data-stu-id="f3085-144">Close and release open resources.</span></span>


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



<span data-ttu-id="f3085-145">Quando il programma scrive i componenti del documento in modo incrementale, come illustrato in questo esempio, deve generare i nomi delle parti per ogni parte del documento che invia al flusso del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="f3085-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="f3085-146">Nell'esempio precedente, l'URI della parte FixedDocumentSequence viene creato da una stringa statica perché esiste solo una parte di questo tipo nel documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f3085-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="f3085-147">L'URI di ogni parte FixedPage e FixedDocument deve essere univoco all'interno del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f3085-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="f3085-148">La compilazione dell'URI della parte mediante l'indice di questi componenti consente di garantire che la stringa URI risultante sia univoca all'interno del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f3085-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


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



<span data-ttu-id="f3085-149">Per ulteriori informazioni sulla struttura di un documento XPS, vedere la [specifica di XML Paper](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="f3085-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3085-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3085-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f3085-151">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="f3085-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="f3085-152">Scrivere un OM XPS in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="f3085-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="f3085-153">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="f3085-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="f3085-154">**CoInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="f3085-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="f3085-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="f3085-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="f3085-156">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="f3085-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="f3085-157">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="f3085-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="f3085-158">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="f3085-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="f3085-159">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="f3085-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="f3085-160">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="f3085-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="f3085-161">**StartXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="f3085-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="f3085-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="f3085-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="f3085-163">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="f3085-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="f3085-164">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f3085-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="f3085-165">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="f3085-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f3085-166">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="f3085-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
