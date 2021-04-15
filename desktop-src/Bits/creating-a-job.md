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
# <a name="creating-a-job"></a>Creazione di un processo

Per creare un processo di trasferimento, chiamare il metodo [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) . Dopo che BITS crea il processo, [aggiungere i file al processo](adding-files-to-a-job.md) e [modificare le proprietà del processo](setting-and-retrieving-the-properties-of-a-job.md) nel modo appropriato per l'applicazione. Per attivare il processo nella coda, chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) .

Il metodo [**CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) crea un GUID che identifica in modo univoco il processo. Usare il GUID per [recuperare il processo dalla coda di trasferimento](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). Il nome visualizzato fornito quando si crea il processo non è univoco. più di un processo può usare lo stesso nome.

BITS limita il numero di processi nella coda ai processi 300 e il numero di processi che un utente può creare per il processo 60. Questi limiti non si applicano agli amministratori o ai servizi. Per modificare questi limiti predefiniti, vedere [criteri di gruppo](group-policies.md).

Nell'esempio seguente viene illustrato come creare un processo di download. Nell'esempio si presuppone che la \_ variabile g pbcm sia un puntatore di interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) valido. Per informazioni dettagliate su come creare il puntatore all'interfaccia **IBackgroundCopyManager** , vedere [connessione al servizio BITS](connecting-to-the-bits-service.md).


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



Per ottenere l'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) più recente, chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** . Nell'esempio seguente viene illustrato come ottenere l'interfaccia [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) .


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



 

 




