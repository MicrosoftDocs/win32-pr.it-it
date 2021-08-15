---
title: Scrittura di un client SSPI autenticato
description: Scrittura di un client SSPI autenticato e rpc (Remote Procedure Call).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- RPC Remote Procedure Call , attività, scrittura di un client SSPI autenticato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445d5340b03f07805a9e2ab89deb8c915a76160db67b504259ae8de0bbabee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010359"
---
# <a name="writing-an-authenticated-sspi-client"></a>Scrittura di un client SSPI autenticato

Tutte le sessioni client/server RPC richiedono un'associazione tra il client e il server. Per aggiungere sicurezza alle applicazioni client/server, i programmi devono utilizzare un'associazione autenticata. In questa sezione viene descritto il processo di creazione di un'associazione autenticata tra il client e il server.

-   [Creazione di handle di associazione lato client](#creating-client-side-binding-handles)
-   [Fornire le credenziali client al server](#providing-client-credentials-to-the-server)

Per informazioni correlate, vedere [Procedure usate con la maggior parte dei pacchetti e dei protocolli](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) di sicurezza in Platform Software Development Kit (SDK).

## <a name="creating-client-side-binding-handles"></a>Creazione di handle di associazione lato client

Per creare una sessione autenticata con un programma server, le applicazioni client devono fornire informazioni di autenticazione con il relativo handle di associazione. Per configurare un handle di associazione autenticato, i client richiamano la [**funzione RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) Queste due funzioni sono quasi identiche. L'unica differenza è che il client può specificare la qualità del servizio con la **funzione RpcBindingSetAuthInfoEx.**

Il frammento di codice seguente illustra l'aspetto di [**una chiamata a RpcBindingSetAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



Dopo che il client ha chiamato correttamente le funzioni [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) la libreria di runtime RPC autentica automaticamente tutte le chiamate RPC sull'associazione. Il livello di sicurezza e autenticazione selezionato dal client si applica solo all'handle di associazione. Gli handle di contesto derivati dall'handle di associazione useranno le stesse informazioni di sicurezza, ma le successive modifiche all'handle di associazione non verranno riflesse negli handle di contesto. Per altre informazioni, vedere [Handle di contesto.](context-handles.md)

Il livello di autenticazione rimane attivo fino a quando il client non sceglie un altro livello o fino al termine del processo. La maggior parte delle applicazioni non richiederà una modifica del livello di sicurezza. Il client può eseguire una query su qualsiasi handle di associazione per ottenere le informazioni di autorizzazione richiamando [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) e passando l'handle di associazione.

## <a name="providing-client-credentials-to-the-server"></a>Fornire le credenziali client al server

I server usano le informazioni di associazione del client per applicare la sicurezza. I client passano sempre un handle di associazione come primo parametro di una chiamata di procedura remota. Tuttavia, i server non possono usare l'handle a meno che non venga dichiarato come primo parametro per le procedure remote nel file IDL o nel file di configurazione dell'applicazione (ACF) del server. È possibile scegliere di elencare l'handle di associazione nel file IDL, ma in questo modo tutti i client dichiarano e modificano l'handle di associazione anziché usare l'associazione automatica o implicita. Per altre informazioni, vedere [File IDL e ACF.](the-idl-and-acf-files.md)

Un altro metodo è lasciare gli handle di associazione al di fuori del file IDL e inserire l'attributo **\_ handle** esplicito nell'ACF del server. In questo modo, il client può usare il tipo di associazione più adatto all'applicazione, mentre il server usa l'handle di associazione come se fosse dichiarato in modo esplicito.

Il processo di estrazione delle credenziali client dall'handle di associazione si verifica come segue:

-   I client RPC [**chiamano RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e includono le informazioni di autenticazione come parte delle informazioni di associazione passate al server.
-   In genere, il server [**chiama RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) per comportarsi come se fosse il client. Se l'handle di associazione non è autenticato, la chiamata ha esito negativo con RPC \_ S \_ NO CONTEXT \_ \_ AVAILABLE. Per ottenere il nome utente del client, chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) durante la rappresentazione o in Windows XP o versioni successive di Windows, chiamare [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) per ottenere il contesto di autorizzazione, quindi usare le funzioni Authz per recuperare il nome.
-   Il server chiamerà in genere [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) per creare oggetti con ACL. Dopo questa operazione, i controlli di sicurezza successivi diventano automatici.

 

 