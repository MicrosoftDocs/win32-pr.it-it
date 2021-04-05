---
description: I qualificatori contengono informazioni sul contesto specifiche dell'implementazione e proprietà del trasporto che definiscono il modo in cui il provider SNMP accede a un agente SNMP. Di seguito sono elencati i qualificatori specifici del provider SNMP.
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: Qualificatori specifici del provider SNMP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753674"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="842bc-104">Qualificatori specifici del provider SNMP</span><span class="sxs-lookup"><span data-stu-id="842bc-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="842bc-105">I qualificatori contengono informazioni sul contesto specifiche dell'implementazione e proprietà del trasporto che definiscono il modo in cui il provider SNMP accede a un agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="842bc-106">Di seguito sono elencati i qualificatori specifici del provider SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="842bc-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="842bc-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-108">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="842bc-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="842bc-109">Indirizzo di trasporto associato all'agente SNMP, ad esempio un indirizzo IP o un nome DNS.</span><span class="sxs-lookup"><span data-stu-id="842bc-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="842bc-110">È necessario impostare **AgentAddress** su un indirizzo host unicast valido o un nome host di dominio che può essere risolto tramite il processo di risoluzione dei nomi di dominio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="842bc-111">**AgentAddress** non ha alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="842bc-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span><span class="sxs-lookup"><span data-stu-id="842bc-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-113">Tipo di dati: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="842bc-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="842bc-114">Numero massimo di richieste SNMP in attesa simultanee che è possibile inviare a questo agente mentre non è stata ancora ricevuta una risposta.</span><span class="sxs-lookup"><span data-stu-id="842bc-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="842bc-115">Una richiesta SNMP viene considerata in attesa fino a quando non viene ricevuta una risposta PDU o si è verificato un timeout. Le dimensioni di una finestra di grandi dimensioni in genere migliorano le prestazioni, ma alcuni agenti potrebbero non funzionare bene con un carico elevato.</span><span class="sxs-lookup"><span data-stu-id="842bc-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="842bc-116">**AgentFlowControlWindowSize** può essere impostato su 0 per indicare una dimensione infinita della finestra o un numero intero compreso tra 1 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="842bc-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="842bc-117">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="842bc-117">The default value is 10.</span></span> <span data-ttu-id="842bc-118">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span><span class="sxs-lookup"><span data-stu-id="842bc-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-120">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="842bc-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="842bc-121">Stringa di ottetto a lunghezza variabile utilizzata dall'agente SNMP per autenticare un'unità dati del protocollo SNMP durante un'operazione di lettura (richieste GET/GET successive SNMP).</span><span class="sxs-lookup"><span data-stu-id="842bc-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="842bc-122">È necessario eseguire il mapping del nome comunità a una stringa Unicode ed è limitato a caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="842bc-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="842bc-123">Il valore predefinito è public.</span><span class="sxs-lookup"><span data-stu-id="842bc-123">The default value is public.</span></span> <span data-ttu-id="842bc-124">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span><span class="sxs-lookup"><span data-stu-id="842bc-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-126">Tipo di dati: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="842bc-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="842bc-127">Numero di volte in cui è possibile ritentare una singola richiesta SNMP quando non è presente alcuna risposta da parte dell'agente SNMP prima che la richiesta venga considerata non riuscita.</span><span class="sxs-lookup"><span data-stu-id="842bc-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="842bc-128">**AgentRetryCount** deve essere impostato su un numero intero compreso tra 0 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="842bc-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="842bc-129">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="842bc-129">The default value is 1.</span></span> <span data-ttu-id="842bc-130">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="842bc-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-132">Tipo di dati: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="842bc-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="842bc-133">Tempo in millisecondi prima che venga considerata eliminata l'unità dati del protocollo SNMP (PDU).</span><span class="sxs-lookup"><span data-stu-id="842bc-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="842bc-134">Il numero di millisecondi di attesa per la risposta a una richiesta SNMP inviata all'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="842bc-135">**AgentRetryTimeout** deve essere impostato su un numero intero compreso tra 0 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="842bc-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="842bc-136">Il valore predefinito è 500.</span><span class="sxs-lookup"><span data-stu-id="842bc-136">The default value is 500.</span></span> <span data-ttu-id="842bc-137">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span><span class="sxs-lookup"><span data-stu-id="842bc-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-139">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="842bc-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="842bc-140">Versione del protocollo SNMP da utilizzare durante la comunicazione con l'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="842bc-141">Attualmente, gli unici valori validi sono 1 (per SNMPv1) e 2C (per SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="842bc-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="842bc-142">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="842bc-142">The default value is 1.</span></span> <span data-ttu-id="842bc-143">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="842bc-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-145">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="842bc-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="842bc-146">Protocollo di trasporto utilizzato per comunicare con l'agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="842bc-147">Attualmente gli unici valori validi sono Internet Protocol (IP) e Internet Packet Exchange (IPX).</span><span class="sxs-lookup"><span data-stu-id="842bc-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="842bc-148">Il valore predefinito è IP.</span><span class="sxs-lookup"><span data-stu-id="842bc-148">The default value is IP.</span></span> <span data-ttu-id="842bc-149">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span><span class="sxs-lookup"><span data-stu-id="842bc-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-151">Tipo di dati: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="842bc-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="842bc-152">Numero massimo di associazioni di variabili contenute in una singola PDU SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="842bc-153">Ogni richiesta SNMP inviata all'agente SNMP contiene una o più variabili SNMP.</span><span class="sxs-lookup"><span data-stu-id="842bc-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="842bc-154">Questo parametro specifica il numero massimo di variabili che è possibile includere in una singola richiesta.</span><span class="sxs-lookup"><span data-stu-id="842bc-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="842bc-155">**AgentVarBindsPerPdu** può essere impostato su 0 (zero) per fare in modo che l'implementazione determini i binding variabili ottimali o un numero intero compreso tra 1 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="842bc-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="842bc-156">Si noti che, mentre l'aumento di questo valore può migliorare le prestazioni, alcuni agenti e reti non possono gestire la richiesta risultante.</span><span class="sxs-lookup"><span data-stu-id="842bc-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="842bc-157">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="842bc-157">The default value is 10.</span></span> <span data-ttu-id="842bc-158">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="842bc-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span><span class="sxs-lookup"><span data-stu-id="842bc-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="842bc-160">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="842bc-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="842bc-161">Stringa di ottetto a lunghezza variabile utilizzata dall'agente SNMP per autenticare un'unità dati del protocollo SNMP durante un'operazione di scrittura (richiesta SET SNMP).</span><span class="sxs-lookup"><span data-stu-id="842bc-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="842bc-162">È necessario eseguire il mapping del nome comunità a una stringa Unicode ed è limitato a caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="842bc-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="842bc-163">Il valore predefinito è public.</span><span class="sxs-lookup"><span data-stu-id="842bc-163">The default value is public.</span></span> <span data-ttu-id="842bc-164">Questo qualificatore è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="842bc-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="842bc-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="842bc-165">Requirements</span></span>



| <span data-ttu-id="842bc-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="842bc-166">Requirement</span></span> | <span data-ttu-id="842bc-167">Valore</span><span class="sxs-lookup"><span data-stu-id="842bc-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="842bc-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="842bc-168">Minimum supported client</span></span><br/> | <span data-ttu-id="842bc-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="842bc-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="842bc-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="842bc-170">Minimum supported server</span></span><br/> | <span data-ttu-id="842bc-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="842bc-171">Windows Server 2008</span></span><br/> |



 

 




