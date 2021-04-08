---
title: Autenticazione per le connessioni remote
description: Gestione remota Windows mantiene la sicurezza per la comunicazione tra i computer, supportando diversi metodi standard di autenticazione e crittografia dei messaggi.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e9aa125f2ccf5d8c224eee645a6dba1ec2fd96e
ms.sourcegitcommit: 25c6d442ab55cbf0e065398a006b1d409349fffd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2020
ms.locfileid: "104046447"
---
# <a name="authentication-for-remote-connections"></a>Autenticazione per le connessioni remote

Gestione remota Windows mantiene la sicurezza per la comunicazione tra i computer, supportando diversi metodi standard di autenticazione e crittografia dei messaggi.

## <a name="default-group-access"></a>Accesso al gruppo predefinito

Durante l'installazione, WinRM crea il gruppo **locale \_ \_ WinRMRemoteWMIUsers**. WinRM limita quindi l'accesso remoto a tutti gli utenti che non sono membri del gruppo di amministrazione locale o del gruppo **WinRMRemoteWMIUsers \_ \_** . È possibile aggiungere un utente locale, un utente di dominio o un gruppo di dominio a **WinRMRemoteWMIUsers \_ \_** digitando **net localgroup WinRMRemoteWMIUsers \_ \_ /Add <domain> \\ <username>** al prompt dei comandi. Facoltativamente, è possibile utilizzare il Criteri di gruppo per aggiungere un utente al gruppo.

## <a name="default-authentication-settings"></a>Impostazioni di autenticazione predefinite

Le credenziali predefinite, il nome utente e la password sono le credenziali per l'account utente connesso che esegue lo script.

**Per passare a un altro account in un computer remoto**

1.  Specificare le credenziali in un oggetto [**ConnectionOptions**](connectionoptions.md) o [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) e fornirle alla chiamata [**CreateSession**](wsman-createsession.md) .
2.  Impostare **WSManFlagCredUserNamePassword** nel parametro *Flags* della chiamata [**CreateSession**](wsman-createsession.md) .

Nell'elenco seguente è incluso un elenco di ciò che accade quando uno script o un'applicazione viene eseguita con le credenziali predefinite:

-   [*Kerberos*](windows-remote-management-glossary.md) è il metodo di autenticazione predefinito quando il client si trova in un dominio e la stringa di destinazione remota non è una delle seguenti: localhost, 127.0.0.1 o \[ :: 1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) è il metodo predefinito quando il client non si trova in un dominio, ma la stringa di destinazione remota è una delle seguenti: localhost, 127.0.0.1 o \[ :: 1 \] .

Se si specificano credenziali esplicite con un oggetto [**ConnectionOptions**](connectionoptions.md) , Negotiate è il metodo predefinito. L'autenticazione Negotiate determina se il metodo di autenticazione in corso è Kerberos o NTLM, a seconda che i computer si trovino in un dominio o in un gruppo di lavoro. Se ci si connette a un computer di destinazione remoto usando un account locale, l'account deve essere preceduto dal nome del computer. Ad esempio, nomecomputer \\ utente.

Se si specifica l'autenticazione Negotiate, digest o Basic e non si fornisce un oggetto [**ConnectionOptions**](connectionoptions.md) , verrà visualizzato un errore che indica che sono necessarie credenziali esplicite. Se HTTPS non è il trasporto, il computer remoto di destinazione deve essere configurato nell'elenco dei computer host attendibili.

Per ulteriori informazioni sui tipi di autenticazione abilitati nelle impostazioni di configurazione predefinite, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="basic-authentication"></a>Autenticazione di base

Per stabilire in modo esplicito l'autenticazione di [*base*](windows-remote-management-glossary.md) nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md), impostare i flag **WSManFlagUseBasic** e **WSManFlagCredUserNamePassword** nel parametro *Flags* . L'autenticazione di base è disabilitata nelle impostazioni di configurazione predefinite sia per il client WinRM che per il server WinRM.

## <a name="digest-authentication"></a>Autenticazione del digest

Per stabilire in modo esplicito l'autenticazione del [*digest*](windows-remote-management-glossary.md) nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md), impostare il flag **WSManFlagUseDigest** nel parametro *Flags* . Il digest non è supportato. Non può essere configurato per il componente server WinRM.

## <a name="negotiate-authentication"></a>Negozia autenticazione

Per stabilire in modo esplicito l'autenticazione di [*negoziazione*](windows-remote-management-glossary.md) , nota anche come autenticazione integrata di Windows, nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md)impostare il flag **WSManFlagUseNegotiate** nel parametro *Flags* .

Il [controllo dell'account utente (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) influiscono sull'accesso al servizio WinRM. Quando si usa l'autenticazione Negotiate in un gruppo di lavoro, solo l'account Administrator predefinito può accedere al servizio. Per consentire a tutti gli account del gruppo Administrators di accedere al servizio, impostare il valore del registro di sistema seguente:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Autenticazione Kerberos

Per stabilire in modo esplicito l'autenticazione [*Kerberos*](windows-remote-management-glossary.md) nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md), impostare il flag **WSManFlagUseKerberos** nel parametro *Flags* . Il client e i computer server devono essere aggiunti a un dominio. Se si usa Kerberos come metodo di autenticazione, non è possibile usare un indirizzo IP nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md) o [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Autenticazione basata su certificati client

Per stabilire l'autenticazione basata sui certificati client nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md), impostare il flag **WSManFlagUseClientCertificate** nel parametro *Flags* .

Per prima cosa, è necessario abilitare l'autenticazione del certificato nel client e nel servizio usando lo strumento da riga di comando WinRM. Per ulteriori informazioni, vedere [Abilitazione delle opzioni di autenticazione](#enabling-or-disabling-authentication-options). È inoltre necessario creare una voce nella tabella mapping certificato nel computer server WinRM. Viene stabilito un mapping tra uno o più certificati e un account locale. Dopo che il certificato è stato utilizzato per l'autenticazione e l'autorizzazione, l'account locale corrispondente viene utilizzato per le operazioni eseguite dal servizio WinRM.

Il mapping può essere creato per un URI di risorsa specifico. Per ulteriori informazioni, tra cui come creare una voce di tabella mapping certificato, digitare **winrm help mapping certificato** al prompt dei comandi.

> [!Note]  
> Il certificato di dimensione massima utilizzabile da WinRM in questo contesto è 16KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Abilitazione o disabilitazione delle opzioni di autenticazione

L'opzione di autenticazione predefinita nell'installazione del sistema è Kerberos. Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

Se lo script o l'applicazione richiede un metodo di autenticazione specifico che non è abilitato, è necessario modificare la configurazione per abilitare questo tipo di autenticazione. Questa modifica può essere eseguita utilizzando lo strumento da riga di comando **WinRM** o tramite criteri di gruppo per l' **oggetto gestione remota Windows Criteri di gruppo**. Si può anche scegliere di disabilitare determinati metodi di autenticazione.

**Per abilitare o disabilitare l'autenticazione con lo strumento WinRM**

1.  Per impostare la configurazione per il client WinRM, utilizzare il comando **winrm set** e specificare il client. Ad esempio, il comando seguente disabilita l'autenticazione del digest per il client.

    **winrm set winrm/config/client/auth @ {digest = "false"}**

2.  Per impostare la configurazione per il server WinRM, utilizzare il comando **winrm set** e specificare il servizio. Il comando seguente, ad esempio, consente di abilitare l'autenticazione Kerberos per il servizio.

    **winrm set winrm/config/Service/auth @ {Kerberos = "true"}**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> </dl>

 

 




