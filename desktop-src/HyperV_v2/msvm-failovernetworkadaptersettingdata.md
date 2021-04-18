---
description: Rappresenta le impostazioni per una scheda di rete all'interno del sistema operativo guest, che verrà applicato al momento di un failover.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Classe Msvm_FailoverNetworkAdapterSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307924"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a>\_Classe MSVM FailoverNetworkAdapterSettingData

Rappresenta le impostazioni per una scheda di rete all'interno del sistema operativo guest, che verrà applicato al momento di un failover.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a>Members

La **classe \_ FailoverNetworkAdapterSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ FailoverNetworkAdapterSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.

</dd> <dt>

**DefaultGateways**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di stringhe che specificano i gateway IP predefiniti configurati nella scheda di rete all'interno del sistema operativo guest. Il numero massimo di gateway IP predefiniti che possono essere configurati in una singola scheda di rete è cinque.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se DHCP è abilitato sull'interfaccia IPv4 della scheda di rete all'interno del sistema operativo guest.

</dd> <dt>

**DNSServers**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di stringhe che specificano i server DNS configurati nella scheda di rete all'interno del sistema operativo guest.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**IPAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di stringhe che specificano gli indirizzi IP configurati nella scheda di rete all'interno del sistema operativo guest.

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica i protocolli Internet a cui si applicano le impostazioni specificate da questa istanza. Deve essere uno dei valori seguenti.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)


</dt> <dd>

IPv4/IPv6

</dd> </dl>

</dd> <dt>

**Subnet**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di stringhe che specificano le subnet configurate nella scheda di rete all'interno del sistema operativo guest. Ogni elemento in questa matrice viene applicato all'elemento corrispondente nella matrice **IPAddresses** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

