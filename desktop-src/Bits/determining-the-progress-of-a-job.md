---
title: Determinazione dello stato di avanzamento di un processo
description: BITS mantiene le informazioni sullo stato di avanzamento per ogni processo. Utilizzare le informazioni sullo stato di avanzamento per determinare il numero di byte e file trasferiti.
ms.assetid: 8bac62b3-cb7e-45ba-85f0-95f3a7e8bffd
keywords:
- trasferimento BITS processo, stato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085ddcdeea106be2998f828879bc92273f22b328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855478"
---
# <a name="determining-the-progress-of-a-job"></a>Determinazione dello stato di avanzamento di un processo

BITS mantiene le informazioni sullo stato di avanzamento per ogni processo. Utilizzare le informazioni sullo stato di avanzamento per determinare il numero di byte e file trasferiti.

Per recuperare informazioni sullo stato di avanzamento del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: getProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) come illustrato nell'esempio seguente. Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


```C++
#define PROGRESS_COMPLETE_LEN 50

HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR szProgressComplete[PROGRESS_COMPLETE_LEN+1];
BG_JOB_PROGRESS Progress;

hr = pJob->GetProgress(&Progress); 
if (FAILED(hr))
{
  //Handle error
}

//Because the BytesTotal member can be 0 or BG_SIZE_UNKNOWN, you may not be able 
//to determine a percentage value to display, such as 57%. It is best to display a 
//string that shows the number of bytes transferred. For example, "123456 of 
//999999" or "123456 of Unknown".
if (BG_SIZE_UNKNOWN == Progress.BytesTotal)
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of Unknown", 
     Progress.BytesTransferred);
}
else
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of %I64d", 
     Progress.BytesTransferred, Progress.BytesTotal); 
}
```



Per recuperare informazioni sullo stato di avanzamento della parte di risposta di un processo di risposta di caricamento, chiamare il metodo [**IBackgroundCopyJob2:: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) , come illustrato nell'esempio seguente. Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


```C++
#define REPLY_COMPLETE_LEN 4

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szReplyComplete[REPLY_COMPLETE_LEN+1];
BG_JOB_REPLY_PROGRESS Progress;

pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
hr = pJob2->GetReplyProgress(&Progress); 
if (SUCCEEDED(hr))
{
  if (0 == Progress.BytesTotal) //The job type is not BG_JOB_TYPE_UPLOAD_REPLY
  {
    //Logic to deal with this case  
  }
  else if (BG_SIZE_UNKNOWN == Progress.BytesTotal) //The reply has not begun
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1, L"0%%");
  }
  else
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1 L"%I64d%%",
       100*Progress.BytesTransferred/Progress.BytesTotal); 
  }
}
```



I file contengono anche informazioni sullo stato di avanzamento. Per recuperare le informazioni sullo stato di avanzamento, usare il metodo [**IBackgroundCopyFile:: getProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyfile-getprogress) . Per informazioni su come recuperare i file di un processo, vedere [enumerazione di file in un processo](enumerating-files-in-a-job.md).

 

 




