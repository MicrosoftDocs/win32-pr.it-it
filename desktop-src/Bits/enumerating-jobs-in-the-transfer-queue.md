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
# <a name="enumerating-jobs-in-the-transfer-queue"></a>Enumerazione dei processi nella coda di trasferimento

Per enumerare i processi dalla coda di trasferimento, chiamare il metodo [**IBackgroundCopyManager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . Il metodo restituisce un puntatore a interfaccia [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) che viene usato per enumerare i processi nella coda.

Per recuperare i processi dell'utente, impostare il primo parametro del metodo [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) su 0. Per recuperare tutti i processi nella coda, impostare il primo parametro del metodo **EnumJobs** su BG \_ Job \_ enum \_ All \_ Users. Solo gli utenti con privilegi di amministratore possono recuperare tutti i processi nella coda di trasferimento.

Si noti che l'elenco enumerato è uno snapshot dei processi nella coda di trasferimento nel momento in cui si chiama il metodo [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) . Tuttavia, i valori delle proprietà di tali processi riflettono i valori correnti del processo.

Se si desidera recuperare singoli processi di trasferimento, chiamare il metodo [**IBackgroundCopyManager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) .

Per enumerare i file in un processo, vedere [enumerazione di file in un processo](enumerating-files-in-a-job.md).

Nell'esempio seguente viene illustrato come enumerare i processi nella coda di trasferimento. La \_ variabile g XferManager nell'esempio è un puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) . Per informazioni dettagliate su come creare il puntatore all'interfaccia **IBackgroundCopyManager** , vedere [connessione al servizio BITS](connecting-to-the-bits-service.md).


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



 

 




