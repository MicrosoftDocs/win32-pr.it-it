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
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="41ba1-103">Configurazione di una sottoscrizione avviata dall'origine</span><span class="sxs-lookup"><span data-stu-id="41ba1-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="41ba1-104">Le sottoscrizioni avviate dall'origine consentono di definire una sottoscrizione in un computer dell'agente di raccolta eventi senza definire i computer di origine eventi, quindi è possibile configurare più computer di origine evento remoto (usando un'impostazione di criteri di gruppo) per inviare gli eventi al computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="41ba1-105">Questo comportamento è diverso da una sottoscrizione avviata dall'agente di raccolta dati perché nel modello di sottoscrizione avviato dall'agente di raccolta, l'agente di raccolta eventi deve definire tutte le origini eventi nella sottoscrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="41ba1-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="41ba1-106">Quando si configura una sottoscrizione avviata dall'origine, valutare se i computer di origine eventi si trovano nello stesso dominio del computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="41ba1-107">Nelle sezioni seguenti vengono descritti i passaggi da seguire quando le origini eventi si trovano nello stesso dominio o non nello stesso dominio del computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="41ba1-108">Qualsiasi computer in un dominio, locale o remoto, può essere un agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="41ba1-109">Tuttavia, quando si sceglie un agente di raccolta eventi, è importante selezionare un computer che sia topologicamente vicino alla posizione in cui verrà generata la maggior parte degli eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="41ba1-110">L'invio di eventi a un computer in un percorso di rete distante su una rete WAN può ridurre le prestazioni e l'efficienza complessive nella raccolta di eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="41ba1-111">Configurazione di una sottoscrizione avviata dall'origine in cui le origini eventi si trovano nello stesso dominio del computer dell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="41ba1-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="41ba1-112">Per configurare una sottoscrizione avviata dall'origine, è necessario che sia il computer di origine dell'evento che il computer dell'agente di raccolta eventi siano configurati.</span><span class="sxs-lookup"><span data-stu-id="41ba1-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="41ba1-113">Queste istruzioni presuppongono che si disponga dell'accesso come amministratore al controller di dominio di Windows Server che funge da dominio in cui il computer remoto o i computer verranno configurati per la raccolta di eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="41ba1-114">Configurazione del computer di origine dell'evento</span><span class="sxs-lookup"><span data-stu-id="41ba1-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="41ba1-115">Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio di Windows Server per configurare Gestione remota Windows:</span><span class="sxs-lookup"><span data-stu-id="41ba1-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="41ba1-116">**gestione remota Windows QC-q**</span><span class="sxs-lookup"><span data-stu-id="41ba1-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="41ba1-117">Avviare Criteri di gruppo eseguendo il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="41ba1-118">**% SYSTEMROOT% \\ system32 \\ . msc**</span><span class="sxs-lookup"><span data-stu-id="41ba1-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="41ba1-119">Nel nodo **Configurazione computer** espandere il nodo **modelli amministrativi** , quindi espandere il nodo **componenti di Windows** , quindi selezionare il nodo di **invio degli eventi** .</span><span class="sxs-lookup"><span data-stu-id="41ba1-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="41ba1-120">Fare clic con il pulsante destro del mouse sull'impostazione **SubscriptionManager** e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="41ba1-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="41ba1-121">Abilitare l'impostazione **SubscriptionManager** e fare clic sul pulsante **Mostra** per aggiungere un indirizzo server all'impostazione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="41ba1-122">Aggiungere almeno un'impostazione che specifichi il computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="41ba1-123">La finestra delle **proprietà di SubscriptionManager** contiene una scheda **explain** che descrive la sintassi per l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="41ba1-124">Dopo aver aggiunto l'impostazione **SubscriptionManager** , eseguire il comando seguente per verificare che i criteri siano applicati:</span><span class="sxs-lookup"><span data-stu-id="41ba1-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="41ba1-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="41ba1-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="41ba1-126">Configurazione del computer dell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="41ba1-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="41ba1-127">Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio di Windows Server per configurare Gestione remota Windows:</span><span class="sxs-lookup"><span data-stu-id="41ba1-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="41ba1-128">**gestione remota Windows QC-q**</span><span class="sxs-lookup"><span data-stu-id="41ba1-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="41ba1-129">Eseguire il comando seguente per configurare il servizio raccolta eventi:</span><span class="sxs-lookup"><span data-stu-id="41ba1-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="41ba1-130">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="41ba1-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="41ba1-131">Creare una sottoscrizione avviata dall'origine.</span><span class="sxs-lookup"><span data-stu-id="41ba1-131">Create a source initiated subscription.</span></span> <span data-ttu-id="41ba1-132">Questa operazione può essere eseguita a livello di codice, usando il Visualizzatore eventi o usando [**Wecutil.exe**](wecutil.md).</span><span class="sxs-lookup"><span data-stu-id="41ba1-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="41ba1-133">Per ulteriori informazioni su come creare la sottoscrizione a livello di codice, vedere l'esempio di codice in [creazione di una sottoscrizione avviata dall'origine](creating-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="41ba1-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="41ba1-134">Se si utilizza Wecutil.exe, è necessario creare un file XML di sottoscrizione evento e utilizzare il seguente comando:</span><span class="sxs-lookup"><span data-stu-id="41ba1-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="41ba1-135">*configurationFile.xml* **CS wecutil**</span><span class="sxs-lookup"><span data-stu-id="41ba1-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="41ba1-136">Il codice XML seguente è un esempio del contenuto di un file di configurazione della sottoscrizione che crea una sottoscrizione avviata dall'origine per l'invio di eventi dal registro eventi dell'applicazione di un computer remoto al registro ForwardedEvents sul computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

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
    > <span data-ttu-id="41ba1-137">Quando si crea una sottoscrizione avviata dall'origine, se AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList e DeniedSubjectList sono tutti vuoti, quindi "O:NSG: NSD: (A;; GA;;;D C) (A;; GA;;; NS) "verrà usato come descrittore di sicurezza predefinito per AllowedSourceDomainComputers.</span><span class="sxs-lookup"><span data-stu-id="41ba1-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="41ba1-138">Il descrittore predefinito concede i membri del gruppo di dominio computer del dominio, così come il gruppo di servizi di rete locale (per il server d'invio locale), la possibilità di generare eventi per questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="41ba1-139">Per verificare il corretto funzionamento della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="41ba1-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="41ba1-140">Sul computer dell'agente di raccolta eventi completare i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="41ba1-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="41ba1-141">Eseguire il comando seguente da un prompt dei comandi con privilegi elevati nel controller di dominio di Windows Server per ottenere lo stato di runtime della sottoscrizione:</span><span class="sxs-lookup"><span data-stu-id="41ba1-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="41ba1-142">**wecutil gr** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="41ba1-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="41ba1-143">Verificare che l'origine evento sia connessa.</span><span class="sxs-lookup"><span data-stu-id="41ba1-143">Verify that the event source has connected.</span></span> <span data-ttu-id="41ba1-144">Potrebbe essere necessario attendere fino al termine dell'intervallo di aggiornamento specificato nei criteri dopo aver creato la sottoscrizione per la connessione dell'origine evento.</span><span class="sxs-lookup"><span data-stu-id="41ba1-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="41ba1-145">Eseguire il comando seguente per ottenere le informazioni sulla sottoscrizione:</span><span class="sxs-lookup"><span data-stu-id="41ba1-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="41ba1-146">**wecutil gs** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="41ba1-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="41ba1-147">Ottenere il valore DeliveryMaxItems dalle informazioni sulla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="41ba1-148">Nel computer di origine evento, generare gli eventi che corrispondono alla query della sottoscrizione di eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="41ba1-149">Per l'invio degli eventi è necessario che venga generato il numero DeliveryMaxItems di eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="41ba1-150">Sul computer dell'agente di raccolta eventi, verificare che gli eventi siano stati trasmessi al log ForwardedEvents o al log specificato nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="41ba1-151">Invio del registro di sicurezza</span><span class="sxs-lookup"><span data-stu-id="41ba1-151">Forwarding the security log</span></span>

