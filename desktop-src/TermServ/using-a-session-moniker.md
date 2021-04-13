---
title: Uso di un moniker di sessione
description: L'attivazione da sessione a sessione consente a un processo client di attivare un processo del server locale in una sessione specificata.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338871"
---
# <a name="using-a-session-moniker"></a>Uso di un moniker di sessione

L'attivazione da sessione a sessione consente a un processo client di attivare un processo del server locale in una sessione specificata. È possibile eseguire questa operazione per ogni singola sessione usando un moniker di sessione fornito dal sistema. Per ulteriori informazioni sulla creazione di un moniker di sessione, vedere [attivazione da sessione a sessione con un moniker di sessione](session-to-session-activation-with-a-session-moniker.md).

Nell'esempio seguente viene illustrato come attivare un processo del server locale con ID di classe "10000013-0000-0000-0000-000000000001" nella sessione con l'ID di sessione 3.

In primo luogo, l'esempio chiama la funzione [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com. L'esempio chiama quindi [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) per recuperare un puntatore a un'implementazione dell'interfaccia [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) . Questo oggetto archivia informazioni sulle operazioni di associazione del moniker. il puntatore è necessario per chiamare i metodi dell'interfaccia [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) . Successivamente, l'esempio chiama la funzione [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) per creare il moniker della sessione composita e quindi il metodo [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) per attivare la connessione tra il client e il processo server, usando il moniker della sessione appena creato. A questo punto è possibile usare il puntatore di interfaccia per eseguire le operazioni desiderate sull'oggetto. Infine, l'esempio rilascia il contesto di associazione e chiama la funzione [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



Poiché "{ID classe del moniker della classe}" è anche un modo per denominare un moniker della classe, è possibile usare la stringa seguente per denominare il moniker composito (il moniker della sessione composto dal moniker della classe) invece del modo illustrato nell'esempio precedente.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Se lo stesso utente è connesso a ogni sessione durante un'attivazione tra sessioni, è possibile attivare tutti i processi server configurati per l'esecuzione nella modalità di attivazione utente interattiva RunAs. Se utenti diversi sono connessi a ogni sessione, il server deve chiamare la funzione [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare i diritti utente appropriati prima che possa verificarsi un'attivazione e una connessione tra il client e il server. Un modo per ottenere questo risultato è che il server implementi un'interfaccia [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizzata e passa l'implementazione a **CoInitializeSecurity**. In ogni caso, l'utente client deve disporre delle autorizzazioni di [**avvio**](../com/launchpermission.md) e di [**accesso**](../com/accesspermission.md) appropriate specificate dall'applicazione in esecuzione nel server. Per ulteriori informazioni, vedere [sicurezza in com](../com/security-in-com.md).

 

Per ulteriori informazioni sui moniker e sulle modalità di attivazione forniti dal sistema, vedere [moniker](../com/monikers.md), l'interfaccia [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) e la [chiave AppID](/windows/desktop/com/appid-key) nella documentazione com di Platform Software Development Kit (SDK).

 

 