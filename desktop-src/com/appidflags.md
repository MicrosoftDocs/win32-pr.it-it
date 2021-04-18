---
title: AppIDFlags
description: Set di flag che controllano il comportamento di attivazione di un server COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Valore AppIDFlags del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdad2b80625d6a60460d43f242d7897e0ae7eb40
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300544"
---
# <a name="appidflags"></a>AppIDFlags

Set di flag che controllano il comportamento di attivazione di un server COM.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore flag | Costante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ attiva \_ IUSERVER \_ indesktop          |
| 0x2        | APPIDREGFLAGS \_ Secure \_ server \_ processo \_ SD \_ e \_ binding |
| 0x4        | APPIDREGFLAGS \_ problema \_ attivazione \_ RPC \_ all' \_ Identificazione   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ attiva la \_ Descrizione di IUSERVER \_ indesktop

Se il **flag \_ APPIDREGFLAGS Activate \_ IUSERVER \_ indesktop** viene cancellato in **AppIDFlags** o se **AppIDFlags** non è presente, il client in una sessione di Terminal Server che effettua una richiesta di attivazione per un server COM [interattivo](interactive-user.md) , eseguirà l'associazione o l'avvio e l'associazione al server com nel desktop "predefinito" della stazione della [finestra](/windows/desktop/winstation/window-stations) "WinSta0" della sessione nella richiesta di attivazione. Se, ad esempio, il client esegue "WinSta0 \\ Desktop1" della sessione 3, la richiesta di attivazione per la sessione 3 verrà associata o avviata e associata al server com in "WinSta0 \\ default" della sessione 3, anche se un'istanza del server com è già in esecuzione in "WinSta0 \\ Desktop1" della sessione 3.

Se il flag **APPIDREGFLAGS \_ Activate \_ IUSERVER \_ indesktop** è impostato sul valore **AppIDFlags** , com eseguirà l'associazione a oppure avvierà e eseguirà l'associazione a, il processo server in esecuzione nel desktop del client e la sessione nella richiesta di attivazione. Se, ad esempio, il client esegue "WinSta0 \\ Desktop1" nella sessione 3, la richiesta di attivazione per la sessione 3 verrà associata o avviata e associata al server com in "WinSta0 \\ Desktop1" nella sessione 3, anche se un'istanza del server com è già in esecuzione in "WinSta0 \\ default" nella sessione 3.

Il client può usare il [moniker della sessione](/windows/desktop/TermServ/session-monikers) per specificare una sessione diversa dalla sessione del client quando effettua la richiesta di attivazione.

Il flag **APPIDREGFLAGS \_ Activate \_ IUSERVER \_ indesktop** si applica solo ai server COM configurati per RunAs "[Interactive User](interactive-user.md)".

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind Description

Se il **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ and \_ Bind** flag è impostato in **AppIDFlags**, i server COM configurati per RunAs "Activator" verranno avviati con un descrittore di sicurezza del processo che consente l' [elaborazione di tutti gli \_ \_ accessi](/windows/desktop/ProcThread/process-security-and-access-rights) al SID IDaccesso del token di processo. Inoltre, il proprietario del descrittore di sicurezza verrà impostato sul SID IDaccesso del token di processo.

Se il **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ and \_ Bind** flag è impostato in **AppIDFlags**, i server COM configurati per RunAs "questo utente" verranno avviati con un descrittore di sicurezza del processo che consente l' [elaborazione di tutti gli \_ \_ accessi](/windows/desktop/ProcThread/process-security-and-access-rights) nel SID IDaccesso del token di processo. Inoltre, il proprietario del descrittore di sicurezza verrà impostato sul SID IDaccesso del token di processo. Inoltre, gestione controllo servizi COM modifica il token del processo del server COM nel modo seguente:

-   Aggiunge un SID APPID al token. Concede l'accesso completo al SID APPID nell'elenco di controllo di accesso discrezionale (DACL) predefinito del token. In Windows Vista e nelle versioni successive di Windows, viene concessa l'autorizzazione OwnerRights SID READ \_ Control nell'elenco DACL predefinito del token. Nelle versioni precedenti a Windows Vista di Windows, il proprietario del token viene impostato sul SID APPID.

