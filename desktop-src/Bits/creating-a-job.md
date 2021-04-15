---
title: Creazione di un processo
description: Per creare un processo di trasferimento, chiamare il metodo IBackgroundCopyManager CreateJob.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- BIT del processo di trasferimento
- trasferimento di bit di processo, creazione
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470998"
---
# <a name="creating-a-job"></a><span data-ttu-id="b8a6f-105">Creazione di un processo</span><span class="sxs-lookup"><span data-stu-id="b8a6f-105">Creating a Job</span></span>

<span data-ttu-id="b8a6f-106">Per creare un processo di trasferimento, chiamare il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="b8a6f-106">To create a transfer job, call the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span> <span data-ttu-id="b8a6f-107">Dopo che BITS crea il processo, [aggiungere i file al processo](adding-files-to-a-job.md) e [modificare le proprietà del processo](setting-and-retrieving-the-properties-of-a-job.md) nel modo appropriato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-107">After BITS creates the job, [add files to the job](adding-files-to-a-job.md) and [modify the job's properties](setting-and-retrieving-the-properties-of-a-job.md) as appropriate for your application.</span></span> <span data-ttu-id="b8a6f-108">Per attivare il processo nella coda, chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .</span><span class="sxs-lookup"><span data-stu-id="b8a6f-108">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) method.</span></span>

<span data-ttu-id="b8a6f-109">Il metodo [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crea un GUID che identifica in modo univoco il processo.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-109">The [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method creates a GUID that uniquely identifies the job.</span></span> <span data-ttu-id="b8a6f-110">Usare il GUID per [recuperare il processo dalla coda di trasferimento](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="b8a6f-110">You use the GUID to [retrieve the job from the transfer queue](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span> <span data-ttu-id="b8a6f-111">Il nome visualizzato fornito quando si crea il processo non è univoco. più di un processo può usare lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-111">The display name that you provide when you create the job is not unique; more than one job can use the same name.</span></span>

<span data-ttu-id="b8a6f-112">BITS limita il numero di processi nella coda ai processi 300 e il numero di processi che un utente può creare per il processo 60.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-112">BITS limits the number of jobs in the queue to 300 jobs and the number of jobs that a user can create to 60 job.</span></span> <span data-ttu-id="b8a6f-113">Questi limiti non si applicano agli amministratori o ai servizi.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-113">These limits do not apply to administrators or services.</span></span> <span data-ttu-id="b8a6f-114">Per modificare questi limiti predefiniti, vedere [criteri di gruppo](group-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b8a6f-114">To change these default limits, see [Group Policies](group-policies.md).</span></span>

<span data-ttu-id="b8a6f-115">Nell'esempio seguente viene illustrato come creare un processo di download.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-115">The following example shows how to create a download job.</span></span> <span data-ttu-id="b8a6f-116">Nell'esempio si presuppone che la \_ variabile g pbcm sia un puntatore di interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) valido.</span><span class="sxs-lookup"><span data-stu-id="b8a6f-116">The example assumes the g\_pbcm variable is a valid [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer.</span></span> <span data-ttu-id="b8a6f-117">Per informazioni dettagliate su come creare il puntatore all'interfaccia **IBackgroundCopyManager** , vedere [connessione al servizio BITS](connecting-to-the-bits-service.md).</span><span class="sxs-lookup"><span data-stu-id="b8a6f-117">For details on how to create the **IBackgroundCopyManager** interface pointer, see [Connecting to the BITS Service](connecting-to-the-bits-service.md).</span></span>


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



<span data-ttu-id="b8a6f-118">Per ottenere l'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) più recente, chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="b8a6f-118">To get the latest [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface, call the **IBackgroundCopyJob::QueryInterface** method.</span></span> <span data-ttu-id="b8a6f-119">Nell'esempio seguente viene illustrato come ottenere l'interfaccia [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .</span><span class="sxs-lookup"><span data-stu-id="b8a6f-119">The following example shows how to get the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface.</span></span>


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




