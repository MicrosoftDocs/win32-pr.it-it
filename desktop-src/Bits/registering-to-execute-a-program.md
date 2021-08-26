---
title: Registrazione per l'esecuzione di un programma
description: È possibile eseguire la registrazione per fare in modo che BITS eserviti un programma in base agli eventi di processo trasferito ed errore, ma non agli eventi di modifica del processo. BITS esegue il programma nel contesto dell'utente.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- bits di notifica degli eventi, riga di comando
- registrazione per bits di notifica della riga di comando
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: db86f67ad899d190b24d74bfb04c501ca7881351cfb2f37ef53300666622c317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922031"
---
# <a name="registering-to-execute-a-program"></a>Registrazione per l'esecuzione di un programma

È possibile eseguire la registrazione per fare in modo che BITS eserviti un programma in base agli eventi di processo trasferito ed errore, ma non agli eventi di modifica del processo. BITS esegue il programma nel contesto dell'utente.

**Per eseguire la registrazione per l'esecuzione di un programma**

1.  Chiamare il **metodo IBackgroundCopyJob::QueryInterface** per recuperare un puntatore a [**interfaccia IBackgroundCopyJob2.**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) Specificare \_ \_ uuidof(IBackgroundCopyJob2) come identificatore di interfaccia.
2.  Chiamare il [**metodo IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) per specificare il programma da eseguire ed eventuali argomenti richiesti dal programma, ad esempio l'identificatore del processo.

3.  Chiamare il [**metodo IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) per specificare quando viene eseguita la riga di comando.

    È possibile specificare solo i flag di evento BG \_ NOTIFY JOB TRANSFERRED e \_ \_ BG NOTIFY JOB \_ \_ \_ ERROR. Il flag BG \_ NOTIFY JOB MODIFICATION viene \_ \_ ignorato.

Si noti che BITS non eseguirà il programma se è stata eseguita la registrazione anche per ricevere [callback COM](registering-a-com-callback.md) e il puntatore dell'interfaccia di callback è valido o se il metodo di notifica chiamato da BITS restituisce un codice di esito positivo. Tuttavia, se il metodo di notifica restituisce un codice di errore, ad esempio E \_ FAIL, BITS eseguirà la riga di comando.

BITS chiama la [**funzione CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per avviare il programma. Se si specifica una stringa di parametro, il primo parametro deve essere il nome del programma.

Nell'esempio seguente viene illustrato come eseguire la registrazione per eseguire un programma quando si verifica l'evento di trasferimento del processo. Nell'esempio si presuppone che il [**puntatore a interfaccia IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



Quando lo stato del processo diventa BG \_ JOB \_ STATE \_ TRANSFERRED, BITS esegue il programma specificato in pProgram. L'esempio seguente è una semplice implementazione di un programma che accetta un identificatore di processo come argomento. Il programma presuppone che al programma sia stato passato il numero corretto di argomenti.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 