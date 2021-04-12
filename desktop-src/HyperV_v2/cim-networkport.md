---
description: Rappresentazione logica di una porta di rete in un dispositivo di rete.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: Classe CIM_NetworkPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233319"
---
# <a name="cim_networkport-class"></a>CIM \_ NetworkPort (classe)

Rappresentazione logica di una porta di rete in un dispositivo di rete.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a>Members

La classe **CIM \_ NetworkPort** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ NetworkPort** dispone di queste proprietà.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")
</dt> </dl>

Unità di trasmissione massima (MTU) attiva o negoziata supportata dalla porta.

</dd> <dt>

**Rilevamento automatico**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato; in caso contrario, **false**.

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se la porta funziona in modalità full duplex; in caso contrario, **false**.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")
</dt> </dl>

Tecnologia di collegamento utilizzata dalla porta. Se impostato su "1" (altro), la proprietà **OtherLinkTechnology** contiene una descrizione del tipo di collegamento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

**IB** (3)


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

**FC** (4)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (5)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (6)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token ring** (7)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (8)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**Infrarossi** (9)


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

**Bluetooth** (10)


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

**LAN wireless** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,3 ")
</dt> </dl>

Matrice che contiene gli indirizzi di rete per la porta.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")
</dt> </dl>

La tecnologia di collegamento quando **LinkTechnology** è impostata su "1", (other).

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")
</dt> </dl>

> [!Note]  
> Descrizione deprecata: tipo di modulo della porta, quando la proprietà **portType** contiene 1 (other).

 

Questa proprietà è deprecata. È invece consigliabile usare la proprietà **portType** nella classe [**CIM \_ LogicalPort**](cim-logicalport.md) .

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Scheda di rete DMTF 802 porta \| 001,2 ")
</dt> </dl>

Indirizzo di rete hardcoded in una porta. È possibile modificare l'indirizzo hardcoded usando un aggiornamento del firmware o una configurazione software. Quando questa modifica viene apportata, questa proprietà deve essere aggiornata nello stesso momento. Se l'indirizzo non esiste, **PermanentAddress** deve essere lasciato vuoto.

</dd> <dt>

**NumeroPorta**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di porta della porta di rete. Le porte di rete spesso sono numerate in relazione a un modulo logico o a un elemento di rete.

</dd> <dt>

**Velocità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits al secondo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ifSpeed "," MIF. \|Scheda di rete DMTF 802 porta \| 001,5 "), **punito** (" bit/secondo ")
</dt> </dl>

Larghezza di banda corrente della porta in bit al secondo. Per le porte che variano a seconda della larghezza di banda o per quelle in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")
</dt> </dl>

Unità di trasmissione massima (MTU) supportata dalla porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LOGICALPORT CIM**](cim-logicalport.md)
</dt> </dl>

 

