---
description: Quando un'applicazione client accede a Windows Management Instrumentation (WMI) per la prima volta, deve impostare il livello di sicurezza del processo predefinito con una chiamata a CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Impostazione del livello di sicurezza del processo predefinito tramite C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcaec4ebbcd39c8cee9ee8aae002621a4a5a1853d1e4cfd4282194115c15ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050289"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Impostazione del livello di sicurezza del processo predefinito tramite C++

Quando un'applicazione client accede a strumentazione Windows gestione (WMI) per la prima volta, deve impostare il livello di sicurezza del processo predefinito con una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM usa le informazioni nella chiamata per determinare la quantità di sicurezza che un altro processo deve avere per accedere al processo dell'applicazione client.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Modifica delle credenziali di autenticazione predefinite tramite C++](#changing-the-default-authentication-credentials-using-c)
-   [Modifica dei livelli di rappresentazione predefiniti con C++](#changing-the-default-impersonation-levels-using-c)

Per la maggior parte delle applicazioni client, gli argomenti illustrati nell'esempio seguente impostano la sicurezza predefinita per WMI.


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



Il codice richiede i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



L'impostazione del livello di autenticazione su **RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT** consente a DCOM di negoziare il livello di autenticazione in modo che corrisponda alle richieste di sicurezza del computer di destinazione. Per altre informazioni, vedere Modifica delle credenziali di autenticazione predefinite tramite [C++](#changing-the-default-authentication-credentials-using-c) e Modifica della rappresentazione [Impostazioni tramite C++.](#changing-the-default-impersonation-levels-using-c)

## <a name="changing-the-default-authentication-credentials-using-c"></a>Modifica delle credenziali di autenticazione predefinite tramite C++

Le credenziali di autenticazione predefinite funzionano nella maggior parte delle situazioni, ma potrebbe essere necessario usare credenziali di autenticazione diverse in situazioni diverse. Ad esempio, potrebbe essere necessario aggiungere la crittografia alle procedure di autenticazione.

Nella tabella seguente sono elencati e descritti i diversi livelli di autenticazione.



| Livello di autenticazione                 | Descrizione                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| IMPOSTAZIONE \_ PREDEFINITA DEL LIVELLO RPC C \_ AUTHN \_ \_        | Autenticazione di sicurezza predefinita.                                                      |
| RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           | Nessuna autenticazione.                                                                    |
| RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        | Autenticazione solo quando il client crea una relazione con il server.           |
| CHIAMATA A LIVELLO DI AUTENTICAZIONE \_ RPC C \_ \_ \_           | Autenticazione ogni volta che il server riceve un RPC.                                  |
| PKT \_ DI LIVELLO RPC C \_ AUTHN \_ \_            | Autenticazione ogni volta che il server riceve dati da un client.                      |
| INTEGRITÀ \_ \_ PKT A \_ LIVELLO DI \_ AUTENTICAZIONE \_ RPC C | Autenticazione che nessun dato del pacchetto è stato modificato.                        |
| PRIVACY \_ \_ PKT A \_ LIVELLO DI AUTENTICAZIONE \_ \_ RPC C   | Include tutti i livelli di autenticazione precedenti e crittografa il valore di ogni chiamata RPC. |



 

È possibile specificare le credenziali di autenticazione predefinite per più utenti usando una struttura **SOLE \_ AUTHENTICATION \_ LIST** nel *parametro pAuthList* di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Nell'esempio di codice seguente viene illustrato come modificare le credenziali di autenticazione.


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a>Modifica dei livelli di rappresentazione predefiniti con C++

COM fornisce i livelli di sicurezza predefiniti letti dal Registro di sistema. Tuttavia, a meno che non siano state modificate in modo specifico, le impostazioni del Registro di sistema impostano un livello di rappresentazione troppo basso per il funzionamento di WMI. In genere, il livello di rappresentazione predefinito è **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY,** ma WMI deve almeno **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE** per funzionare con la maggior parte dei provider e potrebbe verificarsi una situazione in cui è necessario impostare un livello di rappresentazione superiore. Per altre informazioni, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md). Nella tabella seguente sono elencati i diversi livelli di rappresentazione.



| Level                           | Descrizione                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| IMPOSTAZIONE \_ PREDEFINITA DEL LIVELLO IMP RPC C \_ \_ \_     | Il sistema operativo sceglie il livello di rappresentazione.                                                      |
| RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   | Il server può rappresentare il client, ma il token di rappresentazione non può essere usato per alcun elemento.               |
| IDENTIFICAZIONE \_ DEL LIVELLO IMP RPC C \_ \_ \_    | Il server può ottenere l'identità del client e rappresentare il client per il controllo ACL.                 |
| RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE | Il server può rappresentare il client attraverso un limite di computer.                                           |
| DELEGATO \_ A LIVELLO DI IMP RPC C \_ \_ \_    | Il server può rappresentare il client in più limiti e può effettuare chiamate per conto del client. |



 

 

 
