---
title: Supporto di più hop in WinRM
description: Gestione remota Windows (WinRM) supporta la delega delle credenziali utente tra più computer remoti.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22c3d66e8605e932fe15b812f92d51350da2d69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482805"
---
# <a name="multi-hop-support-in-winrm"></a>Supporto di più hop in WinRM

Gestione remota Windows (WinRM) supporta la delega delle credenziali utente tra più computer remoti. La funzionalità di supporto di più hop ora può usare Credential Security Service Provider (CredSSP) per l'autenticazione. CredSSP consente a un'applicazione di delegare le credenziali dell'utente dal computer client al server di destinazione.

L'autenticazione CredSSP è destinata agli ambienti in cui non è possibile usare la delega Kerberos. È stato aggiunto il supporto per CredSSP per consentire a un utente di connettersi a un server remoto e avere la possibilità di accedere a un computer con un secondo hop, ad esempio una condivisione file.

Per ulteriori informazioni su CredSSP, vedere [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> I client e i server WinRM supporteranno l'autenticazione CredSSP solo con le credenziali esplicite.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Installazione e dettagli della configurazione del supporto multihop

Sono disponibili diversi meccanismi per la configurazione delle impostazioni WinRM. Nella procedura seguente vengono utilizzati l'utilità **WinRM** e l'Editor criteri di gruppo (**gpedit. msc**). CredSSP può essere abilitato anche per WinRM usando Windows PowerShell. Per informazioni dettagliate sulla configurazione e sugli esempi di utilizzo, vedere i cmdlet di Windows PowerShell [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)e [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .

La delega CredSSP deve essere abilitata nelle impostazioni client e nelle impostazioni del servizio nel computer remoto. Inoltre, l'uso di CredSSP richiede la configurazione di un [*listener*](windows-remote-management-glossary.md) http o HTTPS sul server.

**Per configurare il supporto di più hop usando l'autenticazione CredSSP per WinRM**

1.  CredSSP deve essere abilitato nelle impostazioni di configurazione del client. Questo flag può essere abilitato manualmente o tramite un'impostazione Criteri di gruppo. L'impostazione predefinita è **False**. Il criterio di **autenticazione Consenti CredSSP** si trova nel percorso seguente: Configurazione computer \\ modello amministrativo di \\ Windows Components \\ gestione remota Windows (WinRM) \\ WinRM client.

    Il comando seguente illustra come usare l'utilità WinRM per abilitare CredSSP nel client WinRM:

    **winrm set winrm/config/client/auth @ {CredSSP = "true"}**

2.  CredSSP deve essere abilitato nelle impostazioni di configurazione del servizio gestione remota Windows. Questo flag può essere abilitato manualmente o tramite un'impostazione Criteri di gruppo. L'impostazione predefinita è **False**. Il criterio di **autenticazione Consenti CredSSP** si trova nel percorso seguente: Configurazione computer \\ modello amministrativo di \\ Windows Components \\ gestione remota Windows (WinRM) \\ WinRM service.

    Il comando seguente illustra come usare l'utilità WinRM per abilitare CredSSP nel servizio gestione remota Windows:

    **winrm set winrm/config/Service/auth @ {CredSSP = "true"}**

3.  È necessario abilitare l'impostazione dei criteri Consenti delega nuove credenziali (**AllowFreshCredentials**) nel client WinRM ed è necessario aggiungere al criterio un nome dell'entità servizio (SPN) con il prefisso WSMan. Il nome SPN rappresenta il computer di destinazione a cui è possibile delegare le credenziali utente. Il nome SPN può essere impostato su uno o più computer. Nella tabella seguente sono riportati alcuni esempi di formati validi per i nomi SPN.

    

    | SPN                                       | Descrizione                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/nomecomputer. dominio. com<br/>  | Server WinRM in esecuzione in myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* . mydomain.com<br/>          | Tutti i server WinRM in esecuzione in myDomain.com.<br/>                               |
    | WSMAN/ \* . fabrikam.mydomain.com<br/> | Tutti i server WinRM in esecuzione in su tutti i computer in. fabrikam.myDomain.com.<br/> |

    

     

    Per ulteriori informazioni sull'impostazione dei criteri di gruppo, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

    Per ulteriori informazioni sui criteri **AllowFreshCredentials** , vedere la descrizione dei criteri fornita dall'Editor criteri di gruppo e dalla [kb 951608](https://support.microsoft.com/kb/951608). Il criterio **AllowFreshCredentials** si trova nel percorso seguente: configurazione computer \\ modelli amministrativi la \\ delega delle credenziali di sistema \\ .

4.  Nel server deve essere configurato un [*listener*](windows-remote-management-glossary.md) HTTPS o http. L'identificazione personale del certificato utilizzata per la configurazione del *listener* HTTPS viene inoltre utilizzata per configurare l'impostazione CertificateThumbprint nelle impostazioni del servizio gestione remota Windows.

    Il comando seguente illustra come usare l'utilità WinRM per configurare un [*listener*](windows-remote-management-glossary.md)https:

    **quickconfig WinRM-trasporto: https**

Se l'autenticazione Kerberos tra il client e il server non è possibile, l'utente deve configurare una delle impostazioni seguenti per il supporto di più hop:

-   Per una maggiore sicurezza, l'utente deve aggiungere l'attributo **CertificateThumbprint** all'impostazione del servizio gestione remota Windows. Se il servizio WinRM è configurato con un attributo **CertificateThumbprint** , il servizio tenterà di individuare il certificato corrispondente nell'archivio del computer locale e utilizzerà il certificato per l'autenticazione CredSSP. Se il servizio WinRM utilizza un certificato dell'archivio del computer locale per autenticare il server, l'account del servizio di rete deve essere autorizzato ad accedere alla chiave privata del certificato.

    > [!Note]  
    > Se l'impostazione del servizio non è configurata, il server WinRM utilizza un certificato autofirmato creato in memoria per crittografare i messaggi inviati al client. Questo certificato, tuttavia, non viene utilizzato per l'autenticazione.

     

-   Se l'autenticazione Kerberos e le identificazioni personali del certificato non sono disponibili, l'utente può abilitare l'autenticazione NTLM. Se viene utilizzata l'autenticazione NTLM, è necessario che il criterio Consenti credenziali aggiornate con autenticazione server solo NTLM (**AllowFreshCredentialsWhenNTLMOnly**) sia abilitato e che al criterio venga aggiunto un nome SPN con il prefisso WSMan. Questa impostazione è meno sicura dell'autenticazione Kerberos e delle identificazioni personali del certificato, perché le credenziali vengono inviate a un server non autenticato.

    Per ulteriori informazioni sui criteri **AllowFreshCredentialsWhenNTLMOnly** , vedere la descrizione dei criteri fornita dall'Editor criteri di gruppo e dalla [kb 951608](https://support.microsoft.com/kb/951608). Il criterio **AllowFreshCredentialsWhenNTLMOnly** si trova nel percorso seguente: configurazione computer \\ modelli amministrativi la \\ delega delle credenziali di sistema \\ .

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Uso dell'autenticazione CredSSP con le credenziali esplicite

Un utente può specificare le credenziali esplicite sia per HTTP che per HTTPS. Il comando seguente illustra come usare l'utilità WinRM per eseguire un'operazione remota usando l'autenticazione CredSSP con le credenziali esplicite su HTTPS:

**OPERAZIONE WinRM-Remote: https://myMachine -Authentication: CredSSP-username: nome utente-password: password**

 

