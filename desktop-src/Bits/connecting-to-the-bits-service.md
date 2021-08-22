---
title: Connessione al servizio BITS
description: Per connettersi al servizio BITS, creare un'istanza dell'oggetto BackgroundCopyManager, come illustrato nell'esempio seguente.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dacd97b78fa9c5d3a1e410a44e3c376368654e99a6f4ace9161d36b127d9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528941"
---
# <a name="connecting-to-the-bits-service"></a>Connessione al servizio BITS

Per connettersi al servizio di sistema BITS, creare un'istanza dell'oggetto BackgroundCopyManager, come illustrato nell'esempio seguente. Il servizio di sistema BITS è il Windows di sistema in esecuzione nel computer client che implementa la funzionalità di trasferimento in background.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



Per testare una versione specifica di BITS, usare un identificatore di classe simbolico per BackgroundCopyManager in base alla versione da controllare. Ad esempio, per testare BITS 10.2, usare CLSID \_ BackgroundCopyManager10 \_ 2.

Nell'esempio seguente viene illustrato come usare uno degli identificatori di classe simbolici.


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



Usare i metodi [**dell'interfaccia IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) per creare processi [di trasferimento,](creating-a-job.md) [enumerare i processi](enumerating-jobs-in-the-transfer-queue.md) nella coda e recuperare i [processi](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



BITS richiede che i proxy di interfaccia del client usino il livello di rappresentazione IDENTIFY o IMPERSONATE. Se l'applicazione non chiama [**CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)COM usa IDENTIFY per impostazione predefinita. BITS ha esito negativo con E \_ ACCESSDENIED se il livello di rappresentazione corretto non è impostato. Se si fornisce una libreria che esercita le interfacce BITS e un'applicazione che chiama la libreria imposta il livello di rappresentazione sotto IDENTIFY, sarà necessario chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare il livello di rappresentazione corretto per ogni interfaccia BITS chiamata.

Prima della chiusura dell'applicazione, rilasciare la copia del puntatore a interfaccia [**IBackgroundCopyManager,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) come illustrato nell'esempio seguente.


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata a BITS da .NET e C#](/windows/desktop/Bits/bits-dot-net) per BITS
</dt> </dl>

 

 