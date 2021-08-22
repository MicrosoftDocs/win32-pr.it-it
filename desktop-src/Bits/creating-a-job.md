---
title: Creazione di un processo
description: Per creare un processo di trasferimento, chiamare il metodo CreateJob IBackgroundCopyManager.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- transfer job BITS
- processo di trasferimento BITS, creazione
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0241d855d60178e87f28820f14b39e497f200fe5770933f293257e62b2d1b601
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528890"
---
# <a name="creating-a-job"></a>Creazione di un processo

Per creare un processo di trasferimento, chiamare [**il metodo IBackgroundCopyManager::CreateJob.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) Dopo che BITS ha creato il processo, [aggiungere file al](adding-files-to-a-job.md) processo e modificare le proprietà [del](setting-and-retrieving-the-properties-of-a-job.md) processo in base alle esigenze dell'applicazione. Per attivare il processo nella coda, chiamare il [**metodo IBackgroundCopyJob::Resume.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)

Il [**metodo CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crea un GUID che identifica in modo univoco il processo. Il GUID viene utilizzato per [recuperare il processo dalla coda di trasferimento](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). Il nome visualizzato specificato al momento della creazione del processo non è univoco. Più processi possono usare lo stesso nome.

BITS limita il numero di processi nella coda a 300 processi e il numero di processi che un utente può creare a 60 processi. Questi limiti non si applicano agli amministratori o ai servizi. Per modificare questi limiti predefiniti, vedere [Criteri di gruppo.](group-policies.md)

Nell'esempio seguente viene illustrato come creare un processo di download. Nell'esempio si presuppone che la variabile \_ g pbcm sia un puntatore a [**interfaccia IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) valido. Per informazioni dettagliate su come creare il puntatore a interfaccia **IBackgroundCopyManager,** vedere [Connessione al servizio BITS.](connecting-to-the-bits-service.md)


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



Per ottenere [**l'interfaccia IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) più recente, chiamare il **metodo IBackgroundCopyJob::QueryInterface.** L'esempio seguente illustra come ottenere [**l'interfaccia IBackgroundCopyJob5.**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)


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



 

 




