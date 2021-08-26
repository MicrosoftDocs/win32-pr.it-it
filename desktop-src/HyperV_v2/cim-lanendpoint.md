---
description: Endpoint di comunicazione in grado di connettersi a una LAN per inviare e ricevere frame di dati. Gli endpoint LAN includono interfacce ethernet, token ring e FDDI.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint classe
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
ms.openlocfilehash: 5e42f5edcc7010b9a84fdaaf3686208c9f82def03493c4c423aa3815b1d0758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046811"
---
# <a name="cim_lanendpoint-class"></a>Classe \_ CIM LANEndpoint

Endpoint di comunicazione in grado di connettersi a una LAN per inviare e ricevere frame di dati. Gli endpoint LAN includono interfacce ethernet, token ring e FDDI.

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

La **classe \_ CIM LANEndpoint** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CIM LANEndpoint** ha queste proprietà.

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene altri indirizzi unicast che possono essere usati per comunicare con l'endpoint LAN.

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice contenente gli indirizzi multicast a cui l'endpoint LAN è in ascolto.

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.LANID, CIM \_ LANSegment.LANID")
</dt> </dl>

Etichetta o identificatore per il segmento LAN a cui è connesso l'endpoint. Se l'endpoint non è attualmente connesso o se queste informazioni sono sconosciute, **LANID** è NULL.

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.ConnectivityType, CIM \_ LANSegment.LANType")
</dt> </dl>

> [!Note]  
> Descrizione deprecata: tipo di tecnologia usata nella lan.

 

Questa proprietà è deprecata. È invece consigliabile usare la **proprietà ProtocolType.**

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

**TokenRing** (3)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Macaddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Indirizzo unicast principale usato dall'endpoint LAN.

L'indirizzo MAC deve essere formattato con le caratteristiche seguenti:

-   L'indirizzo è costituito da dodici cifre esadecimali.
-   Ogni coppia di cifre rappresenta uno dei sei ottetti dell'indirizzo MAC.
-   Ogni coppia di cifre deve essere in ordine di bit canonico in base a RFC 2469.

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit")
</dt> </dl>

Dimensioni massime, in byte, dei campi dati inviati o ricevuti dall'endpoint LAN.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.OtherTypeDescription", "**CIM \_ LANEndpoint**.**LANType**")
</dt> </dl>

> [!Note]  
> Descrizione deprecata: tipo di tecnologia usata nella LAN quando la proprietà **LANType** è impostata su "1" (Altro).

 

Questa proprietà è deprecata. È invece consigliabile usare la **proprietà OtherTypeDescription.**

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

[**Protocollo \_ CIMEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

