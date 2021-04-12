---
description: Per ottenere credenziali diverse da quelle associate alla sessione di accesso corrente, popolare una \_ struttura di identità di autenticazione WinNT sec con le \_ \_ informazioni per l'entità di sicurezza alternativa.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Acquisizione di credenziali del digest alternative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232821"
---
# <a name="obtaining-alternate-digest-credentials"></a>Acquisizione di credenziali del digest alternative

Per ottenere [*credenziali*](../secgloss/c-gly.md) diverse da quelle associate alla [*sessione*](../secgloss/s-gly.md)di accesso corrente, popolare una struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) con le informazioni per l' [*entità di sicurezza*](../secgloss/s-gly.md)alternativa. Passare la struttura alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) utilizzando il parametro *pAuthData* .

Nella tabella seguente vengono descritti i membri della struttura di [**\_ \_ \_ identità dell'autenticazione WinNT del secondo**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .



| Membro             | Descrizione                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Utente**           | Stringa con terminazione null che contiene il nome dell'entità di sicurezza le cui credenziali verranno utilizzate per stabilire un contesto di sicurezza. |
| **UserLength**     | Lunghezza del membro **utente** , in caratteri. Omettere il valore null di terminazione.                                                         |
| **Dominio**         | Stringa con terminazione null che identifica il dominio contenente l'account dell'entità di sicurezza.                                  |
| **DomainLength**   | Lunghezza del membro del **dominio** , in caratteri. Omettere il valore null di terminazione.                                                       |
| **Password**       | Stringa con terminazione null che contiene la password dell'entità di sicurezza.                                                            |
| **PasswordLength** | Lunghezza del membro della **password** , in caratteri. Omettere il valore null di terminazione.                                                     |
| **Flag**          | Indica se i membri della stringa sono in formato ANSI o [*Unicode*](../secgloss/u-gly.md) .  |



 

Nella tabella seguente sono elencati i valori validi per il membro dei **flag** della struttura.



| Costante                            | Descrizione                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| SEC \_ \_ identità auth \_ autenticazione \_ ANSI    | Le stringhe in questa struttura sono in formato ANSI.                                                                    |
| SEC \_ identità di autenticazione WinNT ( \_ \_ \_ Unicode) | Le stringhe in questa struttura sono in formato [*Unicode*](../secgloss/u-gly.md) . |



 

La struttura e le costanti sono dichiarate nel file di intestazione rpcdce. h distribuito con Platform Software Development Kit (SDK).

Nell'esempio seguente viene illustrata una chiamata sul lato client per ottenere le credenziali del digest per un account utente specifico.


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



La funzione **\_ tcslen** restituisce la lunghezza della stringa in caratteri, escluso il carattere null di terminazione.

Se l'applicazione può usare le credenziali stabilite all'accesso, vedere [recupero delle credenziali del digest predefinite](obtaining-default-digest-credentials.md).

 

 
