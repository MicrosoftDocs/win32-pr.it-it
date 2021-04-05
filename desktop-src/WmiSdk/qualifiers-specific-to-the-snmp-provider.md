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
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Qualificatori specifici del provider SNMP

I qualificatori contengono informazioni sul contesto specifiche dell'implementazione e proprietà del trasporto che definiscono il modo in cui il provider SNMP accede a un agente SNMP. Di seguito sono elencati i qualificatori specifici del provider SNMP.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Tipo di dati **: \_ stringa CIM**

Indirizzo di trasporto associato all'agente SNMP, ad esempio un indirizzo IP o un nome DNS. È necessario impostare **AgentAddress** su un indirizzo host unicast valido o un nome host di dominio che può essere risolto tramite il processo di risoluzione dei nomi di dominio del sistema operativo. **AgentAddress** non ha alcun valore predefinito.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

Tipo di dati: **CIM \_ SINT32**

Numero massimo di richieste SNMP in attesa simultanee che è possibile inviare a questo agente mentre non è stata ancora ricevuta una risposta. Una richiesta SNMP viene considerata in attesa fino a quando non viene ricevuta una risposta PDU o si è verificato un timeout. Le dimensioni di una finestra di grandi dimensioni in genere migliorano le prestazioni, ma alcuni agenti potrebbero non funzionare bene con un carico elevato. **AgentFlowControlWindowSize** può essere impostato su 0 per indicare una dimensione infinita della finestra o un numero intero compreso tra 1 e 2 ^ 32-1. Il valore predefinito è 10. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

Tipo di dati **: \_ stringa CIM**

Stringa di ottetto a lunghezza variabile utilizzata dall'agente SNMP per autenticare un'unità dati del protocollo SNMP durante un'operazione di lettura (richieste GET/GET successive SNMP). È necessario eseguire il mapping del nome comunità a una stringa Unicode ed è limitato a caratteri alfanumerici. Il valore predefinito è public. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

Tipo di dati: **CIM \_ SINT32**

Numero di volte in cui è possibile ritentare una singola richiesta SNMP quando non è presente alcuna risposta da parte dell'agente SNMP prima che la richiesta venga considerata non riuscita. **AgentRetryCount** deve essere impostato su un numero intero compreso tra 0 e 2 ^ 32-1. Il valore predefinito è 1. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

Tipo di dati: **CIM \_ SINT32**

Tempo in millisecondi prima che venga considerata eliminata l'unità dati del protocollo SNMP (PDU). Il numero di millisecondi di attesa per la risposta a una richiesta SNMP inviata all'agente SNMP. **AgentRetryTimeout** deve essere impostato su un numero intero compreso tra 0 e 2 ^ 32-1. Il valore predefinito è 500. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

Tipo di dati **: \_ stringa CIM**

Versione del protocollo SNMP da utilizzare durante la comunicazione con l'agente SNMP. Attualmente, gli unici valori validi sono 1 (per SNMPv1) e 2C (per SNMPv2C). Il valore predefinito è 1. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

Tipo di dati **: \_ stringa CIM**

Protocollo di trasporto utilizzato per comunicare con l'agente SNMP. Attualmente gli unici valori validi sono Internet Protocol (IP) e Internet Packet Exchange (IPX). Il valore predefinito è IP. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

Tipo di dati: **CIM \_ SINT32**

Numero massimo di associazioni di variabili contenute in una singola PDU SNMP. Ogni richiesta SNMP inviata all'agente SNMP contiene una o più variabili SNMP. Questo parametro specifica il numero massimo di variabili che è possibile includere in una singola richiesta. **AgentVarBindsPerPdu** può essere impostato su 0 (zero) per fare in modo che l'implementazione determini i binding variabili ottimali o un numero intero compreso tra 1 e 2 ^ 32-1. Si noti che, mentre l'aumento di questo valore può migliorare le prestazioni, alcuni agenti e reti non possono gestire la richiesta risultante. Il valore predefinito è 10. Questo qualificatore è facoltativo.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

Tipo di dati **: \_ stringa CIM**

Stringa di ottetto a lunghezza variabile utilizzata dall'agente SNMP per autenticare un'unità dati del protocollo SNMP durante un'operazione di scrittura (richiesta SET SNMP). È necessario eseguire il mapping del nome comunità a una stringa Unicode ed è limitato a caratteri alfanumerici. Il valore predefinito è public. Questo qualificatore è facoltativo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

 




