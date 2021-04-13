---
description: Per connettersi a un computer remoto tramite WMI, verificare che le impostazioni di sicurezza dello spazio dei nomi WMI e delle impostazioni DCOM corrette siano abilitate per la connessione.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Protezione di una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2a044e49fed5eaa27fbc246dca3306a6c29650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528495"
---
# <a name="securing-a-remote-wmi-connection"></a>Protezione di una connessione WMI remota

Per connettersi a un computer remoto tramite WMI, verificare che le impostazioni di sicurezza dello spazio dei nomi WMI e delle impostazioni DCOM corrette siano abilitate per la connessione.

In WMI sono disponibili impostazioni predefinite per la rappresentazione, l'autenticazione e il servizio di autenticazione (NTLM o Kerberos) richieste dal computer di destinazione in una connessione remota. Il computer locale può utilizzare impostazioni predefinite diverse che non vengono accettate dal sistema di destinazione. È possibile modificare queste impostazioni nella chiamata di connessione.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Impostazioni di autenticazione e rappresentazione DCOM per WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Impostazione della sicurezza DCOM per consentire a un utente di accedere a un computer in modalità remota](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Consentire agli utenti di accedere a uno spazio dei nomi WMI specifico](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Impostazione della sicurezza dello spazio dei nomi per richiedere la crittografia dei dati per le connessioni remote](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Argomenti correlati](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>Impostazioni di autenticazione e rappresentazione DCOM per WMI

In WMI sono disponibili impostazioni predefinite per la rappresentazione DCOM, l'autenticazione e il servizio di autenticazione (NTLM o Kerberos) richieste dal sistema remoto. Il sistema locale può utilizzare impostazioni predefinite diverse che non vengono accettate dal sistema remoto di destinazione. È possibile modificare queste impostazioni nella chiamata di connessione. Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md). Per il servizio di autenticazione, tuttavia, è consigliabile specificare il **\_ \_ \_ valore predefinito** di autenticazione di RPC C e consentire a DCOM di scegliere il servizio appropriato per il computer di destinazione.

È possibile specificare le impostazioni nei parametri per le chiamate a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) in C++. Negli script è possibile definire impostazioni di sicurezza nelle chiamate a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), in un oggetto [**SWbemSecurity**](swbemsecurity.md) o nella stringa del [moniker](constructing-a-moniker-string.md) di scripting.

Per un elenco di tutte le costanti di rappresentazione C++, vedere [impostazione del livello di sicurezza del processo predefinito con c++](setting-the-default-process-security-level-using-c-.md). Per le costanti Visual Basic e le stringhe di scripting per l'utilizzo della connessione del moniker, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

Nella tabella seguente sono elencate le impostazioni predefinite del servizio di autenticazione, autenticazione e rappresentazione DCOM richieste dal computer di destinazione (computer B) in una connessione remota. Per ulteriori informazioni, vedere protezione di una connessione WMI remota.



| Sistema operativo del computer B | Stringa di scripting del livello di rappresentazione | Stringa di scripting del livello di autenticazione | Servizio di autenticazione |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista o versioni successive      | Impersonate                          | PKT                                   | Kerberos               |



 

Le connessioni remote WMI sono interessate da [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)) e [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx). Per ulteriori informazioni, vedere [connessione a WMI in modalità remota a partire da vista](connecting-to-wmi-remotely-starting-with-vista.md) e [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Tenere presente che la connessione a WMI nel computer locale dispone di un livello di autenticazione predefinito di **su PktPrivacy**.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Impostazione della sicurezza DCOM per consentire a un utente di accedere a un computer in modalità remota

La sicurezza in WMI è correlata alla connessione a uno spazio dei nomi WMI. WMI utilizza DCOM per gestire le chiamate remote. Un motivo per cui non è possibile connettersi a un computer remoto è dovuto a un errore DCOM (errore "accesso DCOM negato" decimale-2147024891 o esadecimale 0x80070005). Per ulteriori informazioni sulla sicurezza DCOM in WMI per le applicazioni C++, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md).

È possibile configurare le impostazioni DCOM per WMI utilizzando l'utilità di configurazione DCOM (**DCOMCnfg.exe**) disponibile in **strumenti di amministrazione** nel **Pannello di controllo**. Questa utilità espone le impostazioni che consentono a determinati utenti di connettersi al computer in modalità remota tramite DCOM. Per impostazione predefinita, i membri del gruppo Administrators possono connettersi in remoto al computer. Con questa utilità è possibile impostare la sicurezza per l'avvio, l'accesso e la configurazione del servizio WMI.

Nella procedura seguente viene descritto come concedere le autorizzazioni di avvio e attivazione remota DCOM per determinati utenti e gruppi. Se il computer A si connette in modalità remota al computer B, è possibile impostare queste autorizzazioni sul computer B per consentire a un utente o a un gruppo che non fa parte del gruppo Administrators nel computer B di eseguire chiamate di avvio e attivazione DCOM sul computer B.

