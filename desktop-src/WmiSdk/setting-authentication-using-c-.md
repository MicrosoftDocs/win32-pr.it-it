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
# <a name="setting-authentication-using-c"></a>Impostazione dell'autenticazione mediante C++

Una delle attività principali di [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) per WMI è la restituzione di un puntatore a un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Tramite il proxy **IWbemServices** è possibile accedere alle funzionalità dell'infrastruttura WMI. Il puntatore al proxy **IWbemServices** , tuttavia, ha l'identità del processo dell'applicazione client e non l'identità del processo **IWbemServices** . Pertanto, se si tenta di accedere a **IWbemServices** con il puntatore, è possibile ricevere un codice di accesso negato, ad esempio **E \_ AccessDenied**. Per evitare l'errore di accesso negato, è necessario impostare l'identità del nuovo puntatore con una chiamata all'interfaccia [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .

Un provider può impostare la sicurezza su uno spazio dei nomi in modo che non venga restituito alcun dato, a meno che non si usi il pacchetto privacy (**su PktPrivacy**) nella connessione a tale spazio dei nomi. In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete. Se si tenta di impostare un livello di autenticazione inferiore, si otterrà un messaggio di accesso negato. Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).

Per ulteriori informazioni sull'impostazione dell'autenticazione nello scripting, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Impostazione della sicurezza su un'interfaccia IUnknown remota

In alcune situazioni, è necessario più accesso a un server rispetto a un solo puntatore a un proxy. In alcuni casi, potrebbe essere necessario ottenere una connessione sicura all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy. Utilizzando **IUnknown**, è possibile eseguire una query sul sistema remoto per le interfacce e altre tecniche necessarie.

Quando un proxy si trova in un computer remoto, il server delega tutte le chiamate all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy all'interfaccia **IUnknown** . Se, ad esempio, si chiama [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un proxy e l'interfaccia richiesta non fa parte del proxy, il proxy invia la chiamata al server remoto. Il server remoto controlla a sua volta il supporto dell'interfaccia appropriato. Se il server supporta l'interfaccia, COM esegue il marshalling di un nuovo proxy al client in modo che l'applicazione possa usare la nuova interfaccia.

I problemi si verificano se il client non dispone delle autorizzazioni di accesso al server remoto, ma sta utilizzando le credenziali di un utente che lo esegue. In questa situazione, qualsiasi tentativo di accedere a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul server remoto ha esito negativo. Anche la versione finale sul proxy ha esito negativo, perché l'utente corrente non ha accesso al server remoto. Un sintomo di questo è un ritardo di uno o due secondi prima che l'applicazione client abbia esito negativo sulla versione finale del proxy. L'errore si verifica perché COM ha tentato di accedere al server remoto usando le impostazioni di sicurezza predefinite dell'utente corrente, che non includono le credenziali modificate che hanno consentito l'accesso al server. Per ulteriori informazioni, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

Per evitare la connessione non riuscita, usare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare in modo esplicito l'autenticazione di sicurezza sul puntatore restituito da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Utilizzando **CoSetProxyBlanket**, è possibile verificare che il server remoto riceva l'identità di autenticazione corretta.

Nell'esempio di codice seguente viene illustrato come utilizzare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per accedere a un'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.


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
> Quando si imposta la sicurezza sull'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di un proxy, com crea una copia del proxy che non può essere rilasciata fino a quando non si chiama [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'autenticazione in WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
