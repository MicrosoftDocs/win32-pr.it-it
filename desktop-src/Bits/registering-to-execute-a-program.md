---
title: Registrazione per l'esecuzione di un programma
description: È possibile eseguire la registrazione in modo che BITS esegua un programma basato su eventi trasferiti ed errori di processo, ma non eventi modificati dal processo. BITS esegue il programma nel contesto dell'utente.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- BIT di notifica degli eventi, riga di comando
- registrazione per i bit di notifica della riga di comando
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728146"
---
# <a name="registering-to-execute-a-program"></a><span data-ttu-id="9d8f8-106">Registrazione per l'esecuzione di un programma</span><span class="sxs-lookup"><span data-stu-id="9d8f8-106">Registering to Execute a Program</span></span>

<span data-ttu-id="9d8f8-107">È possibile eseguire la registrazione in modo che BITS esegua un programma basato su eventi trasferiti ed errori di processo, ma non eventi modificati dal processo.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-107">You can register to have BITS execute a program based on job transferred and error events, but not job modified events.</span></span> <span data-ttu-id="9d8f8-108">BITS esegue il programma nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-108">BITS executes the program in the user's context.</span></span>

<span data-ttu-id="9d8f8-109">**Per eseguire la registrazione per eseguire un programma**</span><span class="sxs-lookup"><span data-stu-id="9d8f8-109">**To register to execute a program**</span></span>

1.  <span data-ttu-id="9d8f8-110">Chiamare il metodo **Metodo ibackgroundcopyjob:: QueryInterface** per recuperare un puntatore all'interfaccia [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="9d8f8-110">Call the **IBackgroundCopyJob::QueryInterface** method to retrieve an [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface pointer.</span></span> <span data-ttu-id="9d8f8-111">Specificare \_ \_ uuidof (IBackgroundCopyJob2) come identificatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-111">Specify \_\_uuidof(IBackgroundCopyJob2) as the interface identifier.</span></span>
2.  <span data-ttu-id="9d8f8-112">Chiamare il metodo [**IBackgroundCopyJob2:: SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) per specificare il programma da eseguire e gli eventuali argomenti richiesti dal programma, ad esempio l'identificatore del processo.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-112">Call the [**IBackgroundCopyJob2::SetNotifyCmdLine**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) method to specify the program to execute and any arguments required by the program, such as the job identifier.</span></span>

3.  <span data-ttu-id="9d8f8-113">Chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) per specificare quando viene eseguita la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-113">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to specify when the command line executes.</span></span>

    <span data-ttu-id="9d8f8-114">È possibile specificare solo i flag per gli eventi di errore del processo BG \_ Notify \_ \_ trasferiti e BG \_ Notify \_ Job \_ .</span><span class="sxs-lookup"><span data-stu-id="9d8f8-114">You can only specify the BG\_NOTIFY\_JOB\_TRANSFERRED and BG\_NOTIFY\_JOB\_ERROR event flags.</span></span> <span data-ttu-id="9d8f8-115">Il \_ flag di modifica del processo di notifica BG \_ \_ viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-115">The BG\_NOTIFY\_JOB\_MODIFICATION flag is ignored.</span></span>

<span data-ttu-id="9d8f8-116">Si noti che BITS non eseguirà il programma se è stata registrata anche la [ricezione di callback com](registering-a-com-callback.md) e il puntatore all'interfaccia di callback è valido o se il metodo di notifica chiamato da BITS restituisce un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-116">Note that BITS will not execute the program if you also [registered to receive COM callbacks](registering-a-com-callback.md) and the callback interface pointer is valid or the notification method that BITS calls returns a success code.</span></span> <span data-ttu-id="9d8f8-117">Tuttavia, se il metodo di notifica restituisce un codice di errore, ad esempio E ha \_ esito negativo, BITS eseguirà la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-117">However, if the notification method returns a failure code, such as E\_FAIL, BITS will execute the command line.</span></span>

<span data-ttu-id="9d8f8-118">BITS chiama la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per avviare il programma.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-118">BITS calls the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function to launch the program.</span></span> <span data-ttu-id="9d8f8-119">Se si specifica una stringa di parametro, il primo parametro deve essere il nome del programma.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-119">If you specify a parameter string, the first parameter must be the program name.</span></span>

<span data-ttu-id="9d8f8-120">Nell'esempio seguente viene illustrato come eseguire la registrazione per eseguire un programma quando si verifica l'evento trasferito dal processo.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-120">The following example shows how to register to execute a program when the job-transferred event occurs.</span></span> <span data-ttu-id="9d8f8-121">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-121">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


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



<span data-ttu-id="9d8f8-122">Quando lo stato del processo diventa lo \_ stato del processo BG \_ \_ trasferito, BITS esegue il programma specificato in pProgram.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-122">When the state of the job becomes BG\_JOB\_STATE\_TRANSFERRED, BITS executes the program specified in pProgram.</span></span> <span data-ttu-id="9d8f8-123">L'esempio seguente è un'implementazione semplice di un programma che accetta come argomento un identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-123">The following example is a simple implementation of a program that takes a job identifier as an argument.</span></span> <span data-ttu-id="9d8f8-124">Il programma presuppone che venga passato il numero corretto di argomenti.</span><span class="sxs-lookup"><span data-stu-id="9d8f8-124">The program assumes the correct number of arguments are passed to it.</span></span>


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



 

 