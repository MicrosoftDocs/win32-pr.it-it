---
title: Impostazione e recupero delle proprietà di un processo
description: Il proprietario del processo o un utente con privilegi di amministratore può impostare e recuperare le proprietà del processo in qualsiasi momento.
ms.assetid: 5d0ab96b-b818-4b41-8317-cf50ad17c12d
keywords:
- transfer job BITS , properties
- impostazione delle proprietà del processo BITS
- recupero delle proprietà del processo BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ded532d3c99c8f8063a5c372c60086f35320d321860b056b60f2cb5a9a4003
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004831"
---
# <a name="setting-and-retrieving-the-properties-of-a-job"></a>Impostazione e recupero delle proprietà di un processo

Il proprietario del processo o un utente con privilegi di amministratore può impostare e recuperare le proprietà del processo in qualsiasi momento. Per un elenco completo delle proprietà che è possibile impostare e recuperare, vedere le interfacce [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob), [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2), [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)e [**IBackgroundCopyJob4.**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)

I file contengono anche proprietà. Per informazioni su come recuperare un file e le relative proprietà da un processo, vedere [Enumerazione di file in un processo.](enumerating-files-in-a-job.md)

Per trasferire i file, non è necessario modificare i valori predefiniti delle proprietà del processo. BITS usa i valori predefiniti appropriati per l'applicazione tipica.

## <a name="setting-the-properties-of-a-job"></a>Impostazione delle proprietà di un processo

Nell'esempio seguente viene illustrato come impostare le proprietà che l'applicazione è più probabile [modificare:](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename) [priorità](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority) [,](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)interfaccia di notifica, [flag](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)di notifica e nome del file di risposta . Nell'esempio si presuppone che il puntatore a interfaccia [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, sia valido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob4* pJob4 = NULL;
CNotifyInterface *pNotify = new CNotifyInterface();

hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob4), (void**)&pJob4);
pJob->Release();

//The default priority level for a job is BG_JOB_PRIORITY_NORMAL. 
hr = pJob4->SetPriority(BG_JOB_PRIORITY_HIGH);
if (FAILED(hr))
{
  //Handle error
}

//By default, an application must poll BITS for the status of a job.
//To specify an IBackgroundCopyCallback interface pointer that receives event 
//notification based on the value of the notify flags property, set the notify 
//interface property. For details on the CNotifyInterface example class, see the 
//IBackgroundCopyCallback interface in the reference section.
hr = pJob4->SetNotifyInterface(pNotify);
if (SUCCEEDED(hr))
{
  hr = pJob4->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                            BG_NOTIFY_JOB_ERROR);
}
pNotify->Release();
if (FAILED(hr))
{
  //Handle error - failed to setup notification callbacks
}

