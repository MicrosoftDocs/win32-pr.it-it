---
title: Autenticazione per connessioni remote
description: Windows Gestione remota mantiene la sicurezza per la comunicazione tra computer supportando diversi metodi standard di autenticazione e crittografia dei messaggi.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0622f3d80e923f7d910740c71ee99f0e9a0bc446cea259b292e2d645e3b5a973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858877"
---
# <a name="authentication-for-remote-connections"></a>Autenticazione per connessioni remote

Windows Gestione remota mantiene la sicurezza per la comunicazione tra computer supportando diversi metodi standard di autenticazione e crittografia dei messaggi.

## <a name="default-group-access"></a>Accesso predefinito ai gruppi

Durante l'installazione, WinRM crea il gruppo **locale \_ \_ WinRMRemoteWMIUsers**. WinRM limita quindi l'accesso remoto a qualsiasi utente che non sia membro del gruppo di amministrazione locale o **del gruppo \_ \_ WinRMRemoteWMIUsers.** È possibile aggiungere un utente locale, un utente di dominio o un gruppo di dominio a **\_ \_ WinRMRemoteWMIUsers** digitando **net localgroup WinRMRemoteWMIUsers \_ \_ /add <domain> \\ <username>** al prompt dei comandi. Facoltativamente, è possibile usare il Criteri di gruppo per aggiungere un utente al gruppo.

## <a name="default-authentication-settings"></a>Autenticazione predefinita Impostazioni

Le credenziali predefinite, il nome utente e la password sono le credenziali per l'account utente connesso che esegue lo script.

**Per passare a un altro account in un computer remoto**

1.  Specificare le credenziali in un [**oggetto ConnectionOptions**](connectionoptions.md) o [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) e fornirne le credenziali alla [**chiamata CreateSession.**](wsman-createsession.md)
2.  Impostare **WSManFlagCredUserNamePassword** nel *parametro flags* nella chiamata [**CreateSession.**](wsman-createsession.md)

L'elenco seguente contiene un elenco di ciò che accade quando uno script o un'applicazione viene eseguita con le credenziali predefinite:

-   [*Kerberos*](windows-remote-management-glossary.md) è il metodo di autenticazione predefinito quando il client si trova in un dominio e la stringa di destinazione remota non è una delle seguenti: localhost, 127.0.0.1 o \[ ::1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) è il metodo predefinito quando il client non si trova in un dominio, ma la stringa di destinazione remota è una delle seguenti: localhost, 127.0.0.1 o \[ ::1 \] .

Se si forniscono credenziali esplicite con un [**oggetto ConnectionOptions,**](connectionoptions.md) Negotiate è il metodo predefinito. L'autenticazione con negoziazione determina se il metodo di autenticazione in corso è Kerberos o NTLM, a seconda che i computer siano in un dominio o in un gruppo di lavoro. Se ci si connette a un computer di destinazione remoto usando un account locale, l'account deve essere preceduto dal nome del computer. Ad esempio, myComputer \\ myUsername.

Se si specifica l'autenticazione Negotiate, Digest o Basic e non si specifica un oggetto [**ConnectionOptions,**](connectionoptions.md) verrà visualizzato un errore che indica che sono necessarie credenziali esplicite. Se HTTPS non è il trasporto, il computer remoto di destinazione deve essere configurato nell'elenco dei computer host attendibili.

