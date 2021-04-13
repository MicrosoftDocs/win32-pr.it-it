---
title: Gerarchia del modello a oggetti
description: Gli oggetti nel modello a oggetti SDO sono disposti in una gerarchia. Questo significa che gli oggetti in SDO forniscono l'accesso ad altri oggetti in SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399305"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="22cef-104">Gerarchia del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="22cef-104">Object Model Hierarchy</span></span>

<span data-ttu-id="22cef-105">Gli oggetti nel modello a oggetti SDO sono disposti in una gerarchia.</span><span class="sxs-lookup"><span data-stu-id="22cef-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="22cef-106">Questo significa che gli oggetti in SDO forniscono l'accesso ad altri oggetti in SDO.</span><span class="sxs-lookup"><span data-stu-id="22cef-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="22cef-107">Gli oggetti consentono di accedere ad altri oggetti in due modi.</span><span class="sxs-lookup"><span data-stu-id="22cef-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="22cef-108">Un modo consiste nell'esporre un'interfaccia che fornisce metodi per il recupero di altri oggetti da parte dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="22cef-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="22cef-109">Un esempio di questo approccio è l'oggetto computer.</span><span class="sxs-lookup"><span data-stu-id="22cef-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="22cef-110">L'oggetto computer espone l'interfaccia [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="22cef-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="22cef-111">Il metodo [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera un oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="22cef-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="22cef-112">Il metodo [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="22cef-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![oggetto computer che espone l'interfaccia isdomachine](images/sdo01.png)

<span data-ttu-id="22cef-114">Per ulteriori informazioni, vedere [ottenere il servizio e l'utente SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span><span class="sxs-lookup"><span data-stu-id="22cef-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="22cef-115">Il secondo modo in cui gli oggetti forniscono l'accesso ad altri oggetti è che una raccolta di oggetti viene rappresentata come una proprietà dell'oggetto che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="22cef-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="22cef-116">Per recuperare una raccolta di oggetti, chiamare [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) sulla proprietà di un oggetto che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="22cef-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="22cef-117">Ad esempio, per recuperare la raccolta di criteri, chiamare **ISdo:: GetProperty** sull'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) esposta dall'oggetto NPS.</span><span class="sxs-lookup"><span data-stu-id="22cef-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="22cef-118">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="22cef-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![recupero della raccolta di criteri](images/sdo02.png)

<span data-ttu-id="22cef-120">Per il codice di esempio che recupera la raccolta di criteri, vedere [recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection).</span><span class="sxs-lookup"><span data-stu-id="22cef-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="22cef-121">L' [**oggetto dati del server NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) presenta le proprietà seguenti che rappresentano le raccolte:</span><span class="sxs-lookup"><span data-stu-id="22cef-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="22cef-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Revisori</span><span class="sxs-lookup"><span data-stu-id="22cef-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="22cef-123">L'unico revisore della raccolta revisori è il [**registro eventi NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span><span class="sxs-lookup"><span data-stu-id="22cef-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="22cef-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Criteri</span><span class="sxs-lookup"><span data-stu-id="22cef-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="22cef-125">Ogni [**oggetto Policy**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) dispone di una proprietà che rappresenta una raccolta di condizioni.</span><span class="sxs-lookup"><span data-stu-id="22cef-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="22cef-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profili</span><span class="sxs-lookup"><span data-stu-id="22cef-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="22cef-127">Ogni [**oggetto profilo**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) nelle raccolte di profili dispone di una proprietà che rappresenta una raccolta di attributi.</span><span class="sxs-lookup"><span data-stu-id="22cef-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="22cef-128">Per un elenco degli attributi supportati da SDO, vedere [attributi supportati da SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) .</span><span class="sxs-lookup"><span data-stu-id="22cef-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="22cef-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolli</span><span class="sxs-lookup"><span data-stu-id="22cef-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="22cef-130">La raccolta Protocols contiene l'oggetto protocollo RADIUS, che contiene una raccolta clients che rappresenta i client RADIUS.</span><span class="sxs-lookup"><span data-stu-id="22cef-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="22cef-131">Vedere [aggiunta di un client](/windows/desktop/Nps/sdo-adding-a-client) per il codice di esempio che illustra come recuperare la raccolta client.</span><span class="sxs-lookup"><span data-stu-id="22cef-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="22cef-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Criteri proxy</span><span class="sxs-lookup"><span data-stu-id="22cef-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="22cef-133">Questa raccolta contiene i criteri di accesso alla rete utilizzati per l'elaborazione delle richieste di connessione.</span><span class="sxs-lookup"><span data-stu-id="22cef-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="22cef-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Profili proxy</span><span class="sxs-lookup"><span data-stu-id="22cef-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="22cef-135">Questa raccolta contiene i profili utilizzati per l'elaborazione della richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="22cef-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="22cef-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Gruppi di server RADIUS</span><span class="sxs-lookup"><span data-stu-id="22cef-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="22cef-137">Ogni [**gruppo di server RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) nella raccolta di gruppi di server RADIUS dispone di una proprietà che rappresenta la raccolta di server in tale gruppo di server.</span><span class="sxs-lookup"><span data-stu-id="22cef-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="22cef-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Gestori di richieste</span><span class="sxs-lookup"><span data-stu-id="22cef-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="22cef-139">Questa raccolta contiene la raccolta "Microsoft Realms Evaluator".</span><span class="sxs-lookup"><span data-stu-id="22cef-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="22cef-140">In questa raccolta sono disponibili anche le impostazioni "autenticazione SAM Microsoft NT" e "Accounting Microsoft".</span><span class="sxs-lookup"><span data-stu-id="22cef-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="22cef-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22cef-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22cef-142">Oggetti e proprietà di SDO</span><span class="sxs-lookup"><span data-stu-id="22cef-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="22cef-143">Attributi supportati da SDO</span><span class="sxs-lookup"><span data-stu-id="22cef-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 