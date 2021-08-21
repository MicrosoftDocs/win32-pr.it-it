---
description: La classe SnmpExtendedNotification è la classe di base per qualsiasi classe mappata dalla macro NOTIFICATION-TYPE a una classe CIM dal provider SNMP.
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: Classe SnmpExtendedNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: d8da8533e9ac5c86dfa3291092fb5165b94e2e393e507c55f15b64c1e30cd6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816541"
---
# <a name="snmpextendednotification-class"></a>Classe SnmpExtendedNotification

La **classe SnmpExtendedNotification** è la classe di base per qualsiasi classe mappata dalla macro [NOTIFICATION-TYPE](notification-type-macro.md) a una classe CIM dal [provider SNMP.](snmp-provider.md)

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a>Members

La **classe SnmpExtendedNotification** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SnmpExtendedNotification** ha queste proprietà.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete dell'entità che ha creato la notifica. Questo è l'indirizzo effettivo del dispositivo. Quando l'entità di gestione usa SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP. Quando l'entità di gestione usa SNMP su IPX, l'indirizzo di trasporto è impostato su **NULL.** Questa proprietà è valida solo per SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di trasporto utilizzato dall'entità mittente. Questa proprietà è valida per SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete dell'entità che ha inviato la notifica. Si tratta dell'indirizzo dell'ultima entità che ha inoltrato la notifica. Quando l'entità di gestione usa SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP. Quando l'entità di gestione usa SNMP su IPX, l'indirizzo di trasporto fa riferimento a un indirizzo IPX. Questa proprietà è valida per SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di trasporto utilizzato dall'entità mittente.

</dd> <dt>

**Community**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Community nome associato a un'istanza della PDU. Il nome della community autentica l'origine della PDU. Questa proprietà è valida sia per SNMPv1 che per SNMPv2C.

</dd> <dt>

**Identificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: convenzione **testuale \_** ("OBJECTIDENTIFIER"), codifica ("OBJECTIDENTIFIER"), sintassi dell'oggetto ("OBJECTIDENTIFIER"), identificatore di oggetto ("1.3.6.1.6.3.1.1.4.1")  **\_** **\_**
</dt> </dl>

Identificazione autorevole della notifica. Mappe direttamente all'associazione di variabili SnmpTrapOID della voce MIB. Questa proprietà è valida solo per SNMPv2C.

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md). Per altre informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere [Costanti di sicurezza WMI.](wmi-security-constants.md)

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **convenzione testuale \_** ("TimeTicks"),  codifica ("TimeTicks"), sintassi dell'oggetto ("TimeTicks"), identificatore di oggetto ("1.3.6.1.2.1.1.3") **\_** **\_**
</dt> </dl>

Tempo in centesimi di secondo dall'ultima inizializzazione della parte di gestione di rete dell'agente. Viene mappato alla variabile MIB sysUptime.0, che è di tipo **INTEGER32.** Questa proprietà esegue il mapping alla proprietà della classe CIM **TimeStamp**, che è di **tipo uint32**. Questa proprietà è valida solo per SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una macro [NOTIFICATION-TYPE](notification-type-macro.md) che contiene riferimenti a una macro [OBJECT-TYPE](object-type-macro.md) denominata **TimeStamp** o **Identification** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

Una macro [NOTIFICATION-TYPE](notification-type-macro.md) che contiene riferimenti a una macro [OBJECT-TYPE](object-type-macro.md) denominata **Community** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Root \\ snmp \\ SMIR<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[NOTIFICATION-TYPE Macro](notification-type-macro.md)
</dt> </dl>

 

