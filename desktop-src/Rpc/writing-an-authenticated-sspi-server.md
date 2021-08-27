---
title: Scrittura di un server SSPI autenticato
description: Prima di poter effettuare la comunicazione autenticata tra i programmi client e server, il server deve registrare le informazioni di autenticazione.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- RPC Remote Procedure Call , attività, scrittura di un server SSPI autenticato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462f153905d6b654a0533c7bd05bff0e9627869d6910fb1fea05fe9340b788a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010349"
---
# <a name="writing-an-authenticated-sspi-server"></a>Scrittura di un server SSPI autenticato

Prima di poter effettuare la comunicazione autenticata tra i programmi client e server, il server deve registrare le informazioni di autenticazione. In particolare, il server deve registrare il nome dell'entità e specificare il servizio di autenticazione utilizzato. Per altre informazioni sui nomi delle entità, vedere [Nomi delle entità.](principal-names.md) Per informazioni dettagliate sui servizi di autenticazione, vedere [Servizi di autenticazione.](authentication-services.md)

Per registrare le informazioni di autenticazione, i server chiamano [**la funzione RpcServerRegisterAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) Passare un puntatore al nome dell'entità come valore del primo parametro. Impostare il secondo parametro su una costante che indica il servizio di autenticazione che verrà utilizzato dall'applicazione. Per una descrizione dei servizi di autenticazione, vedere [Costanti del servizio di autenticazione.](authentication-service-constants.md)

Il server può anche passare l'indirizzo di una funzione di acquisizione della chiave come valore del terzo parametro. Vedere [Funzioni di acquisizione delle chiavi.](key-acquisition-functions.md) Per usare la funzione di acquisizione della chiave predefinita per il servizio di autenticazione selezionato, impostare il terzo parametro su **NULL.** L'ultimo parametro per la [**funzione RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) è un puntatore ai dati da passare alla funzione di acquisizione della chiave, se si specifica una funzione di acquisizione della chiave. Una chiamata a **RpcServerRegisterAuthInfo** è illustrata nel frammento di codice seguente.


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



Inoltre, il server può fornire alla libreria di runtime RPC una funzione di autorizzazione. Per impostare una funzione di autorizzazione, chiamare la [**funzione RpcMgmtSetAuthorizationFn.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn)

La parte server di un'applicazione distribuita può chiamare la funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) per eseguire una query su un handle di associazione per ottenere informazioni di autenticazione.

Se il server si registra con un provider di supporto per la sicurezza, le chiamate client con credenziali non valide non verranno spediti. Tuttavia, le chiamate senza credenziali verranno spediti. Esistono tre modi per evitare che ciò accada:

-   Registrare l'interfaccia [**usando RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)con una funzione di callback di sicurezza; In questo modo la libreria di runtime RPC rifiuterà automaticamente le chiamate non autenticate a tale interfaccia. La registrazione di una funzione di callback è compatibile con altri metodi di controllo delle credenziali di accesso. La funzione di callback può chiamare le funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o altre. Tuttavia, queste funzioni non possono usare gli argomenti passati alla funzione, in quanto non sono disashalling a quel punto.

> [!IMPORTANT]
> La registrazione dell'interfaccia [**tramite RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) con una funzione di callback di sicurezza è il metodo più consigliato per controllare le credenziali client.

 

-   Chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) per determinare il livello di sicurezza utilizzato dal client. Lo stub può quindi restituire un errore se il client non è autenticato.

 

 




