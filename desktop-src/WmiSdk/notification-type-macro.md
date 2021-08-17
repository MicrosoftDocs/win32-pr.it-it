---
description: La macro NOTIFICATION-TYPE contiene gli elementi seguenti.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: NOTIFICATION-TYPE Macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e50146d6a6fc71cc78baccd97a7dffc9e4ed4e7091373dd52ae42b2fbc6b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992741"
---
# <a name="notification-type-macro"></a>NOTIFICATION-TYPE Macro

La macro NOTIFICATION-TYPE contiene gli elementi seguenti.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Componenti

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descrittore di oggetti
</dt> <dd>

Associa un nome a un evento SNMP in una macro NOTIFICATION-TYPE. Nell'elenco seguente sono elencate le regole per il mapping del descrittore di oggetto.



| Tipo                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome della classe CIM incapsulata | "SNMP \_ "<br/> Nome dell'identità del modulo MIB<br/> carattere di sottolineatura ( \_ )<br/> descrittore di oggetti<br/> \_"Notification"<br/> Esempio: la **notifica vtpServerDisabled** da **CISCO-VTP-MIB** esegue il mapping a **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ Notification**.<br/>                 |
| Nome della classe CIM referenziato     | "SNMP \_ "<br/> Nome dell'identità del modulo MIB<br/> carattere di sottolineatura ( \_ )<br/> descrittore di oggetti<br/> \_"ExtendedNotification"<br/> Esempio: la **notifica vtpServerDisabled** da **CISCO-VTP-MIB** esegue il mapping a **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Clausola OBJECTS
</dt> <dd>

Enumera il set di oggetti associati all'oggetto notifica.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Clausola REFERENCE
</dt> <dd>

Fa riferimento a un altro documento che contiene altre informazioni sull'oggetto. Esegue il mapping al riferimento del qualificatore di **classe** CIM , che è di tipo string.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Clausola DESCRIPTION
</dt> <dd>

Descrive l'oggetto in questione. Esegue il mapping al qualificatore di classe CIM **Description**, che è di tipo string

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clausola STATUS
</dt> <dd>

Indica se l'oggetto deve essere supportato. Quando lo stato è **obsoleto** **o deprecato,** la notifica viene rimossa dal mapping. In caso contrario, questa clausola esegue il mapping al qualificatore di classe CIM **Status**, che è di tipo **string**.

Per SNMPv1, il valore preferito di **Status** è **obbligatorio** o **facoltativo,** ma il qualificatore può contenere un altro valore. Per SNMPv2C, il valore preferito di **Status** è **current** o **deprecato,** ma il qualificatore può contenere un altro valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider SNMP esegue il mapping della macro **NOTIFICATION-TYPE** a una definizione di classe incapsulata o referenziata.

Una definizione di classe incapsulata non espone le informazioni sull'istanza associate all'oggetto MIB. Al contrario, la definizione della classe codifica la clausola OBJECTS come una serie di proprietà della classe di evento CIM. Ogni proprietà CIM riflette il nome, il tipo e il valore dell'oggetto MIB corrispondente nella clausola OBJECTS. Se sono necessarie informazioni sull'istanza, è necessario eseguire il mapping a una classe referent. Una definizione di classe incapsulata esegue il mapping [alla classe SnmpNotification.](snmpnotification.md)

Una classe referent definisce un oggetto MIB e le informazioni sull'istanza utilizzate per ottenere l'oggetto. La definizione della classe codifica la clausola OBJECTS come una serie di proprietà della classe di evento CIM. Ogni proprietà CIM riflette il nome dell'oggetto MIB corrispondente nella clausola OBJECTS e il tipo come oggetto incorporato che riflette un'istanza della classe associata a tale oggetto MIB. Il provider genera quindi una classe associata all'oggetto MIB. Ad esempio, **ifIndex esegue** il mapping a una classe incorporata denominata **SNMP \_ RFC1213 \_ MIB \_ ifIndex**. Per altre informazioni su questo tipo di classe, vedere [Object-TYPE Macro](object-type-macro.md).

 

 




