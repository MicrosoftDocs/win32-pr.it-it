---
description: La classe SnmpExtendedNotification è la classe di base per qualsiasi classe mappata dalla macro del tipo di notifica a una classe CIM dal provider SNMP.
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
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309878"
---
# <a name="snmpextendednotification-class"></a>Classe SnmpExtendedNotification

La classe **SnmpExtendedNotification** è la classe di base per qualsiasi classe mappata dalla macro del [tipo di notifica](notification-type-macro.md) a una classe CIM dal [provider SNMP](snmp-provider.md).

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

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

La classe **SnmpExtendedNotification** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SnmpExtendedNotification** dispone di queste proprietà.

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

Identificazione autorevole della notifica. Esegue il mapping direttamente alla voce MIB SnmpTrapOID binding della variabile. Questa proprietà è valida solo per SNMPv2C.

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

Tempo in centesimi di secondo dall'ultima reinizializzazione della parte relativa alla gestione della rete dell'agente. Viene eseguito il mapping alla variabile MIB sysUptime. 0, che è di tipo **INTEGER32**. Questa proprietà esegue il mapping al **timestamp** della proprietà della classe CIM, che è di tipo **UInt32**. Questa proprietà è valida solo per SNMPv2C.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **timestamp** o **Identificazione** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

Una macro del [tipo di notifica](notification-type-macro.md) che contiene riferimenti a una macro di [tipo oggetto](object-type-macro.md) denominata **community** causa un conflitto di mapping. Se si verifica questo conflitto, le proprietà obbligatorie hanno la precedenza e i riferimenti in conflitto devono essere rinominati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\Archivio SMIR SNMP \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[Macro del tipo di notifica](notification-type-macro.md)
</dt> </dl>

 