<span data-ttu-id="41ba1-152">Per poter inviare il registro di sicurezza, è necessario aggiungere l'account servizio di rete al gruppo Readers del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="41ba1-153">Configurazione di una sottoscrizione avviata dall'origine in cui le origini eventi non si trovano nello stesso dominio del computer dell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="41ba1-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="41ba1-154">Queste istruzioni presuppongono che si disponga dell'accesso come amministratore a un controller di dominio di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="41ba1-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="41ba1-155">In questo caso, poiché il computer o i computer dell'agente di raccolta eventi remoto non si trovano nel dominio servito dal controller di dominio, è essenziale avviare un singolo client impostando Gestione remota Windows su "automatico" utilizzando servizi (Services. msc).</span><span class="sxs-lookup"><span data-stu-id="41ba1-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="41ba1-156">In alternativa, è possibile eseguire "winrm quickconfig" in ogni client remoto.</span><span class="sxs-lookup"><span data-stu-id="41ba1-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="41ba1-157">Prima di creare la sottoscrizione, è necessario soddisfare i prerequisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="41ba1-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="41ba1-158">Sul computer dell'agente di raccolta eventi eseguire i comandi seguenti da un prompt dei comandi con privilegi elevati per configurare Gestione remota Windows e il servizio raccolta eventi:</span><span class="sxs-lookup"><span data-stu-id="41ba1-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="41ba1-159">**gestione remota Windows QC-q**</span><span class="sxs-lookup"><span data-stu-id="41ba1-159">**winrm qc -q**</span></span>

    <span data-ttu-id="41ba1-160">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="41ba1-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="41ba1-161">Il computer dell'agente di raccolta deve disporre di un certificato di autenticazione server (certificato con scopo di autenticazione server) in un archivio certificati del computer locale.</span><span class="sxs-lookup"><span data-stu-id="41ba1-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="41ba1-162">Nel computer di origine evento, eseguire il comando seguente per configurare Gestione remota Windows:</span><span class="sxs-lookup"><span data-stu-id="41ba1-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="41ba1-163">**gestione remota Windows QC-q**</span><span class="sxs-lookup"><span data-stu-id="41ba1-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="41ba1-164">Il computer di origine deve disporre di un certificato di autenticazione client (certificato con scopo di autenticazione client) in un archivio certificati del computer locale.</span><span class="sxs-lookup"><span data-stu-id="41ba1-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="41ba1-165">La porta 5986 è aperta sul computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="41ba1-166">Per aprire questa porta, eseguire il comando:</span><span class="sxs-lookup"><span data-stu-id="41ba1-166">To open this port, run the command:</span></span>

    <span data-ttu-id="41ba1-167">**netsh firewall add apertura TCP 5986 "WinRM HTTPS Remote Management"**</span><span class="sxs-lookup"><span data-stu-id="41ba1-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="41ba1-168">Requisiti dei certificati</span><span class="sxs-lookup"><span data-stu-id="41ba1-168">Certificates requirements</span></span>

