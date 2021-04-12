---
title: Configurazione di una sottoscrizione avviata dall'origine
description: Le sottoscrizioni avviate dall'origine consentono di definire una sottoscrizione in un computer dell'agente di raccolta eventi senza definire i computer di origine eventi, quindi è possibile configurare più computer di origine evento remoto (usando un'impostazione di criteri di gruppo) per inviare gli eventi al computer dell'agente di raccolta eventi.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/04/2020
ms.locfileid: "104398824"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configurazione di una sottoscrizione avviata dall'origine

Le sottoscrizioni avviate dall'origine consentono di definire una sottoscrizione in un computer dell'agente di raccolta eventi senza definire i computer di origine eventi, quindi è possibile configurare più computer di origine evento remoto (usando un'impostazione di criteri di gruppo) per inviare gli eventi al computer dell'agente di raccolta eventi. Questo comportamento è diverso da una sottoscrizione avviata dall'agente di raccolta dati perché nel modello di sottoscrizione avviato dall'agente di raccolta, l'agente di raccolta eventi deve definire tutte le origini eventi nella sottoscrizione dell'evento.

Quando si configura una sottoscrizione avviata dall'origine, valutare se i computer di origine eventi si trovano nello stesso dominio del computer dell'agente di raccolta eventi. Nelle sezioni seguenti vengono descritti i passaggi da seguire quando le origini eventi si trovano nello stesso dominio o non nello stesso dominio del computer dell'agente di raccolta eventi.

> [!Note]  
> Qualsiasi computer in un dominio, locale o remoto, può essere un agente di raccolta eventi. Tuttavia, quando si sceglie un agente di raccolta eventi, è importante selezionare un computer che sia topologicamente vicino alla posizione in cui verrà generata la maggior parte degli eventi. L'invio di eventi a un computer in un percorso di rete distante su una rete WAN può ridurre le prestazioni e l'efficienza complessive nella raccolta di eventi.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configurazione di una sottoscrizione avviata dall'origine in cui le origini eventi si trovano nello stesso dominio del computer dell'agente di raccolta eventi

Per configurare una sottoscrizione avviata dall'origine, è necessario che sia il computer di origine dell'evento che il computer dell'agente di raccolta eventi siano configurati.

> [!Note]  
> Queste istruzioni presuppongono che si disponga dell'accesso come amministratore al controller di dominio di Windows Server che funge da dominio in cui il computer remoto o i computer verranno configurati per la raccolta di eventi.

### <a name="configuring-the-event-source-computer"></a>Configurazione del computer di origine dell'evento

1. Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio di Windows Server per configurare Gestione remota Windows:

    **gestione remota Windows QC-q**

2. Avviare Criteri di gruppo eseguendo il comando seguente:

    **% SYSTEMROOT% \\ system32 \\ . msc**

3. Nel nodo **Configurazione computer** espandere il nodo **modelli amministrativi** , quindi espandere il nodo **componenti di Windows** , quindi selezionare il nodo di **invio degli eventi** .

4. Fare clic con il pulsante destro del mouse sull'impostazione **SubscriptionManager** e scegliere **Proprietà**. Abilitare l'impostazione **SubscriptionManager** e fare clic sul pulsante **Mostra** per aggiungere un indirizzo server all'impostazione. Aggiungere almeno un'impostazione che specifichi il computer dell'agente di raccolta eventi. La finestra delle **proprietà di SubscriptionManager** contiene una scheda **explain** che descrive la sintassi per l'impostazione.

5. Dopo aver aggiunto l'impostazione **SubscriptionManager** , eseguire il comando seguente per verificare che i criteri siano applicati:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configurazione del computer dell'agente di raccolta eventi

1. Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio di Windows Server per configurare Gestione remota Windows:

    **gestione remota Windows QC-q**

2. Eseguire il comando seguente per configurare il servizio raccolta eventi:

    **wecutil QC/q**

3. Creare una sottoscrizione avviata dall'origine. Questa operazione può essere eseguita a livello di codice, usando il Visualizzatore eventi o usando [**Wecutil.exe**](wecutil.md). Per ulteriori informazioni su come creare la sottoscrizione a livello di codice, vedere l'esempio di codice in [creazione di una sottoscrizione avviata dall'origine](creating-a-source-initiated-subscription.md). Se si utilizza Wecutil.exe, è necessario creare un file XML di sottoscrizione evento e utilizzare il seguente comando:

    *configurationFile.xml* **CS wecutil**

    Il codice XML seguente è un esempio del contenuto di un file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'origine per l'invio di eventi dal registro eventi dell'applicazione di un computer remoto al registro ForwardedEvents sul computer dell'agente di raccolta eventi.

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
    > Quando si crea una sottoscrizione avviata dall'origine, se AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList e DeniedSubjectList sono tutti vuoti, quindi "O:NSG: NSD: (A;; GA;;;D C) (A;; GA;;; NS) "verrà usato come descrittore di sicurezza predefinito per AllowedSourceDomainComputers. Il descrittore predefinito concede i membri del gruppo di dominio computer del dominio, così come il gruppo di servizi di rete locale (per il server d'invio locale), la possibilità di generare eventi per questa sottoscrizione.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Per verificare il corretto funzionamento della sottoscrizione

1. Sul computer dell'agente di raccolta eventi completare i passaggi seguenti:

    1. Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio di Windows Server per ottenere lo stato di runtime della sottoscrizione:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Verificare che l'origine evento sia connessa. Potrebbe essere necessario attendere fino al termine dell'intervallo di aggiornamento specificato nei criteri dopo aver creato la sottoscrizione per la connessione dell'origine evento.
    3. Eseguire il comando seguente per ottenere le informazioni sulla sottoscrizione:

        **wecutil gs** *&lt; subscriptionID &gt;*

    4. Ottenere il valore DeliveryMaxItems dalle informazioni sulla sottoscrizione.

2. Nel computer di origine evento, generare gli eventi che corrispondono alla query della sottoscrizione di eventi. Per l'invio degli eventi è necessario che venga generato il numero DeliveryMaxItems di eventi.
3. Sul computer dell'agente di raccolta eventi, verificare che gli eventi siano stati trasmessi al log ForwardedEvents o al log specificato nella sottoscrizione.

## <a name="forwarding-the-security-log"></a>Invio del registro di sicurezza

Per poter inviare il registro di sicurezza, è necessario aggiungere l'account servizio di rete al gruppo Readers del registro eventi.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configurazione di una sottoscrizione avviata dall'origine in cui le origini eventi non si trovano nello stesso dominio del computer dell'agente di raccolta eventi

> [!Note]  
> Queste istruzioni presuppongono che si disponga dell'accesso come amministratore a un controller di dominio di Windows Server. In questo caso, poiché il computer o i computer dell'agente di raccolta eventi remoto non si trovano nel dominio servito dal controller di dominio, è essenziale avviare un singolo client impostando Gestione remota Windows su "automatico" utilizzando servizi (Services. msc). In alternativa, è possibile eseguire "winrm quickconfig" in ogni client remoto.

Prima di creare la sottoscrizione, è necessario soddisfare i prerequisiti seguenti.

1. Sul computer dell'agente di raccolta eventi eseguire i comandi seguenti da un prompt dei comandi con privilegi elevati per configurare Gestione remota Windows e il servizio raccolta eventi:

    **gestione remota Windows QC-q**

    **wecutil QC/q**

2. Il computer dell'agente di raccolta deve disporre di un certificato di autenticazione server (certificato con scopo di autenticazione server) in un archivio certificati del computer locale.
3. Nel computer di origine evento, eseguire il comando seguente per configurare Gestione remota Windows:

    **gestione remota Windows QC-q**

4. Il computer di origine deve disporre di un certificato di autenticazione client (certificato con scopo di autenticazione client) in un archivio certificati del computer locale.
5. La porta 5986 è aperta sul computer dell'agente di raccolta eventi. Per aprire questa porta, eseguire il comando:

    **netsh firewall add apertura TCP 5986 "WinRM HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Requisiti dei certificati

- Un certificato di autenticazione server deve essere installato sul computer dell'agente di raccolta eventi nell'archivio personale del computer locale. Il soggetto di questo certificato deve corrispondere al nome di dominio completo dell'agente di raccolta.
- Un certificato di autenticazione client deve essere installato nei computer di origine dell'evento nell'archivio personale del computer locale. Il soggetto di questo certificato deve corrispondere al nome di dominio completo (FQDN) del computer.
- Se il certificato client è stato emesso da un'autorità di certificazione diversa da quella dell'agente di raccolta eventi, è necessario installare anche i certificati radice e intermedi nell'agente di raccolta eventi.
- Se il certificato client è stato emesso da un'autorità di certificazione intermedia e l'agente di raccolta esegue Windows 2012 o versione successiva, sarà necessario configurare la chiave del registro di sistema seguente:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Verificare che il server e il client siano in grado di controllare correttamente lo stato di revoca di tutti i certificati. L'uso del comando **certutil** può facilitare la risoluzione di eventuali errori.

Altre informazioni sono disponibili in questo articolo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configurare il listener nell'agente di raccolta eventi

1. Impostare l'autenticazione del certificato con il comando seguente:

    **winrm set winrm/config/Service/Auth @ {Certificate = "true"}**

2. Un listener HTTPS WinRM con il certificato di autenticazione server deve esistere nel computer dell'agente di raccolta eventi. Questo può essere verificato con il comando seguente:

    **WinRM e winrm/config/listener**

3. Se il listener HTTPS non è visibile o se la stampa Thumb del listener HTTPS non è uguale alla stampa Thumb del certificato di autenticazione server nel computer agente di raccolta, è possibile eliminare il listener e crearne uno nuovo con la corretta stampa Thumb. Per eliminare il listener HTTPS, usare il comando seguente:

    **winrm eliminare winrm/config/listener? Address = * + Transport = HTTPS**

    Per creare un nuovo listener, utilizzare il comando seguente:

    **WinRM creare winrm/config/listener? Address =&#42;+ Transport = HTTPS @ {hostname = "** &lt; _FQDN dell'agente di raccolta_ &gt; **"; CertificateThumbprint = "** &lt; _stampa Thumb del certificato di autenticazione server_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configurare il mapping dei certificati nell'agente di raccolta eventi

1. Creare un nuovo utente locale e aggiungerlo al gruppo Administrators locale.
2. Creare il mapping dei certificati utilizzando un certificato presente nelle "autorità di certificazione radice attendibili" del computer o "autorità di certificazione intermedie".

    Si tratta del certificato dell'autorità di certificazione radice o intermedia che ha emesso i certificati installati nei computer di origine dell'evento *(per evitare confusione, si tratta della CA immediatamente sopra il certificato nella catena di certificati)*:

    **WinRM creare winrm/config/Service/mapping certificato?** = &lt; _Identificazione personale dell'autorità di certificazione del certificato della CA emittente_ &gt; **+ Subject =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **"; Password = "** &lt; _password_ &gt; **"}-remoto: localhost**

3. Da un client testare il listener e il mapping del certificato con il comando seguente:

    WinRM **g winrm/config-r:https://** &lt; _FQDN_ &gt; raccolta eventi **: 5986-a:certificate-certificate: "** &lt; _Identificazione personale del certificato_ &gt; di autenticazione client **"**

    Questa operazione dovrebbe restituire la configurazione WinRM dell'agente di raccolta eventi. **Non spostare oltre** questo passaggio se la configurazione non viene visualizzata.

    **Cosa accade in questo passaggio?**
    - Il client si connette all'agente di raccolta eventi e invia il certificato specificato
    - L'agente di raccolta eventi cerca la CA emittente e controlla se è un mapping del certificato corrispondente
    - L'agente di raccolta eventi convalida la catena di certificati client e lo stato delle revoche
    - Se il passaggio precedente ha esito positivo, viene completata l'autenticazione.

> [!NOTE]
> È possibile che si verifichi un errore di accesso negato per il metodo di autenticazione, che potrebbe essere fuorviante. Per risolvere i problemi, controllare il registro CAPI nell'agente di raccolta eventi.

4. Elencare le voci mapping certificato configurate con il comando: **WinRM enum winrm/config/Service/mapping certificato**

### <a name="event-source-computer-configuration"></a>Configurazione computer origine evento

1. Accedere con un account amministratore e aprire il Editor Criteri di gruppo locali (gpedit. msc)
2. Passare al computer locale Locale\configurazione computer\Modelli Amministrativi\componenti di Components\Event.
3. Aprire il criterio "configurare l'indirizzo del server, l'intervallo di aggiornamento e l'autorità di certificazione di un gestore delle sottoscrizioni di destinazione".
4. Abilitare il criterio e fare clic su SubscriptionManagers "Show..." pulsante.
5. Nella finestra SubscriptionManagers immettere la stringa seguente:

    **Server = https://** &lt; _FQDN del server_ &gt; dell'agente di raccolta eventi **: 5986/WSMan/SubscriptionManager/WEC, Refresh =** &lt; _Intervallo di aggiornamento in secondi_ &gt; **, IssuerCA =** &lt; _Identificazione personale del certificato della CA emittente_&gt;

6. Eseguire la seguente riga di comando per aggiornare le impostazioni di Criteri di gruppo locali: GPUpdate/Force
7. Questi passaggi dovrebbero produrre l'evento 104 nel computer di origine Visualizzatore eventi registri applicazioni e servizi Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational con il messaggio seguente:

    "Il server d'indirizzamento si è connesso correttamente al gestore delle sottoscrizioni al &lt; nome FQDN dell'indirizzo &gt; seguito dall'evento 100 con il messaggio:" la sottoscrizione &lt; sub_name &gt; viene creata correttamente ".

8. Nell'agente di raccolta eventi lo stato di runtime della sottoscrizione visualizzerà ora 1 computer attivo.
9. Aprire il registro ForwardedEvents nell'agente di raccolta eventi e verificare se gli eventi sono stati trasmessi dai computer di origine.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Concedere l'autorizzazione per la chiave privata del certificato client nell'origine evento

1. Aprire la console di gestione certificati per computer locale nel computer di origine dell'evento.
2. Fare clic con il pulsante destro del mouse sul certificato client quindi gestire le chiavi private.
3. Concedere l'autorizzazione di lettura per l'utente del servizio di rete.

### <a name="event-subscription-configuration"></a>Configurazione della sottoscrizione di eventi

1. Aprire Visualizzatore eventi nell'agente di raccolta eventi e passare al nodo sottoscrizioni.
2. Fare clic con il pulsante destro del mouse su sottoscrizioni e scegliere "Crea sottoscrizione".
3. Assegnare un nome e una descrizione facoltativa per la nuova sottoscrizione.
4. Selezionare l'opzione "origine computer avviata" e fare clic su "Seleziona gruppi di computer...".
5. In gruppi di computer fare clic su "Aggiungi computer non di dominio..." e digitare il nome host dell'origine evento.
6. Fare clic su "Aggiungi certificati..." e aggiungere il certificato dell'autorità di certificazione che rilascia i certificati client. È possibile fare clic su Visualizza certificato per convalidare il certificato.
7. In autorità di certificazione fare clic su OK per aggiungere il certificato.
8. Al termine dell'aggiunta di computer, fare clic su OK.
9. Tornare alle proprietà della sottoscrizione, fare clic su Seleziona eventi...
10. Configurare il filtro di query degli eventi specificando i livelli di evento, i registri eventi o le origini eventi, gli ID evento e tutte le altre opzioni di filtro.
11. Tornare alle proprietà della sottoscrizione, fare clic su Avanzate...
12. Scegliere una delle opzioni di ottimizzazione per il recapito di eventi dall'evento di origine all'agente di raccolta eventi o lasciare il valore predefinito normale: 
    1. **Ridurre la larghezza di banda**: gli eventi verranno recapitati con una frequenza minore per risparmiare larghezza di banda.
    2. **Riduzione della latenza**: gli eventi vengono recapitati non appena si verificano per ridurre la latenza degli eventi.
13. Modificare il protocollo in HTTPS e fare clic su OK.
14. Fare clic su OK per creare la nuova sottoscrizione.
15. Verificare lo stato di runtime della sottoscrizione facendo clic con il pulsante destro del mouse e scegliendo "stato Runtime".
