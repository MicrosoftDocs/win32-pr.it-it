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
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="a845a-103">Chiedere all'utente le credenziali</span><span class="sxs-lookup"><span data-stu-id="a845a-103">Asking the User for Credentials</span></span>

<span data-ttu-id="a845a-104">È possibile che l'applicazione debba richiedere all'utente le informazioni relative a nome utente e password per evitare di archiviare una password di amministratore o per verificare che il token disponga dei privilegi appropriati.</span><span class="sxs-lookup"><span data-stu-id="a845a-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="a845a-105">Tuttavia, la semplice richiesta di credenziali può consentire agli utenti di fornire tali credenziali a qualsiasi finestra di dialogo casuale non identificata visualizzata sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a845a-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="a845a-106">La procedura seguente è consigliata per ridurre l'effetto di training.</span><span class="sxs-lookup"><span data-stu-id="a845a-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="a845a-107">**Per acquisire correttamente le credenziali utente**</span><span class="sxs-lookup"><span data-stu-id="a845a-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="a845a-108">Informare l'utente, usando un messaggio che fa chiaramente parte dell'applicazione, che visualizzerà una finestra di dialogo che richiede il nome utente e la password.</span><span class="sxs-lookup"><span data-stu-id="a845a-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="a845a-109">È anche possibile usare la struttura di [**\_ informazioni di CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) nella chiamata a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per fornire dati di identificazione o un messaggio.</span><span class="sxs-lookup"><span data-stu-id="a845a-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="a845a-110">Chiamare [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="a845a-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="a845a-111">Si noti che il numero massimo di caratteri specificati per le informazioni sul nome utente e sulla password include il carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="a845a-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="a845a-112">Chiamare [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) e [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) per verificare che siano state ottenute le credenziali appropriate.</span><span class="sxs-lookup"><span data-stu-id="a845a-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="a845a-113">Nell'esempio seguente viene illustrato come chiamare [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per chiedere all'utente un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="a845a-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="a845a-114">Inizia compilando una struttura di \_ informazioni CREDUI con informazioni sulle richieste da usare.</span><span class="sxs-lookup"><span data-stu-id="a845a-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="a845a-115">Successivamente, il codice riempie due buffer con zeri.</span><span class="sxs-lookup"><span data-stu-id="a845a-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="a845a-116">Questa operazione viene eseguita per garantire che non vengano passate informazioni alla funzione che potrebbe rivelare un vecchio nome utente o una password all'utente.</span><span class="sxs-lookup"><span data-stu-id="a845a-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="a845a-117">La chiamata a **CredUIPromptForCredentials** Visualizza la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a845a-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="a845a-118">Per motivi di sicurezza, in questo esempio viene utilizzato il flag CREDUI non rende \_ \_ \_ \_ permanente per impedire al sistema operativo di archiviare la password perché potrebbe essere esposta.</span><span class="sxs-lookup"><span data-stu-id="a845a-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="a845a-119">Se non sono presenti errori, **CredUIPromptForCredentials** compila le variabili PszName e pszPwd e restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a845a-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="a845a-120">Quando l'applicazione ha terminato di usare le credenziali, deve inserire zeri nei buffer per impedire che le informazioni vengano accidentalmente rivelate.</span><span class="sxs-lookup"><span data-stu-id="a845a-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a845a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a845a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a845a-122">**CredUICmdLinePromptForCredentials**</span><span class="sxs-lookup"><span data-stu-id="a845a-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="a845a-123">**\_UINFO CREDUI**</span><span class="sxs-lookup"><span data-stu-id="a845a-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
