---
title: Controllare un download BITS tramite una connessione costosa
description: Blocca il download su una connessione costosa, ad esempio un collegamento cellulare mobile.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- Download di BITS, procedura
- Scarica BITS, evitando costosi
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857866"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a><span data-ttu-id="4e7d0-105">Controllare un download BITS tramite una connessione costosa</span><span class="sxs-lookup"><span data-stu-id="4e7d0-105">Control a BITS download over an expensive connection</span></span>

<span data-ttu-id="4e7d0-106">In questo argomento viene illustrato come bloccare il download di un processo BITS tramite una connessione costosa, ad esempio un collegamento cellulare mobile.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-106">This topic shows how to block a BITS job from downloading over an expensive connection such as a roaming cellular link.</span></span> <span data-ttu-id="4e7d0-107">BITS è un'API asincrona in cui l'applicazione crea un processo, aggiunge URL a tale processo e chiama la funzione [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) dell'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-107">BITS is an asynchronous API where the application creates a job, adds URLs to that job, and calls the job object's [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) function.</span></span> <span data-ttu-id="4e7d0-108">Da questo punto, BITS sceglie quando il processo viene scaricato in base a fattori quali la priorità del processo e i criteri di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-108">From that point, BITS chooses when the job downloads based on factors such as job priority and the transfer policy.</span></span> <span data-ttu-id="4e7d0-109">Al termine del download del processo, BITS invia una notifica all'applicazione che l'URL è stato scaricato (se l'applicazione è stata registrata per la notifica di completamento).</span><span class="sxs-lookup"><span data-stu-id="4e7d0-109">After the job has finished downloading, BITS notifies the application that the URL has been downloaded (if the application has registered for completion notification).</span></span> <span data-ttu-id="4e7d0-110">Durante la durata del processo, se la rete dell'utente finale viene modificata, ad esempio se l'utente è in viaggio e non è attualmente in corso tariffe di roaming, il processo verrà sospeso fino a quando le condizioni della rete non saranno ottimali.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-110">During the job's lifetime, if the end user's network changes—such as if the user is traveling and is currently incurring roaming fees—then BITS will suspend the job until network conditions are optimal.</span></span> <span data-ttu-id="4e7d0-111">Nelle istruzioni dettagliate riportate di seguito viene illustrato come creare il processo e specificare le impostazioni appropriate per i criteri di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-111">The following step-by-step instructions show how to create the job and specify the appropriate transfer policy settings.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4e7d0-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="4e7d0-112">Prerequisites</span></span>

-   <span data-ttu-id="4e7d0-113">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4e7d0-113">Microsoft Visual Studio</span></span>

## <a name="instructions"></a><span data-ttu-id="4e7d0-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4e7d0-114">Instructions</span></span>

### <a name="step-1-include-the-required-bits-header-files"></a><span data-ttu-id="4e7d0-115">Passaggio 1: includere i file di intestazione BITS necessari</span><span class="sxs-lookup"><span data-stu-id="4e7d0-115">Step 1: Include the required BITS header files</span></span>

<span data-ttu-id="4e7d0-116">Inserire le direttive header seguenti all'inizio del file di origine.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-116">Insert the following header directives at the top of the source file.</span></span>


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a><span data-ttu-id="4e7d0-117">Passaggio 2: inizializzare COM</span><span class="sxs-lookup"><span data-stu-id="4e7d0-117">Step 2: Initialize COM</span></span>

<span data-ttu-id="4e7d0-118">Prima di creare un'istanza dell'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (utilizzata per creare un processo BITS), è necessario inizializzare com, impostare il modello di threading com e specificare un livello di rappresentazione di almeno RPC \_ C Imp a livello di \_ \_ \_ rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-118">Before instantiating the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface (used to create a BITS job), you must initialize COM, set the COM threading model, and specify an impersonation level of at least RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a><span data-ttu-id="4e7d0-119">Passaggio 3: creare un'istanza dell'interfaccia IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="4e7d0-119">Step 3: Instantiate the IBackgroundCopyManager interface</span></span>

<span data-ttu-id="4e7d0-120">Utilizzare l'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) per creare processi di trasferimento, recuperare un oggetto enumeratore che contiene i processi nella coda e recuperare i singoli processi dalla coda.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-120">Use the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to create transfer jobs, retrieve an enumerator object that contains the jobs in the queue, and retrieve individual jobs from the queue.</span></span>


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a><span data-ttu-id="4e7d0-121">Passaggio 4: creare il processo BITS</span><span class="sxs-lookup"><span data-stu-id="4e7d0-121">Step 4: Create the BITS job</span></span>

<span data-ttu-id="4e7d0-122">Solo l'utente che crea il processo o un utente con privilegi di amministratore può aggiungere file al processo e modificare le proprietà del processo.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-122">Only the user who creates the job or a user with administrator privileges can add files to the job and change the job's properties.</span></span>


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a><span data-ttu-id="4e7d0-123">Passaggio 5: specificare l'impostazione dei criteri di trasferimento per il processo</span><span class="sxs-lookup"><span data-stu-id="4e7d0-123">Step 5: Specify the transfer policy setting for the job</span></span>

<span data-ttu-id="4e7d0-124">Qui è possibile specificare i criteri di trasferimento dello stato dei costi.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-124">This is where you specify the cost state transfer policy.</span></span> <span data-ttu-id="4e7d0-125">\_ \_ Per ottenere i risultati desiderati, è possibile impostare diversi flag  di stato di costo bits utilizzando una combinazione OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-125">You can set several BITS\_COST\_STATE flags by using a bitwise **OR** combination to achieve the desired results.</span></span>


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a><span data-ttu-id="4e7d0-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="4e7d0-126">Example</span></span>

<span data-ttu-id="4e7d0-127">Nell'esempio di codice seguente viene illustrato come impostare i criteri di trasferimento di un processo BITS in modo che l'elaborazione del processo non venga eseguita mentre vengono soddisfatte determinate condizioni, ad esempio quando l'utente è in roaming o ha superato il limite di trasferimento dati mensile.</span><span class="sxs-lookup"><span data-stu-id="4e7d0-127">The following code example shows how to set a BITS job's transfer policy so that the processing of the job doesn't occur while certain conditions are met—such as when the user is roaming or has exceeded their monthly data transfer limit.</span></span>


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




