---
title: Gestione degli errori (BITS)
description: Esistono due tipi di errori da gestire nell'applicazione.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- gestione degli errori BITS
- trasferimento del processo BITS, errori
- errori BITS
- errori BITS, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b0f389b6f0bdeefdfd5868b444384af26027b9b688a8fb83ba89ea370b9360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528811"
---
# <a name="handling-errors-bits"></a>Gestione degli errori (BITS)

Esistono due tipi di errori da gestire nell'applicazione. Il primo errore è una chiamata al metodo non riuscita. Ogni metodo restituisce un **valore HRESULT.** La pagina di riferimento per ogni metodo identifica i valori restituiti che è più probabile che generi. Per altri valori restituiti, vedere [Valori restituiti BITS.](bits-return-values.md) Per ottenere il testo del messaggio associato al valore restituito, chiamare il [**metodo IBackgroundCopyManager::GetErrorDescription.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription)

Il secondo tipo di errore da gestire è un processo [il](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) cui stato passa a [BG JOB \_ STATE \_ \_ ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR**. Per recuperare informazioni correlate a questi tipi di errori, chiamare il metodo [**IBackgroundCopyJob::GetError del**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) processo. Il metodo restituisce un puntatore a [**interfaccia IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) che contiene le informazioni usate per determinare la causa dell'errore. È anche possibile ricevere una notifica di errore registrando per ricevere la notifica degli eventi. Per informazioni dettagliate, [vedere Registrazione di un callback COM](registering-a-com-callback.md).

BITS considera ogni processo come atomico. Se uno dei file nel processo genera un errore, il processo rimane in uno stato di errore fino a quando l'errore non viene risolto. Non è quindi possibile eliminare il file che causa l'errore dal processo. Tuttavia, se l'errore è causato dalla non disponibilità del server o da un file remoto non valido, è possibile chiamare il metodo [**IBackgroundCopyJob3::ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2::SetRemoteName**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) per identificare un nuovo server o nome file.

Dopo aver determinato la causa dell'errore, eseguire una delle opzioni seguenti:

-   Annullare il processo chiamando il [**metodo IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   Per un processo di download, chiamare il [**metodo IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) per salvare i file trasferiti correttamente prima che si sia verificato l'errore.
-   Correggere l'errore e chiamare il [**metodo IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per completare il processo.

Per un processo di caricamento-risposta, controllare il valore del membro **BytesTotal** della struttura [**BG \_ JOB REPLY \_ \_ PROGRESS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) per determinare se l'errore si è verificato nella parte di caricamento o risposta del processo. L'errore si è verificato durante il caricamento se il valore è BG \_ SIZE \_ UNKNOWN.

Nell'esempio seguente viene illustrato come recuperare un puntatore a [**interfaccia IBackgroundCopyError.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) Nell'esempio si presuppone che il [**puntatore a interfaccia IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




