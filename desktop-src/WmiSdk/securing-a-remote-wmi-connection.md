---
description: Per connettersi a un computer remoto tramite WMI, verificare che siano abilitate le impostazioni DCOM corrette e le impostazioni di sicurezza dello spazio dei nomi WMI per la connessione.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Protezione di una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8650ee47c549121a51e5d131055a84c176da944c6146f0532ffc86f1d2f9e4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739515"
---
# <a name="securing-a-remote-wmi-connection"></a>Protezione di una connessione WMI remota

Per connettersi a un computer remoto tramite WMI, verificare che siano abilitate le impostazioni DCOM corrette e le impostazioni di sicurezza dello spazio dei nomi WMI per la connessione.

WMI dispone delle impostazioni predefinite del servizio di rappresentazione, autenticazione e autenticazione (NTLM o Kerberos) richieste dal computer di destinazione in una connessione remota. Il computer locale può usare impostazioni predefinite diverse che il sistema di destinazione non accetta. È possibile modificare queste impostazioni nella chiamata di connessione.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Impostazioni di rappresentazione e autenticazione DCOM Impostazioni WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Impostazione della sicurezza DCOM su Consenti a un utente di accedere a un computer in modalità remota](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Consentire agli utenti di accedere a uno spazio dei nomi WMI specifico](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Impostazione della sicurezza dello spazio dei nomi per richiedere la crittografia dei dati per le connessioni remote](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Argomenti correlati](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>Impostazioni di rappresentazione e autenticazione DCOM Impostazioni WMI

WMI dispone delle impostazioni predefinite del servizio di rappresentazione, autenticazione e autenticazione DCOM (NTLM o Kerberos) richieste da un sistema remoto. Il sistema locale può usare impostazioni predefinite diverse che il sistema remoto di destinazione non accetta. È possibile modificare queste impostazioni nella chiamata di connessione. Per altre informazioni, vedere [Impostazione della sicurezza del processo dell'applicazione client.](setting-client-application-process-security.md) Tuttavia, per il servizio di autenticazione, è consigliabile specificare **RPC \_ C \_ AUTHN \_ DEFAULT** e consentire a DCOM di scegliere il servizio appropriato per il computer di destinazione.

È possibile specificare le impostazioni nei parametri per le chiamate [**a CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) [**o CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) in C++. Negli script è possibile definire le impostazioni di sicurezza nelle chiamate a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), in un [**oggetto SWbemSecurity**](swbemsecurity.md) o nella stringa del [moniker di](constructing-a-moniker-string.md) scripting.

Per un elenco di tutte le costanti di rappresentazione C++, vedere Impostazione del livello di sicurezza del processo [predefinito tramite C++.](setting-the-default-process-security-level-using-c-.md) Per informazioni Visual Basic costanti e stringhe di scripting per l'uso della connessione moniker, vedere Impostazione del livello di sicurezza del processo predefinito [tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

Nella tabella seguente sono elencate le impostazioni predefinite del servizio di rappresentazione, autenticazione e autenticazione DCOM richieste dal computer di destinazione (Computer B) in una connessione remota. Per altre informazioni, vedere Protezione di una connessione WMI remota.



| Sistema operativo del computer B | Stringa di scripting a livello di rappresentazione | Stringa di scripting a livello di autenticazione | Servizio di autenticazione |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista o versioni successive      | Impersonate                          | Pkt                                   | Kerberos               |



 

Le connessioni remote WMI sono interessate [da Controllo dell'account utente e](/previous-versions/aa905108(v=msdn.10)) Windows [Firewall.](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx) Per altre informazioni, vedere Connessione a WMI in remoto [a partire da Vista](connecting-to-wmi-remotely-starting-with-vista.md) e Connessione tramite Windows [firewall.](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)

Tenere presente che la connessione a WMI nel computer locale ha un livello di autenticazione predefinito **PktPrivacy**.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Impostazione della sicurezza DCOM su Consenti a un utente di accedere a un computer in modalità remota

La sicurezza in WMI è correlata alla connessione a uno spazio dei nomi WMI. WMI usa DCOM per gestire le chiamate remote. Un motivo per cui non è possibile connettersi a un computer remoto è dovuto a un errore DCOM (errore "Accesso DCOM negato" decimale -2147024891 o esadecimale 0x80070005). Per altre informazioni sulla sicurezza DCOM in WMI per le applicazioni C++, vedere [Impostazione della sicurezza del processo dell'applicazione client.](setting-client-application-process-security.md)

È possibile configurare le impostazioni DCOM per WMI usando l'utilità di configurazione DCOM (**DCOMCnfg.exe**) disponibile **in** Strumenti di amministrazione in **Pannello di controllo**. Questa utilità espone le impostazioni che consentono a determinati utenti di connettersi al computer in remoto tramite DCOM. I membri del gruppo Administrators sono autorizzati a connettersi in remoto al computer per impostazione predefinita. Con questa utilità è possibile impostare la sicurezza per avviare, accedere e configurare il servizio WMI.

La procedura seguente descrive come concedere autorizzazioni di avvio e attivazione remote DCOM per determinati utenti e gruppi. Se il computer A si connette in remoto al Computer B, è possibile impostare queste autorizzazioni nel computer B per consentire a un utente o a un gruppo che non fa parte del gruppo Administrators nel Computer B di eseguire chiamate di avvio e attivazione DCOM nel computer B.

**Per concedere autorizzazioni di attivazione e avvio remoto DCOM per un utente o un gruppo**

1.  Fare **clic sul pulsante Start**, **scegliere** Esegui , **digitare DCOMCNFG** e quindi fare clic su **OK.**
2.  Nella finestra **di dialogo Servizi** componenti espandere Servizi componenti , computer , quindi fare clic con il pulsante destro **del** mouse Computer locale e scegliere **Proprietà**.  
3.  Nella finestra **Computer locale proprietà** fare clic sulla scheda **Sicurezza COM** .
4.  In **Autorizzazioni di esecuzione e attivazione**, fare clic su **Modifica limiti**.
5.  Nella finestra **di dialogo Autorizzazione** di avvio seguire questa procedura se il nome o il gruppo non viene visualizzato nell'elenco Gruppi o nomi **utente**:

    1.  Nella finestra **di dialogo Autorizzazione** di avvio fare clic su **Aggiungi**.
    2.  Nella finestra **di dialogo Seleziona utenti,** computer o gruppi aggiungere  il nome e il gruppo nella casella Immettere i nomi degli oggetti da selezionare e quindi fare clic su **OK.**

6.  Nella finestra **di dialogo Autorizzazione** di avvio selezionare l'utente e il gruppo nella casella Gruppi o **nomi** utente . Nella colonna **Consenti** in Autorizzazioni **per** utente selezionare Avvio **remoto,** selezionare **Attivazione remota** e quindi fare clic su **OK.**

Nella procedura seguente viene descritto come concedere autorizzazioni di accesso remoto DCOM per determinati utenti e gruppi. Se il computer A si connette in remoto al Computer B, è possibile impostare queste autorizzazioni nel computer B per consentire a un utente o a un gruppo che non fa parte del gruppo Administrators nel Computer B di connettersi al computer B.

**Per concedere autorizzazioni di accesso remoto DCOM**

1.  Fare **clic sul pulsante Start**, **scegliere** Esegui , **digitare DCOMCNFG** e quindi fare clic su **OK.**
2.  Nella finestra **di dialogo Servizi** componenti espandere Servizi componenti , computer , quindi fare clic con il pulsante destro **del** mouse Computer locale e scegliere **Proprietà**.  
3.  Nella finestra **Computer locale proprietà** fare clic sulla scheda **Sicurezza COM** .
4.  In **Autorizzazioni di accesso**, fare clic su **Modifica limiti**.
5.  Nella finestra **di dialogo Autorizzazione** di accesso selezionare NOME **ACCESSO** ANONIMO nella casella Nomi **gruppo o** utente . Nella colonna **Consenti** in Autorizzazioni **per utente** selezionare **Accesso remoto** e quindi fare clic su **OK.**

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Consentire agli utenti di accedere a uno spazio dei nomi WMI specifico

È possibile consentire o non consentire agli utenti l'accesso a uno spazio dei nomi WMI specifico impostando l'autorizzazione "Abilita remoto" nel controllo WMI per uno spazio dei nomi. Se un utente tenta di connettersi a uno spazio dei nomi a cui non è consentito l'accesso, riceverà un errore 0x80041003. Per impostazione predefinita, questa autorizzazione è abilitata solo per gli amministratori. Un amministratore può abilitare l'accesso remoto a spazi dei nomi WMI specifici per un utente non amministratore.

La procedura seguente imposta le autorizzazioni di abilitazione remota per un utente non amministratore.

**Per impostare le autorizzazioni di abilitazione remota**

1.  Connessione al computer remoto utilizzando il controllo WMI.

    Per altre informazioni sul controllo WMI, vedere Impostazione [della sicurezza dello spazio dei nomi con il controllo WMI.](setting-namespace-security-with-the-wmi-control.md)

2.  Nella scheda **Sicurezza selezionare** lo spazio dei nomi e fare clic su **Sicurezza**.
3.  Individuare l'account appropriato e **selezionare Abilita remoto nell'elenco** Autorizzazioni . 

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Impostazione della sicurezza dello spazio dei nomi per richiedere la crittografia dei dati per le connessioni remote

Un amministratore o un file MOF può configurare uno spazio dei nomi WMI in modo che non vengano restituiti dati a meno che non si usi la privacy dei pacchetti **(RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** o **PktPrivacy** come moniker in uno script) in una connessione a tale spazio dei nomi. In questo modo si garantisce che i dati siano crittografati quando attraversano la rete. Se si tenta di impostare un livello di autenticazione inferiore, verrà visualizzato un messaggio di accesso negato. Per altre informazioni, vedere [Richiesta di una connessione crittografata a uno spazio dei nomi.](requiring-an-encrypted-connection-to-a-namespace.md)

Nell'esempio di codice VBScript seguente viene illustrato come connettersi a uno spazio dei nomi crittografato usando "pktPrivacy".


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega con WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Creazione di processi in remoto con WMI](creating-processes-remotely.md)
</dt> <dt>

[Protezione di client e provider C++](securing-c---clients-and-providers.md)
</dt> <dt>

[Protezione dei client di scripting](securing-scripting-clients.md)
</dt> </dl>

 

 