//Only set the reply file name if the job's type is BG_JOB_TYPE_UPLOAD_REPLY.
//If you do not set the file name before calling the IBackgroundCopyJob::Resume 
//method, BITS generates a file name for you; the directory is the same as that
//specified for the local file name (the file being uploaded). To retrieve the 
//file name, call the IBackgroundCopyJob2::GetReplyFileName method.
hr = pJob4->SetReplyFileName(L"<REPLYPATHGOESHERE>");
if (FAILED(hr))
{
  //Handle error
}
pJob4->Release();
```



Per impostazione predefinita, BITS scarica il contenuto dal server di origine. Per scaricare contenuto da un peer, sia il computer che il processo devono abilitare il peer caching. Per abilitare il peer caching nel computer, impostare l'impostazione di Criteri di gruppo EnablePeerCaching. È anche possibile chiamare il [**metodo IBitsPeerCacheAdministration::SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) per abilitare il peer caching nel computer. Tuttavia, l'impostazione della preferenza viene sostituita dai criteri, se impostata. Per abilitare il peer caching per il processo, è necessario chiamare il metodo [**IBackgroundCopyJob4::SetPeerCachingFlags.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags)

Per specificare intestazioni personalizzate, un certificato client per l'autenticazione client e opzioni HTTP come i criteri di reindirizzamento, il controllo CRL e la specifica degli errori del certificato da ignorare, usare [**l'interfaccia IBackgroundCopyJobHttpOptions.**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) Per ottenere **l'interfaccia IBackgroundCopyJobHttpOptions,** eseguire una query su qualsiasi [**interfaccia IBackgroundCopyJob.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)

## <a name="retrieving-the-properties-of-a-job"></a>Recupero delle proprietà di un processo

Nell'esempio seguente viene illustrato come recuperare il [nome](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)visualizzato, [il proprietario,](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner) [lo](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)stato di avanzamento e [i](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) valori delle proprietà di stato di un processo. Nell'esempio si presuppone che il puntatore a interfaccia [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) pJob, sia valido.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR* pszJobName = NULL;
WCHAR* pszOwnerSid = NULL;
BOOL bResult;
DWORD dwNameSize = 0;
DWORD dwDomainSize = 0;
WCHAR* pszName = NULL;
WCHAR* pszDomain = NULL;
WCHAR* pszFullOwnerName = NULL;
PSID pSid = NULL;
SID_NAME_USE eNameUse;
BG_JOB_PROGRESS Progress;
int PercentOfFiles = 0;
BG_JOB_PRIORITY Priority;
BG_JOB_STATE State;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

//Name of the job to use in the user interface. The name is set when you 
//create the job. You can use the SetDisplayName method to change the name. 
hr = pJob->GetDisplayName(&pszJobName);
if (SUCCEEDED(hr))
{
  //Use the name in a user interface or output.
  CoTaskMemFree(pszJobName);       
}

//The owner property contains the SID of the job's owner. The following code
//shows how to get the domain and user names associated with the SID.
hr = pJob->GetOwner(&pszOwnerSID);
if (SUCCEEDED(hr))
{
  bResult = ConvertStringSidToSid(pszOwnerSid, &pSid);
  CoTaskMemFree(pszOwnerSid);
  if (bResult)
  {
    //Call LookupAccountSid twice. The first call retrieves the buffer size 
    //for name and domain and the second call retrieves the actual name and domain.
    LookupAccountSid(NULL, pSid, NULL, &cbNameSize, 
                               NULL, &cbDomainSize, &eNameUse);
    LastError = GetLastError();
    if (ERROR_INSUFFICIENT_BUFFER == LastError)
    {
      pszName = (WCHAR*)malloc(sizeof(WCHAR) * cbNameSize);
      pszDomain = (WCHAR*)malloc(sizeof(WCHAR) * cbDomainSize);
      if (pszName && pszDomain)
      {
        bResult = LookupAccountSid(NULL, pSid, pszName, &cbNameSize, 
                                   pszDomain, &cbDomainSize, &eNameUse);
        if (bResult)
        {
          pszFullName = (WCHAR*)malloc(sizeof(WCHAR)*(cbDomainSize+1+cbNameSize+1));
          if (pszFullName)
          {
            StringCchPrintf(pszFullName, cbDomainSize+1+cbNameSize+1, L"%s\\%s", pszDomain, pszName);
            //Do something with pszFullName. 
            free(pszFullName);
          }
        }
      }
      if (pszDomain)
        free(pszDomain);
      if(pszName)
        free(pszName);
    }
    else
    {
      //Handle error - most likely ERROR_NONE_MAPPED, could not find the SID.
    }
    LocalFree(pSid);
  }
}

//The state property identifies the current state of the job. For example, the 
//state of the job is BG_JOB_STATE_TRANSFERRING or BG_JOB_STATE_ERROR. 
hr = pJob->GetState(&State);
if (SUCCEEDED(hr))
{
  //Use JobStates[State] to set the text representation of the job's 
  //state in a user interface.
}

//Use the information contained in the BG_JOB_PROGRESS structure to determine the 
//overall progress of the job. The structure contains information on the number of 
//bytes and files transferred. 
hr = pJob->GetProgress(&Progress);
if (SUCCEEDED(hr))
{
  //Determine the progress of the job based on the number of files transferred.
  if (Progress.FilesTotal > 0)
  {
    PercentOfFiles = 100*Progress.FilesTransferred/Progress.FilesTotal
  }
  //For an example that shows determining the progress of the job based on the 
  //number of bytes transferred, see the topic Determing the Progress of a Job.
}
```



 

 




