---
description: WMI usa un descrittore di Windows di sicurezza standard per controllare l'accesso agli spazi dei nomi WMI.
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
ms.openlocfilehash: b750c8dee2b95597636620dc54ad193cb762cd259b2bf7149c52996e85e09b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926027"
---
# <a name="access-to-wmi-namespaces"></a>Accesso agli spazi dei nomi WMI

WMI usa un descrittore di sicurezza Windows *standard* per controllare l'accesso agli spazi dei nomi WMI. Quando ci si connette a WMI, tramite il moniker WMI "winmgmts" o una chiamata a [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) o [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), ci si connette a uno spazio dei nomi specifico.

In questo argomento vengono illustrate le informazioni seguenti:

-   [Sicurezza dello spazio dei nomi WMI](#wmi-namespace-security)
-   [Controllo dello spazio dei nomi WMI](#wmi-namespace-auditing)
-   [Tipi di eventi dello spazio dei nomi](#types-of-namespace-events)
-   [Accesso allo spazio dei nomi Impostazioni](#namespace-access-settings)
-   [Autorizzazioni predefinite per gli spazi dei nomi WMI](#default-permissions-on-wmi-namespaces)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-namespace-security"></a>Sicurezza dello spazio dei nomi WMI

WMI mantiene la sicurezza dello spazio dei nomi confrontando il [*token di accesso*](/windows/desktop/SecGloss/a-gly) dell'utente che si connette allo spazio dei nomi con il [*descrittore*](/windows/desktop/SecGloss/s-gly) di sicurezza dello spazio dei nomi. Per altre informazioni sulla sicurezza Windows, vedere [Accesso agli oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).

Tenere presente che, a partire da Windows Vista, il controllo dell'account utente [influisce](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) sull'accesso ai dati WMI e su ciò che può essere configurato con [*il controllo WMI*](gloss-w.md). Per altre informazioni, vedere [Autorizzazioni predefinite per gli spazi dei nomi WMI](#default-permissions-on-wmi-namespaces) e Controllo account utente e [WMI.](user-account-control-and-wmi.md)

L'accesso agli spazi dei nomi WMI è interessato anche quando la connessione viene stabilita da un computer remoto. Per altre informazioni, vedere [Connessione a WMI](connecting-to-wmi-on-a-remote-computer.md)in un computer remoto , Protezione di una connessione [WMI](securing-a-remote-wmi-connection.md)remota e Connessione tramite [Windows firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

I provider devono basarsi sull'impostazione di rappresentazione per la connessione per determinare se lo script client o l'applicazione deve ricevere dati. Per altre informazioni sulle applicazioni script e client, vedere [Impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md). Per altre informazioni sulla [*rappresentazione del provider,*](gloss-p.md) vedere [Sviluppo di un provider WMI.](developing-a-wmi-provider.md)

## <a name="wmi-namespace-auditing"></a>Controllo dello spazio dei nomi WMI

WMI usa lo spazio dei nomi [*Elenchi di controllo di accesso di sistema (SACL) per*](/windows/desktop/SecGloss/s-gly) controllare l'attività dello spazio dei nomi. Per abilitare il controllo degli spazi dei nomi WMI, usare **la** scheda Sicurezza del controllo [*WMI*](gloss-w.md) per modificare le impostazioni di controllo per lo spazio dei nomi.

Il controllo non è abilitato durante l'installazione del sistema operativo. Per abilitare il controllo, fare clic **sulla scheda** Controllo nella finestra **Sicurezza** standard. È quindi possibile aggiungere una voce di controllo.

Criteri di gruppo per il computer locale deve essere impostato per consentire il controllo. È possibile abilitare il controllo eseguendo lo snap-in  MMC Gpedit.msc e impostando Controlla accesso agli oggetti in Configurazione computer Windows Impostazioni   >    >  **Sicurezza Impostazioni**  >  **Criteri** locali  >  **Criteri di controllo**.

Una voce di controllo modifica il SACL dello spazio dei nomi. Quando si aggiunge una voce di controllo, si tratta di un utente, un gruppo, un computer o un'entità di sicurezza predefinita. Dopo aver aggiunto la voce, è possibile impostare le operazioni di accesso che comportano eventi del registro di sicurezza. Ad esempio, per il gruppo Authenticated Users, è possibile fare clic su Esegui metodi. Questa impostazione comporta eventi del registro di sicurezza ogni volta che un membro del gruppo Authenticated Users esegue un metodo in tale spazio dei nomi. L'ID evento per gli eventi WMI è 4662.

L'account deve essere nel gruppo Administrators ed essere in esecuzione con privilegi elevati per modificare le impostazioni di controllo. L'account Amministratore predefinito può anche modificare la sicurezza o il controllo per uno spazio dei nomi. Per altre informazioni sull'esecuzione in modalità con privilegi elevati, vedere [Controllo dell'account utente e WMI.](user-account-control-and-wmi.md)

Il controllo WMI genera eventi di esito positivo o negativo per i tentativi di accesso agli spazi dei nomi WMI. Il servizio non controlla l'esito positivo o negativo delle operazioni del provider. Ad esempio, quando uno script si connette a WMI e a uno spazio dei nomi, potrebbe non riuscire perché l'account con cui è in esecuzione lo script non ha accesso a tale spazio dei nomi o può tentare un'operazione, ad esempio la modifica dell'elenco DACL, non concessa.

Se si esegue con un account nel gruppo Administrators, è possibile visualizzare gli eventi di controllo dello spazio dei nomi nell'interfaccia Visualizzatore eventi **utente.**

## <a name="types-of-namespace-events"></a>Tipi di eventi dello spazio dei nomi

WMI traccia i tipi di eventi seguenti nel registro eventi di sicurezza:

-   Controllo riuscito

    L'operazione deve completare correttamente due passaggi per un controllo riuscito. In primo luogo, WMI concede l'accesso all'applicazione client o allo script in base al SID client e all'elenco DACL dello spazio dei nomi. In secondo piano, l'operazione richiesta corrisponde ai diritti di accesso nel SACL dello spazio dei nomi per tale utente o gruppo.

-   Errore di controllo

    WMI nega l'accesso allo spazio dei nomi, ma l'operazione richiesta corrisponde ai diritti di accesso nello spazio dei nomi SACL per tale utente o gruppo.

## <a name="namespace-access-settings"></a>Accesso allo spazio dei nomi Impostazioni

È possibile visualizzare i diritti di accesso allo spazio dei nomi per vari account nel controllo WMI. Queste costanti sono descritte in [**Costanti dei diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md). È possibile modificare l'accesso a uno spazio dei nomi WMI usando il controllo WMI o a livello di codice. Per altre informazioni, vedere [Modifica della sicurezza degli accessi in oggetti a protezione diretta](changing-access-security-on-securable-objects.md).

WMI controlla le modifiche in tutte le autorizzazioni di accesso elencate nell'elenco seguente, ad eccezione dell'autorizzazione Abilita remoto. Le modifiche vengono registrate come esito positivo o negativo del controllo corrispondente all'autorizzazione Modifica sicurezza.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Metodi Execute
</dt> <dd>

Consente all'utente di eseguire metodi definiti nelle classi WMI. Corrisponde alla costante di autorizzazione di accesso EXECUTE di **WBEM \_ METHOD. \_**

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Scrittura completa
</dt> <dd>

Consente l'accesso completo in lettura, scrittura ed eliminazione alle classi WMI e alle istanze di classe, sia statiche che dinamiche. Corrisponde alla costante **di autorizzazione di accesso WBEM FULL WRITE \_ \_ \_ REP.**

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Scrittura parziale
</dt> <dd>

Consente l'accesso in scrittura alle istanze della classe WMI statiche. Corrisponde alla costante **di autorizzazione di accesso WBEM PARTIAL WRITE \_ \_ \_ REP.**

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Scrittura del provider
</dt> <dd>

Consente l'accesso in scrittura alle istanze dinamiche della classe WMI. Corrisponde alla costante **di autorizzazione di accesso WBEM WRITE \_ \_ PROVIDER.**

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Abilitare l'account
</dt> <dd>

Consente l'accesso in lettura alle istanze della classe WMI. Corrisponde alla costante **di autorizzazione di accesso \_ ENABLE WBEM.**

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Abilitazione remota
</dt> <dd>

Consente l'accesso allo spazio dei nomi da parte di computer remoti. Corrisponde alla costante **di autorizzazione di accesso WBEM REMOTE \_ \_ ACCESS.**

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sicurezza di lettura
</dt> <dd>

Consente l'accesso in sola lettura alle impostazioni DACL. Corrisponde alla costante **di autorizzazione di accesso READ \_ CONTROL.**

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Modifica sicurezza
</dt> <dd>

Consente l'accesso in scrittura alle impostazioni DACL. Corrisponde alla costante **di autorizzazione di accesso \_ dell'applicazione** livello dati WRITE.

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Autorizzazioni predefinite per gli spazi dei nomi WMI

I gruppi di sicurezza predefiniti sono:

-   Utenti autenticati
-   LOCAL SERVICE
-   NETWORK SERVICE
-   Amministratori (nel computer locale)

Le autorizzazioni di accesso predefinite per Authenticated Users, LOCAL SERVICE e NETWORK SERVICE sono:

-   Esegui metodi
-   Scrittura completa
-   Abilita account

Gli account nel gruppo Administrators dispongono di tutti i diritti disponibili, inclusa la modifica dei descrittori di sicurezza. Tuttavia, a causa del controllo dell'account utente, il controllo WMI o lo script deve essere in esecuzione con sicurezza elevata. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](user-account-control-and-wmi.md)

A volte uno script o un'applicazione deve abilitare un privilegio di amministratore, ad esempio **SeSecurityPrivilege,** per eseguire un'operazione. Ad esempio, uno script può eseguire il metodo [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) della classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) senza **SeSecurityPrivilege e** ottenere le informazioni di sicurezza nell'elenco di controllo di accesso discrezionale [*(DACL)*](/windows/desktop/SecGloss/d-gly) del descrittore di sicurezza dell'oggetto stampante [*.*](/windows/desktop/SecGloss/s-gly) Tuttavia, le informazioni SACL non vengono restituite allo script a meno che il privilegio **SeSecurityPrivilege** non sia disponibile e abilitato per l'account. Se l'account non ha il privilegio disponibile, non può essere abilitato. Per altre informazioni, vedere [Esecuzione di operazioni con privilegi](executing-privileged-operations.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WMI](about-wmi.md)
</dt> </dl>

 

 
