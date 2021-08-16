---
description: Se si sta scrivendo un file GINA per sostituire la DLL GINA standard Microsoft (MSGina.dll), è possibile fornire alcune o tutte le funzionalità STANDARD di GINA.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf5d1e7e9dccf9581b27ea2fef3deb1c2c8aa218a1b0a711b7015134e1d2d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786750"
---
# <a name="msginadll-features"></a>MSGina.dll funzionalità

Se si scrive un [*FILE GINA*](../secgloss/g-gly.md) per sostituire la DLL GINA standard Microsoft (MSGina.dll), è possibile fornire alcune o tutte le funzionalità STANDARD di GINA. Di seguito è riportato un elenco di funzionalità standard e una breve descrizione del modo in cui vengono controllate.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

I valori delle chiavi del Registro di sistema controllano la disponibilità o il comportamento di molte di queste funzionalità STANDARD di GINA. Se non diversamente specificato, questi valori di chiave appartengono alla chiave del Registro di sistema Winlogon e hanno un tipo di valore \[ REG \_ SZ \] . Il percorso effettivo della [*chiave Winlogon*](../secgloss/w-gly.md) è:

**\\HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon**

-   **Finestra di dialogo Notifica legale**

    In alcuni casi, chiunque abbia accesso a una workstation può accedere a una workstation e iniziare a lavorare, a meno che non sia presente un avviso che indica che il sistema è solo per utenti autorizzati. Molti utenti desiderano inoltre che i messaggi specifici dell'azienda vengono visualizzati prima del normale accesso. L'applicazione GINA standard usa due valori di chiave del Registro di sistema Winlogon per consentire a un sistema di visualizzare informazioni prima dell'accesso. Se uno dei due valori di chiave è presente e contiene una stringa non Null, viene visualizzata una finestra di dialogo Nota legale prima della consueta schermata iniziale. Questi nomi dei valori di chiave sono indicati nella tabella seguente.

    

    | Nome del valore della chiave         | Contenuto                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Stringa da visualizzare come didascalia della finestra di dialogo delle note legali |
    | **LegalNoticeText**    | Stringa da visualizzare come messaggio della finestra di dialogo delle note legali |

    

     

-   **Visualizzare il nome dell'ultimo utente**

    Per impostazione predefinita, nella schermata di accesso viene visualizzato il nome dell'ultimo utente che ha eseguito correttamente l'accesso alla workstation. Questa funzionalità è controllata dal valore della chiave del Registro di sistema **DontDisplayLastUserName.** Quando questo valore della chiave è impostato su uno, il nome utente non viene visualizzato nella finestra di dialogo di accesso.

-   **Accesso automatico**

    Questa funzionalità consente a un sistema di accedere automaticamente a un utente ogni volta che il sistema viene avviato usando le informazioni predefinite e disabilitando la casella di accesso CTRL+ALT+CANC.

    Questa funzionalità usa i valori seguenti della chiave Winlogon.

    

    | Valore                 | Contenuto                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | Numero di volte in cui eseguire un accesso automatico       |
    | **DefaultUserName**   | Nome dell'account utente                       |
    | **DefaultDomainName** | Nome del dominio in cui si trova l'account utente |

    

     

    Se il valore della chiave **AutoAdminLogon** è presente e ne contiene uno e il valore della chiave **AutoLogonCount** non è presente, verrà eseguito un accesso automatico ogni volta che l'utente corrente si disconnette o il sistema viene riavviato. L'account connesso viene specificato usando i valori delle chiavi **DefaultUserName** **e DefaultDomainName.** La password per l'account può essere specificata in uno dei due modi seguenti. Per i computer che eseguono uno dei sistemi operativi Windows Server 2003 o Windows XP, la password deve essere archiviata come segreto usando la funzione [**LsaStorePrivateData.**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) Per informazioni dettagliate, vedere [Protezione della password di accesso automatico](protecting-the-automatic-logon-password.md). L'altro modo per archiviare la password è in testo non crittografato nella **voce DefaultPassword** della chiave Winlogon. Per motivi di sicurezza, questa tecnica deve essere evitata. Se si archivia la password usando la funzione **LsaStorePrivateData,** non specificare una **voce DefaultPassword** nella chiave Winlogon.

    Se il valore della chiave **AutoAdminLogon** è presente e ne contiene uno e se il valore della chiave **AutoLogonCount** è presente e non è zero, **AutoLogonCount** determinerà il numero di accessi automatici che si verificano. Ogni volta che il sistema viene riavviato, il valore di **AutoLogonCount** verrà decrementato di uno, fino a raggiungere lo zero. Quando **AutoLogonCount** raggiunge zero, nessun account verrà connesso automaticamente, il valore della chiave **AutoLogonCount** e il valore della chiave **DefaultPassword,** se usato, verranno eliminati dal Registro di sistema e **AutoAdminLogon** verrà impostato su zero.

    Esiste un'ulteriore avvertenza per l'uso di **AutoAdminLogon:** per impostazione predefinita, MSGina.dll lo stato del tasto MAIUSC quando **AutoAdminLogon** è uno. Se il tasto MAIUSC viene premuto durante il processo di avvio, MSGina.dll ignorerà il valore della chiave **AutoAdminLogon** e richiederà all'utente informazioni di identificazione e autenticazione in modo interattivo. Si tratta di una funzionalità utile quando si esegue il debug di un'applicazione dedicata. Per disabilitare il significato del tasto MAIUSC, impostare il valore della chiave **IgnoreShiftOverride** su uno.

-   **Consenti arresto non autenticato**

    È possibile configurare l'impostazione [*PREDEFINITA per*](../secgloss/g-gly.md) includere un **pulsante Arresta** nella finestra di dialogo di accesso. Ciò consente agli utenti di arrestare il sistema senza prima accedere. Il valore della chiave seguente controlla se questo pulsante è incluso.

    

    | Valore                    | Descrizione                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Uno per includere il pulsante. zero per escludere il pulsante |

    

     

-   **Userinit.exe attivazione**

    Userinit.exe è un'applicazione eseguita da MSGina.dll quando l'utente ha eseguito l'accesso. Viene eseguito nel contesto dell'utente appena connesso [*e*](../secgloss/c-gly.md) sul desktop dell'applicazione. Lo scopo è configurare l'ambiente dell'utente, tra cui il ripristino degli usi di rete, la definizione delle impostazioni del profilo, ad esempio i tipi di carattere e i colori dello schermo, e l'esecuzione di script di accesso. Dopo aver completato queste attività, Userinit.exe i programmi della shell utente. I programmi shell ereditano l'ambiente Userinit.exe configurazione. I programmi shell specifici eseguiti Userinit.exe vengono archiviati nel valore **della chiave Shell** nella chiave del Registro di sistema Winlogon.

    Il **valore della** chiave Shell può contenere un elenco delimitato da virgole di programmi da eseguire. Windows Explorer è il programma shell predefinito e verrà eseguito se il valore **della chiave shell** è Null o non è presente. Per impostazione predefinita, Windows Explorer.

-   **Opzioni di sicurezza per l'accesso**

    Dopo l'accesso, se un utente immette una sequenza di attenzione [*sicura,*](../secgloss/s-gly.md) all'utente viene visualizzata una schermata delle opzioni di sicurezza. Tra le opzioni elencate sono:

    -   Arrestare il sistema.
    -   Disconnettersi.
    -   Modificare la password.
    -   Passare all'elenco attività.
    -   Bloccare la workstation.

    Un'istanza DIA sostitutiva può fornire opzioni simili quando viene ricevuto un evento di firma di accesso condiviso mentre un utente è connesso.

 

 
