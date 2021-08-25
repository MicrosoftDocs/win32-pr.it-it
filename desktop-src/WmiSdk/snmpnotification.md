---
description: La classe SnmpNotification esegue il mapping dalla macro NOTIFICATION-TYPE a una classe CIM incapsulata.
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: Classe SnmpNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: be0847c7a7d96fb7491274350c828d0cc319240823fa006e972bb295ad477773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860361"
---
# <a name="snmpnotification-class"></a>Classe SnmpNotification

La **classe SnmpNotification** esegue il mapping dalla macro [NOTIFICATION-TYPE](notification-type-macro.md) a una classe CIM incapsulata. Si tratta di una classe di base usata dal [provider SNMP](snmp-provider.md) per qualsiasi classe mappata dalla macro [NOTIFICATION-TYPE](notification-type-macro.md) a una classe CIM incapsulata dal provider SNMP.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="syntax"></a>Sintassi

``` syntax
class SnmpNotification : __ExtrinsicEvent
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

La **classe SnmpNotification** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SnmpNotification** ha queste proprietà.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete dell'entità che ha creato la notifica. Questo è l'indirizzo effettivo del dispositivo. Quando l'entità di gestione usa SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP. Quando l'entità di gestione usa SNMP su IPX, l'indirizzo di trasporto è impostato su **NULL.** Questa proprietà è valida solo per SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di trasporto utilizzato dall'entità mittente. Questa proprietà è valida per SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete dell'entità che ha inviato la notifica. Si tratta dell'indirizzo dell'ultima entità che ha inoltrato la notifica. Quando l'entità di gestione usa SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP. Quando l'entità di gestione usa SNMP su IPX, l'indirizzo di trasporto fa riferimento a un indirizzo IPX. Questa proprietà è valida per SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di trasporto utilizzato dall'entità mittente.

</dd> <dt>

**Community**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Community nome associato a un'istanza della PDU. Il nome della community autentica l'autore della PDU. Questa proprietà è valida sia per SNMPv1 che per SNMPv2C.

</dd> <dt>

**Identificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: convenzione **testuale \_** ("OBJECTIDENTIFIER"), codifica ("OBJECTIDENTIFIER"), sintassi dell'oggetto ("OBJECTIDENTIFIER"), identificatore di oggetto ("1.3.6.1.6.3.1.1.4.1")  **\_** **\_**
</dt> </dl>

Identificazione autorevole di questa notifica. Mappe direttamente all'associazione di variabili SnmpTrapOID. Questa proprietà è valida solo per SNMPv2C.

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md). Per altre informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere [Costanti di sicurezza WMI](wmi-security-constants.md).

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: convenzione **testuale \_** ("TimeTicks"), codifica ("TimeTicks"), sintassi dell'oggetto ("TimeTicks"), identificatore di oggetto ("1.3.6.1.2.1.1.3")  **\_** **\_**
</dt> </dl>

Tempo in centesimi di secondo dall'ultima inizializzazione della parte di gestione di rete dell'agente. Variabile MIB sysUptime.0, di tipo **INTEGER32**. Questa proprietà esegue il mapping alla proprietà della classe CIM **TimeStamp**, che è di tipo **uint32**. Questa proprietà è valida solo per SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una [macro NOTIFICATION-TYPE](notification-type-macro.md) che contiene riferimenti a una macro [OBJECT-TYPE](object-type-macro.md) denominata **TimeStamp** o **Identification** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà necessarie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

Una [macro NOTIFICATION-TYPE](notification-type-macro.md) che contiene riferimenti a una macro [OBJECT-TYPE](object-type-macro.md) denominata **Community** un conflitto di mapping. Se si verifica questo conflitto, le proprietà necessarie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>         |
| Server minimo supportato<br/> | Windows Server 2008<br/>   |
| Spazio dei nomi<br/>                | Localhost \\ snmp \\ radice<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[NOTIFICATION-TYPE Macro](notification-type-macro.md)
</dt> </dl>

 

