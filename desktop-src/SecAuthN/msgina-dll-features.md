---
description: Se si sta scrivendo un modulo GINA per sostituire la DLL standard di Microsoft GINA (MSGina.dll), è possibile fornire alcune o tutte le funzionalità di GINA standard.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: Funzionalità di MSGina.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51833ab92e47dad01c13df004797e3ab3552b09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883898"
---
# <a name="msginadll-features"></a>Funzionalità di MSGina.dll

Se si sta scrivendo un modulo [*Gina*](../secgloss/g-gly.md) per sostituire la dll standard di Microsoft gina (MSGina.dll), è possibile fornire alcune o tutte le funzionalità di Gina standard. Di seguito è riportato un elenco delle funzionalità standard e una breve descrizione del modo in cui vengono controllate.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

I valori della chiave del registro di sistema controllano la disponibilità o il comportamento di molte di queste funzionalità standard di GINA. Se non specificato diversamente, questi valori di chiave appartengono alla chiave del registro di sistema Winlogon e hanno un tipo di valore \[ reg \_ SZ \] . Il percorso effettivo della chiave [*Winlogon*](../secgloss/w-gly.md) è:

**\\HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**

-   **Finestra di dialogo Notifiche legali**

    In alcuni casi, è lecito per chiunque abbia accesso a una workstation per accedere e iniziare a lavorare a meno che non sia presente un avviso che indica che il sistema è solo per utenti autorizzati. Inoltre, molti utenti vogliono visualizzare messaggi specifici della società prima dell'accesso normale. GINA standard usa due valori della chiave del registro di sistema Winlogon per consentire a un sistema di visualizzare le informazioni prima dell'accesso. Se è presente un valore di chiave che contiene una stringa non null, viene visualizzata una finestra di dialogo di avviso legale prima della normale schermata iniziale. I nomi dei valori di chiave sono riportati nella tabella seguente.

    

    | Nome valore chiave         | Contenuto                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Stringa da visualizzare come didascalia della finestra di dialogo Note legali |
    | **LegalNoticeText**    | Stringa da visualizzare come messaggio della finestra di dialogo Note legali |

    

     

-   **Visualizza ultimo nome utente**

    Per impostazione predefinita, nella schermata di accesso viene visualizzato il nome dell'ultimo utente per accedere correttamente alla workstation. Questa funzionalità è controllata dal valore della chiave del registro di sistema **DontDisplayLastUserName** . Se il valore di questa chiave è impostato su uno, il nome utente non viene visualizzato nella finestra di dialogo di accesso.

-   **Accesso automatico**

    Questa funzionalità consente a un sistema di accedere automaticamente a un utente ogni volta che il sistema viene avviato utilizzando le informazioni predefinite e disabilitando la casella di accesso CTRL + ALT + CANC.

    Questa funzionalità Usa i valori seguenti della chiave Winlogon.

    

    | Valore                 | Contenuto                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | Il numero di volte in cui eseguire un accesso automatico       |
    | **DefaultUserName**   | Nome dell'account utente                       |
    | **DefaultDomainName** | Nome del dominio in cui si trova l'account utente |

    

     

    Se il valore della chiave **AutoAdminLogon** è presente e ne contiene uno e il valore della chiave **AutoLogonCount** non è presente, si verificherà un accesso automatico ogni volta che l'utente corrente si disconnette o il sistema viene riavviato. L'account a cui si è connessi viene specificato con i valori della chiave **DefaultUserName** e **DefaultDomainName** . È possibile specificare la password per l'account in uno dei due modi seguenti. Per i computer che eseguono uno dei sistemi operativi Windows Server 2003 o Windows XP, la password deve essere archiviata come segreto tramite la funzione [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Per informazioni dettagliate, vedere [proteggere la password di accesso automatico](protecting-the-automatic-logon-password.md). L'altro modo per archiviare la password è in testo non crittografato nella voce **DefaultPassword** della chiave Winlogon; per motivi di sicurezza, è consigliabile evitare questa tecnica. Se si archivia la password usando la funzione **LsaStorePrivateData** , non specificare una voce **DefaultPassword** nella chiave Winlogon.

    Se il valore della chiave **AutoAdminLogon** è presente e ne contiene uno, e se il valore della chiave **AutoLogonCount** è presente e è diverso da zero, **AutoLogonCount** determinerà il numero di accessi automatici che si verificano. Ogni volta che il sistema viene riavviato, il valore di **AutoLogonCount** verrà decrementato di uno, fino a quando non raggiunge zero. Quando **AutoLogonCount** raggiunge zero, nessun account verrà connesso automaticamente, il valore della chiave **AutoLogonCount** e il valore della chiave **DefaultPassword** , se usato, verranno eliminati dal registro di sistema e **AutoAdminLogon** verrà impostato su zero.

    Per impostazione predefinita, è necessario un ulteriore avvertimento per l'uso di **AutoAdminLogon**, MSGina.dll controlla lo stato del tasto MAIUSC quando **AutoAdminLogon** è uno. Se il tasto MAIUSC viene tenuto premuto durante il processo di avvio, MSGina.dll ignorerà il valore della chiave **AutoAdminLogon** e chiederà all'utente le informazioni di identificazione e autenticazione in modo interattivo. Questa funzionalità è utile quando si esegue il debug di un'applicazione dedicata. Per disabilitare il significato del tasto MAIUSC, impostare il valore della chiave **IgnoreShiftOverride** su uno.

-   **Consenti arresto non autenticato**

    È possibile configurare il valore predefinito di [*Gina*](../secgloss/g-gly.md) per includere un pulsante di **arresto** nella finestra di dialogo di accesso. Questo consente agli utenti di arrestare il sistema senza prima effettuare l'accesso. Il valore chiave seguente controlla se questo pulsante è incluso.

    

    | Valore                    | Descrizione                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Uno per includere il pulsante; zero per escludere il pulsante |

    

     

-   **AttivazioneUserinit.exe**

    Userinit.exe è un'applicazione eseguita da MSGina.dll quando l'utente ha effettuato l'accesso. Viene eseguito nel [*contesto*](../secgloss/c-gly.md) dell'utente appena connesso e sul desktop dell'applicazione. Lo scopo è quello di configurare l'ambiente dell'utente, tra cui il ripristino degli usi della rete, la definizione delle impostazioni del profilo, ad esempio i tipi di carattere e i colori dello schermo, nonché l'esecuzione di script Al termine di queste attività, Userinit.exe esegue i programmi della shell utenti. I programmi della shell ereditano l'ambiente che Userinit.exe imposta. I programmi shell specifici eseguiti Userinit.exe vengono archiviati nel valore della chiave della **Shell** sotto la chiave del registro di sistema Winlogon.

    Il valore della chiave della **Shell** può contenere un elenco delimitato da virgole di programmi da eseguire. Esplora risorse è il programma shell predefinito e verrà eseguito se il valore della chiave della **Shell** è null o non è presente. Per impostazione predefinita, viene elencato Esplora risorse.

-   **Opzioni di sicurezza per l'accesso**

    Quando si effettua l'accesso, se un utente immette una [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS), viene visualizzata una schermata delle opzioni di sicurezza. Tra le opzioni elencate sono:

    -   Arrestare il sistema.
    -   Disconnettersi.
    -   Modificare la password.
    -   Passare all'elenco attività.
    -   Bloccare la workstation.

    Una sostituzione GINA può fornire opzioni simili quando viene ricevuto un evento SAS mentre un utente è connesso.

 

 
