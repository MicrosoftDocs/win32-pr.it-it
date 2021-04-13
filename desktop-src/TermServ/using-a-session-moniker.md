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
# <a name="using-a-session-moniker"></a><span data-ttu-id="71ae2-103">Uso di un moniker di sessione</span><span class="sxs-lookup"><span data-stu-id="71ae2-103">Using a Session Moniker</span></span>

<span data-ttu-id="71ae2-104">L'attivazione da sessione a sessione consente a un processo client di attivare un processo del server locale in una sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="71ae2-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="71ae2-105">È possibile eseguire questa operazione per ogni singola sessione usando un moniker di sessione fornito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="71ae2-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="71ae2-106">Per ulteriori informazioni sulla creazione di un moniker di sessione, vedere [attivazione da sessione a sessione con un moniker di sessione](session-to-session-activation-with-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="71ae2-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="71ae2-107">Nell'esempio seguente viene illustrato come attivare un processo del server locale con ID di classe "10000013-0000-0000-0000-000000000001" nella sessione con l'ID di sessione 3.</span><span class="sxs-lookup"><span data-stu-id="71ae2-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="71ae2-108">In primo luogo, l'esempio chiama la funzione [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com.</span><span class="sxs-lookup"><span data-stu-id="71ae2-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="71ae2-109">L'esempio chiama quindi [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) per recuperare un puntatore a un'implementazione dell'interfaccia [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="71ae2-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="71ae2-110">Questo oggetto archivia informazioni sulle operazioni di associazione del moniker. il puntatore è necessario per chiamare i metodi dell'interfaccia [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="71ae2-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="71ae2-111">Successivamente, l'esempio chiama la funzione [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) per creare il moniker della sessione composita e quindi il metodo [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) per attivare la connessione tra il client e il processo server, usando il moniker della sessione appena creato.</span><span class="sxs-lookup"><span data-stu-id="71ae2-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="71ae2-112">A questo punto è possibile usare il puntatore di interfaccia per eseguire le operazioni desiderate sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="71ae2-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="71ae2-113">Infine, l'esempio rilascia il contesto di associazione e chiama la funzione [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="71ae2-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


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



<span data-ttu-id="71ae2-114">Poiché "{ID classe del moniker della classe}" è anche un modo per denominare un moniker della classe, è possibile usare la stringa seguente per denominare il moniker composito (il moniker della sessione composto dal moniker della classe) invece del modo illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="71ae2-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="71ae2-115">Se lo stesso utente è connesso a ogni sessione durante un'attivazione tra sessioni, è possibile attivare tutti i processi server configurati per l'esecuzione nella modalità di attivazione utente interattiva RunAs.</span><span class="sxs-lookup"><span data-stu-id="71ae2-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="71ae2-116">Se utenti diversi sono connessi a ogni sessione, il server deve chiamare la funzione [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare i diritti utente appropriati prima che possa verificarsi un'attivazione e una connessione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="71ae2-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="71ae2-117">Un modo per ottenere questo risultato è che il server implementi un'interfaccia [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizzata e passa l'implementazione a **CoInitializeSecurity**.</span><span class="sxs-lookup"><span data-stu-id="71ae2-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="71ae2-118">In ogni caso, l'utente client deve disporre delle autorizzazioni di [**avvio**](../com/launchpermission.md) e di [**accesso**](../com/accesspermission.md) appropriate specificate dall'applicazione in esecuzione nel server.</span><span class="sxs-lookup"><span data-stu-id="71ae2-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="71ae2-119">Per ulteriori informazioni, vedere [sicurezza in com](../com/security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="71ae2-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="71ae2-120">Per ulteriori informazioni sui moniker e sulle modalità di attivazione forniti dal sistema, vedere [moniker](../com/monikers.md), l'interfaccia [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) e la [chiave AppID](/windows/desktop/com/appid-key) nella documentazione com di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="71ae2-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 