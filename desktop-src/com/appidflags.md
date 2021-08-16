---
title: AppIDFlags
description: Set di flag che controllano il comportamento di attivazione di un server COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Valore del Registro di sistema AppIDFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ecf7d0d112d2ceff913f3de6250c130e16455c1810cc6234db63a6aaf463fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048869"
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

Si tratta di **un valore \_ DWORD REG.**



| Valore flag | Costante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ ATTIVA \_ IUSERVER \_ INDESKTOP          |
| 0x2        | APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND |
| 0x4        | APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>Descrizione DI APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP

Se il flag **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** è deselezionato in **AppIDFlags** o se **AppIDFlags** non è presente, il client in una sessione del server terminal che effettua una richiesta di attivazione per un server [COM](interactive-user.md) utente interattivo, esegue l'associazione al server COM nel desktop "predefinito" della finestra "winsta0" [](/windows/desktop/winstation/window-stations) della sessione nella richiesta di attivazione. Ad esempio, se il client esegue "winsta0 desktop1" della sessione 3, la richiesta di attivazione per la sessione 3 verrà associata al server COM "winsta0 desktop1" della sessione 3, anche se un'istanza del server COM è già \\ \\ in esecuzione in "winsta0 \\ desktop1" della sessione 3.

Se il flag **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** è impostato nel valore **AppIDFlags,** COM esegue l'associazione al processo server in esecuzione nel desktop del client o alla sessione nella richiesta di attivazione. Ad esempio, se il client esegue "winsta0 desktop1" nella sessione 3, la richiesta di attivazione per la sessione 3 verrà associata al server COM "winsta0 desktop1" nella sessione 3, anche se un'istanza del server COM è già in esecuzione \\ \\ in "winsta0 default" nella sessione \\ 3.

Il client può usare il [moniker](/windows/desktop/TermServ/session-monikers) di sessione per specificare una sessione diversa dalla sessione del client quando effettua la richiesta di attivazione.

Il flag **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** si applica solo ai server COM configurati per RunAs "[Interactive User](interactive-user.md)".

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND Description

Se il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** è impostato in **AppIDFlags,** i server COM configurati per RunAs "Activator" verranno avviati con un descrittore di sicurezza del processo che consente [a PROCESS ALL \_ \_ ACCESS](/windows/desktop/ProcThread/process-security-and-access-rights) al SID LogonID del token di processo. Inoltre, il proprietario del descrittore di sicurezza verrà impostato sul SID LogonID del token di processo.

Se il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** è impostato in **AppIDFlags,** i server COM configurati per RunAs "This User" verranno avviati con un descrittore di sicurezza del processo che consente [l'accesso PROCESS \_ ALL \_](/windows/desktop/ProcThread/process-security-and-access-rights) nel SID LogonID del token di processo. Inoltre, il proprietario del descrittore di sicurezza verrà impostato sul SID LogonID del token di processo. Inoltre, Gestione controllo servizi COM (SCM) modifica il token del processo del server COM come segue:

-   Aggiunge un SID APPID al token. Concede al SID APPID l'accesso completo nell'elenco di controllo di accesso discrezionale (DACL) predefinito del token. In Windows Vista e versioni successive di Windows, concede l'autorizzazione OWNERRights SID READ CONTROL nell'elenco \_ DACL predefinito del token. Nelle versioni precedenti Windows Vista di Windows, imposta il proprietario del token sul SID APPID.

Quando si usa il flag **APPIDREGFLAGS \_ SECURE \_ SERVER PROCESS \_ \_ SD \_ AND \_ BIND,** è necessario tenere conto delle considerazioni sulla sicurezza seguenti:

-   Il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** deve essere impostato dai server COM avviati in uno dei contesti di sicurezza del servizio predefiniti, ad esempio gli account NetworkService o LocalService. Se i server rappresentano client con privilegi e se il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** non è impostato, il codice dannoso in esecuzione in altri processi con lo stesso contesto di sicurezza può elevare i privilegi di dirottando i token di rappresentazione dei client con privilegi dal processo del server COM.
-   Quando il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** è impostato, COM attiva il descrittore di sicurezza dell'oggetto processo nel caso di server COM RunAs "Activator". Per tali server, è previsto che il client COM esereggere il token utilizzato per l'attivazione COM.
-   Quando il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** è impostato, COM imposta il descrittore di sicurezza dell'oggetto processo nel caso di server COM RunAs "This User". Inoltre, il token di processo del server COM viene hard hard perché gestione servizi COM è l'entità che crea il token.

Il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** è supportato in Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008 solo quando viene applicata la patch MSRC8322 ( bollettino sulla sicurezza [MS09-012).](https://support.microsoft.com/kb/959454) È supportato in modo nativo in Windows 7 e versioni successive di Windows.

Il flag **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** si applica solo ai server COM configurati per RunAs "Activator" o "This User". Non si applica ai server COM che sono servizi NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY Description

Se il flag **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** è impostato in **AppIDFlags,** Gestione controllo servizi COM emettere richieste di attivazione degli oggetti al processo del server COM usando un livello di rappresentazione [RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY](impersonation-levels.md).

Se il flag **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** non è impostato, Gestione controllo servizi COM emettere richieste di attivazione degli oggetti ai processi del server COM usando un livello di rappresentazione [RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE](impersonation-levels.md).

Quando si usa il flag **APPIDREGFLAGS \_ ISSUE \_ ACTIVATION RPC AT \_ \_ \_ IDENTIFY,** è necessario tenere conto delle considerazioni sulla sicurezza seguenti:

-   Il flag **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** deve essere usato dai server COM che non eseguono operazioni per conto dei client nelle richieste di attivazione degli oggetti. Per tali server, la richiesta di attivazione degli oggetti da parte di Gestione controllo servizi COM a [RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY](impersonation-levels.md) riduce al minimo le probabilità che nel processo venga visualizzato un token con privilegi con un livello [**\_ IMPERSONATE \_ NAME**](/windows/desktop/SecAuthZ/privilege-constants) edizione Standard.

Il flag **APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** è supportato in Windows 7 e versioni successive di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Desktop](/windows/desktop/winstation/desktops)
</dt> <dt>

[Livelli di rappresentazione](impersonation-levels.md)
</dt> <dt>

[Utente interattivo](interactive-user.md)
</dt> <dt>

[Moniker di sessione](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Stazioni finestra](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 