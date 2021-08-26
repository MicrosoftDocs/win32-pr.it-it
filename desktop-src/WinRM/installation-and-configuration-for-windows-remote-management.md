---
title: 'Installazione e configurazione per Gestione remota Windows '
description: Per Windows script di gestione remota (WinRM) da eseguire e per lo strumento da riga di comando **Winrm** per eseguire operazioni sui dati, è necessario installare e configurare Windows Gestione remota Windows (WinRM).
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: c031ad9b9d9c888385527c227b102c64bb4dfb65eaea340e52eac3fb9595e591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997621"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Installazione e configurazione per Windows gestione remota

Per Windows script di gestione remota (WinRM) da eseguire e per lo strumento da riga di comando **Winrm** per eseguire operazioni sui dati, è necessario installare e configurare Windows Gestione remota Windows (WinRM).

Questi elementi dipendono anche dalla configurazione di Gestione remota Windows.

- Lo Windows della riga di comando [di Remote Shell](./windows-remote-management-glossary.md#w) (**Winrs**).
- [Inoltro di eventi](./windows-remote-management-glossary.md#e).
- Windows PowerShell remota di Windows PowerShell 2.0.

## <a name="where-winrm-is-installed"></a>Posizione in cui è installato WinRM

WinRM viene installato automaticamente con tutte le versioni attualmente supportate del Windows operativo.

## <a name="configuration-of-winrm-and-ipmi"></a>Configurazione di WinRM e IPMI

Questi componenti del [provider WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WinRM [e Intelligent Platform Management Interface (IPMI)](./windows-remote-management-glossary.md#i) vengono installati con il sistema operativo.

- Il servizio Gestione remota Windows viene avviato automaticamente in Windows Server 2008 e versioni seguenti (in Windows Vista è necessario avviare il servizio manualmente).
- Per impostazione predefinita, non è configurato [alcun listener](./windows-remote-management-glossary.md#l) WinRM. Anche se il servizio Gestione remota Windows [](./windows-remote-management-glossary.md#m) è in esecuzione, WS-Management di protocollo che richiedono dati non possono essere ricevuti né inviati.
- Internet Connection Firewall (ICF) blocca l'accesso alle porte.

Usare il **comando Winrm** per individuare i listener e gli indirizzi digitando il comando seguente al prompt dei comandi.

```console
winrm e winrm/config/listener
```

Per controllare lo stato delle impostazioni di configurazione, digitare il comando seguente.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Configurazione rapida predefinita

È possibile abilitare il WS-Management nel computer locale e configurare la configurazione predefinita per la gestione remota con il comando `winrm quickconfig` .

Il `winrm quickconfig` comando (o la versione abbreviata `winrm qc` ) esegue queste operazioni.

- Avvia il servizio Gestione remota Windows e imposta il tipo di avvio del servizio su avvio automatico.
- Configura un listener per le porte che inviano e ricevono WS-Management di protocollo [usando](./windows-remote-management-glossary.md#m) HTTP o HTTPS in qualsiasi indirizzo IP.
- Definisce le eccezioni ICF per il servizio Gestione remota Windows e apre le porte per HTTP e HTTPS.

> [!NOTE]
> Il `winrm quickconfig` comando crea un'eccezione del firewall solo per il profilo utente corrente. Se il profilo del firewall viene modificato per qualsiasi motivo, è necessario eseguire per abilitare l'eccezione del firewall per il nuovo profilo. In caso contrario, l'eccezione `winrm quickconfig` potrebbe non essere abilitata.

Per recuperare informazioni sulla personalizzazione di una configurazione, digitare `winrm help config` al prompt dei comandi.

### <a name="to-configure-winrm-with-default-settings"></a>Per configurare WinRM con le impostazioni predefinite

1. Digitare `winrm quickconfig` al prompt dei comandi.

   Se non si esegue con l'account Administrator del  computer locale, è necessario selezionare Esegui come amministratore dal menu **Start** oppure usare il comando **Runas** al prompt dei comandi.

2. Quando lo strumento visualizza **apportare queste \[ modifiche y/n \] ?**, digitare **y**.

   Se la configurazione ha esito positivo, viene visualizzato l'output seguente.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Mantenere le impostazioni predefinite per i componenti client e server di Gestione remota Windows o personalizzarle. Ad esempio, potrebbe essere necessario aggiungere determinati computer remoti all'elenco TrustedHosts di configurazione client.

   È consigliabile configurare un elenco di host attendibili quando non è possibile stabilire l'autenticazione reciproca. Kerberos consente l'autenticazione reciproca, ma non può essere usato solo nei gruppi di &mdash; lavoro. Una procedura consigliata quando si configurano host attendibili per un gruppo di lavoro consiste nel rendere l'elenco il più limitato possibile.

4. Creare un listener HTTPS digitando il comando `winrm quickconfig -transport:https` . Tenere presente che è necessario aprire la porta 5986 per il funzionamento del trasporto HTTPS.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Impostazioni predefinite del WS-Management listener e del protocollo

Per ottenere la configurazione del listener, digitare `winrm enumerate winrm/config/listener` al prompt dei comandi. I listener sono definiti da un trasporto (HTTP o HTTPS) e da un indirizzo IPv4 o IPv6.

`winrm quickconfig` crea le impostazioni predefinite seguenti per un listener. È possibile creare più listener. Per altre informazioni, digitare `winrm help config` al prompt dei comandi.

### <a name="address"></a>Indirizzo

Specifica l'indirizzo per cui è stato creato il listener.

### <a name="transport"></a>Trasporto

Specifica il trasporto da usare per inviare e ricevere richieste e risposte del protocollo WS-Management. Il valore deve essere *HTTP* o *HTTPS.* Il valore predefinito è *HTTP.*

### <a name="port"></a>Porta

Specifica la porta TPC per cui viene creato il listener.

**WinRM 2.0:** La porta HTTP predefinita è 5985.

### <a name="hostname"></a>Nome host

Specifica il nome host del computer in cui è in esecuzione il servizio Gestione remota Windows. Il valore deve essere un nome di dominio completo, una stringa letterale IPv4 o IPv6 o un carattere jolly.

### <a name="enabled"></a>Attivato

Specifica se il listener è abilitato o disabilitato. Il valore predefinito è *True*.

### <a name="urlprefix"></a>URLPrefix

Specifica un prefisso URL in base al quale accettare richieste HTTP o HTTPS. Si tratta di una stringa contenente solo i caratteri a-z, A-Z, 9-0, il carattere di sottolineatura ( \_ ) e la barra (/). La stringa non deve iniziare con o terminare con una barra (/). Ad esempio, se il nome del computer è SampleMachine, il client WinRM specifica https://SampleMachine/< *URLPrefix*> nell'indirizzo di destinazione. Il prefisso URL predefinito è "wsman".

### <a name="certificatethumbprint"></a>CertificateThumbprint

Specifica l'identificazione personale del certificato del servizio. Questo valore rappresenta una stringa di valori esadecimali a due cifre trovati nel campo Identificazione personale del certificato. Questa stringa contiene l'hash SHA-1 del certificato. I certificati vengono usati nell'autenticazione basata sui certificati client. I certificati possono essere mappati solo agli account utente locali e non funzionano con gli account di dominio.

### <a name="listeningon"></a>ListeningOn

Specifica gli indirizzi IPv4 e IPv6 utilizzati dal listener. Ad esempio: "111.0.0.1, 111.222.333.444, ::1, 1000:2000:2c:3:c19:9ec8:a715:5e24, 3ffe:8311:ffff:f70f:0:5efe:111.222.333.444, fe80::5efe:111.222.333.444%8, fe80::c19:9ec8:a715:5e24%6".

## <a name="protocol-default-settings"></a>Impostazioni predefinite del protocollo

Molte delle impostazioni di configurazione, ad esempio MaxEnvelopeSizekb o SoapTraceEnabled, determinano il modo in cui i componenti client e server WinRM interagiscono con il WS-Management remoto. Nell'elenco seguente vengono descritte le impostazioni di configurazione disponibili.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Specifica il numero massimo di Simple Object Access Protocol (SOAP) in kilobyte. Il valore predefinito è 150 kilobyte.

> [!NOTE]  
> Il comportamento non è supportato se MaxEnvelopeSizekb è impostato su un valore maggiore di 1039440.

### <a name="maxtimeoutms"></a>MaxTimeoutms

Specifica il timeout massimo, in millisecondi, che può essere usato per qualsiasi richiesta diversa da Richieste pull. Il valore predefinito è 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Specifica il numero massimo di elementi che è possibile usare in una risposta Pull. Il valore predefinito è 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Specifica il numero massimo di richieste simultanee consentite dal servizio. Il valore predefinito è 25.

**WinRM 2.0:** Questa impostazione è deprecata ed è impostata su sola lettura.

## <a name="winrm-client-default-configuration-settings"></a>Impostazioni di configurazione predefinite del client WinRM

La versione client di Gestione remota Windows ha le impostazioni di configurazione predefinite seguenti.

### <a name="networkdelayms"></a>NetworkDelayms

Specifica l'intervallo di tempo aggiuntivo, in millisecondi, durante il quale il computer client attende per supportare il ritardo di rete. Il valore predefinito è 5000 millisecondi.

### <a name="urlprefix"></a>URLPrefix

Specifica un prefisso URL in base al quale accettare richieste HTTP o HTTPS. Il prefisso URL predefinito è "wsman".

### <a name="allowunencrypted"></a>AllowUnencrypted

Consente al computer client di richiedere traffico non crittografato. Per impostazione predefinita, il computer client richiede traffico di rete crittografato e questa impostazione è *False.*

### <a name="basic"></a>Basic

Consente al computer client di usare l'autenticazione di base. L'autenticazione di base è uno schema in cui il nome utente e la password vengono inviati in testo non crittografato al server o al proxy. Si tratta del metodo di autenticazione meno sicuro. Il valore predefinito è *True*.

### <a name="digest"></a>Digest

Consente al client di usare l'autenticazione del digest. L'autenticazione del digest è uno schema In attesa/Risposta che usa una stringa di dati specificata dal server per la parte In attesa. Solo il computer client può avviare una richiesta di autenticazione del digest. Il computer client invia una richiesta al server per l'autenticazione e riceve una stringa di token dal server. Il computer client invia quindi la richiesta di risorsa, inclusi il nome utente e un hash crittografico della password combinati con la stringa del token. L'autenticazione del digest è supportata per HTTP e per HTTPS. Le applicazioni e gli script client della shell WinRM possono specificare l'autenticazione del digest, ma il servizio Gestione remota Windows non accetta l'autenticazione digest. Il valore predefinito è *True*.

> [!NOTE]
> l'autenticazione del digest su HTTP non è considerata sicura.

### <a name="certificate"></a>Certificato

Consente al client di usare l'autenticazione basata su certificati client. L'autenticazione basata su certificati è uno schema in cui il server autentica un client identificato da un certificato X509. Il valore predefinito è *True*.

### <a name="kerberos"></a>Kerberos

Consente al client di usare l'autenticazione Kerberos. L'autenticazione Kerberos è uno schema in cui il client e il server si autenticano reciprocamente tramite certificati Kerberos. Il valore predefinito è *True*.

### <a name="negotiate"></a>Negotiate

Consente al client di usare l'autenticazione con negoziazione. L'autenticazione con negoziazione è uno schema in cui il client invia una richiesta di autenticazione al server. Il server determina se usare il protocollo Kerberos o NTLM. Il protocollo Kerberos viene selezionato per autenticare un account di dominio, mentre NTLM per gli account dei computer locali. Il nome utente deve essere specificato nel formato nome \\ utente di dominio per un utente di \_ dominio. Il nome utente deve essere specificato nel formato "nome server \_ \\ nome \_ utente" per un utente locale in un computer server. Il valore predefinito è *True*.

### <a name="credssp"></a>CredSSP

Consente al client di usare l'autenticazione CredSSP (Credential Security Support Provider). CredSSP consente a un'applicazione di delegare le credenziali dell'utente dal computer client al server di destinazione. Il valore predefinito è *False*.

### <a name="defaultports"></a>DefaultPorts

Specifica le porte che il client userà per HTTP o HTTPS.

**WinRM 2.0:** La porta HTTP predefinita è 5985 e la porta HTTPS predefinita è 5986.

### <a name="trustedhosts"></a>TrustedHosts

Specifica l'elenco di computer remoti considerati attendibili. È necessario aggiungere altri computer in un gruppo di lavoro o computer in un dominio diverso a questo elenco.

> [!Note]
> I computer nell'elenco TrustedHosts non sono autenticati. Il client può inviare informazioni sulle credenziali a questi computer.

Se viene specificato un indirizzo IPv6 per TrustedHost, l'indirizzo deve essere racchiuso tra parentesi quadre, come illustrato dal comando dell'utilità winrm seguente: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Per altre informazioni su come aggiungere computer all'elenco TrustedHosts, digitare `winrm help config` .

## <a name="winrm-service-default-configuration-settings"></a>Impostazioni di configurazione predefinite del servizio Gestione remota Windows

La versione del servizio di Gestione remota Windows ha le impostazioni di configurazione predefinite seguenti.

### <a name="rootsddl"></a>RootSDDL

Specifica il descrittore di sicurezza che controlla l'accesso remoto al listener. Il valore predefinito è "O:NSG:BAD:P(A;; GA;;; BA)(A;; GR;;; ER)S:P(AU;FA; GA;;; WD)(AU;SA; GWGX;;; WD)".

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

Numero massimo di operazioni simultanee. Il valore predefinito è 100.

**WinRM 2.0:** L'impostazione MaxConcurrentOperations è deprecata ed è impostata su sola lettura. Questa impostazione è stata sostituita da MaxConcurrentOperationsPerUser.

### <a name="maxconcurrentoperationsperuser"></a>MaxConcurrentOperationsPerUser

Specifica il numero massimo di operazioni simultanee che qualsiasi utente può aprire in remoto nello stesso sistema. Il valore predefinito è 1500.

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

Specifica il timeout di inattività in millisecondi tra i messaggi pull. Il valore predefinito è 60000.

### <a name="maxconnections"></a>MaxConnections

Specifica il numero massimo di richieste attive che il servizio può elaborare contemporaneamente. Il valore predefinito è 300.

**WinRM 2.0:** Il valore predefinito è 25.

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

Specifica il tempo massimo, in secondi, necessario al servizio Gestione remota Windows per recuperare un pacchetto. Il valore predefinito è 120 secondi.

### <a name="allowunencrypted"></a>AllowUnencrypted

Consente al computer client di richiedere traffico non crittografato. Il valore predefinito è *False*.

### <a name="basic"></a>Basic

Consente al servizio Gestione remota Windows di usare l'autenticazione di base. Il valore predefinito è *False*.

### <a name="certificate"></a>Certificato

Consente al servizio Gestione remota Windows di usare l'autenticazione basata su certificati client. Il valore predefinito è *False*.

### <a name="kerberos"></a>Kerberos

Consente al servizio Gestione remota Windows di usare l'autenticazione Kerberos. Il valore predefinito è *True*.

### <a name="negotiate"></a>Negotiate

Consente al servizio Gestione remota Windows di usare l'autenticazione negotiate. Il valore predefinito è *True*.

### <a name="credssp"></a>CredSSP

Consente al servizio Gestione remota Windows di usare l'autenticazione CredSSP (Credential Security Support Provider). Il valore predefinito è *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Imposta i criteri per i requisiti del token channel-binding nelle richieste di autenticazione. Il valore predefinito è *Relaxed.*

### <a name="defaultports"></a>DefaultPorts

Specifica le porte che il servizio Gestione remota Windows userà per HTTP o HTTPS.

**WinRM 2.0:** La porta HTTP predefinita è 5985 e la porta HTTPS predefinita è 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter e IPv6Filter

Specifica gli indirizzi IPv4 o IPv6 che i listener possono usare. I valori predefiniti sono IPv4Filter = \* e IPv6Filter = \* .

**IPv4:** Una stringa letterale IPv4 è costituita da quattro numeri decimali punteggiati, ognuno nell'intervallo compreso tra 0 e 255. Ad esempio: 192.168.0.0.

**IPv6:** Una stringa letterale IPv6 è racchiusa tra parentesi quadre e contiene numeri esadecimali separati da due punti. Ad esempio: \[ ::1 \] o \[ 3ffe:ffff::6ECB:0101 \] .

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

Specifica se il listener HTTP di compatibilità è abilitato. Se questa impostazione è *True,* il listener sarà in ascolto sulla porta 80 oltre alla porta 5985. Il valore predefinito è *False*.

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

Specifica se il listener HTTPS di compatibilità è abilitato. Se questa impostazione è *True,* il listener sarà in ascolto sulla porta 443 oltre alla porta 5986. Il valore predefinito è *False*.

## <a name="winrs-default-configuration-settings"></a>Configurazione predefinita di Winrs Impostazioni

`winrm quickconfig`configura anche le **impostazioni predefinite di Winrs.**

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Consente l'accesso alle shell remote. Se si imposta questo parametro *su False*, le nuove connessioni shell remota verranno rifiutate dal server. Il valore predefinito è *True*.

### <a name="idletimeout"></a>IdleTimeout

Specifica l'intervallo di tempo massimo, in millisecondi, durante il quale la shell remota rimarrà aperta in assenza di attività utente. Una volta trascorso l'intervallo di tempo specificato, la shell remota viene automaticamente eliminata.

**WinRM 2.0:** Il valore predefinito è 180000. Il valore minimo è 60000. L'impostazione di questo valore inferiore a 60000 non avrà alcun effetto sul timeout.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Specifica il numero massimo di utenti che possono eseguire simultaneamente operazioni remote nello stesso computer tramite una shell remota. Le nuove connessioni shell remota verranno rifiutate se superano il limite specificato. Il valore predefinito è 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Specifica il tempo massimo, in millisecondi, consentito per l'esecuzione del comando o dello script remoto. Il valore predefinito è 28800000.

**WinRM 2.0:** L'impostazione MaxShellRunTime è di sola lettura. La modifica del valore per MaxShellRunTime non avrà alcun effetto sulle shell remote.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Specifica il numero massimo di processi che possono essere avviati da qualsiasi operazione della shell. Il valore 0 consente un numero illimitato di processi. Il valore predefinito è 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Specifica la quantità massima di memoria allocata per shell, inclusi i processi figlio della shell. Il valore predefinito è 150 MB.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Consente di specificare il numero massimo di shell simultanee che qualsiasi utente può aprire in remoto sullo stesso computer. Se l'impostazione di questo criterio è abilitata, l'utente non sarà in grado di aprire nuove shell remote se il conteggio supera il limite specificato. Se l'impostazione dei criteri è disabilitata o non configurata, per impostazione predefinita il limite sarà di 5 shell remote per ciascun utente.

## <a name="configuring-winrm-with-group-policy"></a>Configurazione di WinRM con Criteri di gruppo

Usare l Criteri di gruppo editor per configurare Windows Remote Shell e WinRM per i computer dell'organizzazione.

### <a name="to-configure-with-group-policy"></a>Per configurare con Criteri di gruppo

1. Aprire una finestra del Prompt dei comandi come amministratore.
2. Al prompt dei comandi digitare `gpedit.msc`. Verrà **Editor oggetti Criteri di gruppo** finestra di dialogo.
3. Trovare il **Windows gestione** remota e Windows oggetti **Criteri di gruppo Shell** remota (GPO) in Configurazione computer Modelli amministrativi **Windows \\ \\ componenti**.
4. Nella scheda **Esteso** selezionare un'impostazione per visualizzare una descrizione. Fare doppio clic su un'impostazione per modificarla.

## <a name="windows-firewall-and-winrm-20-ports"></a>Windows Porte Firewall e WinRM 2.0

A partire da WinRM 2.0, le porte del listener predefinite configurate da sono la porta 5985 per il trasporto HTTP e la `Winrm quickconfig` porta 5986 per HTTPS. I listener WinRM possono essere configurati su qualsiasi porta arbitraria.

Se un computer viene aggiornato a WinRM 2.0, viene eseguita la migrazione dei listener configurati in precedenza e viene comunque ricevuto il traffico.

## <a name="winrm-installation-and-configuration-notes"></a>Note sull'installazione e la configurazione di WinRM

WinRM non dipende da altri servizi ad eccezione di WinHttp. Se iis Admin Service è installato nello stesso computer, è possibile che venga visualizzato un messaggio che indica che WinRM non può essere caricato prima di Internet Information Services (IIS). Tuttavia, WinRM non dipende effettivamente da IIS. Questi messaggi si verificano perché l'ordine di caricamento garantisce che il servizio IIS venga avviato &mdash; prima del servizio HTTP. WinRM richiede che `WinHTTP.dll` sia registrato.

Se il client firewall ISA2004 è installato nel computer, è possibile che un client Web Services for Management (WS-Management) smetta di rispondere. Per evitare questo problema, installare ISA2004 Firewall SP1.

Se due servizi listener con indirizzi IP diversi sono configurati con lo stesso numero di porta e nome computer, WinRM è in ascolto o riceve messaggi su un solo indirizzo. Ciò è dovuto al fatto che i prefissi URL usati WS-Management protocollo sono gli stessi.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Note sull'installazione del driver IPMI e del provider

Il driver potrebbe non rilevare l'esistenza di driver IPMI non provenienti da Microsoft. Se l'avvio del driver non riesce, potrebbe essere necessario disabilitarlo.

Se le risorse del controller di gestione della baseboard [(BMC)](./windows-remote-management-glossary.md#b) vengono visualizzate nel BIOS di sistema, ACPI (Plug and Play) rileva l'hardware BMC e installa automaticamente il driver IPMI. Plug and Play il supporto potrebbe non essere presente in tutti i BBC. Se il BMC viene rilevato da Plug and Play, viene visualizzato un dispositivo sconosciuto in Gestione dispositivi prima dell'installazione del componente Gestione hardware. Quando il driver viene installato, in Gestione dispositivi viene visualizzato un nuovo componente, microsoft ACPI Generic IPMI Compliant Device.

Se il sistema non rileva automaticamente il BMC e installa il driver, ma durante il processo di installazione è stato rilevato un BMC, è necessario creare il dispositivo BMC. A tale scopo, digitare il comando seguente al prompt dei comandi: `Rundll32 ipmisetp.dll, AddTheDevice` . Dopo l'esecuzione di questo comando, il dispositivo IPMI viene creato e visualizzato in Gestione dispositivi. Se si disinstalla il componente Gestione hardware, il dispositivo viene rimosso.

Per altre informazioni, vedere [Introduzione a Gestione hardware.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

Il provider IPMI inserisce le classi hardware nello spazio **dei nomi hardware \\ radice** di WMI. [](/windows/desktop/WmiSdk/gloss-n) Per altre informazioni sulle classi hardware, vedere [Provider IPMI.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Per altre informazioni sugli spazi *dei nomi* WMI, vedere [Architettura WMI.](/windows/desktop/WmiSdk/wmi-architecture)

## <a name="wmi-plug-in-configuration-notes"></a>Note sulla configurazione del plug-in WMI

A partire Windows 8 e Windows Server 2012, i [plug-in WMI](./windows-remote-management-glossary.md#w) hanno configurazioni di sicurezza personalizzate. Per consentire a un utente normale o non amministratore di usare il *plug-in WMI,* è necessario abilitare l'accesso per tale utente dopo la configurazione del [listener.](./windows-remote-management-glossary.md#l) Prima di tutto, è necessario configurare l'utente per l'accesso remoto a [WMI](./windows-remote-management-glossary.md#w) tramite uno di questi passaggi.

- Eseguire `lusrmgr.msc` per aggiungere l'utente **al gruppo WinRMRemoteWMIUsers \_ \_** nella finestra Utenti **e** gruppi locali oppure
- usare lo strumento da riga di **comando winrm** per configurare il descrittore di sicurezza per lo spazio dei nomi del [](./windows-remote-management-glossary.md#n) [plug-in WMI](./windows-remote-management-glossary.md#w), come indicato di seguito: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Quando viene visualizzata l'interfaccia utente, aggiungere l'utente.

Dopo aver configurato l'utente per l'accesso remoto a [WMI,](./windows-remote-management-glossary.md#w)è necessario configurare *WMI* per consentire all'utente di accedere al plug-in. A tale scopo, eseguire per modificare la sicurezza WMI per l'accesso allo spazio dei nomi `wmimgmt.msc` nella finestra Controllo **WMI.**  [](./windows-remote-management-glossary.md#n)

La maggior parte delle classi WMI per la gestione è nello **spazio dei nomi radice \\ cimv2.**