Quando si usa **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind flag,** è necessario tenere presenti le considerazioni di sicurezza seguenti:

-   Il flag **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind** deve essere impostato dai server com avviati con uno dei contesti di sicurezza del servizio incorporati, ovvero l'account NetworkService o LocalService. Se i server impersonano i client con privilegi e se il flag di **\_ \_ \_ \_ \_ \_ Binding e la SD del processo del server APPIDREGFLAGS Secure** non è impostato, il codice dannoso in esecuzione in altri processi con lo stesso contesto di sicurezza può elevare i privilegi dividendo i token di rappresentazione dei client con privilegi dal processo del server com.
-   Quando viene impostato il flag **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind** , com consolida il descrittore di sicurezza dell'oggetto processo nel caso di server com RunAs "Activator". Per tali server, il client COM dovrebbe finalizzare il token utilizzato per l'attivazione COM.
-   Quando viene impostato il flag **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind** , com consolida il descrittore di sicurezza dell'oggetto processo nel caso di server com RunAs "questo utente". Consente inoltre di finalizzare il token di processo del server COM poiché il SCM COM è l'entità che crea il token.

Il flag **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind** è supportato in Windows XP, Windows server 2003, Windows Vista e Windows Server 2008 solo quando viene applicata la patch MSRC8322 ([Security Bulletin MS09-012](https://support.microsoft.com/kb/959454)). È supportata in modo nativo in Windows 7 e nelle versioni successive di Windows.

Il flag **APPIDREGFLAGS \_ Secure \_ server \_ Process \_ SD \_ e \_ Bind** flag si applica solo ai server COM configurati per RunAs "Activator" o "This user". Non si applica ai server COM che sono servizi NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ problema \_ attivazione \_ RPC \_ in \_ Identificazione Descrizione

Se il **APPIDREGFLAGS \_ problema di \_ attivazione \_ RPC \_ al \_** flag di identificazione è impostato in **AppIDFlags**, il SCM com emetterà richieste di attivazione degli oggetti al processo del server COM utilizzando un livello di rappresentazione di [ \_ \_ \_ \_ Identificazione del livello di RPC C](impersonation-levels.md).

Se il **APPIDREGFLAGS \_ problema di \_ attivazione \_ RPC \_ al \_** flag di identificazione non è impostato, il SCM com emetterà richieste di attivazione oggetti ai processi del server COM utilizzando un livello di rappresentazione di [RPC \_ C \_ Imp \_ level \_ Impersonate](impersonation-levels.md).

Quando si usa il **APPIDREGFLAGS \_ problema \_ attivazione \_ RPC \_ al flag di \_ Identificazione** , è necessario tenere presenti le seguenti considerazioni sulla sicurezza:

-   Il **APPIDREGFLAGS \_ problema \_ attivazione \_ RPC \_ al \_** flag di identificazione è destinato a essere utilizzato dai server COM che non eseguono operazioni per conto dei client nelle richieste di attivazione oggetti. Per tali server, il fatto che le richieste di attivazione di oggetti di gestione dei servizi di gestione dei servizi di gestione dei servizi di gestione delle identità a livello di utente di [RPC \_ C \_ \_ \_](impersonation-levels.md) riducano al minimo le possibilità di token con privilegi se il livello di [**\_ \_ nome rappresenta**](/windows/desktop/SecAuthZ/privilege-constants)

Il **APPIDREGFLAGS \_ problema \_ attivazione \_ RPC \_ al \_** flag di identificazione è supportato in Windows 7 e versioni successive di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Desktop](/windows/desktop/winstation/desktops)
</dt> <dt>

[Livelli di rappresentazione](impersonation-levels.md)
</dt> <dt>

[Utente interattivo](interactive-user.md)
</dt> <dt>

[Moniker della sessione](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Stazioni finestra](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 