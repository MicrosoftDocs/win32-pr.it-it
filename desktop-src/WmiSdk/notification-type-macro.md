---
description: La macro del tipo di notifica contiene gli elementi seguenti.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Macro del tipo di notifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308846"
---
# <a name="notification-type-macro"></a>Macro del tipo di notifica

La macro del tipo di notifica contiene gli elementi seguenti.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Componenti

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descrittore di oggetto
</dt> <dd>

Connette un nome a un evento SNMP in una macro del tipo di notifica. Nell'elenco seguente sono elencate le regole per il mapping del descrittore di oggetti.



| Tipo                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome classe CIM incapsulato | "SNMP \_ "<br/> Nome identità modulo MIB<br/> carattere di sottolineatura ( \_ )<br/> descrittore di oggetto<br/> " \_ Notifica"<br/> Esempio: la notifica **vtpServerDisabled** da **Cisco-VTP-MIB** esegue il mapping alla **\_ notifica SNMP Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_**.<br/>                 |
| Nome della classe CIM riferente     | "SNMP \_ "<br/> Nome identità modulo MIB<br/> carattere di sottolineatura ( \_ )<br/> descrittore di oggetto<br/> " \_ ExtendedNotification"<br/> Esempio: la notifica **vtpServerDisabled** da **Cisco-VTP-MIB** viene mappata a **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Clausola OBJECTs
</dt> <dd>

Enumera il set di oggetti associati all'oggetto notifica.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Clausola REFERENCE
</dt> <dd>

Fa riferimento a un altro documento che contiene ulteriori informazioni sull'oggetto. Viene eseguito il mapping al **riferimento** al qualificatore di classe CIM, che è di tipo String.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Clausola DESCRIPTION
</dt> <dd>

Descrive l'oggetto in questione. Esegue il mapping alla **Descrizione** del qualificatore di classe CIM, che è di tipo stringa

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clausola STATUS
</dt> <dd>

Indica se l'oggetto deve essere supportato. Quando lo stato è **obsoleto** o **deprecato**, la notifica viene eliminata dal mapping. In caso contrario, questa clausola esegue il mapping allo **stato** del qualificatore della classe CIM, che è di tipo **String**.

Per SNMPv1, il valore preferito dello **stato** è **obbligatorio** o **facoltativo**, ma il qualificatore può contenere un altro valore. Per SNMPv2C, il valore preferito dello **stato** è **Current** o **deprecato**, ma il qualificatore può contenere un altro valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider SNMP esegue il mapping della macro del **tipo di notifica** a una definizione di classe incapsulata o referente.

Una definizione di classe incapsulata non espone le informazioni sull'istanza associate all'oggetto MIB. Al contrario, la definizione di classe codifica la clausola OBJECTs come una serie di proprietà della classe di evento CIM. Ogni proprietà CIM riflette il nome, il tipo e il valore dell'oggetto MIB corrispondente nella clausola OBJECTs. Se sono necessarie informazioni sull'istanza, è necessario eseguire il mapping a una classe referente. Viene eseguito il mapping di una definizione di classe incapsulata alla classe [SnmpNotification](snmpnotification.md) .

Una classe referente definisce un oggetto MIB e le informazioni sull'istanza utilizzate per ottenere l'oggetto. La definizione di classe codifica la clausola OBJECTs come una serie di proprietà della classe di evento CIM. Ogni proprietà CIM riflette il nome dell'oggetto MIB corrispondente nella clausola OBJECTs e il tipo come oggetto incorporato che riflette un'istanza della classe associata a tale oggetto MIB. Il provider genera quindi una classe associata all'oggetto MIB. Ad esempio, **ifindex** esegue il mapping a una classe incorporata denominata **SNMP \_ RFC1213 \_ MIB \_ ifindex**. Per ulteriori informazioni su questo tipo di classe, vedere [macro di tipo di oggetto](object-type-macro.md).

 

 




