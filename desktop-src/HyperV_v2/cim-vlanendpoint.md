---
description: Un endpoint su un'opzione o una stazione finale assegnata a una VLAN oppure accetta il traffico da una o più VLAN.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: Classe CIM_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128123"
---
# <a name="cim_vlanendpoint-class"></a>CIM \_ VLANEndpoint (classe)

Un endpoint su un'opzione o una stazione finale assegnata a una VLAN oppure accetta il traffico da una o più VLAN.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VLANEndpoint** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VLANEndpoint** dispone di queste proprietà.

<dl> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")
</dt> </dl>

La modalità VLAN richiesta per l'endpoint.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Accesso** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Auto dinamica** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Auspicabile dinamico** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Tunnel Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities. SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**")
</dt> </dl>

Tipo di incapsulamento VLAN richiesto.

> [!Note]  
> Questa proprietà viene usata solo quando l'endpoint VLAN è in modalità trunk.

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1 q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco ISL** (4)


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

**Negoziazione** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (6.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768...)


</dt> <dd></dd> </dl>

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities. Dot1QTagging ")
</dt> </dl>

Indica se il protocollo di registrazione VLAN GARP (GVRP) è abilitato o disabilitato nell'endpoint del trunk.

> [!Note]  
> Questa proprietà viene utilizzata solo quando GVRP è supportato dall'endpoint e la modalità di trunking è abilitata.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")
</dt> </dl>

La modalità VLAN corrente per l'endpoint.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Accesso** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Auto dinamica** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Auspicabile dinamico** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Tunnel Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")
</dt> </dl>

Tipo di incapsulamento VLAN corrente.

> [!Note]  
> Questa proprietà viene usata solo quando l'endpoint VLAN è in modalità trunk.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1 q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco ISL** (4)


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

**Negoziazione** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (6.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768...)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OperationalEndpointMode**")
</dt> </dl>

Tipo di modello di endpoint VLAN supportato da VLANEndpoint quando il valore di **DesiredEndpointMode** è impostato su "1" (other); in caso contrario, **null**.

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")
</dt> </dl>

Tipo di incapsulamento VLAN supportato dall'endpoint VLAN quando il valore della proprietà **DesiredVLANTrunkEncapsulation** è impostato su 1 (other); in caso contrario, **null**.

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

 

