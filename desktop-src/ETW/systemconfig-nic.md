---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Classe SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966713"
---
# <a name="systemconfig_nic-class"></a>\_Classe NIC SystemConfig

Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>Members

La **classe \_ NIC SystemConfig** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ NIC SystemConfig** dispone di queste proprietà.

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Indirizzi IP da utilizzare nell'esecuzione di query per i server DNS. L'elenco di indirizzi è delimitato da virgole.

</dd> <dt>

IpAddresses
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Indirizzi IP associati alla scheda di interfaccia di rete. L'elenco di indirizzi è delimitato da virgole.

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Indice dell'adapter per la scheda di interfaccia di rete IPv4. È possibile che l'indice dell'adapter venga modificato quando un adapter viene disabilitato e quindi abilitato oppure in altre circostanze e non deve essere considerato persistente.

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Indice dell'adapter per la scheda di interfaccia di rete IPv6. È possibile che l'indice dell'adapter venga modificato quando un adapter viene disabilitato e quindi abilitato oppure in altre circostanze e non deve essere considerato persistente.

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Descrizione della scheda.

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Format ("x")
</dt> </dl>

Indirizzo hardware per la scheda.

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Lunghezza dell'indirizzo hardware per la scheda.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