- <span data-ttu-id="41ba1-169">Un certificato di autenticazione server deve essere installato sul computer dell'agente di raccolta eventi nell'archivio personale del computer locale.</span><span class="sxs-lookup"><span data-stu-id="41ba1-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="41ba1-170">Il soggetto di questo certificato deve corrispondere al nome di dominio completo dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="41ba1-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="41ba1-171">Un certificato di autenticazione client deve essere installato nei computer di origine dell'evento nell'archivio personale del computer locale.</span><span class="sxs-lookup"><span data-stu-id="41ba1-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="41ba1-172">Il soggetto di questo certificato deve corrispondere al nome di dominio completo (FQDN) del computer.</span><span class="sxs-lookup"><span data-stu-id="41ba1-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="41ba1-173">Se il certificato client è stato emesso da un'autorità di certificazione diversa da quella dell'agente di raccolta eventi, è necessario installare anche i certificati radice e intermedi nell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="41ba1-174">Se il certificato client è stato emesso da un'autorità di certificazione intermedia e l'agente di raccolta esegue Windows 2012 o versione successiva, sarà necessario configurare la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="41ba1-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="41ba1-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="41ba1-176">Verificare che il server e il client siano in grado di controllare correttamente lo stato di revoca di tutti i certificati.</span><span class="sxs-lookup"><span data-stu-id="41ba1-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="41ba1-177">L'uso del comando **certutil** può facilitare la risoluzione di eventuali errori.</span><span class="sxs-lookup"><span data-stu-id="41ba1-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="41ba1-178">Altre informazioni sono disponibili in questo articolo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="41ba1-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="41ba1-179">Configurare il listener nell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="41ba1-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="41ba1-180">Impostare l'autenticazione del certificato con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="41ba1-181">**winrm set winrm/config/Service/Auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="41ba1-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="41ba1-182">Un listener HTTPS WinRM con il certificato di autenticazione server deve esistere nel computer dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="41ba1-183">Questo può essere verificato con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="41ba1-184">**WinRM e winrm/config/listener**</span><span class="sxs-lookup"><span data-stu-id="41ba1-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="41ba1-185">Se il listener HTTPS non è visibile o se la stampa Thumb del listener HTTPS non è uguale alla stampa Thumb del certificato di autenticazione server nel computer agente di raccolta, è possibile eliminare il listener e crearne uno nuovo con la corretta stampa Thumb.</span><span class="sxs-lookup"><span data-stu-id="41ba1-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="41ba1-186">Per eliminare il listener HTTPS, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="41ba1-187">**winrm eliminare winrm/config/listener? Address = \* + Transport = HTTPS**</span><span class="sxs-lookup"><span data-stu-id="41ba1-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="41ba1-188">Per creare un nuovo listener, utilizzare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="41ba1-189">**WinRM creare winrm/config/listener? Address =&#42;+ Transport = HTTPS @ {hostname = "** &lt; _FQDN dell'agente di raccolta_ &gt; **"; CertificateThumbprint = "** &lt; _stampa Thumb del certificato di autenticazione server_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="41ba1-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="41ba1-190">Configurare il mapping dei certificati nell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="41ba1-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="41ba1-191">Creare un nuovo utente locale e aggiungerlo al gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="41ba1-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="41ba1-192">Creare il mapping dei certificati utilizzando un certificato presente nelle "autorità di certificazione radice attendibili" del computer o "autorità di certificazione intermedie".</span><span class="sxs-lookup"><span data-stu-id="41ba1-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="41ba1-193">Si tratta del certificato dell'autorità di certificazione radice o intermedia che ha emesso i certificati installati nei computer di origine dell'evento *(per evitare confusione, si tratta della CA immediatamente sopra il certificato nella catena di certificati)*:</span><span class="sxs-lookup"><span data-stu-id="41ba1-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="41ba1-194">**WinRM creare winrm/config/Service/mapping certificato?** = &lt; _Identificazione personale dell'autorità di certificazione del certificato della CA emittente_ &gt; **+ Subject =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **"; Password = "** &lt; _password_ &gt; **"}-remoto: localhost**</span><span class="sxs-lookup"><span data-stu-id="41ba1-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="41ba1-195">Da un client testare il listener e il mapping del certificato con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="41ba1-196">WinRM **g winrm/config-r:https://** &lt; _FQDN_ &gt; raccolta eventi **: 5986-a:certificate-certificate: "** &lt; _Identificazione personale del certificato_ &gt; di autenticazione client **"**</span><span class="sxs-lookup"><span data-stu-id="41ba1-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="41ba1-197">Questa operazione dovrebbe restituire la configurazione WinRM dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="41ba1-198">**Non spostare oltre** questo passaggio se la configurazione non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="41ba1-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="41ba1-199">**Cosa accade in questo passaggio?**</span><span class="sxs-lookup"><span data-stu-id="41ba1-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="41ba1-200">Il client si connette all'agente di raccolta eventi e invia il certificato specificato</span><span class="sxs-lookup"><span data-stu-id="41ba1-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="41ba1-201">L'agente di raccolta eventi cerca la CA emittente e controlla se è un mapping del certificato corrispondente</span><span class="sxs-lookup"><span data-stu-id="41ba1-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="41ba1-202">L'agente di raccolta eventi convalida la catena di certificati client e lo stato delle revoche</span><span class="sxs-lookup"><span data-stu-id="41ba1-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="41ba1-203">Se il passaggio precedente ha esito positivo, viene completata l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="41ba1-204">È possibile che si verifichi un errore di accesso negato per il metodo di autenticazione, che potrebbe essere fuorviante.</span><span class="sxs-lookup"><span data-stu-id="41ba1-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="41ba1-205">Per risolvere i problemi, controllare il registro CAPI nell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="41ba1-206">Elencare le voci mapping certificato configurate con il comando: **WinRM enum winrm/config/Service/mapping certificato**</span><span class="sxs-lookup"><span data-stu-id="41ba1-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="41ba1-207">Configurazione computer origine evento</span><span class="sxs-lookup"><span data-stu-id="41ba1-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="41ba1-208">Accedere con un account amministratore e aprire il Editor Criteri di gruppo locali (gpedit. msc)</span><span class="sxs-lookup"><span data-stu-id="41ba1-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="41ba1-209">Passare al computer locale Locale\configurazione computer\Modelli Amministrativi\componenti di Components\Event.</span><span class="sxs-lookup"><span data-stu-id="41ba1-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="41ba1-210">Aprire il criterio "configurare l'indirizzo del server, l'intervallo di aggiornamento e l'autorità di certificazione di un gestore delle sottoscrizioni di destinazione".</span><span class="sxs-lookup"><span data-stu-id="41ba1-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="41ba1-211">Abilitare il criterio e fare clic su SubscriptionManagers "Show..." pulsante.</span><span class="sxs-lookup"><span data-stu-id="41ba1-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="41ba1-212">Nella finestra SubscriptionManagers immettere la stringa seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="41ba1-213">**Server = https://** &lt; _FQDN del server_ &gt; dell'agente di raccolta eventi **: 5986/WSMan/SubscriptionManager/WEC, Refresh =** &lt; _Intervallo di aggiornamento in secondi_ &gt; **, IssuerCA =** &lt; _Identificazione personale del certificato della CA emittente_&gt;</span><span class="sxs-lookup"><span data-stu-id="41ba1-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="41ba1-214">Eseguire la seguente riga di comando per aggiornare le impostazioni di Criteri di gruppo locali: GPUpdate/Force</span><span class="sxs-lookup"><span data-stu-id="41ba1-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="41ba1-215">Questi passaggi dovrebbero produrre l'evento 104 nel computer di origine Visualizzatore eventi registri applicazioni e servizi Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational con il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="41ba1-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="41ba1-216">"Il server d'indirizzamento si è connesso correttamente al gestore delle sottoscrizioni al &lt; nome FQDN dell'indirizzo &gt; seguito dall'evento 100 con il messaggio:" la sottoscrizione &lt; sub_name &gt; viene creata correttamente ".</span><span class="sxs-lookup"><span data-stu-id="41ba1-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="41ba1-217">Nell'agente di raccolta eventi lo stato di runtime della sottoscrizione visualizzerà ora 1 computer attivo.</span><span class="sxs-lookup"><span data-stu-id="41ba1-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="41ba1-218">Aprire il registro ForwardedEvents nell'agente di raccolta eventi e verificare se gli eventi sono stati trasmessi dai computer di origine.</span><span class="sxs-lookup"><span data-stu-id="41ba1-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="41ba1-219">Concedere l'autorizzazione per la chiave privata del certificato client nell'origine evento</span><span class="sxs-lookup"><span data-stu-id="41ba1-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="41ba1-220">Aprire la console di gestione certificati per computer locale nel computer di origine dell'evento.</span><span class="sxs-lookup"><span data-stu-id="41ba1-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="41ba1-221">Fare clic con il pulsante destro del mouse sul certificato client quindi gestire le chiavi private.</span><span class="sxs-lookup"><span data-stu-id="41ba1-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="41ba1-222">Concedere l'autorizzazione di lettura per l'utente del servizio di rete.</span><span class="sxs-lookup"><span data-stu-id="41ba1-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="41ba1-223">Configurazione della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="41ba1-223">Event subscription configuration</span></span>

