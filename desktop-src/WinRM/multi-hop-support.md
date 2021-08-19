---
title: Supporto multi hop in WinRM
description: Windows Gestione remota Windows (WinRM) supporta la delega delle credenziali utente tra più computer remoti.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76be3054fc9c0d624c206cf5a26d7788e763dfc81f1b2069f6abff8736be2388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121761"
---
# <a name="multi-hop-support-in-winrm"></a>Supporto multi hop in WinRM

Windows Gestione remota Windows (WinRM) supporta la delega delle credenziali utente tra più computer remoti. La funzionalità di supporto multi hop può ora usare Credential Security Service Provider (CredSSP) per l'autenticazione. CredSSP consente a un'applicazione di delegare le credenziali dell'utente dal computer client al server di destinazione.

L'autenticazione CredSSP è destinata agli ambienti in cui non è possibile usare la delega Kerberos. È stato aggiunto il supporto per CredSSP per consentire a un utente di connettersi a un server remoto e avere la possibilità di accedere a un computer con secondo hop, ad esempio una condivisione file.

Per altre informazioni su CredSSP, vedere [kb 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> I client e i server WinRM supporteranno l'autenticazione CredSSP solo con credenziali esplicite.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Configurazione e dettagli della configurazione del supporto multi hop

Esistono diversi meccanismi per la configurazione delle impostazioni di Gestione remota Windows. Nella procedura seguente vengono usati **l'utilità winrm** Criteri di gruppo editor (**GPEdit.msc**). CredSSP può essere abilitato anche per WinRM usando Windows PowerShell. Vedere i cmdlet Windows PowerShell [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)e [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) per informazioni dettagliate sulla configurazione ed esempi di utilizzo.

La delega CredSSP deve essere abilitata nelle impostazioni client e nelle impostazioni del servizio nel computer remoto. Inoltre, l'uso di CredSSP richiede la configurazione di un [*listener*](windows-remote-management-glossary.md) HTTP o HTTPS nel server.

**Per configurare il supporto multi hop usando l'autenticazione CredSSP per WinRM**

1.  CredSSP deve essere abilitato nelle impostazioni di configurazione del client. Questo flag può essere abilitato manualmente o tramite un'Criteri di gruppo predefinita. L'impostazione predefinita è **False**. Il criterio di autenticazione **Allow CredSSP** si trova nel percorso seguente: Computer Configuration \\ Administrative template Windows Components Windows Remote Management \\ \\ (WinRM) \\ WinRM Client.

    Il comando seguente illustra come usare l'utilità winrm per abilitare CredSSP nel client WinRM:

    **winrm set winrm/config/client/auth @{CredSSP="true"}**

2.  CredSSP deve essere abilitato nelle impostazioni di configurazione del servizio Gestione remota Windows. Questo flag può essere abilitato manualmente o tramite un'Criteri di gruppo predefinita. L'impostazione predefinita è **False**. Il criterio di autenticazione **Allow CredSSP** si trova nel percorso seguente: Computer Configuration \\ Administrative template Windows Components Windows Remote Management \\ \\ (WinRM) \\ WinRM Service.

    Il comando seguente illustra come usare l'utilità winrm per abilitare CredSSP nel servizio Gestione remota Windows:

    **winrm set winrm/config/service/auth @{CredSSP="true"}**

3.  L'impostazione del criterio Allow Delegating Fresh Credentials (**AllowFreshCredentials**) deve essere abilitata nel client WinRM e un nome dell'entità servizio (SPN) con il prefisso WSMAN deve essere aggiunto ai criteri. Il nome SPN rappresenta il computer di destinazione a cui è possibile delegare le credenziali utente. Il nome SPN può essere impostato su uno o più computer. La tabella seguente contiene esempi di formati validi per i nomi SPN.

    

    | SPN                                       | Descrizione                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/myComputer.myDomain.com<br/>  | Server Gestione remota Windows in esecuzione myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* .myDomain.com<br/>          | Tutti i server WinRM in esecuzione in myDomain.com.<br/>                               |
    | WSMAN/ \* .fabrikam.myDomain.com<br/> | Tutti i server WinRM in esecuzione in tutti i computer in .fabrikam.myDomain.com.<br/> |

    

     

    Per altre informazioni sull'impostazione di Criteri di gruppo, vedere [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

    Per altre informazioni sui criteri **AllowFreshCredentials,** vedere la descrizione dei criteri fornita dall'editor di Criteri di gruppo e dalla [Knowledge Base 951608](https://support.microsoft.com/kb/951608). Il **criterio AllowFreshCredentials** si trova nel percorso seguente: Configurazione computer Modelli amministrativi \\ delega delle credenziali di \\ \\ sistema.

4.  È necessario configurare [*un listener*](windows-remote-management-glossary.md) HTTPS o HTTP nel server. L'identificazione personale del certificato usata per configurare il *listener* HTTPS viene usata anche per configurare l'impostazione CertificateThumbprint nelle impostazioni del servizio Gestione remota Windows.

    Il comando seguente illustra come usare l'utilità winrm per configurare un [*listener*](windows-remote-management-glossary.md)HTTPS:

    **winrm quickconfig -transport:https**

Se l'autenticazione Kerberos tra il client e il server non è possibile, l'utente deve configurare una delle impostazioni seguenti per il supporto multi hop:

-   Per una maggiore sicurezza, l'utente deve aggiungere **l'attributo CertificateThumbprint** all'impostazione del servizio Gestione remota Windows. Se il servizio Gestione remota Windows è configurato con un **attributo CertificateThumbprint,** il servizio tenta di individuare il certificato corrispondente nell'archivio del computer locale e usa questo certificato per l'autenticazione CredSSP. Se il servizio Gestione remota Windows usa un certificato dall'archivio del computer locale per autenticare il server, all'account del servizio di rete deve essere consentito l'accesso alla chiave privata del certificato.

    > [!Note]  
    > Se l'impostazione del servizio non è configurata, il server Gestione remota Windows usa un certificato autofirmato creato in memoria per crittografare i messaggi inviati al client. Tuttavia, questo certificato non viene usato per l'autenticazione.

     

-   Se non sono disponibili né l'autenticazione Kerberos né l'identificazione personale del certificato, l'utente può abilitare l'autenticazione NTLM. Se si usa l'autenticazione NTLM, è necessario che sia abilitato il criterio Allow Fresh Credentials with NTLM-only Server Authentication (**AllowFreshCredentialsWhenNTLMOnly**) e che al criterio sia aggiunto un nome SPN con il prefisso WSMAN. Questa impostazione è meno sicura dell'autenticazione Kerberos e delle identificazioni personali del certificato, perché le credenziali vengono inviate a un server non autenticato.

    Per altre informazioni sui criteri **AllowFreshCredentialsWhenNTLMOnly,** vedere la descrizione dei criteri fornita dall'editor di Criteri di gruppo e dalla [Knowledge Base 951608](https://support.microsoft.com/kb/951608). Il **criterio AllowFreshCredentialsWhenNTLMOnly** si trova nel percorso seguente: Configurazione computer Modelli amministrativi \\ delega delle credenziali di \\ \\ sistema.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Uso dell'autenticazione CredSSP con credenziali esplicite

Un utente può specificare credenziali esplicite sia su HTTP che su HTTPS. Il comando seguente illustra come usare l'utilità winrm per eseguire un'operazione remota usando l'autenticazione CredSSP con credenziali esplicite su HTTPS:

**winrm OPERATION -remote: https://myMachine -authentication:CredSSP -username:myUsername -password:myPassword**

 

