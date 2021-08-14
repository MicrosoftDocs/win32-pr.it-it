---
description: Una delle attività principali di IWbemLocator::ConnectServer per WMI è la restituzione di un puntatore a un proxy IWbemServices.
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Impostazione dell'autenticazione tramite C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b0ef3bcd1e9908815c94dacc3815fec77eaea33f2da48119dbe3178563eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315618"
---
# <a name="setting-authentication-using-c"></a>Impostazione dell'autenticazione tramite C++

Una delle attività principali di [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) per WMI è la restituzione di un puntatore a un proxy [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Tramite il proxy **IWbemServices** è possibile accedere alle funzionalità dell'infrastruttura WMI. Tuttavia, il puntatore al proxy **IWbemServices** ha l'identità del processo dell'applicazione client e non l'identità del **processo IWbemServices.** Pertanto, se si tenta di accedere a **IWbemServices** con il puntatore , è possibile ricevere un codice di accesso negato, ad esempio **E \_ ACCESSDENIED.** Per evitare l'errore di accesso negato, è necessario impostare l'identità del nuovo puntatore con una chiamata [**all'interfaccia CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

Un provider può impostare la sicurezza su uno spazio dei nomi in modo che non vengano restituiti dati a meno che non si usi la privacy dei pacchetti (**PktPrivacy**) nella connessione a tale spazio dei nomi. In questo modo si garantisce che i dati siano crittografati quando attraversano la rete. Se si tenta di impostare un livello di autenticazione inferiore, verrà visualizzato un messaggio di accesso negato. Per altre informazioni, vedere [Impostazione dei descrittori di sicurezza di Namepace.](setting-namespace-security-descriptors.md)

Per altre informazioni sull'impostazione dell'autenticazione negli script, vedere [Impostazione del livello di sicurezza del processo predefinito tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Impostazione della sicurezza in un'interfaccia IUnknown remota

In alcune situazioni, è necessario un accesso a un server maggiore rispetto a un semplice puntatore a un proxy. A volte potrebbe essere necessario ottenere una connessione sicura [**all'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy. Usando **IUnknown,** è possibile eseguire una query sul sistema remoto per le interfacce e altre tecniche necessarie.

Quando un proxy si trova in un computer remoto, il server delega tutte le chiamate [**all'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy all'interfaccia **IUnknown.** Ad esempio, se si chiama [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un proxy e l'interfaccia richiesta non fa parte del proxy, il proxy invia la chiamata al server remoto. A sua volta, il server remoto verifica la presenza del supporto dell'interfaccia appropriato. Se il server supporta l'interfaccia , COM effettua il marshalling di un nuovo proxy al client in modo che l'applicazione possa utilizzare la nuova interfaccia.

I problemi si verificano se il client non dispone delle autorizzazioni di accesso al server remoto, ma usa le credenziali di un utente che lo fa. In questo caso, qualsiasi tentativo di accedere [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nel server remoto ha esito negativo. Anche la versione finale del proxy ha esito negativo, perché l'utente corrente non ha accesso al server remoto. Un sintomo di questo problema è un ritardo di uno o due secondi prima che l'applicazione client non riesca la versione finale del proxy. L'errore si verifica perché COM ha tentato di accedere al server remoto utilizzando le impostazioni di sicurezza predefinite dell'utente corrente, che non includono in primo luogo le credenziali modificate che consentivano l'accesso al server. Per altre informazioni, vedere [Impostazione della sicurezza in IWbemServices e altri proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

Per evitare la connessione non riuscita, usare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare in modo esplicito l'autenticazione di sicurezza sul puntatore restituito da [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Usando **CoSetProxyBlanket,** è possibile assicurarsi che il server remoto riceva l'identità di autenticazione corretta.

L'esempio di codice seguente illustra come usare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per accedere a [**un'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.


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
> Quando si imposta la sicurezza [**sull'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di un proxy, COM crea una copia del proxy che non può essere rilasciata fino a quando non si chiama [**CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'autenticazione in WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
