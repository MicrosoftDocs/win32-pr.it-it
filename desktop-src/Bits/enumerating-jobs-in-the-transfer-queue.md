---
title: Enumerazione dei processi nella coda di trasferimento
description: Per enumerare i processi dalla coda di trasferimento, chiamare il metodo IBackgroundCopyManager EnumJobs. Il metodo restituisce un puntatore a interfaccia IEnumBackgroundCopyJobs che viene usato per enumerare i processi nella coda.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- trasferimento di bit di processo, enumerazione
- Enumerazione dei processi nei bit della coda di trasferimento
- BIT della coda di trasferimento, enumerazione
- Enumerazione di bit
- Enumerazione di bit, processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328556"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a><span data-ttu-id="4f935-109">Enumerazione dei processi nella coda di trasferimento</span><span class="sxs-lookup"><span data-stu-id="4f935-109">Enumerating Jobs in the Transfer Queue</span></span>

<span data-ttu-id="4f935-110">Per enumerare i processi dalla coda di trasferimento, chiamare il metodo [**IBackgroundCopyManager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="4f935-110">To enumerate jobs from the transfer queue, call the [**IBackgroundCopyManager::EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="4f935-111">Il metodo restituisce un puntatore a interfaccia [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) che viene usato per enumerare i processi nella coda.</span><span class="sxs-lookup"><span data-stu-id="4f935-111">The method returns an [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) interface pointer that you use to enumerate the jobs in the queue.</span></span>

<span data-ttu-id="4f935-112">Per recuperare i processi dell'utente, impostare il primo parametro del metodo [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) su 0.</span><span class="sxs-lookup"><span data-stu-id="4f935-112">To retrieve the user's jobs, set the first parameter of the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method to 0.</span></span> <span data-ttu-id="4f935-113">Per recuperare tutti i processi nella coda, impostare il primo parametro del metodo **EnumJobs** su BG \_ Job \_ enum \_ All \_ Users.</span><span class="sxs-lookup"><span data-stu-id="4f935-113">To retrieve all jobs in the queue, set the first parameter of the **EnumJobs** method to BG\_JOB\_ENUM\_ALL\_USERS.</span></span> <span data-ttu-id="4f935-114">Solo gli utenti con privilegi di amministratore possono recuperare tutti i processi nella coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4f935-114">Only users with administrator privileges can retrieve all jobs in the transfer queue.</span></span>

<span data-ttu-id="4f935-115">Si noti che l'elenco enumerato è uno snapshot dei processi nella coda di trasferimento nel momento in cui si chiama il metodo [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) .</span><span class="sxs-lookup"><span data-stu-id="4f935-115">Note that the enumerated list is a snapshot of the jobs in the transfer queue at the time you call the [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) method.</span></span> <span data-ttu-id="4f935-116">Tuttavia, i valori delle proprietà di tali processi riflettono i valori correnti del processo.</span><span class="sxs-lookup"><span data-stu-id="4f935-116">However, the property values of those jobs reflect the current values of the job.</span></span>

<span data-ttu-id="4f935-117">Se si desidera recuperare singoli processi di trasferimento, chiamare il metodo [**IBackgroundCopyManager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .</span><span class="sxs-lookup"><span data-stu-id="4f935-117">If you want to retrieve individual transfer jobs, call the [**IBackgroundCopyManager::GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) method.</span></span>

<span data-ttu-id="4f935-118">Per enumerare i file in un processo, vedere [enumerazione di file in un processo](enumerating-files-in-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="4f935-118">To enumerate files in a job, see [Enumerating Files in a Job](enumerating-files-in-a-job.md).</span></span>

<span data-ttu-id="4f935-119">Nell'esempio seguente viene illustrato come enumerare i processi nella coda di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4f935-119">The following example shows how to enumerate jobs in the transfer queue.</span></span> <span data-ttu-id="4f935-120">La \_ variabile g XferManager nell'esempio è un puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="4f935-120">The g\_XferManager variable in the example is an [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="4f935-121">Per informazioni dettagliate su come creare il puntatore all'interfaccia **IBackgroundCopyManager** , vedere [connessione al servizio BITS](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="4f935-121">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