**Per concedere autorizzazioni di avvio e attivazione remote DCOM per un utente o un gruppo**

1.  Fare clic sul pulsante **Start**, scegliere **Esegui**, digitare **DCOMCNFG**, quindi fare clic su **OK**.
2.  Nella finestra di dialogo **Servizi componenti** espandere **Servizi componenti**, espandere **computer**, quindi fare clic con il pulsante destro del mouse su **computer locale** e scegliere **Proprietà**.
3.  Nella finestra di dialogo **proprietà computer locale** fare clic sulla scheda **protezione com** .
4.  In **Autorizzazioni di esecuzione e attivazione**, fare clic su **Modifica limiti**.
5.  Nella finestra di dialogo **autorizzazione di avvio** , attenersi alla procedura seguente se il nome o il gruppo non viene visualizzato nell' **elenco gruppi o nomi utente**:

    1.  Nella finestra di dialogo **autorizzazione di avvio** fare clic su **Aggiungi**.
    2.  Nella finestra di dialogo **Seleziona utenti, computer o gruppi** , aggiungere il nome e il gruppo nella casella **immettere i nomi degli oggetti da selezionare** , quindi fare clic su **OK**.

6.  Nella finestra di dialogo **autorizzazione di avvio** selezionare l'utente e il gruppo nella casella **nome gruppo o utente** . Nella colonna **Consenti** in **autorizzazioni per utente** Selezionare **avvio remoto** e selezionare **attivazione remota**, quindi fare clic su **OK**.

Nella procedura seguente viene descritto come concedere le autorizzazioni di accesso remoto DCOM per determinati utenti e gruppi. Se il computer A si connette in modalità remota al computer B, è possibile impostare queste autorizzazioni sul computer B per consentire a un utente o a un gruppo che non fa parte del gruppo Administrators nel computer B di connettersi al computer B.

**Per concedere autorizzazioni di accesso remoto DCOM**

1.  Fare clic sul pulsante **Start**, scegliere **Esegui**, digitare **DCOMCNFG**, quindi fare clic su **OK**.
2.  Nella finestra di dialogo **Servizi componenti** espandere **Servizi componenti**, espandere **computer**, quindi fare clic con il pulsante destro del mouse su **computer locale** e scegliere **Proprietà**.
3.  Nella finestra di dialogo **proprietà computer locale** fare clic sulla scheda **protezione com** .
4.  In **Autorizzazioni di accesso**, fare clic su **Modifica limiti**.
5.  Nella finestra di dialogo **autorizzazioni di accesso** selezionare nome **accesso anonimo** nella casella nome **gruppo o utente** . Nella colonna **Consenti** in **autorizzazioni per utente** Selezionare **accesso remoto** e quindi fare clic su **OK**.

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Consentire agli utenti di accedere a uno spazio dei nomi WMI specifico

È possibile consentire o impedire agli utenti di accedere a uno specifico spazio dei nomi WMI impostando l'autorizzazione "Remote Enable" nel controllo WMI per uno spazio dei nomi. Se un utente tenta di connettersi a uno spazio dei nomi a cui non è consentito accedere, riceverà un errore 0x80041003. Per impostazione predefinita, questa autorizzazione è abilitata solo per gli amministratori. Un amministratore può abilitare l'accesso remoto a specifici spazi dei nomi WMI per un utente non amministratore.

La procedura seguente imposta le autorizzazioni di abilitazione remota per un utente non amministratore.

**Per impostare le autorizzazioni di abilitazione remota**

1.  Connettersi al computer remoto utilizzando il controllo WMI.

    Per ulteriori informazioni sul controllo WMI, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).

2.  Nella scheda **sicurezza** selezionare lo spazio dei nomi e fare clic su **sicurezza**.
3.  Individuare l'account appropriato e selezionare **Abilita remoto** nell'elenco **autorizzazioni** .

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Impostazione della sicurezza dello spazio dei nomi per richiedere la crittografia dei dati per le connessioni remote

Un amministratore o un file MOF può configurare uno spazio dei nomi WMI in modo che non venga restituito alcun dato, a meno che non si usi la riservatezza dei pacchetti (**RPC \_ C Authentication \_ \_ level \_ PKT \_ privacy** o **su PktPrivacy** come moniker in uno script) in una connessione a tale spazio dei nomi. In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete. Se si tenta di impostare un livello di autenticazione inferiore, si otterrà un messaggio di accesso negato. Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

Nell'esempio di codice VBScript riportato di seguito viene illustrato come connettersi a uno spazio dei nomi crittografato utilizzando "su PktPrivacy".


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega con WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Creazione di processi in modalità remota con WMI](creating-processes-remotely.md)
</dt> <dt>

[Protezione di client e provider C++](securing-c---clients-and-providers.md)
</dt> <dt>

[Protezione dei client di scripting](securing-scripting-clients.md)
</dt> </dl>

 

 
