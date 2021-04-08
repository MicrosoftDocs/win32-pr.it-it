---
description: WMI utilizza un descrittore di sicurezza standard di Windows per controllare l'accesso agli spazi dei nomi WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Accesso agli spazi dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968373"
---
# <a name="access-to-wmi-namespaces"></a>Accesso agli spazi dei nomi WMI

WMI utilizza un *descrittore di sicurezza* standard di Windows per controllare l'accesso agli spazi dei nomi WMI. Quando ci si connette a WMI, tramite il moniker "winmgmts" WMI o una chiamata a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) o [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), si esegue la connessione a uno spazio dei nomi specifico.

Le informazioni seguenti sono illustrate in questo argomento:

-   [Sicurezza dello spazio dei nomi WMI](#wmi-namespace-security)
-   [Controllo dello spazio dei nomi WMI](#wmi-namespace-auditing)
-   [Tipi di eventi dello spazio dei nomi](#types-of-namespace-events)
-   [Impostazioni di accesso allo spazio dei nomi](#namespace-access-settings)
-   [Autorizzazioni predefinite per gli spazi dei nomi WMI](#default-permissions-on-wmi-namespaces)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-namespace-security"></a>Sicurezza dello spazio dei nomi WMI

WMI mantiene la sicurezza dello spazio dei nomi confrontando il [*token di accesso*](/windows/desktop/SecGloss/a-gly) dell'utente che si connette allo spazio dei nomi con il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) dello spazio dei nomi. Per ulteriori informazioni sulla sicurezza di Windows, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).

Tenere presente che, a partire da Windows Vista, [controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) influisca sull'accesso ai dati WMI e su cosa può essere configurato con il [*controllo WMI*](gloss-w.md). Per ulteriori informazioni, vedere [autorizzazioni predefinite per gli spazi dei nomi WMI](#default-permissions-on-wmi-namespaces) e [controllo dell'account utente e WMI](user-account-control-and-wmi.md).

L'accesso agli spazi dei nomi WMI viene inoltre influenzato quando la connessione è da un computer remoto. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md), [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)e [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

I provider devono basarsi sull'impostazione di rappresentazione per la connessione per determinare se lo script client o l'applicazione deve ricevere dati. Per ulteriori informazioni sullo script e sulle applicazioni client, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md). Per ulteriori informazioni sulla rappresentazione del [*provider*](gloss-p.md) , vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).

## <a name="wmi-namespace-auditing"></a>Controllo dello spazio dei nomi WMI

WMI utilizza lo spazio dei nomi [*elenchi di controllo di accesso di sistema (SACL)*](/windows/desktop/SecGloss/s-gly) per controllare l'attività dello spazio dei nomi Per abilitare il controllo degli spazi dei nomi WMI, utilizzare la scheda **sicurezza** del [*controllo WMI*](gloss-w.md) per modificare le impostazioni di controllo per lo spazio dei nomi.

Il controllo non è abilitato durante l'installazione del sistema operativo. Per abilitare il controllo, fare clic sulla scheda **controllo** nella finestra **sicurezza** standard. È quindi possibile aggiungere una voce di controllo.

Criteri di gruppo per il computer locale deve essere impostato in modo da consentire il controllo. Per abilitare il controllo, è possibile eseguire lo snap-in MMC gpedit. msc e impostare **controllo accesso oggetti** in **Configurazione computer** impostazioni di Windows impostazioni di sicurezza Criteri di  >    >    >    >  **controllo** locali.

Una voce di controllo modifica l'elenco SACL dello spazio dei nomi. Quando si aggiunge una voce di controllo, si tratta di un utente, un gruppo, un computer o un'entità di sicurezza predefinita. Dopo aver aggiunto la voce, è possibile impostare le operazioni di accesso che generano eventi del registro di sicurezza. Ad esempio, per il gruppo Authenticated Users, è possibile fare clic su Execute methods. Questa impostazione determina gli eventi del registro di sicurezza ogni volta che un membro del gruppo Authenticated Users esegue un metodo nello spazio dei nomi. L'ID evento per gli eventi WMI è 4662.

Per modificare le impostazioni di controllo, l'account deve appartenere al gruppo Administrators ed essere in esecuzione con privilegi elevati. L'account Administrator predefinito può anche modificare la sicurezza o il controllo per uno spazio dei nomi. Per ulteriori informazioni sull'esecuzione in modalità con privilegi elevati, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).

Il controllo WMI genera eventi di esito positivo o negativo per i tentativi di accesso agli spazi dei nomi WMI. Il servizio non controlla l'esito positivo o negativo delle operazioni del provider. Ad esempio, quando uno script si connette a WMI e a uno spazio dei nomi, potrebbe non riuscire perché l'account con cui viene eseguito lo script non ha accesso a tale spazio dei nomi o può tentare di eseguire un'operazione, ad esempio la modifica del DACL, non concesso.

Se si esegue un account nel gruppo Administrators, è possibile visualizzare gli eventi di controllo dello spazio dei nomi nell'interfaccia utente di **Visualizzatore eventi** .

## <a name="types-of-namespace-events"></a>Tipi di eventi dello spazio dei nomi

WMI traccia i tipi di eventi seguenti nel registro eventi di sicurezza:

-   Controllo riuscito

    L'operazione deve completare due passaggi per un controllo completato correttamente. In primo luogo, WMI concede l'accesso all'applicazione client o allo script in base al SID client e all'elenco DACL dello spazio dei nomi. In secondo luogo, l'operazione richiesta corrisponde ai diritti di accesso nel SACL dello spazio dei nomi per tale utente o gruppo.

-   Controllo non riuscito

    WMI nega l'accesso allo spazio dei nomi, ma l'operazione richiesta corrisponde ai diritti di accesso nel SACL dello spazio dei nomi per tale utente o gruppo.

## <a name="namespace-access-settings"></a>Impostazioni di accesso allo spazio dei nomi

È possibile visualizzare i diritti di accesso allo spazio dei nomi per diversi account nel controllo WMI. Queste costanti sono descritte in [**costanti di diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md). È possibile modificare l'accesso a uno spazio dei nomi WMI utilizzando il controllo WMI o a livello di codice. Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

WMI controlla le modifiche apportate a tutte le autorizzazioni di accesso elencate nell'elenco seguente, ad eccezione dell'autorizzazione Abilita remota. Le modifiche vengono registrate come controllo riuscito o errore corrispondente all'autorizzazione Modifica sicurezza.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Metodi Execute
</dt> <dd>

Consente all'utente di eseguire metodi definiti nelle classi WMI. Corrisponde alla costante di autorizzazione per l' **\_ \_ esecuzione del metodo WBEM** .

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Scrittura completa
</dt> <dd>

Consente l'accesso completo in lettura, scrittura ed eliminazione alle classi e alle istanze di classi WMI, sia statiche che dinamiche. Corrisponde alla costante di autorizzazione per l'accesso alla **\_ \_ \_ Rep Full Write di WBEM** .

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Scrittura parziale
</dt> <dd>

Consente l'accesso in scrittura alle istanze di classi WMI statiche. Corrisponde alla costante di autorizzazione per l'accesso con **\_ \_ scrittura \_ parziale WBEM** .

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Scrittura del provider
</dt> <dd>

Consente l'accesso in scrittura alle istanze di classi WMI dinamiche. Corrisponde alla costante di autorizzazione di accesso del **\_ \_ provider di scrittura WBEM** .

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Abilita account
</dt> <dd>

Consente l'accesso in lettura alle istanze della classe WMI. Corrisponde alla costante di autorizzazione **\_ abilitata** per l'accesso WBEM.

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Abilita remoto
</dt> <dd>

Consente l'accesso allo spazio dei nomi da parte dei computer remoti. Corrisponde alla costante di autorizzazione per l'accesso **\_ \_ remoto WBEM** .

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sicurezza di lettura
</dt> <dd>

Consente l'accesso in sola lettura alle impostazioni DACL. Corrisponde alla costante di autorizzazione per l'accesso al **\_ controllo Read** .

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Modifica sicurezza
</dt> <dd>

Consente l'accesso in scrittura alle impostazioni DACL. Corrisponde alla costante di autorizzazione per l'accesso alla **\_ DAC di scrittura** .

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Autorizzazioni predefinite per gli spazi dei nomi WMI

I gruppi di sicurezza predefiniti sono:

-   Utenti autenticati
-   LOCAL SERVICE
-   NETWORK SERVICE
-   Amministratori (nel computer locale)

Le autorizzazioni di accesso predefinite per gli utenti, il servizio locale e il servizio di rete autenticato sono:

-   Esegui metodi
-   Scrittura completa
-   Abilita account

Gli account del gruppo Administrators dispongono di tutti i diritti disponibili, inclusa la modifica dei descrittori di sicurezza. Tuttavia, a causa del controllo dell'account utente, il controllo WMI o lo script deve essere eseguito con privilegi elevati di sicurezza. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).

In alcuni casi uno script o un'applicazione deve abilitare un privilegio di amministratore, ad esempio **SeSecurityPrivilege**, per eseguire un'operazione. Uno script può ad esempio eseguire il metodo [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) della classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) senza **SeSecurityPrivilege** e ottenere le informazioni di sicurezza nell'elenco di [*controllo di accesso discrezionale (DACL)*](/windows/desktop/SecGloss/d-gly) del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)dell'oggetto Printer. Tuttavia, le informazioni relative al SACL non vengono restituite allo script, a meno che il privilegio **SeSecurityPrivilege** non sia disponibile e abilitato per l'account. Se per l'account non è disponibile il privilegio, non è possibile abilitarlo. Per altre informazioni, vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
