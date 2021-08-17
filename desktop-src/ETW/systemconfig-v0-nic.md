---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6abe9356ce222d8f461509ec9cfa25ab0a49b8583022ee5e1d832cf29a226dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746471"
---
# <a name="systemconfig_v0_nic-class"></a>Classe NIC SystemConfig \_ V0 \_

Questa classe è la classe del tipo di evento per gli eventi di configurazione della scheda di interfaccia di rete.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a>Members

La **classe NIC SystemConfig \_ V0 \_** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe NIC SystemConfig \_ V0 \_** ha queste proprietà.

<dl> <dt>

**Dati**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (16)
</dt> </dl>

Campo dati.

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8)
</dt> </dl>

Indirizzo IP del server DHCP (Dynamic Host Configuration Protocol). Il valore 255.255.255.255 indica che il server DHCP non è stato raggiunto o è in corso di raggiungere. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (12)
</dt> </dl>

Primo indirizzo IP del server da usare nell'esecuzione di query per i server DNS. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (13)
</dt> </dl>

Secondo indirizzo IP del server da usare nell'esecuzione di query per i server DNS. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (14)
</dt> </dl>

Indirizzi IP del terzo server da usare nell'esecuzione di query per i server DNS. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (15)
</dt> </dl>

Quarto indirizzo IP del server da usare nell'esecuzione di query per i server DNS. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**Gateway**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9)
</dt> </dl>

Indirizzo IP del gateway predefinito utilizzato dal sistema informatico. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2)
</dt> </dl>

Indice dell'adapter. L'indice dell'adapter può cambiare quando un adapter viene disabilitato e quindi abilitato o in altre circostanze e non deve essere considerato permanente.

</dd> <dt>

**Ipaddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6)
</dt> </dl>

Indirizzi IP associati alla scheda di interfaccia di rete. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1), **Max** (256)
</dt> </dl>

Nome della scheda di interfaccia di rete.

</dd> <dt>

**PhysicalAddr**
</dt> <dd> <dl> <dt>

Tipo di dati: **char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4), **Max** (8)
</dt> </dl>

Indirizzo hardware per la scheda.

</dd> <dt>

**PhysicalAddrLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3)
</dt> </dl>

Lunghezza dell'indirizzo hardware per la scheda.

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10)
</dt> </dl>

Indirizzo IP per il server WINS primario. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11)
</dt> </dl>

Indirizzo IP per il server WINS secondario. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> <dt>

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5)
</dt> </dl>

Dimensioni, in byte, della proprietà Data.

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7)
</dt> </dl>

Subnet mask associata alla scheda di interfaccia di rete. Ogni byte di sint32 rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




