---
title: Interfacce di virtualizzazione Desktop remoto
description: L'API di virtualizzazione Desktop remoto supporta le interfacce seguenti.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338279"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="0eabf-103">Interfacce di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0eabf-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="0eabf-104">L'API di virtualizzazione Desktop remoto supporta le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="0eabf-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0eabf-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0eabf-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="0eabf-106">**ITsSbBaseNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-107">Espone metodi che segnalano messaggi di stato e di errore a Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="0eabf-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-108">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="0eabf-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="0eabf-109">Espone i metodi e le proprietà che archiviano le informazioni sullo stato relative a una richiesta di connessione in ingresso da un client Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="0eabf-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-110">**ITsSbClientConnectionPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0eabf-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="0eabf-111">Può essere usato per definire le proprietà personalizzate di una connessione client nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="0eabf-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-112">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="0eabf-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="0eabf-113">Espone metodi e proprietà che contengono informazioni sull'ambiente che ospita il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0eabf-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="0eabf-114">Questa interfaccia può essere utilizzata per archiviare le informazioni su un server fisico che ospita macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0eabf-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-115">**ITsSbEnvironmentPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0eabf-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="0eabf-116">Può essere usato per definire le proprietà personalizzate di un ambiente che ospita i computer di destinazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0eabf-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-117">**ITsSbFilterPluginStore**</span><span class="sxs-lookup"><span data-stu-id="0eabf-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="0eabf-118">Filtra archivio plug-in</span><span class="sxs-lookup"><span data-stu-id="0eabf-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-119">**ITsSbGenericNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-120">Espone metodi che segnalano il completamento di e ottiene il tempo di attesa dal gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-121">**ITsSbGlobalStore**</span><span class="sxs-lookup"><span data-stu-id="0eabf-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="0eabf-122">Espone metodi che eseguono query per computer di destinazione, sessioni, ambienti e farm che sono stati aggiunti all'archivio gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-123">**ITsSbLoadBalanceResult**</span><span class="sxs-lookup"><span data-stu-id="0eabf-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="0eabf-124">Espone metodi e proprietà che archiviano il nome di destinazione restituito da un algoritmo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="0eabf-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-125">**ITsSbLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="0eabf-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="0eabf-126">Espone metodi che è possibile usare per fornire un algoritmo di bilanciamento del carico personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0eabf-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-127">**ITsSbLoadBalancingNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-128">Espone metodi che restituiscono il risultato di un algoritmo di bilanciamento del carico a gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-129">**ITsSbOrchestration**</span><span class="sxs-lookup"><span data-stu-id="0eabf-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="0eabf-130">Espone i metodi utilizzati da gestore connessione Desktop remoto per assicurarsi che la destinazione sia pronta prima di reindirizzare un client.</span><span class="sxs-lookup"><span data-stu-id="0eabf-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-131">**ITsSbOrchestrationNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-132">Espone metodi che restituiscono un oggetto [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) al gestore connessione Desktop remoto dopo che la destinazione è stata preparata correttamente per una connessione.</span><span class="sxs-lookup"><span data-stu-id="0eabf-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-133">**ITsSbPlacement**</span><span class="sxs-lookup"><span data-stu-id="0eabf-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="0eabf-134">Espone metodi che preparano l'ambiente (il computer che ospita la macchina virtuale).</span><span class="sxs-lookup"><span data-stu-id="0eabf-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-135">**ITsSbPlacementNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-136">Espone metodi che restituiscono informazioni sugli ambienti al gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-137">**ITsSbPlugin**</span><span class="sxs-lookup"><span data-stu-id="0eabf-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="0eabf-138">Espone metodi che inizializzano e terminano plug-in.</span><span class="sxs-lookup"><span data-stu-id="0eabf-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-139">**ITsSbPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-140">Espone metodi che notificano a gestore connessione Desktop remoto l'inizializzazione o la terminazione di un plug-in.</span><span class="sxs-lookup"><span data-stu-id="0eabf-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-141">**ITsSbPluginPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0eabf-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="0eabf-142">Può essere usato per definire le proprietà del plug-in personalizzato in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0eabf-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-143">**ITsSbPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0eabf-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="0eabf-144">Può essere usato per definire le proprietà personalizzate nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="0eabf-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-145">**ITsSbProvider**</span><span class="sxs-lookup"><span data-stu-id="0eabf-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="0eabf-146">Espone metodi che creano implementazioni predefinite di oggetti utilizzati nella virtualizzazione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-147">**ITsSbProvisioning**</span><span class="sxs-lookup"><span data-stu-id="0eabf-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="0eabf-148">Espone metodi che creano e gestiscono macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0eabf-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-149">**ITsSbProvisioningPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-150">Espone metodi che notificano a gestore connessione Desktop remoto il provisioning delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0eabf-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-151">**ITsSbResourceNotification**</span><span class="sxs-lookup"><span data-stu-id="0eabf-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="0eabf-152">Espone i metodi utilizzati da gestore connessione Desktop remoto per notificare i plug-in delle modifiche di stato che si verificano negli oggetti sessione, destinazione e connessione client.</span><span class="sxs-lookup"><span data-stu-id="0eabf-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-153">**ITsSbResourceNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="0eabf-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="0eabf-154">Espone i metodi utilizzati da gestore connessione Desktop remoto per notificare i plug-in delle modifiche di stato che si verificano negli oggetti sessione, destinazione e connessione client.</span><span class="sxs-lookup"><span data-stu-id="0eabf-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-155">**ITsSbResourcePlugin**</span><span class="sxs-lookup"><span data-stu-id="0eabf-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="0eabf-156">Espone metodi che estendono le funzionalità di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-157">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="0eabf-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="0eabf-158">Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.</span><span class="sxs-lookup"><span data-stu-id="0eabf-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-159">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="0eabf-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="0eabf-160">Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.</span><span class="sxs-lookup"><span data-stu-id="0eabf-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-161">**ITsSbServiceNotification**</span><span class="sxs-lookup"><span data-stu-id="0eabf-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="0eabf-162">Espone i metodi utilizzati da gestore connessione Desktop remoto per notificare i plug-in delle modifiche di stato che si verificano nel gestore connessione Desktop remoto stesso.</span><span class="sxs-lookup"><span data-stu-id="0eabf-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-163">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="0eabf-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="0eabf-164">Espone le proprietà che archiviano le informazioni relative a una sessione utente.</span><span class="sxs-lookup"><span data-stu-id="0eabf-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-165">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="0eabf-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="0eabf-166">Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0eabf-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-167">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="0eabf-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="0eabf-168">Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0eabf-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-169">**ITsSbTargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0eabf-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="0eabf-170">Derivare da questa interfaccia per definire un set di proprietà di destinazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0eabf-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-171">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="0eabf-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="0eabf-172">Espone le proprietà utilizzate da Connessione Desktop remoto broker per impostare la coda di un plug-in.</span><span class="sxs-lookup"><span data-stu-id="0eabf-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-173">**ITsSbTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="0eabf-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="0eabf-174">Espone metodi che aggiornano la coda delle attività per i plug-in di Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="0eabf-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-175">**ITsSbTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0eabf-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="0eabf-176">Espone metodi che segnalano lo stato e i messaggi di errore relativi alle attività al gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0eabf-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="0eabf-177">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="0eabf-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="0eabf-178">Utilizzato per estendere le funzionalità di gestore sessioni Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="0eabf-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="0eabf-179">Implementare questa interfaccia quando si desidera fornire un plug-in che esegue l'override della logica di reindirizzamento di broker di sessione di Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="0eabf-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 