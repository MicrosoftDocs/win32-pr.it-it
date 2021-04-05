---
title: Scrittura di un server SSPI autenticato
description: Prima che la comunicazione autenticata possa essere eseguita tra i programmi client e server, il server deve registrare le informazioni di autenticazione.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- RPC (Remote Procedure Call), attività, scrittura di un server SSPI autenticato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044665"
---
# <a name="writing-an-authenticated-sspi-server"></a>Scrittura di un server SSPI autenticato

Prima che la comunicazione autenticata possa essere eseguita tra i programmi client e server, il server deve registrare le informazioni di autenticazione. In particolare, il server deve registrare il nome principale e specificare il servizio di autenticazione usato. Per ulteriori informazioni sui nomi di entità, vedere [nomi principali](principal-names.md). Per informazioni dettagliate sui servizi di autenticazione, vedere [servizi di autenticazione](authentication-services.md).

Per registrare le informazioni di autenticazione, i server chiamano la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Passare un puntatore al nome dell'entità come valore del primo parametro. Impostare il secondo parametro su una costante che indica il servizio di autenticazione che l'applicazione utilizzerà. Per una descrizione dei servizi di autenticazione, vedere [costanti del servizio di autenticazione](authentication-service-constants.md).

Il server può anche passare l'indirizzo di una funzione di acquisizione chiave come valore del terzo parametro. Vedere [funzioni di acquisizione chiavi](key-acquisition-functions.md). Per usare la funzione di acquisizione chiave predefinita per il servizio di autenticazione selezionato, impostare il terzo parametro su **null**. L'ultimo parametro della funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) è costituito dai dati del puntatore da passare alla funzione di acquisizione della chiave, se si specifica una funzione di acquisizione della chiave. Nel frammento di codice seguente viene mostrata una chiamata a **RpcServerRegisterAuthInfo** .


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



Inoltre, il server può fornire la libreria di runtime RPC con una funzione di autorizzazione. Per impostare una funzione di autorizzazione, chiamare la funzione [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .

La parte relativa al server di un'applicazione distribuita può chiamare la funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) per eseguire una query su un handle di binding per le informazioni di autenticazione.

Se il server viene registrato con un Security Support Provider, le chiamate client con credenziali non valide non verranno inviate. Tuttavia, le chiamate senza credenziali verranno inviate. Esistono tre modi per evitare che ciò accada:

-   Registrare l'interfaccia usando [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)con una funzione di callback di sicurezza. in questo modo la libreria di runtime RPC rifiuterà automaticamente le chiamate non autenticate a tale interfaccia. La registrazione di una funzione di callback è compatibile con altri metodi di controllo delle credenziali di accesso. la funzione di callback può chiamare le funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o altre. Tuttavia, queste funzioni non possono usare gli argomenti passati alla funzione, in quanto non vengono sottoposte a marshalling.

> [!IMPORTANT]
> La registrazione dell'interfaccia tramite [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) con una funzione di callback di sicurezza è il metodo più consigliato per verificare le credenziali client.

 

-   Chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) per determinare il livello di sicurezza utilizzato dal client. Lo stub può quindi restituire un errore se il client non è autenticato.

 

 




