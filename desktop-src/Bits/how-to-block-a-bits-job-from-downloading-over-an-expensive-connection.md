---
title: Controllare un download BITS su una connessione costosa
description: Bloccare il download su una connessione costosa, ad esempio un collegamento cellulare mobile.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- download di BITS, procedura
- scarica BITS, evitando costi elevati
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7cb09dbd277d9ec74ce4988db210bf80c22d97ccaa3054a170fc1c9913282cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959490"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a>Controllare un download BITS su una connessione costosa

Questo argomento illustra come bloccare il download di un processo BITS tramite una connessione costosa, ad esempio un collegamento cellulare mobile. BITS è un'API asincrona in cui l'applicazione crea un processo, aggiunge URL al processo e chiama la funzione [**Resume dell'oggetto**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) processo. A questo punto, BITS sceglie quando il processo viene scaricato in base a fattori come la priorità del processo e i criteri di trasferimento. Al termine del download del processo, BITS notifica all'applicazione che l'URL è stato scaricato (se l'applicazione è stata registrata per la notifica di completamento). Durante la durata del processo, se la rete dell'utente finale cambia, ad esempio se l'utente è in viaggio e attualmente incorre in tariffe di roaming, BITS sospende il processo fino a quando le condizioni di rete non sono ottimali. Le istruzioni dettagliate seguenti illustrano come creare il processo e specificare le impostazioni dei criteri di trasferimento appropriate.

### <a name="prerequisites"></a>Prerequisiti

-   Microsoft Visual Studio

## <a name="instructions"></a>Istruzioni

### <a name="step-1-include-the-required-bits-header-files"></a>Passaggio 1: Includere i file di intestazione BITS necessari

Inserire le direttive di intestazione seguenti all'inizio del file di origine.


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a>Passaggio 2: Inizializzare COM

Prima di creare un'istanza dell'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (usata per creare un processo BITS), è necessario inizializzare COM, impostare il modello di threading COM e specificare un livello di rappresentazione di almeno RPC \_ C IMP LEVEL \_ \_ \_ IMPERSONATE.


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



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a>Passaggio 3: Creare un'istanza dell'interfaccia IBackgroundCopyManager

Usare [**l'interfaccia IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) per creare processi di trasferimento, recuperare un oggetto enumeratore contenente i processi nella coda e recuperare singoli processi dalla coda.


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a>Passaggio 4: Creare il processo BITS

Solo l'utente che crea il processo o un utente con privilegi di amministratore può aggiungere file al processo e modificare le proprietà del processo.


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a>Passaggio 5: Specificare l'impostazione dei criteri di trasferimento per il processo

Qui è possibile specificare i criteri di trasferimento dello stato dei costi. È possibile impostare diversi flag BITS COST STATE usando una combinazione \_ OR bit per bit per ottenere i risultati \_ desiderati. 


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



## <a name="example"></a>Esempio

L'esempio di codice seguente illustra come impostare i criteri di trasferimento di un processo BITS in modo che l'elaborazione del processo non si verifichi quando vengono soddisfatte determinate condizioni, ad esempio quando l'utente è in roaming o ha superato il limite di trasferimento dati mensile.


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



 

 




