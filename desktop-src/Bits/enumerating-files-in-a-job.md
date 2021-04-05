---
title: Enumerazione dei file in un processo
description: Per enumerare i file in un processo, chiamare il metodo Metodo ibackgroundcopyjob EnumFiles. Il metodo restituisce un puntatore a interfaccia IEnumBackgroundCopyFiles che viene usato per enumerare i file.
ms.assetid: 0e1fa024-4576-434c-bc5f-518d246b5faa
keywords:
- trasferimento di bit di processo, enumerazione di file
- Enumerazione dei bit di file
- Enumerazione di bit, file
- BIT di trasferimento di file, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0db704e47a0e075801de2434ed30ba6fb8d8c91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708137"
---
# <a name="enumerating-files-in-a-job"></a><span data-ttu-id="342bb-108">Enumerazione dei file in un processo</span><span class="sxs-lookup"><span data-stu-id="342bb-108">Enumerating Files in a Job</span></span>

<span data-ttu-id="342bb-109">Per enumerare i file in un processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) .</span><span class="sxs-lookup"><span data-stu-id="342bb-109">To enumerate files in a job, call the [**IBackgroundCopyJob::EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) method.</span></span> <span data-ttu-id="342bb-110">Il metodo restituisce un puntatore a interfaccia [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) che viene usato per enumerare i file.</span><span class="sxs-lookup"><span data-stu-id="342bb-110">The method returns an [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) interface pointer that you use to enumerate the files.</span></span>

<span data-ttu-id="342bb-111">Si noti che l'elenco enumerato è uno snapshot dei file nel processo nel momento in cui si chiama il metodo [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) .</span><span class="sxs-lookup"><span data-stu-id="342bb-111">Note that the enumerated list is a snapshot of the files in the job at the time you call the [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) method.</span></span> <span data-ttu-id="342bb-112">Tuttavia, i valori delle proprietà di tali oggetti file riflettono i valori correnti del file.</span><span class="sxs-lookup"><span data-stu-id="342bb-112">However, the property values of those file objects reflect the current values of the file.</span></span>

<span data-ttu-id="342bb-113">Nell'esempio seguente viene illustrato come enumerare i file in un processo e recuperare le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="342bb-113">The following example shows how to enumerate files in a job and retrieve their properties.</span></span> <span data-ttu-id="342bb-114">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.</span><span class="sxs-lookup"><span data-stu-id="342bb-114">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr = 0;
IBackgroundCopyJob* pJob;
IEnumBackgroundCopyFiles* pFiles = NULL;
IBackgroundCopyFile* pFile = NULL;
IBackgroundCopyFile3* pFile3 = NULL;
WCHAR* pLocalFileName = NULL;
ULONG cFileCount = 0;
ULONG idx = 0;

hr = pJob->EnumFiles(&pFiles);
if (SUCCEEDED(hr))
{
  //Get the count of files in the job. 
  pFiles->GetCount(&cFileCount);

  //Enumerate the files in the job.
  for (idx=0; idx<cFileCount; idx++)
  {
    hr = pFiles->Next(1, &pFile, NULL);
    if (S_OK == hr)
    {
      // Query for the latest file interface.
      hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile3), (void**)&pFile3);
      pFile->Release();
      if (FAILED(hr))
      {
        wprintf(L"pFile->QueryInterface failed with 0x%x.\n", hr);
        goto cleanup;
      }

      // You can use the interface to retrieve the local and remote file
      // names, get the ranges to download if only part of the file content
      // is requested, determine the progress of the transfer, change the remote file
      // name, get the name of the temporary file that BITS uses to download
      // the file, determine if the file is downloaded from a peer, and set
      // the validation state of the file so it can be shared with peers.

      //Get the local name of the file.
      hr = pFile3->GetLocalName(&pLocalFileName);
      if (SUCCEEDED(hr))
      {
        //Do something with the file information.
      }

      CoTaskMemFree(pLocalFileName); 
      pFile3->Release();
      pFile3 = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pFiles->Release();
  pFiles = NULL;
}
```



 

 




