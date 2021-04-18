---
description: È possibile che l'applicazione debba richiedere all'utente le informazioni relative a nome utente e password per evitare di archiviare una password di amministratore o per verificare che il token disponga dei privilegi appropriati.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Chiedere all'utente le credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316185"
---
# <a name="asking-the-user-for-credentials"></a>Chiedere all'utente le credenziali

È possibile che l'applicazione debba richiedere all'utente le informazioni relative a nome utente e password per evitare di archiviare una password di amministratore o per verificare che il token disponga dei privilegi appropriati.

Tuttavia, la semplice richiesta di credenziali può consentire agli utenti di fornire tali credenziali a qualsiasi finestra di dialogo casuale non identificata visualizzata sullo schermo. La procedura seguente è consigliata per ridurre l'effetto di training.

**Per acquisire correttamente le credenziali utente**

1.  Informare l'utente, usando un messaggio che fa chiaramente parte dell'applicazione, che visualizzerà una finestra di dialogo che richiede il nome utente e la password. È anche possibile usare la struttura di [**\_ informazioni di CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) nella chiamata a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per fornire dati di identificazione o un messaggio.
2.  Chiamare [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa). Si noti che il numero massimo di caratteri specificati per le informazioni sul nome utente e sulla password include il carattere di terminazione null.
3.  Chiamare [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) e [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) per verificare che siano state ottenute le credenziali appropriate.

Nell'esempio seguente viene illustrato come chiamare [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per chiedere all'utente un nome utente e una password. Inizia compilando una struttura di \_ informazioni CREDUI con informazioni sulle richieste da usare. Successivamente, il codice riempie due buffer con zeri. Questa operazione viene eseguita per garantire che non vengano passate informazioni alla funzione che potrebbe rivelare un vecchio nome utente o una password all'utente. La chiamata a **CredUIPromptForCredentials** Visualizza la finestra di dialogo. Per motivi di sicurezza, in questo esempio viene utilizzato il flag CREDUI non rende \_ \_ \_ \_ permanente per impedire al sistema operativo di archiviare la password perché potrebbe essere esposta. Se non sono presenti errori, **CredUIPromptForCredentials** compila le variabili PszName e pszPwd e restituisce zero. Quando l'applicazione ha terminato di usare le credenziali, deve inserire zeri nei buffer per impedire che le informazioni vengano accidentalmente rivelate.


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**\_UINFO CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
