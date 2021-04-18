---
description: 'Una delle attività principali di IWbemLocator:: ConnectServer per WMI è la restituzione di un puntatore a un proxy IWbemServices.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Impostazione dell'autenticazione mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314576"
---
# <a name="setting-authentication-using-c"></a><span data-ttu-id="90d66-103">Impostazione dell'autenticazione mediante C++</span><span class="sxs-lookup"><span data-stu-id="90d66-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="90d66-104">Una delle attività principali di [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) per WMI è la restituzione di un puntatore a un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="90d66-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="90d66-105">Tramite il proxy **IWbemServices** è possibile accedere alle funzionalità dell'infrastruttura WMI.</span><span class="sxs-lookup"><span data-stu-id="90d66-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="90d66-106">Il puntatore al proxy **IWbemServices** , tuttavia, ha l'identità del processo dell'applicazione client e non l'identità del processo **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="90d66-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="90d66-107">Pertanto, se si tenta di accedere a **IWbemServices** con il puntatore, è possibile ricevere un codice di accesso negato, ad esempio **E \_ AccessDenied**.</span><span class="sxs-lookup"><span data-stu-id="90d66-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="90d66-108">Per evitare l'errore di accesso negato, è necessario impostare l'identità del nuovo puntatore con una chiamata all'interfaccia [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="90d66-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="90d66-109">Un provider può impostare la sicurezza su uno spazio dei nomi in modo che non venga restituito alcun dato, a meno che non si usi il pacchetto privacy (**su PktPrivacy**) nella connessione a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="90d66-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="90d66-110">In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete.</span><span class="sxs-lookup"><span data-stu-id="90d66-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="90d66-111">Se si tenta di impostare un livello di autenticazione inferiore, si otterrà un messaggio di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="90d66-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="90d66-112">Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="90d66-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="90d66-113">Per ulteriori informazioni sull'impostazione dell'autenticazione nello scripting, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="90d66-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="90d66-114">Impostazione della sicurezza su un'interfaccia IUnknown remota</span><span class="sxs-lookup"><span data-stu-id="90d66-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="90d66-115">In alcune situazioni, è necessario più accesso a un server rispetto a un solo puntatore a un proxy.</span><span class="sxs-lookup"><span data-stu-id="90d66-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="90d66-116">In alcuni casi, potrebbe essere necessario ottenere una connessione sicura all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy.</span><span class="sxs-lookup"><span data-stu-id="90d66-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="90d66-117">Utilizzando **IUnknown**, è possibile eseguire una query sul sistema remoto per le interfacce e altre tecniche necessarie.</span><span class="sxs-lookup"><span data-stu-id="90d66-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="90d66-118">Quando un proxy si trova in un computer remoto, il server delega tutte le chiamate all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy all'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="90d66-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="90d66-119">Se, ad esempio, si chiama [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un proxy e l'interfaccia richiesta non fa parte del proxy, il proxy invia la chiamata al server remoto.</span><span class="sxs-lookup"><span data-stu-id="90d66-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="90d66-120">Il server remoto controlla a sua volta il supporto dell'interfaccia appropriato.</span><span class="sxs-lookup"><span data-stu-id="90d66-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="90d66-121">Se il server supporta l'interfaccia, COM esegue il marshalling di un nuovo proxy al client in modo che l'applicazione possa usare la nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="90d66-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="90d66-122">I problemi si verificano se il client non dispone delle autorizzazioni di accesso al server remoto, ma sta utilizzando le credenziali di un utente che lo esegue.</span><span class="sxs-lookup"><span data-stu-id="90d66-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="90d66-123">In questa situazione, qualsiasi tentativo di accedere a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul server remoto ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="90d66-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="90d66-124">Anche la versione finale sul proxy ha esito negativo, perché l'utente corrente non ha accesso al server remoto.</span><span class="sxs-lookup"><span data-stu-id="90d66-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="90d66-125">Un sintomo di questo è un ritardo di uno o due secondi prima che l'applicazione client abbia esito negativo sulla versione finale del proxy.</span><span class="sxs-lookup"><span data-stu-id="90d66-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="90d66-126">L'errore si verifica perché COM ha tentato di accedere al server remoto usando le impostazioni di sicurezza predefinite dell'utente corrente, che non includono le credenziali modificate che hanno consentito l'accesso al server.</span><span class="sxs-lookup"><span data-stu-id="90d66-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="90d66-127">Per ulteriori informazioni, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="90d66-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="90d66-128">Per evitare la connessione non riuscita, usare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare in modo esplicito l'autenticazione di sicurezza sul puntatore restituito da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="90d66-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="90d66-129">Utilizzando **CoSetProxyBlanket**, è possibile verificare che il server remoto riceva l'identità di autenticazione corretta.</span><span class="sxs-lookup"><span data-stu-id="90d66-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="90d66-130">Nell'esempio di codice seguente viene illustrato come utilizzare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per accedere a un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.</span><span class="sxs-lookup"><span data-stu-id="90d66-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> <span data-ttu-id="90d66-131">Quando si imposta la sicurezza sull'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di un proxy, com crea una copia del proxy che non può essere rilasciata fino a quando non si chiama [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="90d66-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="90d66-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90d66-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d66-133">Impostazione dell'autenticazione in WMI</span><span class="sxs-lookup"><span data-stu-id="90d66-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