Per altre informazioni sui tipi di autenticazione abilitati nelle impostazioni di configurazione predefinite, vedere [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

## <a name="basic-authentication"></a>Autenticazione di base

Per stabilire [](windows-remote-management-glossary.md) in modo esplicito l'autenticazione di base nella chiamata a [**WSMan.CreateSession,**](wsman-createsession.md)impostare i flag **WSManFlagUseBasic** e **WSManFlagCredUserNamePassword** nel parametro *flags.* L'autenticazione di base è disabilitata nelle impostazioni di configurazione predefinite sia per il client WinRM che per il server WinRM.

## <a name="digest-authentication"></a>Autenticazione del digest

Per stabilire in modo [*esplicito*](windows-remote-management-glossary.md) l'autenticazione digest nella chiamata a [**WSMan.CreateSession,**](wsman-createsession.md)impostare il flag **WSManFlagUseDigest** nel *parametro flags.* Il digest non è supportato. Non può essere configurato per il componente server WinRM.

## <a name="negotiate-authentication"></a>Negoziazione dell'autenticazione

Per stabilire [](windows-remote-management-glossary.md) in modo esplicito l'autenticazione negotiate, nota anche come autenticazione integrata di Windows, nella chiamata a [**WSMan.CreateSession**](wsman-createsession.md)impostare il flag **WSManFlagUseNegotiate** nel parametro *flags.*

[Controllo dell'account utente influisce sull'accesso](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) al servizio Gestione remota Windows. Quando l'autenticazione Negotiate viene usata in un gruppo di lavoro, solo l'account Administrator predefinito può accedere al servizio. Per consentire a tutti gli account del gruppo Administrators di accedere al servizio, impostare il valore del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Autenticazione Kerberos

Per stabilire in modo esplicito l'autenticazione [*Kerberos*](windows-remote-management-glossary.md) nella chiamata a [**WSMan.CreateSession,**](wsman-createsession.md)impostare il flag **WSManFlagUseKerberos** nel *parametro flags.* Sia il client che i computer server devono essere aggiunti a un dominio. Se si usa Kerberos come metodo di autenticazione, non è possibile usare un indirizzo IP nella chiamata a [**WSMan.CreateSession**](wsman-createsession.md) o [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Autenticazione basata su certificati client

Per stabilire l'autenticazione basata su certificati client nella chiamata a [**WSMan.CreateSession,**](wsman-createsession.md)impostare il flag **WSManFlagUseClientCertificate** nel *parametro flags.*

È prima necessario abilitare l'autenticazione del certificato sia nel client che nel servizio usando lo strumento da riga di comando Winrm. Per altre informazioni, vedere [Abilitazione delle opzioni di autenticazione.](#enabling-or-disabling-authentication-options) È anche necessario creare una voce nella tabella CertMapping nel computer server WinRM. In questo modo viene stabilito un mapping tra uno o più certificati e un account locale. Dopo che il certificato è stato usato per l'autenticazione e l'autorizzazione, l'account locale corrispondente viene usato per le operazioni eseguite dal servizio Gestione remota Windows.

Il mapping può essere creato per un URI di risorsa specifico. Per altre informazioni, tra cui come creare una voce di tabella CertMapping, digitare **winrm help certmapping** al prompt dei comandi.

> [!Note]  
> Il certificato di dimensione massima utilizzabile da WinRM in questo contesto è 16 KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Abilitazione o disabilitazione delle opzioni di autenticazione

L'opzione di autenticazione predefinita al momento dell'installazione del sistema è Kerberos. Per altre informazioni, vedere [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

Se lo script o l'applicazione richiede un metodo di autenticazione specifico non abilitato, è necessario modificare la configurazione per abilitare questo tipo di autenticazione. Questa modifica può essere apportata tramite lo strumento da riga di comando **Winrm** o tramite Criteri di gruppo per l'oggetto Windows **gestione remota Criteri di gruppo remoto**. È anche possibile scegliere di disabilitare determinati metodi di autenticazione.

**Per abilitare o disabilitare l'autenticazione con lo strumento Winrm**

1.  Per impostare la configurazione per il client WinRM, usare il **comando Winrm Set** e specificare il client. Ad esempio, il comando seguente disabilita l'autenticazione del digest per il client.

    **winrm set winrm/config/client/auth @{Digest="false"}**

2.  Per impostare la configurazione per il server WinRM, usare il **comando Winrm Set** e specificare il servizio. Ad esempio, il comando seguente abilita l'autenticazione Kerberos per il servizio.

    **winrm set winrm/config/service/auth @{Kerberos="true"}**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> </dl>

 

 




