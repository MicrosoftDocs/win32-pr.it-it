---
description: Rappresenta i dati di configurazione per un endpoint VLAN.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Classe CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885868"
---
# <a name="cim_vlanendpointsettingdata-class"></a>CIM \_ VLANEndpointSettingData (classe)

Rappresenta i dati di configurazione per un endpoint VLAN.

## <a name="syntax"></a>Sintassi

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VLANEndpointSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VLANEndpointSettingData** dispone di queste proprietà.

<dl> <dt>

**AccessVLAN**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

VLAN di accesso per l'endpoint.

</dd> <dt>

**DefaultVLAN**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Valore predefinito per la VLAN nativa sull'endpoint trunk.

> [!Note]  
> Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **OperationalEndpointMode** .

 

</dd> <dt>

**NativeVLAN**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

ID VLAN usato per contrassegnare il traffico non contrassegnato ricevuto sull'endpoint trunk.

> [!Note]  
> Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **SwitchEndpointMode** .

 

</dd> <dt>

**PruneEligibleVLANList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Matrice che contiene gli ID di VLAN che il sistema può rimuovere dall'endpoint del trunk.

> [!Note]  
> Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **OperationalEndpointMode** .

 

</dd> <dt>

**TrunkedVLANList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Matrice che contiene gli ID degli endpoint VLAN con trunking abilitato.

> [!Note]  
> Questa proprietà viene usata solo quando l'endpoint VLAN funziona in modalità di trunking, specificato nella proprietà **OperationalEndpointMode** .

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

