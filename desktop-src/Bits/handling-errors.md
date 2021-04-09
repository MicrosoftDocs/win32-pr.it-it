---
title: Gestione degli errori (BITS)
description: Esistono due tipi di errori da gestire nell'applicazione.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- gestione dei bit degli errori
- BIT del processo di trasferimento, errori
- BIT errori
- errori bit, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047679"
---
# <a name="handling-errors-bits"></a><span data-ttu-id="12894-107">Gestione degli errori (BITS)</span><span class="sxs-lookup"><span data-stu-id="12894-107">Handling Errors (BITS)</span></span>

<span data-ttu-id="12894-108">Esistono due tipi di errori da gestire nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="12894-108">There are two types of errors to handle in your application.</span></span> <span data-ttu-id="12894-109">Il primo errore è una chiamata al metodo non riuscita.</span><span class="sxs-lookup"><span data-stu-id="12894-109">The first error is a failed method call.</span></span> <span data-ttu-id="12894-110">Ogni metodo restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12894-110">Each method returns an **HRESULT** value.</span></span> <span data-ttu-id="12894-111">La pagina di riferimento per ogni metodo identifica i valori restituiti che è più probabile generare.</span><span class="sxs-lookup"><span data-stu-id="12894-111">The reference page for each method identifies the return values that it is most likely to generate.</span></span> <span data-ttu-id="12894-112">Per ulteriori valori restituiti, vedere [valori restituiti bits](bits-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="12894-112">For additional return values, see [BITS Return Values](bits-return-values.md).</span></span> <span data-ttu-id="12894-113">Per ottenere il testo del messaggio associato al valore restituito, chiamare il metodo [**IBackgroundCopyManager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .</span><span class="sxs-lookup"><span data-stu-id="12894-113">To get the message text associated with the return value, call the [**IBackgroundCopyManager::GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) method.</span></span>

<span data-ttu-id="12894-114">Il secondo tipo di errore da gestire è un processo il cui [stato](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) passa a [stato \_ processo \_ \_ BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **\_ \_ \_ \_ errore temporaneo stato processo BG**.</span><span class="sxs-lookup"><span data-stu-id="12894-114">The second type of error to handle is a job whose [state](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) transitions to [BG\_JOB\_STATE\_ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) or **BG\_JOB\_STATE\_TRANSIENT\_ERROR**.</span></span> <span data-ttu-id="12894-115">Per recuperare informazioni correlate a questi tipi di errori, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) del processo.</span><span class="sxs-lookup"><span data-stu-id="12894-115">To retrieve information related to these types of errors, call the job's [**IBackgroundCopyJob::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) method.</span></span> <span data-ttu-id="12894-116">Il metodo restituisce un puntatore a interfaccia [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) che contiene le informazioni utilizzate per determinare la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="12894-116">The method returns an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer that contains information you use to determine the cause of the error.</span></span> <span data-ttu-id="12894-117">È anche possibile ricevere la notifica di errore registrandosi per ricevere la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="12894-117">You can also receive error notification by registering to receive event notification.</span></span> <span data-ttu-id="12894-118">Per informazioni dettagliate, vedere la pagina relativa alla [registrazione di un callback com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="12894-118">For details, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="12894-119">BITS considera atomici ogni processo.</span><span class="sxs-lookup"><span data-stu-id="12894-119">BITS considers each job to be atomic.</span></span> <span data-ttu-id="12894-120">Se uno dei file del processo genera un errore, il processo rimane in uno stato di errore fino a quando l'errore non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="12894-120">If one of the files in the job generates an error, the job remains in an error state until the error is resolved.</span></span> <span data-ttu-id="12894-121">Pertanto, non è possibile eliminare il file che causa l'errore dal processo.</span><span class="sxs-lookup"><span data-stu-id="12894-121">Thus, you cannot delete the file that is causing the error from the job.</span></span> <span data-ttu-id="12894-122">Tuttavia, se l'errore è causato dal fatto che il server non è disponibile o un file remoto non valido, è possibile chiamare il metodo [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2:: seremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) per identificare un nuovo nome del server o del file.</span><span class="sxs-lookup"><span data-stu-id="12894-122">However, if the error is caused by the server not being available or an invalid remote file, you can call the [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) or [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) method to identify a new server or file name.</span></span>

<span data-ttu-id="12894-123">Dopo aver determinato la cause dell'errore, eseguire una delle seguenti opzioni:</span><span class="sxs-lookup"><span data-stu-id="12894-123">After determining the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="12894-124">Annullare il processo chiamando il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="12894-124">Cancel the job by calling the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span>
-   <span data-ttu-id="12894-125">Per un processo di download, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) per salvare i file che sono stati trasferiti correttamente prima dell'errore.</span><span class="sxs-lookup"><span data-stu-id="12894-125">For a download job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method to save the files that transferred successfully before the error occurred.</span></span>
-   <span data-ttu-id="12894-126">Correggere l'errore e chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per completare il processo.</span><span class="sxs-lookup"><span data-stu-id="12894-126">Fix the error and call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method to finish the job.</span></span>

<span data-ttu-id="12894-127">Per un processo di caricamento-risposta, controllare il valore del membro **bytesTotal** della struttura dello [**stato di \_ \_ \_ avanzamento della risposta del processo BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) per determinare se l'errore si è verificato durante la parte del processo di caricamento o risposta.</span><span class="sxs-lookup"><span data-stu-id="12894-127">For an upload-reply job, check the value of the **BytesTotal** member of the [**BG\_JOB\_REPLY\_PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) structure to determine if the error occurred on the upload or reply portion of the job.</span></span> <span data-ttu-id="12894-128">Si è verificato un errore durante il caricamento se il valore è di \_ dimensioni BG \_ sconosciute.</span><span class="sxs-lookup"><span data-stu-id="12894-128">The error occurred on the upload if the value is BG\_SIZE\_UNKNOWN.</span></span>

<span data-ttu-id="12894-129">Nell'esempio seguente viene illustrato come recuperare un puntatore di interfaccia [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) .</span><span class="sxs-lookup"><span data-stu-id="12894-129">The following example shows how to retrieve an [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) interface pointer.</span></span> <span data-ttu-id="12894-130">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.</span><span class="sxs-lookup"><span data-stu-id="12894-130">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




