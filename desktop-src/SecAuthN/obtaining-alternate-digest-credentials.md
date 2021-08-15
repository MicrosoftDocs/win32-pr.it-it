---
description: Per ottenere credenziali diverse da quelle associate alla sessione di accesso corrente, popolare una struttura SEC WINNT AUTH IDENTITY con informazioni per \_ \_ \_ l'entità di sicurezza alternativa.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Recupero di credenziali digest alternative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260aa1c4cb3bd52395352e2e5dcadcaed7e3fea3cf478367a9e3432c7d2c8d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921290"
---
# <a name="obtaining-alternate-digest-credentials"></a>Recupero di credenziali digest alternative

Per ottenere [*credenziali diverse*](../secgloss/c-gly.md) da quelle associate alla sessione di accesso [*corrente,*](../secgloss/s-gly.md)popolare una struttura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) con informazioni per l'entità [*di sicurezza alternativa.*](../secgloss/s-gly.md) Passare la struttura alla [**funzione AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) usando il *parametro pAuthData.*

Nella tabella seguente vengono descritti i membri della struttura [**SEC \_ WINNT \_ AUTH \_ IDENTITY.**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)



| Membro             | Descrizione                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Utente**           | Stringa con terminazione Null contenente il nome dell'entità di sicurezza le cui credenziali verranno usate per stabilire un contesto di sicurezza. |
| **UserLength**     | Lunghezza del **membro User,** in caratteri. Omettere il valore Null di terminazione.                                                         |
| **Dominio**         | Stringa con terminazione Null che identifica il dominio contenente l'account dell'entità di sicurezza.                                  |
| **DomainLength**   | Lunghezza del membro **di dominio,** in caratteri. Omettere il valore Null di terminazione.                                                       |
| **Password**       | Stringa con terminazione Null contenente la password dell'entità di sicurezza.                                                            |
| **PasswordLength** | Lunghezza del **membro Password,** in caratteri. Omettere il valore Null di terminazione.                                                     |
| **Flag**          | Indica se i membri stringa sono in formato ANSI [*o Unicode.*](../secgloss/u-gly.md)  |



 

Nella tabella seguente sono elencati i valori validi per il **membro Flags** della struttura .



| Costante                            | Descrizione                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| SEC \_ WINNT \_ AUTH \_ IDENTITY \_ ANSI    | Le stringhe in questa struttura sono in formato ANSI.                                                                    |
| SEC \_ WINNT \_ AUTH \_ IDENTITY \_ UNICODE | Le stringhe in questa struttura sono in [*formato Unicode.*](../secgloss/u-gly.md) |



 

La struttura e le costanti vengono dichiarate nel file di intestazione Rpcdce.h distribuito con Platform Software Development Kit (SDK).

Nell'esempio seguente viene illustrata una chiamata sul lato client per ottenere le credenziali digest per un account utente specifico.


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



La **\_ funzione tcslen** restituisce la lunghezza della stringa in caratteri, senza includere il carattere Null di terminazione.

Se l'applicazione può usare le credenziali stabilite all'accesso, vedere [Recupero delle credenziali digest predefinite](obtaining-default-digest-credentials.md).

 

 
