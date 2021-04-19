---
description: Un endpoint di comunicazione che può connettersi a una LAN per inviare e ricevere frame di dati. Gli endpoint LAN includono Ethernet, token ring e interfacce FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: Classe CIM_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320044"
---
# <a name="cim_lanendpoint-class"></a>CIM \_ LANEndpoint (classe)

Un endpoint di comunicazione che può connettersi a una LAN per inviare e ricevere frame di dati. Gli endpoint LAN includono Ethernet, token ring e interfacce FDDI.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a>Members

La classe **CIM \_ LANEndpoint** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ LANEndpoint** dispone di queste proprietà.

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene altri indirizzi unicast che possono essere utilizzati per comunicare con l'endpoint LAN.

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene gli indirizzi multicast su cui è in ascolto l'endpoint LAN.

</dd> <dt>

**LANId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment. LanID, CIM \_ LANSegment. LanID")
</dt> </dl>

Etichetta o identificatore per il segmento LAN a cui è connesso l'endpoint. Se l'endpoint non è attualmente connesso o se queste informazioni sono sconosciute, **LanID** è null.

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. ConnectivityType, CIM \_ LANSegment. LANType ")
</dt> </dl>

> [!Note]  
> Descrizione deprecata: tipo di tecnologia utilizzata nella LAN.

 

Questa proprietà è deprecata. È invece consigliabile usare la proprietà **ProtocolType** .

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

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**Tokenring** (3)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Indirizzo unicast principale utilizzato dall'endpoint LAN.

L'indirizzo MAC deve essere formattato con le caratteristiche seguenti:

-   L'indirizzo è costituito da dodici cifre esadecimali.
-   Ogni coppia di cifre rappresenta uno dei sei ottetti dell'indirizzo MAC.
-   Ogni coppia di cifre deve essere in ordine di bit canonico in base allo standard RFC 2469.

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Dimensione massima, in byte, dei campi dati inviati o ricevuti dall'endpoint LAN.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANConnectivitySegment. OtherTypeDescription ","**CIM \_ LANEndpoint**.**LANType**")
</dt> </dl>

> [!Note]  
> Descrizione deprecata: tipo di tecnologia utilizzata sulla LAN quando la proprietà **LANType** è impostata su "1" (other).

 

Questa proprietà è deprecata. È invece consigliabile usare la proprietà **OtherTypeDescription** .

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

[**\_PROTOCOLENDPOINT CIM**](cim-protocolendpoint.md)
</dt> </dl>

 

