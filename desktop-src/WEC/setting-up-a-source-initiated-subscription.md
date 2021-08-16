---
title: Configurazione di una sottoscrizione avviata dall'origine
description: Le sottoscrizioni avviate dall'origine consentono di definire una sottoscrizione in un computer dell'agente di raccolta eventi senza definire i computer di origine eventi e quindi è possibile configurare più computer di origine eventi remoti (usando un'impostazione di Criteri di gruppo) per inoltrare gli eventi al computer dell'agente di raccolta eventi.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: f9d0ade037c0332f390bbea4c9f126f78f4172879fc50465fcf9e329e89fa23d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620651"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configurazione di una sottoscrizione avviata dall'origine

Le sottoscrizioni avviate dall'origine consentono di definire una sottoscrizione in un computer dell'agente di raccolta eventi senza definire i computer di origine eventi e quindi è possibile configurare più computer di origine eventi remoti (usando un'impostazione di Criteri di gruppo) per inoltrare gli eventi al computer dell'agente di raccolta eventi. Questo comportamento differisce da una sottoscrizione avviata dall'agente di raccolta perché nel modello di sottoscrizione avviato dall'agente di raccolta, l'agente di raccolta eventi deve definire tutte le origini eventi nella sottoscrizione di eventi.

Quando si configura una sottoscrizione avviata dall'origine, valutare se i computer di origine eventi si nello stesso dominio del computer dell'agente di raccolta eventi. Nelle sezioni seguenti vengono descritti i passaggi da seguire quando le origini eventi si riferiscono allo stesso dominio o meno del computer dell'agente di raccolta eventi.

> [!Note]  
> Qualsiasi computer in un dominio, locale o remoto, può essere un agente di raccolta eventi. Tuttavia, quando si sceglie un agente di raccolta eventi, è importante selezionare un computer topologicamente vicino al punto in cui verrà generata la maggior parte degli eventi. L'invio di eventi a un computer in un percorso di rete distante in una rete WAN può ridurre le prestazioni complessive e l'efficienza nella raccolta di eventi.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configurazione di una sottoscrizione avviata dall'origine in cui le origini eventi si trovano nello stesso dominio del computer dell'agente di raccolta eventi

Sia i computer di origine eventi che il computer dell'agente di raccolta eventi devono essere configurati per configurare una sottoscrizione avviata dall'origine.

> [!Note]  
> Queste istruzioni presuppongono che l'utente abbia accesso come amministratore al controller di dominio Windows Server che serve il dominio in cui il computer remoto o i computer saranno configurati per raccogliere gli eventi.

### <a name="configuring-the-event-source-computer"></a>Configurazione del computer dell'origine evento

1. Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio Windows Server per configurare Windows Gestione remota:

    **winrm qc -q**

2. Avviare Criteri di gruppo eseguendo il comando seguente:

    **%SYSTEMROOT% \\ System32 \\ gpedit.msc**

3. Nel nodo **Configurazione computer** espandere il nodo **Modelli amministrativi,** espandere il nodo Componenti **Windows** e quindi selezionare il **nodo Inoltro** eventi.

4. Fare clic con il pulsante destro **del mouse sull'impostazione SubscriptionManager** e **scegliere Proprietà.** Abilitare **l'impostazione SubscriptionManager** e fare clic sul **pulsante Mostra** per aggiungere un indirizzo del server all'impostazione. Aggiungere almeno un'impostazione che specifica il computer dell'agente di raccolta eventi. La **finestra Proprietà SubscriptionManager** contiene una **scheda Spiega** che descrive la sintassi per l'impostazione.

5. Dopo aver **aggiunto l'impostazione SubscriptionManager,** eseguire il comando seguente per assicurarsi che i criteri siano applicati:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configurazione del computer dell'agente di raccolta eventi

1. Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio Windows Server per configurare Windows Gestione remota:

    **winrm qc -q**

2. Eseguire il comando seguente per configurare il servizio Agente di raccolta eventi:

    **wecutil qc /q**

3. Creare una sottoscrizione avviata dall'origine. Questa operazione può essere eseguita a livello di codice, usando Visualizzatore eventi o [**usando**](wecutil.md)Wecutil.exe. Per altre informazioni su come creare la sottoscrizione a livello di codice, vedere l'esempio di codice in [Creazione di una sottoscrizione avviata dall'origine.](creating-a-source-initiated-subscription.md) Se si usa Wecutil.exe, è necessario creare un file XML della sottoscrizione di eventi e usare il comando seguente:

    **wecutil cs** *configurationFile.xml*

    Il codice XML seguente è un esempio del contenuto di un file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'origine per inoltrare gli eventi dal registro eventi dell'applicazione di un computer remoto al registro ForwardedEvents nel computer dell'agente di raccolta eventi.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > Quando si crea una sottoscrizione avviata dall'origine, se AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList e DeniedSubjectList sono tutti vuoti, allora "O:NSG:NSD:(A;; GA; ; ;D C)(A;; GA;;; NS)" verrà usato come descrittore di sicurezza predefinito per AllowedSourceDomainComputers. Il descrittore predefinito concede ai membri del gruppo di dominio Domain Computers, nonché al gruppo di servizi di rete locale (per il server d'inoltro locale), la possibilità di generare eventi per questa sottoscrizione.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Per verificare il corretto funzionamento della sottoscrizione

1. Nel computer dell'agente di raccolta eventi completare i passaggi seguenti:

    1. Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio Windows Server per ottenere lo stato di runtime della sottoscrizione:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Verificare che l'origine evento sia connessa. Potrebbe essere necessario attendere il termine dell'intervallo di aggiornamento specificato nei criteri dopo aver creato la sottoscrizione per l'origine evento da collegare.
    3. Eseguire il comando seguente per ottenere le informazioni sulla sottoscrizione:

        **wecutil gs** *&lt; subscriptionID &gt;*

    4. Ottenere il valore DeliveryMaxItems dalle informazioni sulla sottoscrizione.

2. Nel computer di origine eventi generare gli eventi che corrispondono alla query dalla sottoscrizione di eventi. Il numero di eventi DeliveryMaxItems deve essere generato per l'inoltro degli eventi.
3. Nel computer dell'agente di raccolta eventi verificare che gli eventi siano stati inoltrati al log ForwardedEvents o al log specificato nella sottoscrizione.

## <a name="forwarding-the-security-log"></a>Inoltro del log di sicurezza

Per poter inoltrare il registro di sicurezza, è necessario aggiungere l'account SERVIZIO DI RETE al gruppo Lettori registro eventi.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configurazione di una sottoscrizione avviata dall'origine in cui le origini eventi non si trovano nello stesso dominio del computer dell'agente di raccolta eventi

> [!Note]  
> Queste istruzioni presuppongono che l'utente abbia accesso come amministratore a un controller Windows di dominio di Windows Server. In questo caso, poiché il computer o i computer dell'agente di raccolta eventi remoti non si trova nel dominio servito dal controller di dominio, è essenziale avviare un singolo client impostando Windows Gestione remota su "automatico" tramite Servizi (services.msc). In alternativa, è possibile eseguire "winrm quickconfig" in ogni client remoto.

Prima di creare la sottoscrizione, è necessario che siano soddisfatti i prerequisiti seguenti.

1. Nel computer dell'agente di raccolta eventi eseguire i comandi seguenti da un prompt dei comandi con privilegi elevati per configurare Windows gestione remota e il servizio Agente di raccolta eventi:

    **winrm qc -q**

    **wecutil qc /q**

2. Il computer dell'agente di raccolta deve disporre di un certificato di autenticazione server (certificato con scopo di autenticazione server) in un archivio certificati del computer locale.
3. Nel computer di origine eventi eseguire il comando seguente per configurare Windows gestione remota:

    **winrm qc -q**

4. Il computer di origine deve avere un certificato di autenticazione client (certificato con scopo di autenticazione client) in un archivio certificati del computer locale.
5. La porta 5986 viene aperta nel computer dell'agente di raccolta eventi. Per aprire questa porta, eseguire il comando:

    **netsh firewall add portapening TCP 5986 "Winrm HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Requisiti per i certificati

- È necessario installare un certificato di autenticazione server nel computer dell'agente di raccolta eventi nell'archivio personale del computer locale. Il soggetto di questo certificato deve corrispondere al nome di dominio completo dell'agente di raccolta.
- È necessario installare un certificato di autenticazione client nei computer dell'origine evento nell'archivio personale del computer locale. Il soggetto di questo certificato deve corrispondere al nome di dominio completo del computer.
- Se il certificato client è stato emesso da un'autorità di certificazione diversa da quella dell'agente di raccolta eventi, i certificati radice e intermedio devono essere installati anche nell'agente di raccolta eventi.
- Se il certificato client è stato emesso da un'autorità di certificazione intermedia e l'agente di raccolta esegue Windows 2012 o versioni successive, sarà necessario configurare la chiave del Registro di sistema seguente:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Verificare che sia il server che il client siano in grado di controllare correttamente lo stato di revoca in tutti i certificati. L'uso **del comando certutil** consente di risolvere eventuali errori.

Per altre informazioni, vedere questo articolo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configurare il listener nell'agente di raccolta eventi

1. Impostare l'autenticazione del certificato con il comando seguente:

    **winrm set winrm/config/service/auth @{Certificate="true"}**

2. Nel computer dell'agente di raccolta eventi deve essere presente un listener HTTPS WinRM con la stampa thumb del certificato di autenticazione server. Questa operazione può essere verificata con il comando seguente:

    **winrm e winrm/config/listener**

3. Se il listener HTTPS non viene visualizzato o se la stampa del pollice del listener HTTPS non corrisponde all'identificazione digitale del certificato di autenticazione server nel computer dell'agente di raccolta, è possibile eliminare il listener e crearne uno nuovo con la stampa del cursore corretta. Per eliminare il listener https, usare il comando seguente:

    **winrm delete winrm/config/Listener? Address=*+Transport=HTTPS**

    Per creare un nuovo listener, usare il comando seguente:

    **winrm create winrm/config/Listener? Address=&#42;+Transport=HTTPS @{Hostname="** &lt; _FQDN dell'agente di raccolta_ &gt; **"; CertificateThumbprint="** &lt; _Identificazione personale del certificato di autenticazione server_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configurare il mapping dei certificati nell'agente di raccolta eventi

1. Creare un nuovo utente locale e aggiungerlo al gruppo Administrators locale.
2. Creare il mapping del certificato usando un certificato presente nell'elenco "Autorità di certificazione radice disponibile nell'elenco locale" o "Autorità di certificazione intermedie" del computer.

    Si tratta del certificato della CA radice o intermedia che ha emesso i certificati installati nei computer dell'origine evento (per evitare confusione, si tratta della CA immediatamente sopra il certificato nella catena di *certificati):*

    **winrm create winrm/config/service/certmapping? Identificazione personale** dell'autorità di certificazione emittente = &lt;  &gt; **+Subject=&#42;+URI=&#42; @{UserName="** &lt; _username_ &gt; **"; Password="** &lt; _password_ &gt; **"} -remote:localhost**

3. Da un client testare il listener e il mapping del certificato con il comando seguente:

    **winrm g winrm/config -r:https://** &lt; _Nome di dominio completo dell'agente di raccolta eventi_ &gt; **:5986 -a:certificate -certificate:"** &lt; _Identificazione personale del certificato di autenticazione client_ &gt; **"**

    Verrà restituita la configurazione WinRM dell'agente di raccolta eventi. **Non superare** questo passaggio se la configurazione non viene visualizzata.

    **Cosa accade in questo passaggio?**
    - Il client si connette all'agente di raccolta eventi e invia il certificato specificato
    - L'agente di raccolta eventi cerca la CA emittente e controlla se è un mapping di certificato corrispondente
    - L'agente di raccolta eventi convalida la catena di certificati client e lo stato delle revoche
    - Se i passaggi precedenti hanno esito positivo, l'autenticazione viene completata.

> [!NOTE]
> È possibile che venga visualizzato un errore di accesso negato che indica il metodo di autenticazione, che potrebbe essere fuorviante. Per risolvere il problema, controllare il log CAPI nell'agente di raccolta eventi.

4. Elencare le voci di mapping dei certificati configurate con il comando: **winrm enum winrm/config/service/certmapping**

### <a name="event-source-computer-configuration"></a>Configurazione del computer dell'origine evento

1. Accedere con un account amministratore e aprire il Editor Criteri di gruppo locali (gpedit.msc)
2. Passare a Criteri del computer locale\Configurazione computer\Modelli amministrativi\Windows\Inoltro eventi.
3. Aprire il criterio "Configurare l'indirizzo del server, l'intervallo di aggiornamento e l'autorità di certificazione dell'autorità di certificazione di un gestore di sottoscrizioni di destinazione".
4. Abilitare il criterio e fare clic su SubscriptionManagers "Mostra..." Pulsante.
5. Nella finestra SubscriptionManagers immettere la stringa seguente:

    **Server=HTTPS://** &lt; _FQDN del server dell'agente di raccolta eventi_ &gt; **:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt; _Intervallo di aggiornamento in secondi_ &gt; **,IssuerCA=** &lt; _Identificazione personale del certificato della CA emittente_&gt;

6. Eseguire la riga di comando seguente per aggiornare localmente Criteri di gruppo impostazioni:Gpupdate /force
7. Questi passaggi dovrebbero generare l'evento 104 nel registro applicazioni e servizi del computer di origine Visualizzatore eventi\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational con il messaggio seguente:

    "The forwarder has successfully connected to the subscription manager at address FQDN followed by event &lt; &gt; 100 with the message: "The subscription &lt; sub_name is created &gt; successfully".

8. Nell'agente di raccolta eventi, lo stato del runtime della sottoscrizione mostrerà ora 1 computer attivo.
9. Aprire il log ForwardedEvents nell'agente di raccolta eventi e verificare se gli eventi sono stati inoltrati dai computer di origine.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Concedere l'autorizzazione per la chiave privata del certificato client nell'origine evento

1. Aprire la console di gestione certificati per Computer locale nel computer di origine eventi.
2. Fare clic con il pulsante destro del mouse sul certificato client e quindi scegliere Gestisci chiavi private.
3. Concedere l'autorizzazione Lettura all'utente NETWORK SERVICE.

### <a name="event-subscription-configuration"></a>Configurazione della sottoscrizione di eventi

1. Aprire Visualizzatore eventi agente di raccolta eventi e passare al nodo Sottoscrizioni.
2. Fare clic con il pulsante destro del mouse su Sottoscrizioni e scegliere "Crea sottoscrizione..."
3. Assegnare un nome e una descrizione facoltativa per la nuova sottoscrizione.
4. Selezionare l'opzione "Avviato dal computer di origine" e fare clic su "Seleziona gruppi di computer...".
5. In Gruppi di computer fare clic su "Aggiungi computer non di dominio..." e digitare il nome host dell'origine evento.
6. Fare clic su "Aggiungi certificati..." e aggiungere il certificato dell'autorità di certificazione che emettere i certificati client. È possibile fare clic su Visualizza certificato per convalidare il certificato.
7. In Autorità di certificazione fare clic su OK per aggiungere il certificato.
8. Al termine dell'aggiunta di Computer, fare clic su OK.
9. Tornare a Proprietà sottoscrizione e fare clic su Seleziona eventi.
10. Configurare il filtro query eventi specificando i livelli di evento, i log eventi o le origini evento, gli ID evento e qualsiasi altra opzione di filtro.
11. Tornare a Proprietà sottoscrizione e fare clic su Avanzate...
12. Scegliere una delle opzioni di ottimizzazione per il recapito degli eventi dall'evento di origine all'agente di raccolta eventi oppure lasciare l'impostazione predefinita Normale: 
    1. **Ridurre al minimo la** larghezza di banda: gli eventi verranno recapitati ridurrà la frequenza per risparmiare larghezza di banda.
    2. **Ridurre al minimo la latenza:** gli eventi verranno recapitati non appena si verificano per ridurre la latenza degli eventi.
13. Impostare Protocollo su HTTPS e fare clic su OK.
14. Fare clic su OK per creare la nuova sottoscrizione.
15. Controllare lo stato di runtime della sottoscrizione facendo clic con il pulsante destro del mouse e scegliendo "Stato runtime"