1. <span data-ttu-id="41ba1-224">Aprire Visualizzatore eventi nell'agente di raccolta eventi e passare al nodo sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="41ba1-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="41ba1-225">Fare clic con il pulsante destro del mouse su sottoscrizioni e scegliere "Crea sottoscrizione".</span><span class="sxs-lookup"><span data-stu-id="41ba1-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="41ba1-226">Assegnare un nome e una descrizione facoltativa per la nuova sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="41ba1-227">Selezionare l'opzione "origine computer avviata" e fare clic su "Seleziona gruppi di computer...".</span><span class="sxs-lookup"><span data-stu-id="41ba1-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="41ba1-228">In gruppi di computer fare clic su "Aggiungi computer non di dominio..."</span><span class="sxs-lookup"><span data-stu-id="41ba1-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="41ba1-229">e digitare il nome host dell'origine evento.</span><span class="sxs-lookup"><span data-stu-id="41ba1-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="41ba1-230">Fare clic su "Aggiungi certificati..."</span><span class="sxs-lookup"><span data-stu-id="41ba1-230">Click “Add Certificates…”</span></span> <span data-ttu-id="41ba1-231">e aggiungere il certificato dell'autorità di certificazione che rilascia i certificati client.</span><span class="sxs-lookup"><span data-stu-id="41ba1-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="41ba1-232">È possibile fare clic su Visualizza certificato per convalidare il certificato.</span><span class="sxs-lookup"><span data-stu-id="41ba1-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="41ba1-233">In autorità di certificazione fare clic su OK per aggiungere il certificato.</span><span class="sxs-lookup"><span data-stu-id="41ba1-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="41ba1-234">Al termine dell'aggiunta di computer, fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="41ba1-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="41ba1-235">Tornare alle proprietà della sottoscrizione, fare clic su Seleziona eventi...</span><span class="sxs-lookup"><span data-stu-id="41ba1-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="41ba1-236">Configurare il filtro di query degli eventi specificando i livelli di evento, i registri eventi o le origini eventi, gli ID evento e tutte le altre opzioni di filtro.</span><span class="sxs-lookup"><span data-stu-id="41ba1-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="41ba1-237">Tornare alle proprietà della sottoscrizione, fare clic su Avanzate...</span><span class="sxs-lookup"><span data-stu-id="41ba1-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="41ba1-238">Scegliere una delle opzioni di ottimizzazione per il recapito di eventi dall'evento di origine all'agente di raccolta eventi o lasciare il valore predefinito normale:</span><span class="sxs-lookup"><span data-stu-id="41ba1-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="41ba1-239">**Ridurre la larghezza di banda**: gli eventi verranno recapitati con una frequenza minore per risparmiare larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="41ba1-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="41ba1-240">**Riduzione della latenza**: gli eventi vengono recapitati non appena si verificano per ridurre la latenza degli eventi.</span><span class="sxs-lookup"><span data-stu-id="41ba1-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="41ba1-241">Modificare il protocollo in HTTPS e fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="41ba1-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="41ba1-242">Fare clic su OK per creare la nuova sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="41ba1-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="41ba1-243">Verificare lo stato di runtime della sottoscrizione facendo clic con il pulsante destro del mouse e scegliendo "stato Runtime".</span><span class="sxs-lookup"><span data-stu-id="41ba1-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>
