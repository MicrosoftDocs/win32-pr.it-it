---
title: Uso di un moniker di sessione
description: L'attivazione da sessione a sessione consente a un processo client di attivare un processo server locale in una sessione specificata.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fc5c65c3e2efd3e566a3fdde6982fefe5bb14fbefd98ca8abd335955b7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868851"
---
# <a name="using-a-session-moniker"></a>Uso di un moniker di sessione

L'attivazione da sessione a sessione consente a un processo client di attivare un processo server locale in una sessione specificata. È possibile eseguire questa operazione per sessione usando un moniker di sessione fornito dal sistema. Per altre informazioni sulla creazione di un moniker di sessione, vedere [Attivazione da sessione a sessione con un moniker di sessione](session-to-session-activation-with-a-session-moniker.md).

L'esempio seguente illustra come attivare un processo del server locale con ID classe "100000013-0000-0000-0000-000000000000001" nella sessione con ID sessione 3.

In primo luogo, l'esempio chiama [**la funzione CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM. L'esempio chiama quindi [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) per recuperare un puntatore a un'implementazione [**dell'interfaccia IBindCtx.**](/windows/win32/api/objidl/nn-objidl-ibindctx) Questo oggetto archivia informazioni sulle operazioni di associazione di moniker. Il puntatore è necessario per chiamare i metodi [**dell'interfaccia IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker) Successivamente, l'esempio chiama la funzione [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) per creare il moniker di sessione composita e quindi il metodo [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) per attivare la connessione tra il client e il processo server, usando il moniker di sessione appena creato. A questo punto è possibile usare il puntatore a interfaccia per eseguire le operazioni desiderate sull'oggetto . Infine, l'esempio rilascia il contesto di associazione e chiama la [**funzione CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


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



Poiché anche "{class id of the class moniker}" è un modo per assegnare un nome a un moniker di classe, è possibile usare la stringa seguente per assegnare un nome al moniker composito (il moniker di sessione composto con il moniker di classe) anziché il modo illustrato nell'esempio precedente.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Se lo stesso utente è connesso a ogni sessione durante un'attivazione tra sessioni, è possibile attivare correttamente qualsiasi processo server configurato per l'esecuzione nella modalità di attivazione utente interattivo RunAs. Se utenti diversi sono connessi a ogni sessione, il server deve chiamare la funzione [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare i diritti utente appropriati prima che possa verificarsi una corretta attivazione e connessione tra il client e il server. A tale scopo, il server può implementare un'interfaccia [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizzata e passare l'implementazione a **CoInitializeSecurity.** In ogni caso, l'utente client [](../com/accesspermission.md) deve disporre delle [**autorizzazioni**](../com/launchpermission.md) di avvio e accesso appropriate specificate dall'applicazione in esecuzione nel server. Per altre informazioni, vedere [Sicurezza in COM](../com/security-in-com.md).

 

Per altre informazioni sui moniker e i moniker forniti dal sistema e sulle modalità di attivazione, vedere [Moniker](../com/monikers.md), interfaccia [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) e [Chiave AppId](/windows/desktop/com/appid-key) nella documentazione COM in Platform Software Development Kit (SDK).

 

 