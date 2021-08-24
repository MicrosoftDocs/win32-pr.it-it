---
description: Rappresentazione logica di una porta di rete in un dispositivo di rete.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: CIM_NetworkPort classe
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
ms.openlocfilehash: aa69b2728f3d0cdb97bcc972ef6b72ab5bd0df3202df60e92f87e161ea9a1702
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694711"
---
# <a name="cim_networkport-class"></a>Classe \_ CiM NetworkPort

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

La **classe \_ CiM NetworkPort** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM NetworkPort** ha queste proprietà.

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Byte"), **PUnit** ("byte")
</dt> </dl>

L'unità massima di trasmissione attiva o negoziata (MTU) supportata dalla porta.

</dd> <dt>

**AutoSense**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se la porta può determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato; in caso contrario, **false.**

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se la porta funziona in modalità full duplex; in caso contrario, **false.**

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")
</dt> </dl>

Tecnologia di collegamento utilizzata dalla porta. Se impostata su "1" (altro), la **proprietà OtherLinkTechnology** contiene una descrizione del tipo di collegamento.

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

**Bancomat** (6)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token ring** (7)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (8)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**A lor** (9)


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

**BlueTooth** (10)


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

**LAN wireless** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**Indirizzi di rete**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Network Adapter 802 Port \| 001.3")
</dt> </dl>

Matrice che contiene gli indirizzi di rete per la porta.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")
</dt> </dl>

Tecnologia di collegamento quando **LinkTechnology** è impostato su "1", (altro).

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")
</dt> </dl>

> [!Note]  
> Descrizione deprecata: tipo di modulo della porta, quando la **proprietà PortType** contiene 1 (altro).

 

Questa proprietà è deprecata. È invece consigliabile usare **la proprietà PortType** nella [**classe \_ CiM LogicalPort.**](cim-logicalport.md)

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Network Adapter 802 Port \| 001.2")
</dt> </dl>

Indirizzo di rete hardcoded in una porta. L'indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software. Quando viene apportata questa modifica, questa proprietà deve essere aggiornata contemporaneamente. **PermanentAddress** deve essere lasciato vuoto se l'indirizzo non esiste.

</dd> <dt>

**Portnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di porta della porta di rete. Le porte di rete sono spesso numerate in relazione a un modulo logico o a un elemento di rete.

</dd> <dt>

**Velocità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II.ifSpeed", "MIF. DmTF \| Network Adapter 802 Port \| 001.5"), **PUnit** ("bit/second")
</dt> </dl>

Larghezza di banda corrente della porta in bit al secondo. Per le porte che variano in larghezza di banda o per quelle in cui non è possibile eseguire una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Byte"), **PUnit** ("byte")
</dt> </dl>

Unità massima di trasmissione (MTU) supportata dalla porta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalPort**](cim-logicalport.md)
</dt> </dl>

 

