---
description: L'applicazione potrebbe dover richiedere all'utente le informazioni su nome utente e password per evitare di archiviare una password amministratore o per verificare che il token contieni i privilegi appropriati.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Richiesta di credenziali all'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9b9941be168a307e35b3575f4d12241dc624553686a61b232f2c5ba86e9c0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480491"
---
# <a name="asking-the-user-for-credentials"></a>Richiesta di credenziali all'utente

L'applicazione potrebbe dover richiedere all'utente le informazioni su nome utente e password per evitare di archiviare una password amministratore o per verificare che il token contieni i privilegi appropriati.

Tuttavia, la semplice richiesta di credenziali può consentire agli utenti di fornire tali credenziali a qualsiasi finestra di dialogo casuale non identificata visualizzata sullo schermo. La procedura seguente è consigliata per ridurre tale effetto di training.

**Per acquisire correttamente le credenziali utente**

1.  Informare l'utente, usando un messaggio che fa chiaramente parte dell'applicazione, che verrà visualizzata una finestra di dialogo che richiede il nome utente e la password. È anche possibile usare la [**struttura CREDUI \_ INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) nella chiamata a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per comunicare i dati di identificazione o un messaggio.
2.  Chiamare [**CredUIPromptForCredentials.**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Si noti che il numero massimo di caratteri specificato per le informazioni su nome utente e password include il carattere null di terminazione.
3.  Chiamare [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) e [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) per verificare di aver ottenuto le credenziali appropriate.

L'esempio seguente illustra come chiamare [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per chiedere all'utente un nome utente e una password. Inizia compilando una struttura CREDUI \_ INFO con informazioni sulle richieste da usare. Successivamente, il codice riempie due buffer con zeri. Questa operazione viene eseguita per garantire che non venga passata alcuna informazione alla funzione che potrebbe rivelare all'utente un nome utente o una password precedente. La chiamata a **CredUIPromptForCredentials** apre la finestra di dialogo. Per motivi di sicurezza, in questo esempio viene utilizzato il flag CREDUI FLAGS DO NOT PERSIST per impedire al sistema operativo di archiviare la password perché potrebbe \_ \_ quindi essere \_ \_ esposta. Se non sono presenti errori, **CredUIPromptForCredentials** inserisce le variabili pszName e pszPwd e restituisce zero. Quando l'applicazione ha terminato di usare le credenziali, deve inserire zeri nei buffer per impedire che le informazioni vengano rivelate accidentalmente.


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

[**CREDUI \_ UINFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
