---
description: La classe SnmpNotification esegue il mapping dalla macro del tipo di notifica a una classe CIM incapsulata.
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
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530210"
---
# <a name="snmpnotification-class"></a>Classe SnmpNotification

La classe **SnmpNotification** esegue il mapping dalla macro del [tipo di notifica](notification-type-macro.md) a una classe CIM incapsulata. Si tratta di una classe di base utilizzata dal provider [SNMP](snmp-provider.md) per qualsiasi classe mappata dalla macro del [tipo di notifica](notification-type-macro.md) a una classe CIM incapsulata dal provider SNMP.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

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

La classe **SnmpNotification** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SnmpNotification** dispone di queste proprietà.

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete dell'entità che ha creato la notifica. Si tratta dell'indirizzo effettivo del dispositivo. Quando l'entità di gestione USA SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP. Quando l'entità di gestione utilizza SNMP su IPX, l'indirizzo di trasporto viene impostato su **null**. Questa proprietà è valida solo per SNMPv1.

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di trasporto utilizzato dall'entità mittente. Questa proprietà è valida per SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo di rete dell'entità che ha inviato la notifica. Si tratta dell'indirizzo dell'ultima entità che ha inviato la notifica. Quando l'entità di gestione USA SNMP su UDP, l'indirizzo di trasporto fa riferimento a un indirizzo IP. Quando l'entità di gestione utilizza SNMP su IPX, l'indirizzo di trasporto fa riferimento a un indirizzo IPX. Questa proprietà è valida per SNMPv1 e SNMPv2C.

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Protocollo di trasporto utilizzato dall'entità mittente.

</dd> <dt>

**Community**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della community associato a un'istanza della PDU. Il nome della community autentica il creatore della PDU. Questa proprietà è valida sia per SNMPv1 che per SNMPv2C.

</dd> <dt>

**Identificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **\_ convenzione testuale** ("OBJECTIDENTIFIER"), **codifica** ("OBJECTIDENTIFIER"), **\_ sintassi degli oggetti** ("OBJECTIDENTIFIER"), **\_ identificatore di oggetto** ("1.3.6.1.6.3.1.1.4.1")
</dt> </dl>

Identificazione autorevole della notifica. Esegue il mapping direttamente al binding della variabile SnmpTrapOID. Questa proprietà è valida solo per SNMPv2C.

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md). Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time). Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **\_ convenzione testuale** ("TimeTicks"), **codifica** ("TimeTicks"), **\_ sintassi degli oggetti** ("TimeTicks"), **\_ identificatore di oggetto** ("1.3.6.1.2.1.1.3")
</dt> </dl>

Tempo in centesimi di secondo dall'ultima reinizializzazione della parte relativa alla gestione della rete dell'agente. Variabile MIB sysUptime. 0, che è di tipo **INTEGER32**. Questa proprietà esegue il mapping al **timestamp** della proprietà della classe CIM, che è di tipo **UInt32**. Questa proprietà è valida solo per SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **timestamp** o **Identificazione** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **community** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>         |
| Server minimo supportato<br/> | Windows Server 2008<br/>   |
| Spazio dei nomi<br/>                | \\Localhost SNMP \\ radice<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Macro del tipo di notifica](notification-type-macro.md)
</dt> </dl>

 

