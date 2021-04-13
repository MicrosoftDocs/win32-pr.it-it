---
description: Per la connessione a uno spazio dei nomi WMI in un computer remoto potrebbe essere necessario modificare le impostazioni di Windows Firewall, controllo dell'account utente (UAC), DCOM o Common Information Model Object Manager (CIMOM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configurazione di una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528615"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configurazione di una connessione WMI remota

Per la connessione a uno spazio dei nomi WMI in un computer remoto potrebbe essere necessario modificare le impostazioni di [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM o Common Information Model Object Manager (CIMOM).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Impostazioni Windows Firewall](#windows-firewall-settings)
-   [Impostazioni di Controllo dell'account utente](#user-account-control-settings)
-   [Impostazioni DCOM](#dcom-settings)
-   [Impostazioni CIMOM](#cimom-settings)
-   [Argomenti correlati](#related-topics)

## <a name="windows-firewall-settings"></a>Impostazioni di Windows Firewall

Le impostazioni WMI per Windows Firewall impostazioni abilitano solo le connessioni WMI, anziché altre applicazioni DCOM.

È necessario impostare un'eccezione nel firewall per WMI nel computer di destinazione remoto. L'eccezione per WMI consente a WMI di ricevere connessioni remote e callback asincroni per Unsecapp.exe. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

Se un'applicazione client crea un sink personalizzato, è necessario aggiungerlo esplicitamente alle eccezioni del firewall per consentire la riuscita dei callback.

L'eccezione per WMI funziona anche se WMI è stato avviato con una porta fissa, usando il comando **winmgmt/standalonehost** . Per ulteriori informazioni, vedere [configurazione di una porta fissa per WMI](setting-up-a-fixed-port-for-wmi.md).

È possibile abilitare o disabilitare il traffico WMI tramite l'interfaccia utente di Windows Firewall.

**Per abilitare o disabilitare il traffico WMI mediante l'interfaccia utente del firewall**

1.  Nel **Pannello di controllo** fare clic su **sicurezza** e quindi su **Windows Firewall**.
2.  Fare clic su **Cambia impostazioni** , quindi fare clic sulla scheda **eccezioni** .
3.  Nella finestra eccezioni selezionare la casella di controllo **Strumentazione gestione Windows (WMI)** per abilitare il traffico WMI attraverso il firewall. Per disabilitare il traffico WMI, deselezionare la casella di controllo.

È possibile abilitare o disabilitare il traffico WMI attraverso il firewall al prompt dei comandi.

**Per abilitare o disabilitare il traffico WMI al prompt dei comandi utilizzando il gruppo di regole WMI**

-   Usare i comandi seguenti al prompt dei comandi. Digitare quanto segue per abilitare il traffico WMI attraverso il firewall.

    **netsh advfirewall firewall set Rule Group = "Strumentazione gestione Windows (WMI)" nuovo enable = Yes**

    Digitare il comando seguente per disabilitare il traffico WMI attraverso il firewall.

    **netsh advfirewall firewall set Rule Group = "Strumentazione gestione Windows (WMI)" nuovo Enable = no**

Anziché utilizzare il singolo comando del gruppo di regole WMI, è possibile utilizzare i singoli comandi per ogni DCOM, servizio WMI e sink.

**Per abilitare il traffico WMI con regole separate per DCOM, WMI, il sink di callback e le connessioni in uscita**

1.  Per stabilire un'eccezione del firewall per la porta DCOM 135, usare il comando seguente.

    **netsh advfirewall firewall add rule dir = in Name = "DCOM" Program =% SystemRoot% \\ system32 \\svchost.exe Service = RPCSS action = allow Protocol = TCP LocalPort = 135**

2.  Per stabilire un'eccezione del firewall per il servizio WMI, utilizzare il comando seguente.

    **netsh advfirewall firewall add rule dir = in Name = "WMI" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt action = allow Protocol = TCP LocalPort = any**

3.  Per stabilire un'eccezione del firewall per il sink che riceve i callback da un computer remoto, usare il comando seguente.

    **netsh advfirewall firewall add rule dir = in Name = "UnsecApp" Program =% SystemRoot% \\ system32 \\ WBEM \\unsecapp.exe action = allow**

4.  Per stabilire un'eccezione del firewall per le connessioni in uscita a un computer remoto con cui il computer locale comunica in modo asincrono, utilizzare il comando seguente.

    **netsh advfirewall firewall add rule dir = out Name = "WMI \_ out" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt action = allow Protocol = TCP LocalPort = any**

Per disabilitare le eccezioni del firewall separatamente, usare i comandi seguenti.

**Per disabilitare il traffico WMI con regole separate per DCOM, WMI, il sink di callback e le connessioni in uscita**

1.  Per disabilitare l'eccezione DCOM.

    **netsh advfirewall firewall delete rule name = "DCOM"**

2.  Per disabilitare l'eccezione del servizio WMI.

    **netsh advfirewall firewall delete rule name = "WMI"**

3.  Per disabilitare l'eccezione del sink.

    **netsh advfirewall firewall delete rule name = "UnsecApp"**

4.  Per disabilitare l'eccezione in uscita.

    **netsh advfirewall firewall delete rule name = "WMI \_ out"**

## <a name="user-account-control-settings"></a>Impostazioni di Controllo dell'account utente

Controllo dell'account utente (UAC) l'applicazione di filtri ai token può influire sulle operazioni consentite negli spazi dei nomi WMI o sui dati restituiti. In controllo dell'account utente, tutti gli account nel gruppo Administrators locale vengono eseguiti con un [*token di accesso*](/windows/desktop/SecGloss/a-gly)utente standard, noto anche come filtro di accesso del controllo dell'account utente. Un account amministratore può eseguire uno script con privilegi elevati, ovvero "Esegui come amministratore".

Quando non ci si connette all'account Administrator predefinito, il controllo dell'account utente influiscono sulle connessioni a un computer remoto in modo diverso a seconda che i due computer si trovino in un dominio o in un gruppo di lavoro. Per ulteriori informazioni su UAC e connessioni remote, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).

## <a name="dcom-settings"></a>Impostazioni DCOM

Per ulteriori informazioni sulle impostazioni DCOM, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md). Tuttavia, UAC influiscono sulle connessioni per gli account utente non di dominio. Se ci si connette a un computer remoto usando un account utente non di dominio incluso nel gruppo Administrators locale del computer remoto, è necessario concedere in modo esplicito l'accesso DCOM remoto, l'attivazione e i diritti di avvio per l'account.

## <a name="cimom-settings"></a>Impostazioni CIMOM

Se la connessione remota è tra computer che non hanno una relazione di trust, è necessario aggiornare le impostazioni CIMOM. in caso contrario, la connessione asincrona avrà esito negativo. Questa impostazione non deve essere modificata per i computer nello stesso dominio o in domini trusted.

La seguente voce del registro di sistema deve essere modificata per consentire callback anonimi:

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Se il valore **AllowAnonymousCallback** è impostato su 0, il servizio WMI impedisce i callback anonimi al client. Se il valore è impostato su 1, il servizio WMI consente callback anonimi al client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
