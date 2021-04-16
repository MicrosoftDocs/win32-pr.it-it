---
description: Quando un'applicazione client accede per la prima volta a Strumentazione gestione Windows (WMI), deve impostare il livello di sicurezza del processo predefinito con una chiamata a CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Impostazione del livello di sicurezza del processo predefinito mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530133"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Impostazione del livello di sicurezza del processo predefinito mediante C++

Quando un'applicazione client accede per la prima volta a Strumentazione gestione Windows (WMI), deve impostare il livello di sicurezza del processo predefinito con una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM utilizza le informazioni della chiamata per determinare la sicurezza che un altro processo deve avere per accedere al processo dell'applicazione client.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Modifica delle credenziali di autenticazione predefinite con C++](#changing-the-default-authentication-credentials-using-c)
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



L'impostazione del livello di autenticazione sul **\_ \_ \_ \_ valore predefinito del livello di autenticazione RPC C** consente a DCOM di negoziare il livello di autenticazione in modo che corrisponda alle richieste di sicurezza del computer di destinazione. Per altre informazioni, vedere [modifica delle credenziali di autenticazione predefinite con c++](#changing-the-default-authentication-credentials-using-c) e [modifica delle impostazioni di rappresentazione predefinite con c++](#changing-the-default-impersonation-levels-using-c).

## <a name="changing-the-default-authentication-credentials-using-c"></a>Modifica delle credenziali di autenticazione predefinite con C++

Le credenziali di autenticazione predefinite funzionano per la maggior parte delle situazioni, ma potrebbe essere necessario usare credenziali di autenticazione diverse in situazioni diverse. Ad esempio, potrebbe essere necessario aggiungere la crittografia alle procedure di autenticazione.

Nella tabella seguente sono elencati e descritti i diversi livelli di autenticazione.



| Livello di autenticazione                 | Descrizione                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| \_ \_ \_ valore predefinito del livello auth C RPC \_        | Autenticazione di sicurezza predefinita.                                                      |
| \_ \_ livello auth C \_ RPC \_           | Nessuna autenticazione.                                                                    |
| \_connessione a \_ livello auth \_ C \_ RPC        | Autenticazione solo quando il client crea una relazione con il server.           |
| \_chiamata al \_ livello auth \_ C \_ RPC           | Autenticazione ogni volta che il server riceve una chiamata RPC.                                  |
| \_ \_ \_ PKT livello auth C RPC \_            | Autenticazione ogni volta che il server riceve i dati da un client.                      |
| \_ \_ \_ integrità PKT del livello auth \_ C \_ RPC | Autenticazione che non sono stati modificati dati dal pacchetto.                        |
| \_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_   | Include tutti i livelli di autenticazione precedenti e consente di crittografare il valore di ogni chiamata RPC. |



 

È possibile specificare le credenziali di autenticazione predefinite per più utenti usando una **sola struttura dell' \_ \_ elenco di autenticazione** nel parametro *pAuthList* di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Nell'esempio di codice riportato di seguito viene illustrato come modificare le credenziali di autenticazione.


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

COM fornisce livelli di sicurezza predefiniti letti dal registro di sistema. Tuttavia, a meno che non sia stato modificato specificamente, le impostazioni del registro di sistema impostano il livello di rappresentazione troppo basso per il funzionamento di WMI. In genere, il livello di rappresentazione predefinito è **l' \_ \_ Identificazione del \_ livello \_ Imp c di RPC**, ma WMI richiede almeno la rappresentazione a **\_ \_ livello di \_ entità \_ RPC c** per funzionare con la maggior parte dei provider e potrebbe verificarsi una situazione in cui è necessario impostare un livello di rappresentazione superiore. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md). Nella tabella seguente sono elencati i diversi livelli di rappresentazione.



| Level                           | Descrizione                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ impostazione predefinita livello IMP C RPC \_     | Il sistema operativo sceglie il livello di rappresentazione.                                                      |
| \_ \_ livello IMP C \_ RPC \_ Anonimo   | Il server può rappresentare il client, ma il token di rappresentazione non può essere utilizzato per nulla.               |
| \_ \_ \_ Identificazione livello IMP C \_ RPC    | Il server può ottenere l'identità del client e rappresentare il client per il controllo ACL.                 |
| RAPPRESENTAZIONE a livello di RPC \_ C \_ Imp \_ \_ | Il server può rappresentare il client in un limite di computer.                                           |
| \_ \_ \_ delegato livello IMP C \_ RPC    | Il server può rappresentare il client tra più limiti e può effettuare chiamate per conto del client. |



 

 

 
