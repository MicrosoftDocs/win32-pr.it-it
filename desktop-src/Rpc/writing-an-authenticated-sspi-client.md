---
title: Scrittura di un client SSPI autenticato
description: Scrittura di un client SSPI autenticato e di una chiamata di procedura remota (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- RPC (Remote Procedure Call), attività, scrittura di un client SSPI autenticato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118138"
---
# <a name="writing-an-authenticated-sspi-client"></a>Scrittura di un client SSPI autenticato

Per tutte le sessioni client/server RPC è necessaria un'associazione tra il client e il server. Per aggiungere sicurezza alle applicazioni client/server, i programmi devono utilizzare un'associazione autenticata. In questa sezione viene descritto il processo di creazione di un'associazione autenticata tra il client e il server.

-   [Creazione di handle di binding lato client](#creating-client-side-binding-handles)
-   [Fornire le credenziali client al server](#providing-client-credentials-to-the-server)

Per informazioni correlate, vedere [procedure utilizzate con la maggior parte dei pacchetti di sicurezza e protocolli](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) nel Software Development Kit (SDK) della piattaforma.

## <a name="creating-client-side-binding-handles"></a>Creazione di handle di binding lato client

Per creare una sessione autenticata con un programma server, le applicazioni client devono fornire informazioni di autenticazione con il relativo handle di binding. Per impostare un handle di binding autenticato, i client richiamano la funzione [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Queste due funzioni sono quasi identiche. L'unica differenza è che il client può specificare la qualità del servizio con la funzione **RpcBindingSetAuthInfoEx** .

Il frammento di codice seguente mostra come potrebbe apparire una chiamata a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) .


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



Dopo che il client ha correttamente chiamato le funzioni [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , la libreria di runtime RPC autentica automaticamente tutte le chiamate RPC nell'associazione. Il livello di sicurezza e autenticazione selezionato dal client si applica solo a tale handle di associazione. Gli handle di contesto derivati dall'handle di associazione utilizzeranno le stesse informazioni di sicurezza, ma le modifiche successive all'handle di associazione non verranno riflesse negli handle di contesto. Per altre informazioni, vedere [handle di contesto](context-handles.md).

Il livello di autenticazione rimane attivo fino a quando il client non sceglie un altro livello o fino a quando non termina il processo. Per la maggior parte delle applicazioni non è necessaria una modifica nel livello di sicurezza. Il client può eseguire una query su qualsiasi handle di binding per ottenere le informazioni di autorizzazione richiamando [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) e passando l'handle di associazione.

## <a name="providing-client-credentials-to-the-server"></a>Fornire le credenziali client al server

Per applicare la sicurezza, i server utilizzano le informazioni di associazione del client. I client passano sempre un handle di associazione come primo parametro di una chiamata di procedura remota. Tuttavia, i server non possono utilizzare l'handle a meno che non venga dichiarato come primo parametro per le procedure remote nel file IDL o nel file di configurazione dell'applicazione (ACF) del server. È possibile scegliere di elencare il punto di controllo dell'associazione nel file IDL, ma ciò impone a tutti i client di dichiarare e manipolare l'handle di binding anziché utilizzare l'associazione automatica o implicita. Per ulteriori informazioni, vedere [i file IDL e ACF](the-idl-and-acf-files.md).

Un altro metodo consiste nel lasciare gli handle dell'associazione fuori dal file IDL e inserire l' **attributo \_ handle esplicito** nell'ACF del server. In questo modo, il client può utilizzare il tipo di associazione più adatto all'applicazione, mentre il server utilizza l'handle di associazione come se fosse stato dichiarato in modo esplicito.

Il processo di estrazione delle credenziali client dall'handle di binding si verifica nel modo seguente:

-   I client RPC chiamano [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e includono le informazioni di autenticazione come parte delle informazioni di binding passate al server.
-   Il server chiama in genere [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) per comportarsi come se fosse il client. Se l'handle di associazione non è autenticato, la chiamata ha esito negativo e \_ \_ non è \_ disponibile alcun contesto \_ . Per ottenere il nome utente del client, chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) durante la rappresentazione o in Windows XP o versioni successive di Windows, chiamare [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) per ottenere il contesto di autorizzazione, quindi utilizzare le funzioni Authz per recuperare il nome.
-   Il server di solito chiamerà [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) per creare oggetti con ACL. Una volta completata questa operazione, i controlli di sicurezza successivi diventano automatici.

 

 