---
title: Gestione degli errori (BITS)
description: Esistono due tipi di errori da gestire nell'applicazione.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- gestione dei bit degli errori
- BIT del processo di trasferimento, errori
- BIT errori
- errori bit, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047679"
---
# <a name="handling-errors-bits"></a>Gestione degli errori (BITS)

Esistono due tipi di errori da gestire nell'applicazione. Il primo errore è una chiamata al metodo non riuscita. Ogni metodo restituisce un valore **HRESULT** . La pagina di riferimento per ogni metodo identifica i valori restituiti che è più probabile generare. Per ulteriori valori restituiti, vedere [valori restituiti bits](bits-return-values.md). Per ottenere il testo del messaggio associato al valore restituito, chiamare il metodo [**IBackgroundCopyManager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) .

Il secondo tipo di errore da gestire è un processo il cui [stato](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) passa a [stato \_ processo \_ \_ BG](/windows/desktop/api/Bits/ne-bits-bg_job_state) o **\_ \_ \_ \_ errore temporaneo stato processo BG**. Per recuperare informazioni correlate a questi tipi di errori, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) del processo. Il metodo restituisce un puntatore a interfaccia [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) che contiene le informazioni utilizzate per determinare la ragione dell'errore. È anche possibile ricevere la notifica di errore registrandosi per ricevere la notifica degli eventi. Per informazioni dettagliate, vedere la pagina relativa alla [registrazione di un callback com](registering-a-com-callback.md).

BITS considera atomici ogni processo. Se uno dei file del processo genera un errore, il processo rimane in uno stato di errore fino a quando l'errore non viene risolto. Pertanto, non è possibile eliminare il file che causa l'errore dal processo. Tuttavia, se l'errore è causato dal fatto che il server non è disponibile o un file remoto non valido, è possibile chiamare il metodo [**IBackgroundCopyJob3:: ReplaceRemotePrefix**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) o [**IBackgroundCopyFile2:: seremotename**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) per identificare un nuovo nome del server o del file.

Dopo aver determinato la cause dell'errore, eseguire una delle seguenti opzioni:

-   Annullare il processo chiamando il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .
-   Per un processo di download, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) per salvare i file che sono stati trasferiti correttamente prima dell'errore.
-   Correggere l'errore e chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per completare il processo.

Per un processo di caricamento-risposta, controllare il valore del membro **bytesTotal** della struttura dello [**stato di \_ \_ \_ avanzamento della risposta del processo BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) per determinare se l'errore si è verificato durante la parte del processo di caricamento o risposta. Si è verificato un errore durante il caricamento se il valore è di \_ dimensioni BG \_ sconosciute.

Nell'esempio seguente viene illustrato come recuperare un puntatore di interfaccia [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) . Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


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



 

 




