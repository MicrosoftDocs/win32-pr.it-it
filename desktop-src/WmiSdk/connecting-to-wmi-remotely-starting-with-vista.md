---
description: Per la connessione a uno spazio dei nomi WMI in un computer remoto potrebbe essere necessario modificare le impostazioni per Windows Firewall, Controllo dell'account utente, DCOM o Common Information Model Object Manager (CIMOM).
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
ms.openlocfilehash: b88aa453646e60bf17e31f1197d76506bb4f75453eb800dc0fa272946a3bf8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925703"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configurazione di una connessione WMI remota

La connessione a uno spazio dei nomi WMI in un computer remoto può richiedere la modifica delle impostazioni per [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), Controllo [dell'account](/previous-versions/aa905108(v=msdn.10))utente , DCOM o Common Information Model Object Manager (CIMOM).

In questo argomento vengono illustrate le sezioni seguenti:

-   [Windows Firewall Impostazioni](#windows-firewall-settings)
-   [Impostazioni di Controllo dell'account utente](#user-account-control-settings)
-   [DCOM Impostazioni](#dcom-settings)
-   [CiMOM Impostazioni](#cimom-settings)
-   [Argomenti correlati](#related-topics)

## <a name="windows-firewall-settings"></a>Impostazioni di Windows Firewall

Le impostazioni WMI per Windows firewall abilitano solo le connessioni WMI, anziché altre applicazioni DCOM.

È necessario impostare un'eccezione nel firewall per WMI nel computer di destinazione remoto. L'eccezione per WMI consente a WMI di ricevere connessioni remote e callback asincroni Unsecapp.exe. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

Se un'applicazione client crea un proprio sink, tale sink deve essere aggiunto in modo esplicito alle eccezioni del firewall per consentire l'esito positivo dei callback.

L'eccezione per WMI funziona anche se WMI è stato avviato con una porta fissa, usando il **comando winmgmt /standalonehost.** Per altre informazioni, vedere [Impostazione di una porta fissa per WMI.](setting-up-a-fixed-port-for-wmi.md)

È possibile abilitare o disabilitare il traffico WMI tramite l'interfaccia Windows'interfaccia utente del firewall.

**Per abilitare o disabilitare il traffico WMI tramite l'interfaccia utente del firewall**

1.  Nel **Pannello di controllo** fare clic su **Sicurezza** e quindi su **Windows Firewall**.
2.  Fare **clic Impostazioni** modifica e quindi sulla **scheda** Eccezioni .
3.  Nella finestra Eccezioni selezionare la casella di controllo Windows **Management Instrumentation (WMI) per** abilitare il traffico WMI attraverso il firewall. Per disabilitare il traffico WMI, deselezionare la casella di controllo.

È possibile abilitare o disabilitare il traffico WMI attraverso il firewall al prompt dei comandi.

**Per abilitare o disabilitare il traffico WMI al prompt dei comandi usando il gruppo di regole WMI**

-   Usare i comandi seguenti al prompt dei comandi. Digitare quanto segue per abilitare il traffico WMI attraverso il firewall.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**

    Digitare il comando seguente per disabilitare il traffico WMI attraverso il firewall.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**

Anziché usare il singolo comando del gruppo di regole WMI, è anche possibile usare singoli comandi per ogni DCOM, servizio WMI e sink.

**Per abilitare il traffico WMI usando regole separate per DCOM, WMI, sink di callback e connessioni in uscita**

1.  Per stabilire un'eccezione del firewall per la porta DCOM 135, usare il comando seguente.

    **netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot% \\ system32 \\svchost.exe service=rpcss action=allow protocol=TCP localport=135**

2.  Per stabilire un'eccezione del firewall per il servizio WMI, usare il comando seguente.

    **netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**

3.  Per stabilire un'eccezione del firewall per il sink che riceve callback da un computer remoto, usare il comando seguente.

    **netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot% \\ system32 \\ wbem \\unsecapp.exe action=allow**

4.  Per stabilire un'eccezione del firewall per le connessioni in uscita a un computer remoto con cui il computer locale comunica in modo asincrono, usare il comando seguente.

    **netsh advfirewall firewall add rule dir=out name ="WMI \_ OUT" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**

Per disabilitare separatamente le eccezioni del firewall, usare i comandi seguenti.

**Per disabilitare il traffico WMI usando regole separate per DCOM, WMI, sink di callback e connessioni in uscita**

1.  Per disabilitare l'eccezione DCOM.

    **netsh advfirewall firewall delete rule name="DCOM"**

2.  Per disabilitare l'eccezione del servizio WMI.

    **netsh advfirewall firewall delete rule name="WMI"**

3.  Per disabilitare l'eccezione sink.

    **netsh advfirewall firewall delete rule name="UnsecApp"**

4.  Per disabilitare l'eccezione in uscita.

    **netsh advfirewall firewall delete rule name="WMI \_ OUT"**

## <a name="user-account-control-settings"></a>Impostazioni di Controllo dell'account utente

Il filtro dei token di accesso di Controllo dell'account utente può influire sulle operazioni consentite negli spazi dei nomi WMI o sui dati restituiti. In Controllo dell'account utente tutti gli account nel gruppo Administrators locale vengono eseguiti con un [*token*](/windows/desktop/SecGloss/a-gly)di accesso utente standard, noto anche come filtro dei token di accesso di Controllo dell'account utente. Un account amministratore può eseguire uno script con privilegi elevati: "Esegui come amministratore".

Quando non ci si connette all'account administrator predefinito, controllo dell'account utente influisce sulle connessioni a un computer remoto in modo diverso a seconda che i due computer si uniranno a un dominio o a un gruppo di lavoro. Per altre informazioni sul controllo dell'account utente e sulle connessioni remote, vedere [Controllo dell'account utente e WMI.](user-account-control-and-wmi.md)

## <a name="dcom-settings"></a>DCOM Impostazioni

Per altre informazioni sulle impostazioni DCOM, vedere [Protezione di una connessione WMI remota.](securing-a-remote-wmi-connection.md) Tuttavia, Controllo dell'account utente influisce sulle connessioni per gli account utente non di dominio. Se ci si connette a un computer remoto usando un account utente non di dominio incluso nel gruppo Administrators locale del computer remoto, è necessario concedere esplicitamente diritti di accesso, attivazione e avvio DCOM remoto all'account.

## <a name="cimom-settings"></a>CiMOM Impostazioni

Le impostazioni CIMOM devono essere aggiornate se la connessione remota è tra computer che non hanno una relazione di trust. In caso contrario, una connessione asincrona avrà esito negativo. Questa impostazione non deve essere modificata per i computer nello stesso dominio o in domini trusted.

La voce del Registro di sistema seguente deve essere modificata per consentire i callback anonimi:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Se il **valore AllowAnonymousCallback** è impostato su 0, il servizio WMI impedisce i callback anonimi al client. Se il valore è impostato su 1, il servizio WMI consente callback anonimi al client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
